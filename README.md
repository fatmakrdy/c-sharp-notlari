<h1> C# Notlari </h1>
- C#;etkileşimli web siteleri, mobil uygulamalar, video oyunları, artırılmış gerçeklik (AR), sanal gerçeklik (VR), masaüstü uygulamaları ve back-end hizmetleri oluşturmak için kullanılabilir.
- C#, static typing sahip bir programlama dilidir. Bu, bir program yazılırken veri tipinin önceden belirtilmesi gerektiği anlamına gelir. Bu kavram, "tür güvenliği" (type safety) olarak da adlandırılır ve programın daha güvenli ve hatasız olmasına yardımcı olur.

# Value Types: 
Veri tiplerinin değer sınırları vardır.
sayı veri tipleri:
int veri tipi 32 bit
long veri tipi 64 bit
short veri tipi 16 bit
byte 8 bit

- long veri tipi integer veri tipinden daha büyük değeri kapsar. *küçük bir veri için long kullanılırsa bellekte gereksiz bir yer kullanmış oluruz.
```
public static void Main(string[] args)
    {
      int num1=10;
      int num2=5;
    Console.WriteLine("Number one: {0}",num1); //index virgülden sonraki ilk sayı
        Console.ReadLine();
    }
  ```
    -bool mantıksal bir veri tipidir. Şart ifadelerinde kullanılır.
     char karakter atamalarında kullanılır
     char character ='A'; 
     (int)char character ='A';//veri tipini değiştirip ASCII de sayısal karşılığını alırız.
     double ondalıkla değerler tutulur.integer bir değer de atanabilir.
     double bir değer integer tipine atanamaz
     double 64 bit
     daha hassas double değerler için decimal kullanılır.virgülden sonra daha fazla değer taşır.
     double değerini decimal türüne dönüştürmeye çalıştığınızda ortaya çıkar. C# dili, bu tür bir dönüşümü açıkça belirtmenizi ister, çünkü double ve decimal farklı sayı veri tipleridir ve otomatik olarak dönüşüm yapmazlar. 
     Açıkça Tür Dönüşümü:
double değerini decimal türüne dönüştürmek için açıkça tür dönüşümü operatörünü kullanabilirsiniz. İşte örnek bir kod:
double doubleValue = 3.14159;
decimal decimalValue = (decimal)doubleValue;
m Takısı Kullanımı:
Alternatif olarak, double bir literali decimal türüne dönüştürmek isterseniz, m takısı kullanabilirsiniz. Örnek:
double doubleValue = 3.14159;
decimal decimalValue = 3.14159m;
# enum  veri tipi, özellikle belirli bir değer kümesini temsil etmek için kullanılır. Enumerations, sabit değerlerin sembolik olarak adlandırılmasına ve gruplandırılmasına yardımcı olur
// Bir enum tanımlama
enum Gunler
{
    Pazartesi,
    Salı,
    Çarşamba,
    Perşembe,
    Cuma,
    Cumartesi,
    Pazar
}

Yukarıdaki örnekte, "Gunler" adında bir enum tanımlanmıştır. Bu enum, haftanın günlerini sembolik olarak temsil eder. Enum tanımlamaları genellikle büyük harfle başlar.

Enum içindeki her öğe, sabit bir değeri temsil eder ve sıfırdan başlayarak artan bir sayısal değere sahiptir. Örneğin, "Pazartesi" enumunun değeri 0'dır, "Salı" 1'dir ve böyle devam eder. Ancak, bu değerlere doğrudan erişmek zorunda değilsiniz, çünkü enum öğeleri genellikle sembolik olarak kullanılırlar.
Gunler bugun = Gunler.Çarşamba;
Bu kodda, "bugun" adlı değişken "Çarşamba" enum öğesini temsil eder. Bu, kodun daha anlaşılır ve düzenli olmasına yardımcı olabilir.
(int)Gunler.Çarşamba--> 2 çıktıısnı verir
Enum veri tipi, programlarınızda sabit değerler kullanmanız gerektiğinde oldukça faydalıdır ve kodunuzun daha okunaklı ve bakımı daha kolay hale gelmesine yardımcı olur.

var atanan değere göre veri tipi belli olur.
 var num=5;
 num='A'; var ilk olarak int değerini aldığında çıktı 65 olur.
