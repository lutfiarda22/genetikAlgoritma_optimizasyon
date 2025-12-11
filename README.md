🖥️ Genetik Algoritma ile Web Sunucusu Ayarlarının Optimizasyonu (Senaryo 8)

Bu proje, BLG307 Yapay Zeka Sistemleri dersi kapsamında verilen Senaryo 8 için geliştirilmiştir.
Amaç, bir web sunucusunun performansını belirleyen iki temel parametre olan:

x₁ → CPU çekirdek sayısı

x₂ → RAM miktarı (GB)

değerlerini Genetik Algoritma (GA) kullanarak optimize etmek ve maksimum performansı veren ayar kombinasyonunu bulmaktır.

🎯 Amaç Fonksiyonu

Projede kullanılan performans fonksiyonu:

𝑦
=
5
𝑥
1
+
7
𝑥
2
−
0.1
𝑥
1
2
−
0.2
𝑥
2
2
y=5x
1
	​

+7x
2
	​

−0.1x
1
2
	​

−0.2x
2
2
	​


Bu fonksiyon:

CPU ve RAM arttıkça sunucu performansını yükseltir,

Ancak çok yüksek donanım değerlerini verimsizlik ve maliyet sebebiyle cezalandırır.

📌 Kısıtlar

Kodda kullanılan kısıt denetimleri:

x₁ ⋅ x₂ ≤ 512

x₁ ≥ 4

🔢 Değişken Aralıkları

CPU (x₁): [4, 12]

RAM (x₂): [4, 64]

Kısıt ihlali durumunda bireylere 500 puan ceza uygulanır.

⚙️ Kullanılan Genetik Algoritma Bileşenleri

Başlangıç popülasyonu: 10 birey

Seçim yöntemi: Rank temelli seçim

Çaprazlama: Tek noktalı çaprazlama

Mutasyon: %20 ihtimal, 0.5 büyüklüğünde

Elitizm: En iyi birey her nesilde korunur

Nesil sayısı: Kullanıcı tarafından belirlenebilir (varsayılan 20)

🔄 Algoritma Akışı

Her nesilde:

En iyi CPU–RAM kombinasyonu görüntülenir

Bireylerin uygunluk skorları hesaplanır

En başarılı birey bir sonraki nesle elit birey olarak taşınır

Son nesilde maksimum performans yazdırılır

Jenerasyonlara göre performans değişim grafiği oluşturulur

📊 Çıktılar

Algoritma çalıştırıldığında:

Önerilen optimum CPU çekirdek sayısı

Önerilen optimum RAM miktarı

Maksimum performans skoru

Fitness (uygunluk) grafiği

elde edilir.

📁 Proje Hakkında

Bu proje, web sunucusu donanım ayarlarının optimizasyonunu Genetik Algoritma ile gerçekleştirmektedir.
Kısıt kontrollü GA, elitizm ve rank selection gibi yöntemler kullanılarak yüksek performanslı ayar kombinasyonu bulunur.
