# Islamic-Lecture (ইসলামিক লেকচার সিডিএন ও ডাটাবেজ)
> DeenOne অফিসিয়াল ইসলামিক অডিও লেকচার ভান্ডার, সিডিএন অডিও স্ট্রিমিং ও দ্বৈতভাষিক (Bangla & English) API ডাটাবেজ।

[![CDN jsDelivr](https://data.jsdelivr.com/v1/package/gh/riadmonir/Islamic-Lecture/badge)](https://www.jsdelivr.com/package/gh/riadmonir/Islamic-Lecture)
[![Total Speakers](https://img.shields.io/badge/Speakers-6-teal)](islamic_lectures.json)
[![Total Lectures](https://img.shields.io/badge/Lectures-23-blue)](islamic_lectures.json)

---

## 📖 পরিচিতি (Overview)
এই রিপোজিটরিটি মূলত **DeenOne** অ্যাপ্লিকেশনের জন্য খ্যাতনামা ইসলামিক স্কলারদের অডিও লেকচার সংগ্রহ, ফাস্ট সিডিএন স্ট্রিমিং এবং সেন্ট্রালাইজড দ্বৈতভাষিক JSON API প্রদান করে।

এখানে প্রতিটি স্কলারের জন্য স্বতন্ত্র ফোল্ডারে অডিও ফাইলসমূহ সুবিন্যস্ত রয়েছে এবং রুট ডিরেক্টরিতে বিদ্যমান [`islamic_lectures.json`](islamic_lectures.json) ফাইলের মাধ্যমে অতি দ্রুত অডিও প্লেয়ারে স্ট্রিম ও ক্যাশ করা যায়।

---

## 🌐 গ্লোবাল সিডিএন এন্ডপয়েন্ট (Global CDN Endpoints)

### ১. মাস্টার লেকচার JSON API (Master Lectures JSON):
- **jsDelivr CDN (Fast Global Delivery):**  
  [`https://cdn.jsdelivr.net/gh/riadmonir/Islamic-Lecture@main/islamic_lectures.json`](https://cdn.jsdelivr.net/gh/riadmonir/Islamic-Lecture@main/islamic_lectures.json)
- **GitHub Raw Fallback:**  
  [`https://raw.githubusercontent.com/riadmonir/Islamic-Lecture/main/islamic_lectures.json`](https://raw.githubusercontent.com/riadmonir/Islamic-Lecture/main/islamic_lectures.json)

### ২. অডিও স্ট্রিমিং ইউআরএল প্যাটার্ন (Audio Streaming URL Pattern):
- **jsDelivr CDN:**  
  `https://cdn.jsdelivr.net/gh/riadmonir/Islamic-Lecture@main/{folder_name}/{audio_file_name}.mp3`
- **GitHub Raw:**  
  `https://raw.githubusercontent.com/riadmonir/Islamic-Lecture/main/{folder_name}/{audio_file_name}.mp3`

---

## 📂 রিপোজিটরি ফোল্ডার স্ট্রাকচার (Repository Structure)

```plaintext
Islamic-Lecture/
├── islamic_lectures.json       # মূল দ্বৈতভাষিক JSON ডাটাবেজ (Master API)
├── lectures.json               # অল্টারনেট সিম্পল পাথ এন্ডপয়েন্ট
├── README.md                   # পূর্ণাঙ্গ ডকুমেন্টেশন
├── mizanur_rahman_azhari/      # মিজানুর রহমান আজহারী
│   ├── README.md
│   ├── .gitkeep
│   └── sundor_choritrer_gurutto.mp3 ...
├── tarek_monowar/              # মাওলানা তারেক মনোয়ার
│   ├── README.md
│   ├── .gitkeep
│   └── rasuler_onupom_adorsho.mp3 ...
├── delwar_hossain_sayeedi/     # আল্লামা দেলাওয়ার হোসাইন সাঈদী
│   ├── README.md
│   ├── .gitkeep
│   └── surah_ar_rahman_tafsir.mp3 ...
├── shaykh_ahmadullah/          # শায়খ আহমাদুল্লাহ
│   ├── README.md
│   ├── .gitkeep
│   └── moner_oshanti_dur_korar_upay.mp3 ...
├── abdul_hi_saifullah/         # মাওলানা আব্দুল হাই সাইফুল্লাহ
│   ├── README.md
│   ├── .gitkeep
│   └── kiyamoter_alamot.mp3 ...
└── dr_zakir_naik/              # ড. জাকির নায়েক
    ├── README.md
    ├── .gitkeep
    └── quran_o_adhunik_biggan.mp3 ...
```

---

## 🎙️ ক্যাটাগরি ও স্কলার তালিকা (Scholars & Categories)

| স্কলার / ক্যাটাগরি | Category / Scholar (English) | ফোল্ডার (Folder) | মোট লেকচার |
|---|---|---|:---:|
| **মিজানুর রহমান আজহারী** | Mizanur Rahman Azhari | `mizanur_rahman_azhari/` | 6 |
| **মাওলানা তারেক মনোয়ার** | Maulana Tarek Monowar | `tarek_monowar/` | 5 |
| **আল্লামা দেলাওয়ার হোসাইন সাঈদী** | Allama Delwar Hossain Sayeedi | `delwar_hossain_sayeedi/` | 5 |
| **শায়খ আহমাদুল্লাহ** | Shaykh Ahmadullah | `shaykh_ahmadullah/` | 3 |
| **মাওলানা আব্দুল হাই সাইফুল্লাহ** | Maulana Abdul Hi Saifullah | `abdul_hi_saifullah/` | 2 |
| **ড. জাকির নায়েক** | Dr. Zakir Naik | `dr_zakir_naik/` | 2 |

---

## 🧩 JSON ডাটা স্কিমা (JSON Data Schema)

JSON ফাইলের প্রতিটি লেকচার অবজেক্টে নিম্নলিখিত ফিল্ডসমূহ শতভাগ দ্বৈতভাষিক (Bangla & English) সাপোর্টে অন্তর্ভুক্ত রয়েছে:

```json
{
  "id": "mra_001",
  "title_bn": "সুন্দর চরিত্রের গুরুত্ব ও আখলাক",
  "title_en": "Importance of Noble Character and Akhlaq",
  "author_name_bn": "মিজানুর রহমান আজহারী",
  "author_name_en": "Mizanur Rahman Azhari",
  "category_bn": "মিজানুর রহমান আজহারী",
  "category_en": "Mizanur Rahman Azhari",
  "category_id": "mizanur_rahman_azhari",
  "topic_bn": "আখলাক ও আত্মশুদ্ধি",
  "topic_en": "Manners & Self-Purification",
  "duration": "42:15",
  "duration_seconds": 2535,
  "file_name": "sundor_choritrer_gurutto.mp3",
  "audio_url": "https://cdn.jsdelivr.net/gh/riadmonir/Islamic-Lecture@main/mizanur_rahman_azhari/sundor_choritrer_gurutto.mp3",
  "fallback_url": "https://raw.githubusercontent.com/riadmonir/Islamic-Lecture/main/mizanur_rahman_azhari/sundor_choritrer_gurutto.mp3"
}
```

---

## 🚀 DeenOne অ্যাপ্লিকেশনে ব্যবহারের পদ্ধতি (Integration in App)

1. অ্যাপ শুরু বা লেকচার পেজ ওপেন করার সময় সরাসরি সিডিএন এন্ডপয়েন্ট থেকে JSON ফেচ করা যাবে:
   ```
   GET https://cdn.jsdelivr.net/gh/riadmonir/Islamic-Lecture@main/islamic_lectures.json
   ```
2. ইউজার ইন্টারফেসে ভাষা নির্বাচন (`bn` বা `en`) অনুযায়ী `title_bn` বা `title_en`, এবং `author_name_bn` বা `author_name_en` ডায়নামিকালি প্রদর্শিত হবে।
3. অডিও প্লেয়ার বা ExoPlayer-এ সরাসরি `audio_url` সেট করে স্ট্রিমিং বা অফলাইনে ডাউনলোড সংরক্ষণ করা যাবে।
