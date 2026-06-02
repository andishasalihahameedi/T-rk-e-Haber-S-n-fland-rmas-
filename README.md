# Türkçe Haber Metinleri Sınıflandırma (Turkish News Classification via LoRA)

Bu proje; Türkçe haber metinlerini doğru kategorilere (Ekonomi, Yaşam, Kültür-Sanat, Seyahat vb.) sınıflandırmak amacıyla modern Büyük Dil Modellerinin (LLM) parametre verimli bir şekilde ince ayar (Fine-Tuning) yapılmasını kapsamaktadır.

## 🚀 Kullanılan Modeller ve Yöntem
Proje kapsamında 3 farklı açık kaynaklı dil modeli üzerinde denemeler yapılmış ve performansları kıyaslanmıştır:
1. **Gemma (e2b)**
2. **Qwen 2.5 (1.5B)**
3. **SmolLM2**

Eğitim süreçlerinde modellerin tüm parametrelerini güncellemek yerine bellek dostu ve hızlı bir yöntem olan **LoRA (Low-Rank Adaptation)** mimarisi ve **PEFT (Parameter-Efficient Fine-Tuning)** kütüphanesi kullanılmıştır.

## 📊 Veri Kümesi
Projede **Interpress Haber Veri Kümesi** temel alınarak hazırlanan prompt tabanlı `interpress_prompt_sample_dataset` kullanılmıştır. Metinler belirli şablonlara (Başlık, İçerik) göre modellere beslenmiş ve modelden doğrudan kategori tahmini (Ham Çıktı) üretmesi istenmiştir.

## 🛠️ Kurulum ve Çalıştırma

Bağımlılıkları yüklemek için:
```bash
pip install -r requirements.txt
