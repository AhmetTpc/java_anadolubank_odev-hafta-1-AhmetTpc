# Ayrıştırma ( Decomposition ) Nedir?
    
Nesne yönelimli tasarımın ilk prensibi olan ayrıştırmanın tanımı; problem alanındaki ilgili varlıkların tespit edilip, doğru nesneler biçiminde ifade edilmesidir. Bir yöntem olarak da nitelendirilebilecek ayrıştırma, sistemdeki karmaşıklıkla (complexity) başa çıkabilmek için yapılır. Buna kısaca böl ve fethet (divide and conquer) denilmektedir.

# Ayrıştırma ( Decomposition ) Neden Uygulanır?

Yazılımcının çözümlemeyi gerçekleştirirken en büyük yardımcısı analiz sırasında ortaya çıkan use case tanımlarıdır. Analizle alakalı bir prensip diyebiliriz. Use case tanımlarını isim ve fiilleri ortaya çıkaracak şekilde okumak olası nesnelerin tespitine yardımcı olacaktır.
Bu aşamada yazılımcı, “NASIL?” sorusu yerine “NE(LER)?” sorusunun cevabına odaklanmalıdır. Böylece algoritma düşünmek yerine nesneleri düşünmeye yoğunlaşabilir

# Ayrıştırma ( Decomposition ) Nasıl Uygulanır?

Fonksiyonel ayrıştırma: Büyük ve karmaşık fonksiyonlar bu yöntemle daha küçük ve anlaşılabilir alt fonksiyonlara ayrılırlar. Bu yüzden Yapısal Programlamaya daha yakındır ve Nesne yönelimli programlamadan biraz uzaklaştırabilir. Genellikle analiz aşamasında diagram şeklinde üretilirler. İlk seviye bileşenler ve fonksiyonları ayrıştırılarak başlanır. İstenilen detayda alt seviyelere inildiğinde işlem durdurulur.
Örnek diyagramlar aşağıdadır.

![Örnek diyagram 1](https://nerdbook.files.wordpress.com/2018/04/4-3.jpg)

![Örnek diyagram 2](https://nerdbook.files.wordpress.com/2018/04/4-4.jpg?w=648)