# Temel JavaScript Bilgileri

Bu doküman, JavaScript programlama diline yeni başlayanlar için temel kuralları ve dikkat edilmesi gereken noktaları açıklamaktadır.  

let ile değişken oluşturulur.<br>
console.log ile konsola çıktı yazdırılır.

Bu iki komutun ne işe yaradığını bilmemiz şuanlık yeterli gelecektir. İleride detaylı açıklaması yapılacaktır.

Aşağıda JavaScript yazım kuralları ve genel bilgiler örneklerle desteklenerek sunulmuştur.

---

## Noktalı Virgül (`;`) Kullanımı

JavaScript'te her komutun sonunda **noktalı virgül (`;`)** koymak iyi bir programlama alışkanlığıdır. Noktalı virgül, derleyiciye "bu komut burada sona eriyor" mesajı verir.

### Neden Önemli?

JavaScript çoğu zaman satır sonlarında noktalı virgül koymasanız bile otomatik olarak ekleyebilir. Buna **Otomatik Noktalı Virgül Ekleme (Automatic Semicolon Insertion - ASI)** denir. Ancak ASI bazen beklenmedik sonuçlara veya hatalara yol açabilir.

Bu yüzden noktalı virgül kullanımı hataları önlemek ve kodun daha okunabilir olması için önerilir.

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

JavaScript'te **string (karakter dizisi)** oluştururken **tırnak işaretleri (quotes)** kullanılır. Tırnak işaretlerinin açıldığı gibi aynı türde kapatılması gereklidir. Ayrıca, açılan parantezlerin de mutlaka kapatılması gerekir.

### Tırnak İşaretleri

JavaScript'te üç farklı tırnak türü kullanılır:

- Çift tırnak: `"Merhaba Dünya"`
- Tek tırnak: `'Merhaba Dünya'`
- Backtick (ters tırnak): `` `Merhaba Dünya` `` (template literal olarak da kullanılır)

### Neden Önemli?

Tırnakların uyumsuz kullanımı veya eksik kapatma, kodun hata vermesine neden olur.

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
Süslü parantez `{ }` ile oluşturulan bloklar, bir arada çalışan komutlar topluluğudur ve JavaScript yapılarının temel yapı taşlarından biridir.

## Büyük-Küçük Harf Duyarlılığı ve Boşluk Karakterleri

JavaScript, **büyük-küçük harf duyarlıdır (case-sensitive)**. Yani `degisken`, `Degisken` ve `DEGISKEN` farklı isimler olarak kabul edilir ve farklı değişkenlerdir.

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

## `<script>` Etiketi ve Dosya Yolları
JavaScript kodları HTML sayfasına `<script>` etiketi ile eklenir. Kodları sayfaya ekleme yöntemleri şunlardır:

### 1. Satır İçi (Inline) JavaScript
Kod doğrudan HTML içinde yazılabilir:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Inline JS Örneği</title>
</head>
<body>
    <h1>Merhaba Dünya!</h1>

    <script>
        alert("Bu satır içi JavaScript örneğidir!");
    </script>
</body>
</html>
```

### 2. Harici JavaScript Dosyası
Kodları ayrı bir `.js` dosyasında tutmak tercih edilen yöntemdir. Bu, okunabilirliği ve bakım kolaylığını artırır.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Harici JS Örneği</title>
    <script src="./script.js"></script> <!-- Dosya yolu belirtilir -->
</head>
<body>
    <h1>Merhaba Dünya!</h1>
</body>
</html>
```

`script.js` dosyası içeriği:

```js
alert("Bu bir harici JavaScript dosyasıdır!");
```

Dosya Yolları
- . → geçerli dizin
- .. → bir üst dizin
- Birden fazla `.js` dosyası eklenebilir:
  
```js
<script src="dosya1.js"></script>
<script src="dosya2.js"></script>
```

### 3. Performans Önerisi
- `<script>` etiketi `<head>` içinde veya `<body>` sonunda kullanılabilir.
- `<body>` sonunda kullanmak sayfanın daha hızlı yüklenmesini sağlar.

## Yazım düzenine (indentation) dikkat edilmelidir.  
Kodun okunabilirliği ve bakımının kolay olması için girintileme kurallarına uymak önemlidir.  
JavaScript'te blok yapıları `{ }` ile belirlenir; iç içe geçmiş yapılar uygun şekilde girintilenmelidir.

  ```js
  // Doğru girintileme
  function selamla(isim) {
      if (isim) {
          console.log(`Merhaba, ${isim}!`);
      } else {
          console.log("Merhaba!");
      }
  }

  // Yanlış girintileme
  function selamla(isim){
  if(isim){
  console.log(`Merhaba, ${isim}!`);
  }else{
  console.log("Merhaba!");
  }
  }
```

### Özet
Düzenli yazım, kodun okunmasını kolaylaştırır ve hata yapma riskini azaltır.

## Satır uzunluğu ve okunabilirlik
Eğer bir kod satırı çok uzunsa, yatayda takip zorlaşır. Bu yüzden uzun satırlar **alt satırlara bölünerek** yazılmalıdır. Bu, kodun okunabilirliğini ve bakımını artırır.

```js
  // Uzun ve okunması zor
  let sonuc = sayi1 + sayi2 + sayi3 + sayi4 + sayi5 + sayi6 + sayi7;

  // Daha okunabilir şekilde satırlara bölünmüş
  let sonuc = sayi1 + sayi2 + sayi3 +
              sayi4 + sayi5 + sayi6 +
              sayi7;
```

### Özet
Kod satırlarını makul uzunlukta tutmak ve gerektiğinde alt satırlara bölmek, kodu takip etmeyi ve hataları önlemeyi kolaylaştırır.

## `"use strict"` kullanımı  
JavaScript'te `"use strict"` ifadesi, kodu **sıkı modda** çalıştırır. Bu mod, hatalara karşı daha duyarlı, güvenli ve temiz bir kod yazmanızı sağlar.  
  Örneğin, değişkenleri tanımlamadan kullanmak veya silinemez özellikleri değiştirmek gibi hataları tespit eder.

  ```js
  // Sıkı mod kullanılmadan
  x = 10; // Hata vermez, global değişken oluşturulur
  console.log(x); // 10

  // Sıkı mod ile
  "use strict";
  y = 20; // Hata: y tanımlanmadan kullanılamaz
  console.log(y);
```

### Özet
**"use strict"** kullanmak, hataları erken tespit etmenizi sağlar ve kodunuzu daha güvenli hale getirir. Tarayıcılar modern kodlarda genellikle bunu otomatik uygular, ancak manuel eklemek iyi bir pratiktir.

# Bazı Temel Komutlar ve Kullanımları

## Yorum Satırları

Kodun okunabilirliğini artırmak için yorum satırları kullanılır.  
Yorumlar, tarayıcı veya JavaScript motoru tarafından çalıştırılmaz, sadece geliştiriciye açıklama yapar. 

- **Tek Satırlık Yorum (`//`)**  
`//` işareti ile başlayan ifadeler satırın sonuna kadar yorum kabul edilir.  
Daha çok kısa notlar veya tek satırlık açıklamalar için kullanılır.  

```js
// Bu değişken kullanıcı adını tutar
let kullaniciAdi = "Ahmet";
```

- **Çok Satırlık Yorum `(/* ... */)`**
`/*` ile başlar, `*/` ile biter. Arada kalan her şey yorum olarak kabul edilir.
Daha uzun açıklamalar veya kod bloklarını geçici olarak kapatmak için tercih edilir.

 ```js
/*
  Bu fonksiyon kullanıcıyı selamlar.
  Parametre olarak isim alır.
*/
function selamVer(isim) {
  console.log("Merhaba " + isim);
}
```

- **Kısayollar**
  - <kbd>Ctrl + /</kbd> → Seçili satır(lar)ı tek satır yorum haline getirir.
  - <kbd>Ctrl + Shift + /</kbd> → Seçili kısmı çok satırlı yorum haline getirir.

### Not
Yorumları, kodun ne yaptığını değil, neden yapıldığını açıklamak için kullan. Kod zaten ne yaptığını göstermelidir.

## Alert() ile Ekrana Popup Çıkarma
Tarayıcıda ekrana **uyarı (popup) penceresi** çıkarmak için kullanılır.  
Örneğin hata mesajı, bilgi mesajı veya kullanıcıya bildirim vermek için tercih edilir.  

```js
  alert("Merhaba Dünya!");
```

İçine değişken de yazılabilir.

```js
let isim = "Derda";
alert(isim); // ekranda "Derda" çıkar
```

Virgül ile birden fazla değişken yazılamaz onun yerine + kullanılmalıdır.

```js
let isim = "Derda";
let soyisim = "Yetim";
alert(isim + soyisim);
```

`+` işareti kullanarak string ve değişkenleri yan yana ekleyebilirsin.

```js
let isim = "Derda";
alert("Merhaba " + isim + "!");
```

Template literal (şablon string) ile `${}` kullanarak değişkenleri metinle birlikte gösterebilirsin. Bu kullanım ile değişkenler farklı yazım tarzında olduğu için kod okunabilirliğini artırabilirsin.
Bu özellik sadece backtick ``` ` ``` işaretiyle yazılır:

```js
let isim = "Derda";
let yas = 25;
alert(`Merhaba ${isim}, yaşın ${yas}`);
```

## console.log() ile Konsola Yazı Yazdırma

JavaScript'te **console.log()** fonksiyonu, kod çalışırken bilgi veya değişken değerlerini **tarayıcı konsoluna** yazdırmak için kullanılır. Bu, hata ayıklama (debug) ve kodu takip etme açısından çok faydalıdır.

```js
console.log("Merhaba Dünya");
```

`+` operatörü ile birleştirerek kullanım:
```js
let isim = "Ahmet";
console.log("Kullanıcı adı: " + isim); // Çıktı: Kullanıcı adı: Ahmet
```

`${}` ( Template literalle ) birlikte kullanım:
```js
let yas = 25;
let isim = "Ahmet";
console.log(`Kullanıcı adı: ${isim}, Yaşı: ${yas}`); // Çıktı: Kullanıcı adı: Ahmet, Yaşı: 25
```

Birden fazla değişkeni virgülle ayırarak kullanım (+ ile de yapılabilir):
```js
let meslek = "Öğrenci";
let yas = 25;
let isim = "Ahmet";
console.log("Bilgiler:", isim, yas, meslek); // Çıktı: Ahmet 25 Öğrenci
```

## Prompt() ile Veri Alma
`prompt()` fonksiyonu, kullanıcıdan veri almak için kullanılan en temel yöntemlerden biridir.<br>

```js
let isim = prompt("Lütfen isminizi giriniz:", "Varsayılan");
```

- İlk parametre `("Lütfen isminizi giriniz:")` kullanıcıya gösterilecek mesajdır.
- İkinci parametre `("Varsayılan")` giriş kutusunda hazır olarak yazılı gelen değerdir (kullanıcı isterse değiştirir, isterse boş bırakabilir).

### Not:
- Varsayılan değer yazılmayacaksa bile `"" (çift tırnak)` kullanmak iyi bir pratiktir.
- Kullanıcı ***Tamam*** butonuna basarsa girilen değer ***string*** olarak döner.
- Kullanıcı ***İptal*** butonuna basarsa fonksiyon ***null*** döndürür.

```js
let yas = prompt("Yaşınızı giriniz:", "");
alert("Girdiğiniz yaş: " + yas);
```

Eğer 25 girilirse, ekranda: `Girdiğiniz yaş : 25` <br>
Eğer iptal edilirse, ekranda: `Girdiğiniz yaş : null`

### Not:
- Girilen değer her zaman **string** tipindedir.
- Kullanıcı ***iptal*** ettiğinde değer **null** olur.
- Varsayılan değer eklemek kullanıcı deneyimini iyileştirir yoksa bile boş bırakmak daha sağlıklıdır.

## confirm() ile Onay Alma

JavaScript'te kullanıcıdan **onay** almak için `confirm()` fonksiyonu kullanılır.  
Bu fonksiyon, ekranda **Tamam** ve **İptal** seçenekleri olan bir dialog kutusu açar.

- Eğer kullanıcı **Tamam** derse: `true` döner  
- Eğer kullanıcı **İptal** derse: `false` döner

```js
let eminMisin = confirm("Devam etmek istiyor musunuz?");

if (eminMisin) {
    console.log("Kullanıcı devam etmek istedi.");
} else {
    console.log("Kullanıcı iptal etti.");
}
```
Bu şekilde `confirm()` ile basit onay kontrolleri yapabilirsiniz.

## Özet 

JavaScript'te kullanıcıyla etkileşim kurmak için üç temel fonksiyon vardır *(console.log() doğrudan kullanıcıyla değil, geliştiriciyle etkileşim kurar)* :

1. **alert()** → Ekrana bilgi veya uyarı mesajı gösterir.  
2. **prompt()** → Kullanıcıdan veri girmesini sağlar; girilen değer string olarak döner.  
3. **confirm()** → Kullanıcıdan onay alır; `true` veya `false` döner.
4. **console.log()** → Konsola istenilen veriyi yazdırır.

### Örnek Kullanım

```js
// alert ile mesaj gösterme
alert("Merhaba! JavaScript'e hoş geldiniz.");

// prompt ile kullanıcıdan bilgi alma
let isim = prompt("Lütfen adınızı giriniz:", "Ahmet");
console.log("Kullanıcı adı:", isim);

// confirm ile onay alma
let eminMisin = confirm("Devam etmek istiyor musunuz?");
if (eminMisin) {
    console.log("Kullanıcı devam etmek istedi.");
} else {
    console.log("Kullanıcı iptal etti.");
}
```
## document.write() ile HTML Sayfasına Yazı Yazdırma

JavaScript'te `document.write()` metodu, HTML sayfasına **doğrudan içerik yazdırmak** için kullanılır. Sayfa yüklendiği anda çalışır ve belirtilen metni veya ifadeyi doğrudan ekrana basar.

```js
document.write("Merhaba Dünya");
```

`+` operatörü ile birleştirerek kullanım:
```js
let isim = "Ahmet";
document.write("Merhaba " + isim + "!");

let yas = 25;
document.write("Adınız: " + "Ali" + "<br>" + "Yaşınız: " + yas); // <br> = html'de alt satıra geçme tagıdır.
```

### Not:
`document.write()` sayfa yüklendikten sonra çalıştırılırsa, mevcut içeriği silip sadece yazdırılan ifadeyi gösterir. Bu yüzden modern projelerde kullanımı önerilmez. Daha güvenli ve kontrollü yöntemler tercih edilmelidir.

### Özet

- `document.write()` → HTML sayfasına direkt içerik yazar.
- `+` ile metinler ve değişkenler birleştirilebilir.
- Günümüzde genellikle öğrenme amaçlı veya basit denemelerde kullanılır.

## innerHTML ile HTML elementinin içine ekleme ve düzenleme yapma

`innerHTML`, bir HTML elementinin içine **HTML kodu da dahil olmak üzere** içerik eklemek için kullanılır. Yani sadece düz metin değil, HTML etiketlerini de çalıştırır.

```html
<p id="mesaj"></p>

<script>
  document.getElementById("mesaj").innerHTML = "Merhaba <b>Dünya</b>";
</script>
```

Çıktı (sayfada) : Merhaba Dünya

### Avantajları
- HTML etiketlerini çalıştırabilir (`<b>`, `<i>`, `<br>` vb.).
- Dinamik olarak içerik oluşturmak için esnek bir yöntemdir.

### Dezavantajları
- Kullanıcıdan alınan veriler direkt olarak `innerHTML` ile eklenirse, **XSS (Cross-Site Scripting)** gibi güvenlik açıklarına neden olabilir. Bu yüzden dışarıdan gelen verilerde `innerHTML` kullanımı önerilmez.

## textContent ile HTML elementinin içine ekleme düzenleme yapma

`textContent`, bir HTML elementine **sadece düz metin** ekler. HTML etiketleri yazılsa bile çalıştırılmaz, düz yazı olarak gösterilir.

```html
<p id="mesaj"></p>

<script>
  document.getElementById("mesaj").textContent = "Merhaba <b>Dünya</b>";
</script>
```

Çıktı (sayfada) : Merhaba &lt;b&gt;Dünya&lt;/b&gt;

### Avantajları
- Daha **güvenli** bir yöntemdir çünkü HTML etiketlerini çalıştırmaz.
- Kullanıcıdan alınan veriler eklenirken tercih edilmelidir.

### Dezavantajları
- HTML etiketleri çalıştırılamaz. Yalnızca düz metin eklenir.

## Özet

- **document.write()** → Sayfa yüklenirken içerik basar, sonradan kullanılırsa tüm sayfayı siler. Modern projelerde önerilmez genelde eğitim amaçlı kullanılır.  
- **innerHTML** → HTML etiketleriyle içerik ekler/değiştirir, ancak kullanıcı verilerinde XSS riski vardır.  
- **textContent** → Sadece düz metin ekler, HTML çalıştırmaz. En güvenli yöntemdir.  
