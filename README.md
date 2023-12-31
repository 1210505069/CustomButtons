# CustomButtons
Bu metin Java programlama dilli kullanılarak yazılan Custom Buttons isimli programın nasıl kullanılacağını, nasıl test edileceğini ve nasıl çalıştığını açıklamaktadır. GUI üzerinde düzenlenmiş 4x4 boyutunda toplamda 16 adet butonu bulunduran bir arayüz içerir. GraphQL ile çalışmaktadır ve her buton belirli bir durumu teslim etmektedir. Her buton, tıklanma ile birlikte bu durumu değiştirmektedir. 

# Programda kullanılan GraphQL Nedir?
GraphQL, istemcilerin tam olarak ihtiyaç duydukları verileri talep etmelerine izin veren API çağrıları yapmaya yönelik bir sorgu ve API tarafından döndürülen verilerin şeklini ve yapısını tanımlamak için kullanılan bir veri modelleme dilidir. Facebook tarafından geliştirilmiş olup geleneksel API'lerden oldukça farklıdır. Geleneksel API'ler belirli bir uygulama için gereken tüm verileri almak için birden çok istek gerektir ve gerekenden daha fazla veri döndürürken, GraphQL ile client istediklerini tek bir sorguda belirtebilir ve server istenen verileri tek bir istekte yanıt verir. Bu durum clientın istediği verileri çok daha verimli bir şekilde almasını sağlar.

GraphQL REST API'leri tarafından döndürülen sabit bir veri kümesiyle çalışmak yerine tam olarak istenen verileri sağlayarak iyileştirilmiş tasarımcı deneyimi sunar, yine bu özellik sayesinde daha esnek ve sürdürülebilir API'lerin yaratılmasında yardımcı olur, istenen verileri azaltmaya yardımcı olarak performansı arttırır ve genel olarak GraphQL API'leri çok daha ayrıntılı belgeler sunarak geliştiricilerin API'leri anlamasını kolaylaştırır.

# CustomButtons nasıl kullanılır?
Öncelikle, programı başlatmak için 'ButtonControlPanel sınıfındaki main metodu çalıştırın, böylece buton kontrol paneli ekrana gelecektir. Ekranda toplamda 16 buton, 4 satır ve 4 sütun olacak şekilde yerleştirilmiş olacaktır. Bu butonların her biri farklı bir durumu teslim etmekte olup, bir butona tıklandığında durumları değiştirebilirsiniz. Butonlara tıklandığında buton aktif hale gelir ve rengi ile simgesi değişir. İlk tıklanan buton program kapatılana dek aktif olarak kalacakken, diğer butonlar kapatılabilir ve ilk butona tekrar tıklandığında diğer tüm butonları deaktive edecektir. Her bir düğme kendisine özgü bir GraphQL şeması ile ilişkilidir ve düğmeye tıklandığında bu şema çalıştırılır.

# CustomButtons nasıl test edilir?
Programı test etmek için öncelikle programı çalıştırmanız gerekmektedir. Program açıldığında düğmelere tıklayarak renk ve simgelerinin değişmesini gözlemleyebilirsiniz. Farklı butonlara farklı sıralarla tıklayarak değişimlerini test edebilirsiniz. İlk tıklanan butona tekrar tıklayarak onun yaptığı işlemi, yani diğer düğmeleri deaktive etmesini gözlemleyebilirsiniz. Her bir buton bir GraphQL şeması gösterdiğinden butona basıldığında 'Butona basıldı! GraphQL değişimi uygulanıyor: Değişim<ButonNumarası>' şeklinde bir yazıyı konsolda gözlemleyebilirsiniz.

# CustomButtons kodu nasıl çalışır?
CustomButtons uygulamasının kodu CustomButton ve ButtonControlPanel isimlik iki sınıftan oluşmaktadır. Temel olarak CustomButton sınıfında sınıf düğmelerinin özellikleri yönetilirken ButtonControlPanel sınıfında bu pencere oluşturulur ve düğmeler eklenir.
CustomButton sınıfında düğmenin metnini, GraphQL şemasını, renklerini, simgelerini ve aktif olup olmadığını belirleyen değişkenler bulunmaktadır. CustomButton sınıfı aynı zamanda butona tıklandığında tetiklenen dinleyiciyi bulundurmaktadır. Tıklama ile birlikte tetikleyici butonun durumunu değiştirir ve ilgili GraphQL şemasını çalıştırır. 

ButtomControlPanel sınıfı ise pencereyi oluşturur ve GridLayout aracılığı ile düğmeleri pencereye yerleştirir. Bu sınıf ayrıca düğmelerin renkleri ve simgelerini tanımlayan değerleri bulundurur.

# Sonuç
CustomButtons uygulaması kullanıcı arayüzünde GraphQL kullanmanın basit bir örneği olarak yazılmıştır. Bu uygulamadaki kodları referans olarak kullanarak kendi uygulamanazı yazabilir ve GraphQL'in nasıl çalıştığını anlayabilirsiniz. 

# Ek notlar
Bu uygulama bir simülasyon olup gerçek bir GraphQL çıktısı yerine konsola bunu temsil eden bir çıktı vermektedir. Butonların aktif veya deaktiflik durumları renkler ve farklı renkli simgelerle temsil edilmektedir.

