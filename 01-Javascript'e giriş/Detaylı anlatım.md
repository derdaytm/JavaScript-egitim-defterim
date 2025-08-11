# Temel JavaScript Bilgileri

JavaScript programlama diline yeni başlayanlar için temel kurallar ve dikkat edilmesi gereken noktalar bu dokümanda açıklanmıştır. Kod yazarken uyulması gereken standartlar, kodun doğru ve tutarlı çalışmasını sağlar.

Aşağıda JavaScript yazım kuralları ve genel bilgiler örneklerle desteklenerek sunulmuştur.

---

## Noktalı Virgül (`;`) Kullanımı

JavaScript'te her komutun sonunda **noktalı virgül (`;`)** koymak iyi bir programlama alışkanlığıdır. Noktalı virgül, derleyiciye "bu komut burada sona eriyor" mesajı verir.

### Neden Önemli?

JavaScript çoğu zaman satır sonlarında noktalı virgül koymazsanız bile otomatik olarak ekleyebilir. Buna **Otomatik Noktalı Virgül Ekleme (Automatic Semicolon Insertion - ASI)** denir. Ancak ASI bazen beklenmedik sonuçlara veya hatalara yol açabilir.

Bu yüzden noktalı virgül kullanımı hataları önlemek ve kodun daha okunabilir olması için önerilir.

### Örnekler

```js
// Noktalı virgül kullanımı (doğru ve önerilen)
let x = 5;
let y = 10;
console.log(x + y);

// Noktalı virgül kullanılmadığında da çalışabilir, ancak risklidir
let a = 3
let b = 4
console.log(a + b)

// Otomatik noktalı virgül eklenmediğinde sorun oluşabilir
let c = 5
let d = 10
[1, 2, 3].forEach(n => console.log(n))

// Bu kod, [1, 2, 3] dizisini, 10 değişkenine atama gibi algılayıp hata verir.
```
## Tırnak İşaretleri ve Parantez Kullanımı

JavaScript'te **string (karakter dizisi)** oluştururken tırnak işaretleri (quotes) kullanılır. Tırnak işaretlerinin açıldığı gibi aynı türde kapatılması gereklidir. Ayrıca, açılan parantezlerin de mutlaka kapatılması gerekir.

### Tırnak İşaretleri

JavaScript'te üç farklı tırnak türü kullanılır:

- Çift tırnak: `"Merhaba Dünya"`
- Tek tırnak: `'Merhaba Dünya'`
- Backtick (ters tırnak): `` `Merhaba Dünya` `` (template literal olarak da kullanılır)

### Neden Önemli?

Tırnakların uyumsuz kullanımı veya eksik kapatma, kodun hata vermesine neden olur.

### Örnekler

```js
// Doğru kullanımlar:
let mesaj1 = "Merhaba Dünya";
let mesaj2 = 'JavaScript öğreniyorum';
let mesaj3 = `Bugün hava çok güzel`;

// Yanlış kullanımlar (hata verir):
let yanlis1 = "Merhaba Dünya'; // Çift tırnak açıldı, tek tırnak kapandı
let yanlis2 = 'JavaScript öğreniyorum"; // Tek tırnak açıldı, çift tırnak kapandı
let yanlis3 = "Eksik kapatma; // Tırnak kapatılmadı
```
### Parantezler

Fonksiyon çağrıları, koşul blokları, döngüler gibi yapılarda açılan parantezlerin mutlaka kapatılması gerekir.

```js
// Doğru örnek
if (x > 5) {
  console.log("x 5'ten büyük");
}

// Yanlış örnek - kapatma eksik
if (x > 5 {
  console.log("Hata!");
}
```
### Özet
Kodunuzda tırnakları ve parantezleri açtığınız gibi kapatmaya dikkat edin. Bu basit kural, sözdizimi hatalarını önler ve kodunuzu çalıştırır hale getirir.

## Kod Blokları ( `{ }` )

JavaScript'te süslü parantezler `{ }`, bir veya daha fazla komutun bir arada olduğu bölgeyi, yani **blok**u tanımlar. Bloklar genellikle koşul ifadeleri, döngüler veya fonksiyon tanımları gibi yapılarda kullanılır.

```js
// if koşulunda blok kullanımı
if (sayi > 0) {
  console.log("Sayı pozitif.");
  console.log("Blok içindeki ikinci komut.");
}

// Fonksiyon tanımı ve bloğu
function selamla() {
  console.log("Merhaba!");
  console.log("Fonksiyon bloğu burada biter.");
}
```
### Blok kullanmanın önemi
  - Birden fazla komutun birlikte çalışmasını sağlar.
  - Koşul, döngü veya fonksiyon gibi yapılar içinde gruplandırma yapar.
  - Blok dışındaki kodlardan değişken kapsamını (scope) kontrol eder.

### Özet
Süslü parantez { } ile oluşturulan bloklar, bir arada çalışan komutlar topluluğudur ve JavaScript yapılarının temel yapı taşlarından biridir.

## Büyük-Küçük Harf Duyarlılığı ve Boşluk Karakterleri

JavaScript, **büyük-küçük harf duyarlıdır** (case-sensitive). Yani `degisken`, `Degisken` ve `DEGISKEN` farklı isimler olarak kabul edilir ve farklı değişkenlerdir.

```js
let isim = "Ali";
let Isim = "Ayşe";

console.log(isim);  // Çıktı: Ali
console.log(Isim);  // Çıktı: Ayşe
```
Ayrıca, JavaScript boşluk karakterlerini derlemez yani kodun çalışmasını engellemez, ancak kodun okunabilirliği için boşluklar önemlidir. Aşağıdaki iki kod da aynı işlevi yapar:
```js
// Boşluklu ve düzenli yazım
if (sayi > 10) {
  console.log("Sayı 10'dan büyük");
}

// Boşluksuz yazım (okunması zor)
if(sayi>10){console.log("Sayı 10'dan büyük");}
```
### Özet
  - Değişken, fonksiyon ve diğer isimlerde büyük/küçük harf farkı önemlidir.
  - Boşluklar kodun çalışmasını etkilemez ama okunabilirliği artırır.
