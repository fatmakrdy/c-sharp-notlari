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

- **bool:** Mantıksal bir veri tipidir ve genellikle şart ifadelerinde kullanılır.
- **char:** Karakterleri temsil eder ve karakter atamaları için kullanılır. Karakterin ASCII değerini almak için `(int)` kullanılabilir.
- **double:** 64 bitlik ondalık değerleri temsil eder. Tam sayı bir değer de atanabilir, ancak tam tersi mümkün değildir.
- **decimal:** 128 bitlik hassas ondalık değerleri temsil eder ve virgülden sonra daha fazla hassasiyet sunar.C# dili, bu tür bir dönüşümü (double'dan decimal'a dönüştürme) açıkça belirtmenizi ister, çünkü double ve decimal farklı sayı veri tipleridir ve otomatik olarak dönüşüm yapmazlar.

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
``` Gunler bugun = Gunler.Çarşamba;```<br>
Bu kodda, "bugun" adlı değişken "Çarşamba" enum öğesini temsil eder. Bu, kodun daha anlaşılır ve düzenli olmasına yardımcı olabilir.
 <br>
``` (int)Gunler.Çarşamba -- 2 çıktıısnı verir```<br>
Enum veri tipi, programlarınızda sabit değerler kullanmanız gerektiğinde oldukça faydalıdır ve kodunuzun daha okunaklı ve bakımı daha kolay hale gelmesine yardımcı olur.
- var anahtar kelimesi: <br>
`var` anahtar kelimesi, atanan değere göre veri tipini belirler. Örneğin:
```
var num = 5; // num otomatik olarak int olarak tanımlanır
num = 'A';   // Şimdi num char tipine sahiptir ve ASCII değeri 65'tir.
```
- **Single Line if bloğu:**
```static void Main(string[] args)
{
    var number = 10;
    Console.WriteLine(number==10 ? "sayı 10 dur" : "sayı 10 değil");
    Console.ReadLine();
}
```
- **Methodlar:**
Aynı işlemi birden fazla kez yapmanız gerektiğinde, her seferinde aynı kodu yeniden yazmak yerine, aynı işlemi gerçekleştiren bir method kullanabilirsiniz. Bu, kod tekrarını azaltır ve bakımı kolaylaştırır.

```static void Main(string[] args)
{
    Add();
    Console.ReadLine();
}
 static void Add()
{
    Console.WriteLine("added");
}
```
- **Parametreli Method:**
```
static void Main(string[] args)
{
    Console.WriteLine(Add1(5, 7));
    Console.ReadLine();
}
static int Add1(int num1,int num2)
{
    return num1 + num2;
}
```
- **Default parametreli methodlar:**
default değer her zaman sonda olmalıdır ilk parametreye default değer veremeyiz.<br>

```
static int Add2(int num1, int num2=15)
{
    return num1 + num2;
}
```

-ref keywordü ile method içindeki değişikliği main methodunda da görebiliriz.<br>
ref keywordü yerine out keywordü kullanabilirz; out keywordünde number1 verisinde ilk değer vermek zorunda değiliz.<br>
```
static void Main(string[] args)
{
    int number1 = 20;
    int number2 = 100;

    Console.WriteLine(Add(ref number1, number2));
    Console.WriteLine(number1);
    Console.ReadLine();
}
static int Add(ref int number1, int number2)
{
    number1 = 30;
    return number1 + number2;
}
```
- **Method Overloading:**

```
static int Multiply( int num1, int num2)
 {
     return num1 * num2;
 }
 static int Multiply(int num1, int num2,int num3)
 {
     return num1 * num2 * num3;
 }
 ```

- **Params Keyword:** Çok fazla overloading işlemi yapmak gerektiğinde kullanılabilir.<br>

```
static void Main(string[] args)
{
    Console.WriteLine(Add(1,6, 5, 2));
    Console.ReadLine();
}
 
static int Add( params int[] numbers)
{
    return numbers.Sum();
}
```
- **Arrays:**
- 1.dizi tanımlama yolu: <br>

```
string[] studens = new string[3];
studens[0]= "Fatma";
studens[1]= "Mehmet";
studens[2]= "Özlem";
```
- 2.dizi tanımlama yolu: <br>

```string[] students = { "Fatma", "Mehmet", "Özlem" };```
- **Multidimensional Array:**

```
-3 satır 2 sutünlü çok boyutlu dizi
string[,] regions = new string[3, 2];
regions[0, 0] = "ankara";
regions[0, 1] = "konya";
regions[1, 0] = "istanbul";
regions[1, 1] = "kocaeli";
regions[2, 0] = "izmir";
regions[2, 1] = "manisa";
```
 
```
string[,] regions = new string[3, 2]
{
    {"ankara","konya"},
    {"istanbul","kocaeli"},
    {"izmir","manisa"},
};
```
- **for loops:**
```
string[] students = { "Fatma", "Mehmet", "Özlem" };
for (int i = 0; i < students.Length; i++)
{
    Console.WriteLine(i + 1 + ":" + students[i]);

}
```
-"GetUpperBound" metodu bir dizinin en büyük indeksini döndürür.<br>
```
 for (int i = 0; i <= regions.GetUpperBound(0); i++)
 {
     for ( int j = 0;  j <= regions.GetUpperBound(1); j++)
     {
         Console.WriteLine(regions[i, j]);
     }
 }
```
-**for each döngüsü:**
```
foreach (var i in students)
{
    Console.WriteLine(i);
}
```
