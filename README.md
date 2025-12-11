Genetik Algoritma ile Web Sunucusu Ayarlarının Optimizasyonu (Senaryo 8):

Bu proje, BLG307 Yapay Zeka Sistemleri dersi kapsamında verilen Senaryo 8 için geliştirilmiştir.
Amaç, bir web sunucusunun performansını belirleyen iki temel parametre olan:

x₁ → CPU çekirdek sayısı

x₂ → RAM miktarı (GB)

değerlerini Genetik Algoritma (GA) kullanarak optimize etmek ve maksimum performansı veren ayar kombinasyonunu bulmaktır.

Amaç Fonksiyonu:

Projede kullanılan performans fonksiyonu:  y=5x₁​+7x₂​−0.1x₁^2​−0.2x₂^2​
Bu fonksiyon:
ve RAM arttıkça performansı yükseltir,
Ancak çok yüksek donanım değerlerini maliyet/verimlilik açısından cezalandırır.

Kısıtlar
Kodda kullanılan kısıt denetimleri:

x1 ⋅ x2 ≤ 512
x1 ≥ 4
Değişken aralıkları:
CPU (x1) → [4, 12]
RAM (x2) → [4, 64]
Kısıt ihlali durumunda bireylere 500 puan ceza uygulanır.

Kullanılan Genetik Algoritma Bileşenleri
-Başlangıç popülasyonu: 10 birey
-Seçim: Rank temelli seçim
-Çaprazlama: Tek noktalı çaprazlama
-Mutasyon: %20 ihtimal, 0.5 büyüklüğünde
-Elitizm: Her neslin en iyi bireyi doğrudan aktarılır
-Nesil Sayısı: Kullanıcı tarafından belirlenebilir (varsayılan 20)

Algoritma her nesilde:
-En iyi CPU–RAM kombinasyonunu yazdırır
-Uygunluk skorunu hesaplar
-Son nesilde maksimum performansı gösterir
-Ek olarak performansın jenerasyonlara göre değişimi grafik olarak çizilir.
