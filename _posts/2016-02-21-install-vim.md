---
title: Vim Kurulumu ve Kullanımı
categories:
  - programs
tags:
  - vim
  - editors
  - programming
  - coding
---

Vim vi metin düzenleyici temel alınarak yazılmış açık kaynaklı bir yazılımdır. Özellikle linuxda komut satırından çalışmayı sevenler için kullanışlı bir metin editörüdür. Başlangıçda öğrenmesi biraz zor olsa da öğrendikten sonra alışkanlık haline gelir. Eklenti sayısının çok olması ve çok çeşitli ayarlamalar yaparak kişiselleştirebilmeye imkan tanıması güzel özelliklerindendir.

Vimde değişik kipler vardır. Bunlar komut kipi, yazma kipi ve görünüm kipleridir.

* Komut Kipi : Dosya ilk açıldığında bu kiptedir. Eğer en altta dosya ismi gözüküyorsa bu kipte olduğumuzu anlarız. Başka bir kipteyken **esc**
tuşuna basarak bu kipe geçiş yapabiliriz.

* Yazma Kipi : Klavyedeki **i(insert)** tuşuna basarak bu kipe geçiş yapabiliriz. En altta INSERT yazıyorsa bu kipte olduğumuzu anlarız. Bu kipteyken dosyaya yazma işlemini yapabiliriz.

* Görünüm Kipi : Eğer terminalin en altında VISUAL yazıyorsa bu kipte olduğumuzu anlarız. Sadece dosyayı görüntüleme içindir değişiklik yapılamaz. **v** tuşuna basılarak bu kipe geçilir.

## Ubuntuda Vim Kurulumu

**sudo apt-get install vim** komutunu yazdıktan sonra sudo parolanızı girin.

## Ayarlamalar

Vim editörünü bazı ayarlamalar yaparak çok daha kullanışlı hale getirebilirsiniz. Vim ayarlamalarını yapmak için .vimrc dosyasını kullanmalısınız. Bu dosyanın bilgisayarınızda nerede olduğunu bulmak için vim editörünü açıp esc tuşuna basarak komut kipine geçin ve **:version** yazın. Ekrana gelen çıktıda .vimrc dosyasının nerede bulunduğunu görebilirsiniz. Büyük ihtimalle **$Home/.vimrc** dizininde bulunur ama kontrol etmekte fayda var. Vim yönetici kipindeyken **:e $Home/.vimrc** komutuyla vimrc dosyasını açın. Ayarlar için aşağıdaki linkten yararlanabilirsiniz.

[vimrc ayarları](http://vimconfig.com/)

Ayarların bazılarını aşağıda açıklayalım.

* set number => satır numaralarının gözükmesini sağlar.
* syntax on => dosya uzantısına göre renklendirme yapar.
* set is => aranılacak kelime yazılırken bulmaya başlar.
* set ic => büyük-küçük harf ayrımı yapmadan arar.
* set hls => sayfada arama yapılan kelimeleri beirginleştirir.
* set encoding=utf-8 => dosyanın otomatik utf8 formatında olmasını sağlar.
* set tabstop=8 => tab uzunluğunu 8 karakter yapar.
* set autoindent => girintileme özelliğini aktifleştirir.

## Kullanım

Vim editöründe bir dosya açmak için terminali açın ve **vim dosya_adı.uzantısı** şeklinde dosyanın adını ve uzantısını belirtin. Vim uzantıya göre renklendirme yapacaktır. Daha sonra insert moduna geçip kodunuzu yazabilirsiniz.

* Dosyayı kaydetmeden çıkmak için **:q**
* Dosyayı kaydet ve çık için **:wq**
* Dosyayı kaydet ama çıkma **:w**
* İki yatay dosya açmak için **vim -o dosya1.uzantı dosya2.uzantı**
* İki dikey dosya açmak için **vim -O dosya1.uzantı dosya2.uzantı**
* İki dosya arası geçiş yapmak için **ctrl+w**

komutları kullanılır.

