# Liskov Subsitute Nedir?

Türeyen sınıf yani alt sınıflar ana(üst) sınıfın tüm özelliklerini ve metotlarını aynı işlevi gösterecek şekilde kullanabilme ve kendine ait yeni özellikler barındırabilmelidir.

“Alt seviye sınıflardan oluşan  nesnelerin/sınıfların, ana(üst)  sınıfın nesneleri ile yer    değiştirdikleri zaman, aynı davranışı  sergilemesi gerekmektedir. Türetilen     sınıflar, türeyen sınıfların tüm    özelliklerini kullanabilmelidir.” 

# Liskov Subsitute Neden Uygulanır?

Kısaca şöyle özetlenebilir; 

"Kodlarımızda herhangi birdeğişiklik yapmaya gerekduymadan alt sınıfları,türedikleri(üst) sınıflarınyerine kullanılabilmeprensibidir."

Özetten anlaşıldığı üzeretüretilen sınıflar, türeyensınıfların tümözelliklerini kullanmakzorundadır. Eğer kullanmazise ortaya işlevsiz, dummykodlar çıkacaktır. Budurumda üst sınıfta if elseblokları kullanarak tipkontrolü yapmamızgerekebilir ve böylelikleAçık Kapalı prensibine deters düşmüş oluruz.


# Liskov Subsitute Nasıl Uygulanır?

  ![Liskov Subsitute örnek 1](https://i.hizliresim.com/8lmrrom.png)

Burada IDeveloperinterface’ini implementeeden Junior Developer veSenior Developer class’larıolduğunu görüyoruz. Ancakproje geliştirilirken birsorun olduğunu farkettik.Junior Developer’ımız solidilkelerini kullanamıyor.Yapıyı bu şekilde kurmayadevam edersek ya bumethodun içini boşbırakıcaz ya da NotImplementedExceptionthrow edicez ve ClientAppuygulamamız IDeveloperinterface’i üzerinden,IDeveloper’dan implementeolan tiplerini kullanıpAçık Kapalı prensibinebağlı kalabilecekken eğerJuniorDeveloper değil iseSolidIlkeleriniKullan()diyen bir if else bloğunasahip olucak.
Peki böyle bir durumdaçözüm nasıl olabilirdi? Buyanlış tasarımın önünenasıl geçeriz?

![Liskov Subsitute örnek 2](https://i.hizliresim.com/jm0xvk8.png)

Class Diagramından daanlaşıldığı gibi Developersınıfını soyut yaptık veISolidKullanabilir isimlibir Interface oluşturduk.Böylelikle Liskovprensibine bağlı kaldığımızgibi, oluştuduğum dll’ikullanan Client Uygulamasıda if else bloğuna gerekkalmadan Açık Kapalıprensibine uygun olabilecek.