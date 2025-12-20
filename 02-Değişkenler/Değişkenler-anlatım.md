# Değişkenler

## Değişken Türleri (Primitive & Non-Primitive)

JavaScript’te değişkenler **ikiye ayrılır**: **Primitive** ve **Non-Primitive**.


### Primitive (İlkel) Tipler
- Tek bir değer tutarlar ve karşılaştırılabilirler.
- Basit veri tipleridir.

**Primitive tipler:**
- Number
- String
- Boolean
- Null
- Undefined

### Non-Primitive Tipler
- Birden fazla veri tutabilirler ancak karşılaştırılamazlar.
- Daha karmaşık yapılardır

**Non-Primitive tipler:**
- Object
- Array
- Function

---

## let ile Değişken Tanımlama

JavaScript’te değişken tanımlamak için **let**  ve **const** kullanılır.  
Her tür veri atanabilir.

### Değişken İsimlendirme Kuralları
- Rakam ile başlayamaz.
- Boşluk içermez.
- Genelde **camelCase** kullanılır (küçük harfle başlayıp sonrasında diğer kelimeye büyük harfle başlamanması).
- Sadece **`$`** ve **`_`** özel karakter olarak kullanılabilir diğer özel karakterler kullanılamaz.
- `-` (orta tire) kullanılamaz.
- JavaScript anahtar kelimeleri değişken adı olamaz.

### Değer Atama
- Değişken oluşturulurken değer verilebilir.
- İstenirse **boş** da tanımlanabilir.
- Aynı değişken sonradan farklı türde değer alabilir.

### Örnek
```js
let kullanici = "Ahmet", yas = 25, mesaj;
```

Bu kullanım temiz görünse de, değişkenleri alt alta ve ayrı ayrı tanımlamak daha sağlıklıdır; ancak tek satırda veya virgülle yazmak da bir hata değildir.

### Örnek
```js
let kullanici = "Ahmet",
    yas = 25,
    mesaj;

// ya da

let kullanici = "Ahmet";
let yas = 25;
let mesaj;
```

