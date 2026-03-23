## Javascript Nedir ?
- JavaScript, başlangıçta web sayfalarına etkileşim ve dinamizm kazandırmak amacıyla geliştirilmiştir.
- Bu dilde yazılan kod parçalarına **betik (script)** denir ve doğrudan HTML içerisine eklenerek sayfa yüklendiği anda çalıştırılabilir.
- JavaScript kodları, diğer birçok dilin aksine derleme sürecine ihtiyaç duymadan doğrudan çalıştırılır. Bu özelliği sayesinde JavaScript, çalışma mantığı açısından birçok programlama dilinden farklıdır.

## Neden JavaScript ?
- JavaScript ilk ortaya çıktığında “LiveScript” adıyla geliştirilmiştir. Ancak o dönemde Java dili çok popüler olduğu için, daha fazla dikkat çekmesi amacıyla adı JavaScript olarak değiştirilmiştir.
- Zamanla JavaScript gelişerek kendi standartları olan **ECMAScript** yapısına sahip, bağımsız bir programlama dili haline gelmiştir.
- Günümüzde Java ile isim benzerliği dışında herhangi bir bağlantısı yoktur.

## JavaScript Ne Yapabilir ?
- Günümüz JavaScript’i güvenli bir dildir ve bellek veya işlemciye doğrudan erişmez.  
- Ne yapabileceği büyük ölçüde çalıştığı ortama bağlıdır.
  - Örneğin:
    - `node.js` ile dosya okuma, yazma ve ağ işlemleri yapılabilir.
    - Tarayıcıda ise kullanıcı ile etkileşim ve sayfa yönetimi sağlanır.

### Tarayıcıda JavaScript’in Yapabildikleri

- HTML içeriğini değiştirme ve yeni içerik ekleme  
- CSS stillerini değiştirme  
- Kullanıcı etkileşimlerini yakalama (tıklama, mouse hareketi vb.)  
- Sunucuya istek gönderme (API, veri alma/gönderme)  
- Tarayıcı verilerini yönetme (cookie, localStorage)  


## JavaScript Ne Yapamaz ?

Tarayıcıdaki JavaScript, kullanıcı güvenliği için bazı kısıtlamalara sahiptir.

### Sınırlamalar

- Bilgisayardaki dosyalara doğrudan erişemez.  
- İşletim sistemine müdahale edemez.  
- Kamera ve mikrofonu izinsiz kullanamaz.  
- Farklı siteler arasında veri alışverişi yapamaz.  

Bu kurallar **Same Origin Policy (Aynı Kaynak Politikası)** olarak adlandırılır.

> Not:
>
> Dosya seçme veya kamera kullanma gibi işlemler **yalnızca kullanıcı izniyle** yapılabilir.
> Bu kısıtlamalar tarayıcı içindir, sunucu tarafında (örneğin Node.js) daha geniş yetkiler vardır.

## JavaScript’i Eşsiz Yapan Nedir ?
JavaScript’i öne çıkaran temel özellikler şunlardır:

- HTML ve CSS ile tamamen uyumlu çalışır.  
- Basit işlemler kolayca yapılabilir.  
- Tüm modern tarayıcılarda desteklenir ve varsayılan olarak aktiftir.  

Bu özellikler sayesinde JavaScript, web geliştirmede en yaygın kullanılan dillerden biridir.

## Şartname
**ECMA-262 Şartnamesi**, JavaScript dilinin resmi tanımını ve en derin teknik detaylarını içeren kaynaktır.  

- Resmi ve teknik bir dil kullanıldığından, ilk kez okuyanlar için anlaşılması zordur.  
- En güvenilir kaynak olmasına rağmen, hızlı ve kolay başvuru için uygun değildir.  

Erişim linkleri:  
- Son taslak: [ECMA-262](https://tc39.es/ecma262/)  
- Yeni özellikler ve öneriler: [TC39 Proposals](https://github.com/tc39/proposals)

## Kılavuz
**MDN (Mozilla) JavaScript Reference**, örnekler ve kılavuzların yer aldığı kapsamlı bir kaynaktır.  
İstediğiniz konuları derinlemesine incelemek için harika bir başvuru kaynağıdır.  

- Erişim: [MDN JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference)  
- Google arama: `"MDN [term]"` örneğin parseInt için [Google Arama](https://google.com/search?q=MDN+parseInt)  

**MSDN – Microsoft kılavuzu** da çok sayıda bilgi içerir.  
- JavaScript (JScript olarak da adlandırılır) ve Internet Explorer konularını kapsar.  
- Erişim: [MSDN](http://msdn.microsoft.com/)  
- Örnek arama: `"RegExp MSDN"` veya `"RegExp MSDN jscript"`

## Özelliklerin Desteği
JavaScript sürekli gelişen bir dil olduğu için yeni özellikler eklenmektedir.  
Bu özelliklerin tarayıcılarda veya motorlarda desteklenip desteklenmediğini kontrol etmek için kullanabileceğiniz kaynaklar:

- [Can I Use](http://caniuse.com) – Özellik bazlı destek tabloları sunar.  
  Örnek: JavaScript `cryptography` desteği → [caniuse.com/#feat=cryptography](http://caniuse.com/#feat=cryptography)

- [Kangax Compatibility Table](https://kangax.github.io/compat-table) – Dil özelliklerinin farklı motorlarda desteklenip desteklenmediğini gösterir.

---

### 📚 Konu Akışı
 
**➡️ Sonraki:** [**Temel Kavramlar**](01-Temel-kavramlar.md)   
