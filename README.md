# C# Notları

Bu README dosyası, C# programlama dili hakkında temel bilgileri içerir. C#, çeşitli uygulamalar oluşturmak için kullanılabilir, bunlar arasında etkileşimli web siteleri, mobil uygulamalar, video oyunları, artırılmış gerçeklik (AR), sanal gerçeklik (VR), masaüstü uygulamaları ve back-end hizmetleri bulunur.

## Tür Güvenliği (Type Safety)

C#, bir program yazılırken veri tipinin önceden belirtilmesi gereken bir programlama dilidir. Bu özellik, programların daha güvenli ve hatasız olmasına yardımcı olur.

## Değer Tipleri

C# içerisinde kullanılan bazı temel değer tipleri şunlardır:

- **int:** 32 bitlik tamsayıları temsil eder.
- **long:** 64 bitlik tamsayıları temsil eder.
- **short:** 16 bitlik tamsayıları temsil eder.
- **byte:** 8 bitlik verileri temsil eder.

Not: Daha küçük bir veri için long kullanmak, gereksiz bellek kullanımına yol açabilir.

## bool Veri Tipi

- **bool:** Mantıksal bir veri tipidir ve genellikle şart ifadelerinde kullanılır.

## char Veri Tipi

- **char:** Karakterleri temsil eder ve karakter atamaları için kullanılır. Karakterin ASCII değerini almak için `(int)` kullanılabilir.

## double ve decimal Veri Tipleri

- **double:** Ondalık değerleri temsil eder ve 64 bit kullanır. Tam sayı bir değer de atanabilir, ancak tam tersi mümkün değildir.
- **decimal:** Hassas ondalık değerleri temsil eder ve virgülden sonra daha fazla hassasiyet sunar. double'dan decimal'a dönüştürme işlemini açıkça belirtmek gerekebilir.

## enum Veri Tipi

- **enum:** Belirli bir değer kümesini sembolik olarak temsil etmek için kullanılır. Özellikle sabit değerlerin adlandırılmasına ve gruplandırılmasına yardımcı olur. Örnek olarak haftanın günlerini sembolik olarak temsil eden bir enum tanımlayabiliriz.

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

var Anahtar Kelimesi
`var` anahtar kelimesi, atanan değere göre veri tipini belirler. Örneğin:
```var num = 5; // num otomatik olarak int olarak tanımlanır
num = 'A';   // Şimdi num char tipine sahiptir ve ASCII değeri 65'tir.```
