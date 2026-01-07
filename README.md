# [BURSA TEKNİK ÜNİVERSİTESİ]
## [MÜHENDİSLİK VE DOĞA BİLİMLERİ FAKÜLTESİ] - [BİLGİSAYAR MÜHENDİSLİĞİ]

---

### Proje Kimlik Bilgileri
* **Ders:** Algoritmalar ve Programlama Dersi Donem Projesi
* **Hazirlayan:** [Yusufcan Yılmaz]
* **Ogrenci No:** [25360859310]
* **Gelistirme Dili:** ANSI C (C99 Standartlari)

---

# Uzay Simulasyonu Projesi

Bu yazilim, bir bilim insaninin Gunes sistemindeki 8 farkli gezegende (Merkur'den Neptun'e) fizik deneyleri yapmasini saglayan konsol tabanli bir simulasyon platformudur. Proje, bellek yonetimi ve veri erisimi konularinda **Pointer Aritmetigi** prensiplerini temel alarak gelistirilmistir.

---

## Teknik Zorunluluklar ve Uygulama Standartlari

Proje degerlendirme kriterleri kapsaminda asagidaki akademik kurallar kati bir sekilde uygulanmistir:

> **1. Pointer Mantigi:** Dizilere erisimde `dizi[i]` yapisi tamamen yasaklanmistir. Tum veri erisimleri `*(dizi + i)` seklinde pointer aritmetigi ile dogrudan bellek adresi uzerinden yapilmistir.
> 
> **2. Ternary Operator:** Kutle, sure ve uzunluk gibi negatif olamayacak girislerin kontrolu ve mutlak degere donusturulmesi sadece `(kosul) ? dogru : yanlis` yapisiyla saglanmistir.
> 
> **3. Moduler Fonksiyonlar:** 9 deneyin her biri `main` disinda, parametreleri adres (pointer) olarak alan bagimsiz fonksiyonlarda tanimlanmistir.
> 
> **4. ASCII Uyumlulugu:** Terminal ekranlarinda dogru goruntulenme adina Turkce karakter kullanilmamistir.



---

## Simulasyon Kapsamindaki Deneyler (Ozet Tablo)

Program icerisinde asagidaki 9 temel fizik deneyi, tum gezegenlerin yercekimi ivmeleri altinda es zamanli olarak hesaplanir:

| # | Deney Adi | Fiziksel Formul | Birim |
| :--- | :--- | :--- | :--- |
| 1 | **Serbest Dusme** | $h = 0.5 \cdot g \cdot t^2$ | Metre (m) |
| 2 | **Yukari Atis** | $h_{max} = v_0^2 / (2 \cdot g)$ | Metre (m) |
| 3 | **Agirlik** | $G = m \cdot g$ | Newton (N) |
| 4 | **Potansiyel Enerji** | $E_p = m \cdot g \cdot h$ | Joule (J) |
| 5 | **Hidrostatik Basinc** | $P = \rho \cdot g \cdot h$ | Pascal (Pa) |
| 6 | **Arsimet Kaldirma** | $F_k = \rho \cdot g \cdot V$ | Newton (N) |
| 7 | **Basit Sarkac** | $T = 2\pi\sqrt{L/g}$ | Saniye (s) |
| 8 | **Sabit Ip Gerilmesi** | $T = m \cdot g$ | Newton (N) |
| 9 | **Asansor Deneyi** | $N = m(g \pm a)$ | Newton (N) |



---

## Deney Detaylari ve Metrikleri

1.  **Serbest Dusme Deneyi:** Kullanicidan alinan $t$ suresi boyunca cismin kat ettigi mesafeyi simule eder.
2.  **Yukari Atis Deneyi:** Belirli bir $v_0$ hiziyla dikey olarak firlatilan cismin yercekimi altinda ulasabilecegi tepe noktasini hesaplar.
3.  **Agirlik Deneyi:** Verilen sabit bir kütlenin farklı gezegen yüzeylerindeki agirlik degisimini gosterir.
4.  **Kutlecekimsel Potansiyel Enerji:** Cismin kutlesi ve bulundugu yukseklige bagli olarak sahip oldugu enerjiyi Joule cinsinden hesaplar.
5.  **Hidrostatik Basinc Deneyi:** Sivinin birim hacimdeki kutlesi ($\rho$) ve derinlige ($h$) bagli olarak tabana uyguladigi basinci bulur.
6.  **Arsimet Kaldirma Kuvveti:** Sivi icindeki cismin batan hacmine ($V$) ve sivi yogunluguna gore uygulanan kaldırma kuvvetini simule eder.
7.  **Basit Sarkac Periyodu:** Ip uzunluguna ($L$) bagli olarak sarkacin bir tam salinim suresini saniye cinsinden hesaplar.
8.  **Sabit Ip Gerilmesi Deneyi:** Dusey dogrultuda asili olan bir cismin ip uzerinde olusturdugu gerilme kuvvetini analiz eder.
9.  **Asansor Deneyi:** Asansorun ivmesine ($a$) ve hareket yonune bagli olarak cismin hissettigi etkin agirlik (N) degisimini hesaplar.



---

## Kurulum ve Calistirma

1.  Bilgisayarinizda bir C derleyicisi (GCC, Dev-C++, Visual Studio vb.) oldugundan emin olun.
2.  `proje.c` kaynak kodunu derleyin:
    ```bash
    gcc proje.c -o uzay_simulasyonu -lm
    ```
3.  Uygulamayi calistirin:
    ```bash
    ./uzay_simulasyonu
    ```
4.  Ekranda isminizi girdikten sonra menuden deney secimi yapin.
5.  Programdan cikmak icin secim ekraninda `-1` degerini girin.

---
*Bu proje bireysel olarak Algoritmalar ve Programlama dersi kapsaminda akademik amaclarla gelistirilmistir.*
