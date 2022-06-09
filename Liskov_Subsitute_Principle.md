# Liskov Subsitute Nedir?

    Türeyen sınıf yani alt sınıflar ana(üst) sınıfın tüm özelliklerini ve metotlarını aynı işlevi gösterecek şekilde kullanabilme ve kendine ait yeni özellikler barındırabilmelidir.

    “Alt seviye sınıflardan oluşan  nesnelerin/sınıfların, ana(üst)  sınıfın nesneleri ile yer    değiştirdikleri zaman, aynı davranışı  sergilemesi gerekmektedir. Türetilen     sınıflar, türeyen sınıfların tüm    özelliklerini kullanabilmelidir.” 

# Liskov Subsitute Neden Uygulanır?

    Kısaca şöyle özetlenebilir; 

    "Kodlarımızda herhangi bir değişiklik yapmaya gerek duymadan alt sınıfları, türedikleri(üst) sınıfların yerine kullanılabilme prensibidir."
    
    Özetten anlaşıldığı üzere türetilen sınıflar, türeyen sınıfların tüm özelliklerini kullanmak zorundadır. Eğer kullanmaz ise ortaya işlevsiz, dummy kodlar çıkacaktır. Bu durumda üst sınıfta if else blokları kullanarak tip kontrolü yapmamız gerekebilir ve böylelikle Açık Kapalı prensibine de ters düşmüş oluruz.


# Liskov Subsitute Nasıl Uygulanır?

  ![Liskov Subsitute örnek 1](https://i.hizliresim.com/8lmrrom.png)

    Burada IDeveloper interface’ini implemente eden Junior Developer ve Senior Developer class’ları olduğunu görüyoruz. Ancak proje geliştirilirken bir sorun olduğunu farkettik. Junior Developer’ımız solid ilkelerini kullanamıyor. Yapıyı bu şekilde kurmaya devam edersek ya bu methodun içini boş bırakıcaz ya da  NotImplementedException throw edicez ve ClientApp uygulamamız IDeveloper interface’i üzerinden, IDeveloper’dan implemente olan tiplerini kullanıp Açık Kapalı prensibine bağlı kalabilecekken eğer JuniorDeveloper değil ise SolidIlkeleriniKullan() diyen bir if else bloğuna sahip olucak.
    Peki böyle bir durumda çözüm nasıl olabilirdi? Bu yanlış tasarımın önüne nasıl geçeriz?

![Liskov Subsitute örnek 2](https://i.hizliresim.com/jm0xvk8.png)

    Class Diagramından da anlaşıldığı gibi Developer sınıfını soyut yaptık ve ISolidKullanabilir isimli bir Interface oluşturduk. Böylelikle Liskov prensibine bağlı kaldığımız gibi, oluştuduğum dll’i kullanan Client Uygulaması da if else bloğuna gerek kalmadan Açık Kapalı prensibine uygun olabilecek.