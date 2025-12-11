# **Genetik Algoritma ile Web Sunucusu Ayarlarının Optimizasyonu (Senaryo 8)**

Bu proje, **BLG307 Yapay Zeka Sistemleri** dersi kapsamında verilen Senaryo 8 için geliştirilmiştir.
Amaç, bir web sunucusunun performansını belirleyen iki temel parametre olan **CPU çekirdek sayısı (x₁)** ve **RAM miktarı (x₂)** değerlerini **Genetik Algoritma (GA)** kullanarak optimize etmek ve maksimum performansı sağlayan sunucu ayarlarını bulmaktır.

---

## 📌 **Projenin Amacı**

Optimizasyon yapılacak performans fonksiyonu:

[
y = 5x_1 + 7x_2 - 0.1x_1^2 - 0.2x_2^2
]

Bu fonksiyon:

* CPU ve RAM arttıkça performansı artırır,
* Ancak çok yüksek donanım değerlerini **maliyet** ve **verimsizlik** açısından cezalandırır.

Amaç, kısıtlar altında **maksimum performansı** veren x₁ ve x₂'yi bulmaktır.

### **Kısıtlar:**

* Minimum CPU çekirdeği:
  [
  x_1 \ge 4
  ]

* Donanım sınırı:
  [
  x_1 \cdot x_2 \le 512
  ]

### **Değişken Aralıkları:**

* x₁ (CPU) ∈ [4, 12]
* x₂ (RAM) ∈ [4, 64]

Kısıt ihlali yapan bireylere **500 puan ceza** uygulanmaktadır.

---

## ⚙️ **Kullanılan Yöntem: Genetik Algoritma (GA)**

Projede kullanılan GA bileşenleri:

* **Popülasyon Oluşturma:**
  10 bireyden oluşan rastgele başlangıç popülasyonu.

* **Fitness Fonksiyonu:**
  Amaç fonksiyonu + kısıt kontrolü + ceza yöntemi.

* **Seçilim (Selection):**
  **Rank temelli seçim** yöntemi kullanılır.

* **Çaprazlama (Crossover):**
  Tek noktalı çaprazlama uygulanır.

* **Mutasyon (Mutation):**
  %20 ihtimal ile 0.5 büyüklüğünde rastgele değişim uygulanır.

* **Elitizm:**
  Her neslin en iyi bireyi bir sonraki nesle doğrudan aktarılır.

* **Jenerasyon Sayısı:**
  Kullanıcı tarafından belirlenebilir (varsayılan 20).

* **Görselleştirme:**
  Fitness değerinin jenerasyonlara göre değişimi grafikle gösterilir.

---

## ▶️ **Çalıştırma Adımları**

Aşağıdaki adımlar Google Colab üzerinde çalıştırmak içindir.

### **1. Colab’de .ipynb dosyasını açın**

* Dosyayı yükleyin veya GitHub üzerinden açın.

### **2. Tüm hücreleri sırayla çalıştırın**

Hücreler şu sırayı içerir:

1. Projenin açıklaması ve amaç
2. Kütüphanelerin import edilmesi
3. Amaç fonksiyonu ve kısıtların tanımlanması
4. Popülasyonun rastgele oluşturulması
5. Seçilim, çaprazlama ve mutasyon fonksiyonları
6. Genetik Algoritma döngüsü
7. En iyi bireyin çıktısı
8. Fitness grafiği
9. Sonuç yorumları

### **3. Sonuçları inceleyin**

Algoritma çalıştığında şu çıktılar görünür:

* Optimum CPU çekirdek sayısı (x₁)
* Optimum RAM miktarı (x₂)
* Elde edilen maksimum performans skoru
* Fitness evrim grafiği

---

## 🛠️ **Kurulum Yönergeleri**

Bu proje **Google Colab** üzerinde çalışmak üzere tasarlanmıştır ve ek kurulum gerektirmez.

Yerel çalıştırmak isteyenler için gerekli kütüphaneler:

```bash
pip install numpy
pip install matplotlib
```

---

Hazır! Bundan sonra direkt olarak **README.md içine yapıştırabilirsin**.
İstersen ek olarak:

* görsel/grafik ekleme alanı
* kod blokları
* sonuç değerlendirmesi
* proje sahibi bölümü

de ekleyebilirim.
