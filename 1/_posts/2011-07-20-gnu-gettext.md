---
layout: post
title: GNU gettext nedir? .po ve .mo uzantılı dosyalar nedir?
---

1Yazılımlara çoklu dil desteği sağlamak için çevirilerinin yapılması gerekir. Yazılımın hangi dilde çalışacağına kullanıcı karar verir ve dil seçimini yapar. Yazılım İngilizce olarak hazırlandığına göre başka bir dilde çalışması için o dile ait çevirisinin bulunması ve bunun çalıştırılması gerekmektedir. Burada kullanılacak olan farklı dillerde yazılmış olan mesajlar veya dökümantasyonlar .mo uzantılı dosyanın içinde bulunurlar. Bu dosyalar bir editör yardımıyla düzenlenebilen .po uzantılı dosyalardan oluşurlar. Kısaca .mo uzantılı dosyalar .po uzantılı dosyaların derlenmiş halidir. .po uzantılı dosyaların içeriğine gelecek olursak çevirilerden oluşurlar. herhangi bir yazılımdaki dizgileri ve bu dizgilerin farklı bir dile çevrilmiş halini bulundururlar. örnek verecek olursak bu dosyaların içeriği aşağıdaki gibidir.

msgid "hello world"
msgstr "merhaba dünya"

msgid "welcome to our site"
msgstr "sitemize hoşgeldiniz"


Buradaki .po uzantılı dosya poedit veya başka herhangi uygun bir editörle açılabilir ve içeriği görüntülenebilir. Düzenlenmesi gereken yerler varsa burdan düzenlenir ve kaydedildiği takdirde .mo uzantılı dosya oluşturulmuş olur. Kayıt işlemi esnasında çevilen dilin kısaltması kullanılarak kaydedilmelidir. Türkçe için "tr_TR" ingilizce için "en_US" vb.(burada tr çevirilen dili ve TR de bölgeyi temsil eder). bu sayede yazılımların kullanıcının seçtiği dile çevirisi yapılmakta ve gettext paketi sayesinde herkesin kullanımına sunulmaktadır.

GNU GETTEXT NEDİR? NE İŞE YARAR?(GNU ULUSALLAŞTIRMA VE YERELLEŞTİRME PROJESI) 

Bildiğimiz üzere neredeyse bütün programlar ingilizce yazılmaktadır. Bu genel olarak bir bütünlük sağlamak açısından ve diğer ülkelerdekilerle kolay iletişim kurmak açısından  programcıların yararına olsa da, bazen geliştiriciler veya kulanıcılar yazılımları kendi dillerinde kullanmak isterler. Elbette programcının bu özelliği yazdığı programlara katması o programın kullanılabilirlik açısından önemini artıracak ve sadece ingilizce bilenlerin veya programın dökümantasyonunun hazırlandığı dili konuşan insanların değil; o programın çevirisinin yapıldığı bütün dillerden herhangi birisini bilen herkesin kullanmasına olanak sağlayacaktır.

Tam bu noktada GNU Gettext, programcıların bu ihtiyaçlarını karşılamak için devreye girmektedir. Bu paket programcılara ve kullanıcılara programların ve dökümantasyonların çevirisi konusunda  yardımcı olmaktadır. Gettext işlevinin görevi kendisine argüman olarak verilen dizgeyi alıp, ileti kataloğundaki dizgelerle karşılaştırarak çeviriyi bulup, bunu döndürmektir. Gettext işlevi ileti katalogları denilen .po uzantılı dosyaların içerisindeki msgid ile belirtilen dizgiye karşılık gelen çeviriyi arar. Çevrilecek olan dizgeyi tek bir argüman şeklinde alır. Bundan dolayı ileti kataloglarının hem özgün dizgeyi hem de çeviriyi birlikte içermesi gerekir. Bu sayede yazılımlara çoklu dil desteği sağlanmaktadır.

