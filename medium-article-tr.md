# Kaggle Verisinden Braze Canvas’a: İki CRM Müşteri Yolculuğu Tasarlamak

Bir yemek siparişi uygulamasında yeni kullanıcıyla uzun süredir geri dönmeyen müşteriye aynı mesajı göndermek doğru olmaz. Bu kişisel projede, Kaggle tabanlı sipariş verisini Braze’e uygun hale getirerek iki farklı müşteri yaşam döngüsü senaryosu tasarladım: yeni kullanıcı karşılama ve pasif müşteri geri kazanma.

## Projenin amacı

Çalışmanın temel sorusu şuydu: Hazırlanan kullanıcı verisi, doğru hedef kitleleri oluşturmak ve davranışa göre ilerleyen CRM yolculukları tasarlamak için nasıl kullanılabilir?

Projeyi FoodieGo adını verdiğim kurgusal bir yemek siparişi markası üzerinden geliştirdim. Braze ücretsiz deneme ortamı kullandığım için yolculuklar gerçek müşterilere gönderilmedi; taslak olarak tasarlandı ve doğrulandı.

## Veriyi CRM için hazırlamak

Sipariş geçmişini doğrudan Braze’e aktarmak yerine önce Python ve Pandas ile kullanıcı seviyesinde düzenledim. Veri kalitesi kontrolleri, kullanıcı bazlı birleştirme ve Braze uyumlu CSV çıktısı hazırlama adımlarını Kaggle Notebook üzerinde gerçekleştirdim.

Bu aşama, kampanya tasarımından önce gelen önemli bir gerçeği gösterdi: CRM otomasyonu ancak doğru kullanıcı kimlikleri ve anlamlı özelliklerle çalışabilir.

## Segment 1: Yeni kullanıcılar

İlk segment, uygulamayı ilk kez bir haftadan kısa süre önce kullanmış kişileri hedefledi. Bu grubu `New Users–First week` adıyla oluşturdum.

Bu segment için hazırladığım Welcome Journey:

- Canvas başlatıldığında kullanıcıyı hemen içeri alıyor.
- Her kullanıcı yolculuğa yalnızca bir kez giriyor.
- FoodieGo’ya hoş geldin e-postası gönderiyor.
- Başarı göstergesi olarak üç gün içindeki oturum başlangıcını takip ediyor.

Amaç yalnızca bir e-posta göndermek değil, yeni kullanıcının uygulamaya geri dönmesini teşvik etmekti.

## Segment 2: Pasif müşteriler

İkinci segmentte uygulamayı en son 23 Temmuz 2026’dan önce kullanmış kişileri hedefledim. `Inactive Customers – Win Back` segmentinde 81 tahmini kullanıcı bulunuyordu; bu sayı demo workspace’in %8,1’ine karşılık geliyordu.

Bu sayı bir kampanya sonucu değil, hedef kitle büyüklüğüdür.

## Davranış bazlı Win-Back yolculuğu

Win-Back Canvas’ında önce “Seni özledik” e-postası gönderiliyor. Ardından Action Paths, kullanıcının üç gün içinde uygulamada yeni bir oturum başlatıp başlatmadığını değerlendiriyor.

- `Returned to App`: Uygulamaya dönenler Canvas’tan çıkıyor.
- `Everyone Else`: Üç gün içinde dönmeyenlere ikinci bir hatırlatma e-postası gönderiliyor.

Bu yapı sayesinde herkes aynı mesaj dizisini almıyor. Kullanıcı geri döndüyse gereksiz hatırlatma gönderilmiyor; dönmediyse iletişim devam ediyor.

## Neler öğrendim?

Bu projede:

- Kullanıcı yaşam döngüsüne göre segment oluşturmayı,
- Braze Canvas giriş ve yeniden giriş kurallarını,
- E-posta konu, önizleme metni ve CTA tasarımını,
- Dönüşüm olayı tanımlamayı,
- Action Paths ile davranış bazlı dallanma kurmayı,
- Hedef kitle büyüklüğü ile gerçek kampanya sonucunu ayırmayı uyguladım.

## Sınırlamalar

Çalışma Braze ücretsiz deneme ortamında oluşturuldu. Canvas başlatma özelliği bu ortamda desteklenmediği için gerçek gönderim, açılma, dönüşüm veya gelir artışı sonucu bulunmuyor. Proje; veri hazırlama, segmentasyon ve CRM yolculuğu tasarlama yetkinliklerini göstermek amacıyla hazırlanmış kişisel bir vaka çalışmasıdır.

## Proje bağlantıları

- GitHub: eklenecek
- Kaggle Notebook: eklenecek
- Portföy: eklenecek

