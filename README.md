# Gömme Rezervuar Ustası — müşteri sitesi

İstanbul'da gömme rezervuar tamiri yapan işletme için hazırlanan tek dosyalık tanıtım sitesi.
Yayın: GitHub Pages.

## Durum

Site kaynak kodu 2026-09-10'da denetlendi ve kritik hatalar düzeltildi. En önemlisi: Google Ads
dönüşüm etiketinde `event_timeout` eksikti ve fonksiyon her tıklamayı iptal ediyordu — reklam
engelleyicisi olan bir ziyaretçide telefon ve WhatsApp bağlantıları hiç açılmıyordu.

Yapılan düzeltmeler:

- Dönüşüm fonksiyonuna `event_timeout` ve iki güvenlik ağı eklendi; buton her koşulda çalışıyor.
- WhatsApp bağlantıları yeni sekmede açılıyor (önce aynı sekmede açılıp ziyaretçiyi siteden çıkarıyordu).
- Sayfadaki dört `h1` teke indirildi.
- KVKK için Consent Mode v2 ve çerez onay bandı kuruldu.
- Erişilebilirlik: klavye odak çerçevesi, slayta duraklat düğmesi, karusel rolleri, dekoratif SVG'lere `aria-hidden`.
- Performans: görsellerde `loading="lazy"`, sekme arka plandayken animasyonların durması.
- Ölü `meta keywords` etiketi kaldırıldı.

## Eksik

**Görsel dosyaları bu depoda yok.** `index.html` şu dosyaları göreli yoldan çağırıyor:

`resim1.png`, `resim2.png`, `mekanizma.jpg`, `su-kacirma.jpg`, `buton.jpg`,
`hizmet-gorseli.jpg`, `logo-vitra.png`, `logo-kale.png`, `logo-siamp.png`,
`logo-serel.png`, `logo-creavit.png`, `logo-japar.png`

Bu dosyalar depoya eklenene kadar görsellerin yeri boş görünür — sayfa bozulmaz, kırık ikon
göstermez. Dosyalar `index.html` ile aynı klasöre konur, kodda değişiklik gerekmez.

## Bekleyen kararlar

- GA4 ölçüm kimliği (`G-…`) eklenecek mi? Şu an yalnızca Google Ads dönüşüm etiketi kurulu,
  ziyaretçi analitiği toplanmıyor.
- Google Ads dönüşüm etiketinin (`AW-18265217831/…`) hesapta doğru olduğu panelden teyit edilmeli.

---

Site: [DijiKod](https://mrmerkus.github.io/dijikod-ornekler/)
