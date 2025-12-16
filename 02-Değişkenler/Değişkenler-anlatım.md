#Değişkenler

## Değişken Türleri (Primitive & Non-Primitive)

JavaScript’te değişkenler **iki ana gruba** ayrılır: **Primitive (ilkel)** ve **Non-Primitive (referans)** tipler.  
Bu ayrım, verilerin **nasıl saklandığını**, **nasıl kopyalandığını** ve **nasıl karşılaştırıldığını** anlamak için önemlidir.

---

### Primitive (İlkel) Tipler
Primitive tipler **tek bir değer** tutar ve **değiştirilemezdir (immutable)**.  
Bir primitive değişken kopyalandığında, **değerin kendisi kopyalanır**.

**Primitive veri tipleri:**
- `Number`
- `String`
- `Boolean`
- `Null`
- `Undefined`

**Özellikleri:**
- Bellekte değeriyle birlikte tutulur
- Karşılaştırmalar **değer üzerinden** yapılır
- İçeriği sonradan değiştirilemez (yeni değer atanır)

---

### Non-Primitive (Referans) Tipler
Non-primitive tipler **birden fazla veri** tutabilir ve bellekte **referans (adres)** ile saklanır.

**Non-primitive veri tipleri:**
- `Object`
- `Array`
- `Function`

**Özellikleri:**
- Değişken, verinin kendisini değil **adresini** tutar
- Karşılaştırmalar **referans üzerinden** yapılır
- İçerikleri değiştirilebilir (mutable)

> ⚠️ İki farklı object veya array, içeriği aynı olsa bile `===` ile karşılaştırıldığında **eşit kabul edilmez**, çünkü referansları farklıdır.

---

### Kısa Özet
- **Primitive** → Tek değer, immutable, değer üzerinden karşılaştırılır  
- **Non-Primitive** → Referans tutar, mutable, adres üzerinden karşılaştırılır
