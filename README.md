🚀 CyberPy-Instruct-TR: Siber Güvenlik & Defansif Python Veri Seti

CyberPy-Instruct-TR, siber güvenlik uzmanları, "legal hacker"lar ve sistem yöneticileri için özel olarak tasarlanmış, yüksek kaliteli bir Türkçe Python komut dosyası (script) veri setidir.

Bu veri seti, LLM (Büyük Dil Modelleri) modellerini siber güvenlik otomasyonu, defansif programlama ve tehdit avcılığı (threat hunting) konularında eğitmek veya ince ayar (fine-tuning) yapmak için oluşturulmuştur.
📌 Veri Seti Hakkında

    Dil: %100 Türkçe (Teknik terimler korunmuştur).

    Format: original, alpaca ve gpt formatlarında 3 farklı JSONL çıktısı.

    İçerik: Ağ tarama, log analizi, kriptografi, süreç izleme, zafiyet tespiti ve güvenli dosya yönetimi gibi 100'den fazla alt senaryo.

🛠 Üretim Metodolojisi

Veri seti üretilirken "kısır döngü" ve "kendini tekrar etme" sorunlarını aşmak için Dinamik Senaryo Enjeksiyonu ve RAM Tabanlı Hafıza Filtreleme teknikleri kullanılmıştır.

Her bir örnek, bir Ana Konu (örn: Network Security) ve bir Senaryo Hedefi (örn: Cloud uyumlu / Gizli çalışan) eşleştirilerek üretilmiştir. Bu sayede modelin yaratıcılığı en üst seviyeye çıkarılmıştır.
📂 Veri Yapısı

Veri seti üç ana formatta sunulmaktadır:
1. Alpaca Formatı
code JSON

{
  "instruction": "Kendi kendini imha edebilen gizli bir ağ tarayıcı yaz.",
  "input": "",
  "output": "Açıklama metni ve ```python\n# kodlar buraya...```"
}

2. GPT (Chat) Formatı
code JSON

{
  "messages": [
    {"role": "user", "content": "Soru..."},
    {"role": "assistant", "content": "Cevap ve Kod..."}
  ]
}

🛡 Kapsanan Temel Konular
Kategori	Açıklama
Network Security	Socket programlama, port tarama, sniffing araçları.
Defensive Coding	Parola güvenliği (bcrypt/argon2), güvenli API erişimi.
Forensics & Logs	Anomali tespiti, PCAP analizi, sistem günlük izleme.
Malware Analysis	Sandbox otomasyonu, bellek dökümü analizi.
Automation	Subprocess yönetimi, güvenli SFTP dosya transferi.
🚀 Kullanım (Fine-Tuning)

Bu veri setini kullanarak kendi siber güvenlik asistanınızı eğitmek için Hugging Face trl veya unsloth kütüphanelerini kullanabilirsiniz:
code Python

from datasets import load_dataset

dataset = load_dataset("kullanici_adin/CyberPy-Instruct-TR")
# Fine-tuning işlemlerine başlayın...

⚠️ Sorumluluk Reddi (Disclaimer)

Bu veri seti eğitim amaçlıdır. İçerisinde bulunan scriptler siber güvenlik farkındalığını artırmak ve defansif araçlar geliştirmek için tasarlanmıştır. Veri setinin kötü niyetli kullanımından doğacak sorumluluk kullanıcıya aittir. Sadece yasal (legal) sınırlar içerisinde kullanınız.
🤝 Katkıda Bulunma

Yeni konular eklemek veya mevcut scriptleri iyileştirmek isterseniz lütfen bir Pull Request gönderin veya bir Issue açın.
🌟 Yıldızlamayı Unutmayın!

Bu veri seti işinize yaradıysa projeyi yıldızlayarak destek olabilirsiniz!
GitHub için İpucu:

    Tags (Etiketler): python, dataset, cybersecurity, turkish, nlp, fine-tuning, llm, qwen.

    License: Veri setini yayınlarken MIT veya Apache 2.0 lisansı eklemeyi unutma.

    Hugging Face: Eğer veri seti büyükse (5000+ satır), dosyayı GitHub'a yüklemek yerine Hugging Face Datasets'e yükleyip GitHub üzerinden oraya link verebilirsin.

Bu proje Apache License 2.0 temel alınarak lisanslanmıştır; ancak bu veri seti ve beraberindeki kodlar için aşağıdaki ÖZEL KISITLAMA geçerlidir:

⚠️ TİCARİ KULLANIM YASAĞI (NON-COMMERCIAL RESTRICTION):
Bu veri setinin (CyberPy-Instruct-TR) tamamı veya bir kısmı; herhangi bir ticari ürün, ücretli servis, kapalı kaynaklı model eğitimi veya gelir getiren herhangi bir faaliyet için KULLANILAMAZ.

    İzin Verilenler: Akademik araştırma, kişisel öğrenme, hobi projeleri, açık kaynaklı ve ücretsiz araçların geliştirilmesi.

    İzin Verilmeyenler: Veri setinin satılması, ücretli bir API'ye dahil edilmesi, kurumsal/ticari modellerin eğitilmesi.

Bu kısıtlama, Apache License 2.0'ın sağladığı genel izinlerin üzerinde öncelikli bir hak teşkil eder. Ticari kullanım talepleri için lütfen proje sahibi ile iletişime geçiniz.

