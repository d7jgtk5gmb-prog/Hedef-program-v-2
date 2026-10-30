# Hedeflerim v2

Koyu temalı, iPhone ana ekranına eklenebilen PWA prototipi.

## İçerik
- Günlük görevler ve hedefler; son tarih, alt görev metinleri ve tamamlanma.
- Alışkanlık takibi ve ardışık gün serisi.
- Kilo, yağ oranı, adım ve koşu kaydı.
- Kitap ve gitar çalışma günlüğü.
- Gelir, gider, birikim takibi.
- Son 7 günlük alışkanlık grafiği ve geçmiş özeti.
- JSON yedekleme ve geri yükleme.
- PWA manifesti ve service worker.

## Yayımlama
1. ZIP'i açıp tüm dosyaları GitHub repository köküne yükleyin.
2. GitHub → Settings → Pages → Deploy from a branch → `main` → `/ (root)` seçin.
3. HTTPS adresini iPhone Safari'de açın.
4. Paylaş → Ana Ekrana Ekle.

## Önemli teknik kapsam
Bu paket çalışan yerel prototiptir. Veriler aynı cihazın tarayıcı depolamasında tutulur. Gerçek hesap, cihazlar arası otomatik bulut senkronizasyonu ve sunucu yedeklemesi henüz etkin değildir. Bunlar için Supabase/Firebase backend'i, kullanıcı girişi, kullanıcıya özel veritabanı erişim kuralları (RLS), eşitleme ve çakışma çözümü geliştirilmelidir. Gizli servis anahtarlarını istemci dosyalarına koymayın.

Hatırlatıcı kayıtları saklanır; uygulama kapalıyken belirli saatte push bildirimi gönderimi bu prototipte yoktur. Bunun için HTTPS, bildirim izni, service worker ve sunucu taraflı push altyapısı gerekir.

Düzenli olarak Ayarlar bölümünden JSON yedeği indirin; tarayıcı verilerinin silinmesi kayıtları silebilir.
