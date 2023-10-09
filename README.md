# C# Notları

Bu README dosyası, C# programlama dili hakkında temel bilgileri içerir. C#, çeşitli uygulamalar oluşturmak için kullanılabilir, bunlar arasında etkileşimli web siteleri, mobil uygulamalar, video oyunları, artırılmış gerçeklik (AR), sanal gerçeklik (VR), masaüstü uygulamaları ve back-end hizmetleri bulunur.

## Tür Güvenliği (Type Safety)

C#, bir program yazılırken veri tipinin önceden belirtilmesi gereken bir programlama dilidir. Bu özellik, programların daha güvenli ve hatasız olmasına yardımcı olur.

## Value Types: 
C# içerisinde kullanılan bazı temel değer tipleri şunlardır:

- **int:** 32 bitlik tamsayıları temsil eder.
- **long:** 64 bitlik tamsayıları temsil eder.
- **short:** 16 bitlik tamsayıları temsil eder.
- **byte:** 8 bitlik verileri temsil eder.
- **double:** 64 bitlik verileri temsil eder.
  
  ```
   public static void Main(string[] args)
  {
      int num1=10;
      int num2=5;
    Console.WriteLine("Number one: {0}",num1); //index virgülden sonraki ilk sayı
    Console.ReadLine();
    }
  ```
Not: Daha küçük bir veri için long kullanmak, gereksiz bellek kullanımına yol açabilir.

## bool Veri Tipi

- **bool:** Mantıksal bir veri tipidir ve genellikle şart ifadelerinde kullanılır.

## char Veri Tipi

- **char:** Karakterleri temsil eder ve karakter atamaları için kullanılır. Karakterin ASCII değerini almak için `(int)` kullanılabilir.

## double ve decimal Veri Tipleri

- **double:** Ondalık değerleri temsil eder. Tam sayı bir değer de atanabilir, ancak tam tersi mümkün değildir.
- **decimal:** Hassas ondalık değerleri temsil eder ve virgülden sonra daha fazla hassasiyet sunar.C# dili, bu tür bir dönüşümü (double'dan decimal'a dönüştürme) açıkça belirtmenizi ister, çünkü double ve decimal farklı sayı veri tipleridir ve otomatik olarak dönüşüm yapmazlar.

 ## Açıkça Tür Dönüşümü:
double değerini decimal türüne dönüştürmek için açıkça tür dönüşümü operatörünü kullanabilirsiniz. İşte örnek bir kod:

```
double doubleValue = 3.14159;
decimal decimalValue = (decimal)doubleValue;
```

- m Takısı Kullanımı:
Alternatif olarak, double bir literali decimal türüne dönüştürmek isterseniz, m takısı kullanabilirsiniz. Örnek:
 
```
double doubleValue = 3.14159;
decimal decimalValue = 3.14159m;
```

## enum Veri Tipi

- **enum:** <br> Belirli bir değer kümesini sembolik olarak temsil etmek için kullanılır. Özellikle sabit değerlerin adlandırılmasına ve gruplandırılmasına yardımcı olur. Örnek olarak haftanın günlerini sembolik olarak temsil eden bir enum tanımlayabiliriz.

```
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
```
Bu enum, günleri sembolik olarak temsil eder ve her biri bir sayısal değere karşılık gelir.
Örneğin, "Pazartesi" enumunun değeri 0'dır, "Salı" 1'dir ve böyle devam eder. Ancak, bu değerlere doğrudan erişmek zorunda değilsiniz, çünkü enum öğeleri genellikle sembolik olarak kullanılırlar.
<br>
> Gunler bugun = Gunler.Çarşamba;
Bu kodda, "bugun" adlı değişken "Çarşamba" enum öğesini temsil eder. Bu, kodun daha anlaşılır ve düzenli olmasına yardımcı olabilir.
 <br>
> (int)Gunler.Çarşamba -- 2 çıktıısnı verir
Enum veri tipi, programlarınızda sabit değerler kullanmanız gerektiğinde oldukça faydalıdır ve kodunuzun daha okunaklı ve bakımı daha kolay hale gelmesine yardımcı olur.
** var anahtar kelimesi: **
`var` anahtar kelimesi, atanan değere göre veri tipini belirler. Örneğin:
```
var num = 5; // num otomatik olarak int olarak tanımlanır
num = 'A';   // Şimdi num char tipine sahiptir ve ASCII değeri 65'tir.
```
