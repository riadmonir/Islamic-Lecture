# Islamic-Lecture (ইসলামিক লেকচার সিডিএন ও ডাটাবেজ)
> DeenOne অফিসিয়াল ইসলামিক অডিও লেকচার ভান্ডার, Cloudflare Pages / Workers ও jsDelivr হাই-স্পিড অডিও স্ট্রিমিং এবং দ্বৈতভাষিক (Bangla & English) API ডাটাবেজ।

[![CDN jsDelivr](https://data.jsdelivr.com/v1/package/gh/riadmonir/Islamic-Lecture/badge)](https://www.jsdelivr.com/package/gh/riadmonir/Islamic-Lecture)
[![Cloudflare Pages](https://img.shields.io/badge/Cloudflare-Wrangler%20Ready-F38020?logo=cloudflare)](wrangler.json)
[![Total Speakers](https://img.shields.io/badge/Speakers-7-teal)](islamic_lectures.json)
[![Total Lectures](https://img.shields.io/badge/Lectures-27-blue)](islamic_lectures.json)

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
├── index.html                  # Cloudflare Pages পোর্টাল ও ওয়েব অডিও প্লেয়ার
├── wrangler.json               # Cloudflare Workers / Pages Static Assets কনফিগ
├── wrangler.toml               # Wrangler ডেপ্লয় কনফিগ
├── package.json                # npm স্ক্রিপ্ট ও ডিপেন্ডেন্সি
├── islamic_lectures.json       # মূল দ্বৈতভাষিক JSON ডাটাবেজ (Master API)
├── lectures.json               # অল্টারনেট সিম্পল পাথ এন্ডপয়েন্ট
├── README.md                   # পূর্ণাঙ্গ ডকুমেন্টেশন
├── mizanur_rahman_azhari/      # মিজানুর রহমান আজহারী
│   ├── README.md
│   ├── .gitkeep
│   ├── জান্নাতের জন্য পাগল হওয়া এক আনসারী সাহাবার ঘটনা.mp3 (15.5 MB)
│   └── jannater_jonno_pagol_howa_ek_ansari_sahabar_ghotona.mp3
├── abu_toha_adnan/             # আবু ত্বহা মুহাম্মদ আদনান
│   ├── README.md
│   └── .gitkeep
├── tarek_monowar/              # মাওলানা তারেক মনোয়ার
│   ├── README.md
│   └── .gitkeep
├── delwar_hossain_sayeedi/     # আল্লামা দেলাওয়ার হোসাইন সাঈদী
│   ├── README.md
│   └── .gitkeep
├── shaykh_ahmadullah/          # শায়খ আহমাদুল্লাহ
│   ├── README.md
│   └── .gitkeep
├── abdul_hi_saifullah/         # মাওলানা আব্দুল হাই সাইফুল্লাহ
│   ├── README.md
│   └── .gitkeep
└── dr_zakir_naik/              # ড. জাকির নায়েক
    ├── README.md
    └── .gitkeep
```

---

## 🎙️ ক্যাটাগরি ও স্কলার তালিকা (Scholars & Categories)

| স্কলার / ক্যাটাগরি | Category / Scholar (English) | ফোল্ডার (Folder) | মোট লেকচার |
|---|---|---|:---:|
| **মিজানুর রহমান আজহারী** | Mizanur Rahman Azhari | `mizanur_rahman_azhari/` | 7 |
| **আবু ত্বহা মুহাম্মদ আদনান** | Abu Toha Muhammad Adnan | `abu_toha_adnan/` | 3 |
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
  "title_bn": "জান্নাতের জন্য পাগল হওয়া এক আনসারী সাহাবার ঘটনা",
  "title_en": "The Story of an Ansari Sahabi Who Yearned for Paradise",
  "author_name_bn": "মিজানুর রহমান আজহারী",
  "author_name_en": "Mizanur Rahman Azhari",
  "category_bn": "মিজানুর রহমান আজহারী",
  "category_en": "Mizanur Rahman Azhari",
  "category_id": "mizanur_rahman_azhari",
  "topic_bn": "সাহাবাদের ঈমানী জিন্দেগী ও জান্নাতের আকাঙ্ক্ষা",
  "topic_en": "Faith of the Sahabah & Yearning for Paradise",
  "duration": "19:12",
  "duration_seconds": 1152,
  "file_name": "jannater_jonno_pagol_howa_ek_ansari_sahabar_ghotona.mp3",
  "audio_url": "https://cdn.jsdelivr.net/gh/riadmonir/Islamic-Lecture@main/mizanur_rahman_azhari/jannater_jonno_pagol_howa_ek_ansari_sahabar_ghotona.mp3",
  "fallback_url": "https://raw.githubusercontent.com/riadmonir/Islamic-Lecture/main/mizanur_rahman_azhari/jannater_jonno_pagol_howa_ek_ansari_sahabar_ghotona.mp3"
}
```

---

## 🚀 Cloudflare Wrangler ডেপ্লয়মেন্ট (Deploying with Wrangler)

রিপোজিটরিতে সরাসরি `wrangler.json`, `wrangler.toml` ও `index.html` কনফিগার করা রয়েছে।  
Cloudflare ড্যাশবোর্ড থেকে অটো-বিল্ড কমান্ড:
```bash
npx wrangler deploy
```
কিংবা লোকাল টার্মিনালে:
```bash
npm run deploy
```
