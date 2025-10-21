# akbank-genai-movie-chatbot
# CineBot: RAG Destekli Film ve Dizi Rehberi

Akbank GenAI Bootcamp kapsamında geliştirilmiş, RAG (Retrieval-Augmented Generation) mimarisi kullanan bir film ve dizi tavsiye chatbot'udur.

## Projenin Amacı
Bu projenin temel amacı, kullanıcılara doğal dilde sordukları sorulara göre film ve dizi önerileri sunmak, yapımlar hakkında bilgi vermek ve bu süreci RAG mimarisi ile zenginleştirerek daha doğru ve bağlama uygun cevaplar üretmektir. Kullanıcılar, "bana bilim kurgu filmi öner" gibi genel sorulardan, "Inception filminin konusu ne?" gibi spesifik sorulara kadar geniş bir yelpazede etkileşim kurabilirler.

## Veri Seti Hakkında Bilgi
Projede, Kaggle üzerinde bulunan [IMDb movies extensive dataset](https://www.kaggle.com/datasets/stefanoleone992/imdb-extensive-dataset) veri seti kullanılmıştır. Bu veri seti, filmlerin adı, yılı, türü, süresi, yönetmeni, oyuncuları ve en önemlisi **özet (plot)** bilgilerini içermektedir. RAG mimarisi için özellikle film özetleri (plot), anlamsal arama (semantic search) yapılarak en uygun filmlerin bulunmasında temel alınmıştır.

## Kullanılan Yöntemler ve Teknolojiler
- **Veri İşleme:** Pandas
- **Vektör Veritabanı:** FAISS (veya ChromaDB) - Film özetlerinin vektör temsillerini saklamak için.
- **Embedding Modeli:** `sentence-transformers` kütüphanesinden bir model (örn. `all-MiniLM-L6-v2`) - Metinleri vektörlere dönüştürmek için.
- **Orkestrasyon (Pipeline):** LangChain - RAG akışını kolayca yönetmek için.
- **Generation Modeli (LLM):** Google Gemini API - Gelişmiş dil anlama ve üretme yetenekleri için.
- **Web Arayüzü:** Streamlit

## Elde Edilen Sonuçlar
Geliştirilen CineBot, kullanıcıların film ve dizi zevklerine uygun, yaratıcı ve bilgilendirici cevaplar üretebilmektedir. RAG mimarisi sayesinde, sadece anahtar kelime eşleşmesi yapmak yerine, sorunun anlamsal içeriğine en uygun filmleri bularak Gemini modeline bağlam olarak sunar. Bu da cevapların doğruluğunu ve kalitesini önemli ölçüde artırmaktadır.

## Web Arayüzü (Demo Linki)
**[Streamlit uygulamanızın linkini buraya ekleyeceksiniz]**
