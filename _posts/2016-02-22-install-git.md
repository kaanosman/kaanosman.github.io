---
layout: post
categories: programs
title: Git Kurulumu ve Kullanımı
excerpt: "Ubuntuda git kurulumu ve kullanımı"
tags: [git, github, cvs, version]
comments: true
--- 

Git bir versiyon kontrol ve kaynak kod yönetim sistemidir. Linus Torvalds tarafından geliştirilmiştir. Çok kişinin çalıştığı projelerde uyumlu bir şekilde çalışma yapılmasını sağlar. 


## Ubuntuda Git Kurulumu

* **sudo apt-get install git** komutunu yazdıktan sonra sudo parolanızı girin. 
* Daha sonra terminale **ssh-keygen** komutunu yazarak açık ve gizli anahtarınızı üretin.(ssh ile bağlanmak için)
* **gedit .ssh/id_rsa.pub** komutu ile geditte açılan açık anahtar kodunuzu kopyalayın. Bu kodu githubdaki settings->ssh keys->new ssh key bölümüne yapıştırıp kaydedin.

## Ayarlamalar

Git kurulduktan sonra aşağıdaki komular ile ayarlamalarını yapabilirsiniz.

* git config --global user.name "username" => git için kullanıcı adı
* git config --global user.email mail@gmail.com => git için email
* git config --global core.editor vim => git için standart editör
* git config --global merge.tool diffmerge => git için standart karşılaştırıcı

Aşağıdaki linkten daha detaylı ayarlarını bulabilirsiniz.

[git ayarları](https://git-scm.com/book/tr/v2/Customizing-Git-Git-Configuration)

## Çalışma Mantığı

Gitin çalışma mantığında proje üç dizine ayrılır. Bunlar çalışma dizini, stage ve head dizinleridir.

* Çalışma Dizini : Git init diyerek projemize giti dahil ederiz. Daha sonra yapacağımız değişiklikler gitin çalışma dizinine kaydedilir. Çalışma dizininden stage dizinine aktarmak için **git add file_name** komutu kullanılır. Bütün değişiklikleri atmak için **git add .** komutu kullanılabilir.

* Stage Dizini : Çalışma dizininde git add komutu ile bu dizine geçilir. Bu dizinden ise **git commit -m "commit message"** komutu ile head dizinine geçilir.

* Head Dizini : Bu dizin projenin gönderilmeden önceki son durağıdır. **git push origin master** komutu ile proje githuba gönderilir.

## Kullanım

Öncelikle [githuba](https://github.com/) üye olun. Daha sonra sağ üstteki + işaretine tıklayarak new repository seçeneğini seçin ve bir repo oluşturun. Daha sonra localdeki projenizin içine girip **git init** komutunu çalıştırarak projenize giti ekleyin. Localinizdeki proje ile uzak deponuzun haberleşebilmesi için **git remote add origin https://github.com/user/repo.git** komutu ile remote eklemeniz gerekir.


