# ByabshaGhor — Marketing Plan & Content Ideas

> Promotion material for "ব্যবসা ঘর" POS. Assets in `pos/_shots/` (modi dokan = `modi-dokan/`, pharmacy = root `01-13` + `web_*`), rendered video in `pos/_shots/_video/`, builder script `pos/_shots/build_video.py`.

---

## 1. Customer Personas → Feature Mapping (core positioning)

**একই অ্যাপ, তিন রকম ব্যবহারকারী** — এটাই main marketing angle। persona ভাগ করা যায়:

### Persona A — "শুধু হিসাব রাখা চায়" (simple-ledger shopkeeper)
- স্টক নিয়ে চিন্তা নেই, শুধু বিক্রি/কেনা/খরচ/দেনা-পাওনা ঢুকিয়ে রাখতে চায়।
- তাড়াহুড়ায় বিক্রি করে দেয়, entry পরে মেলায়।
- **App features:** তালি খাতা mode (সহজ ভিউ — Settings-এ toggle, বা cashOnly auto), কুইক সেল (শুধু টাকার পরিমাণ + payment), দিন বন্ধ (day closing — দিনশেষে নগদ মিলানো), ক্যাশ বক্স, বাকি আদায়।
- **Hook:** *"স্টক-বাটক মাথা না ঘামিয়ে শুধু হিসাব রাখুন — খাতা যতটা সহজ, অ্যাপও ততটা।"*

### Persona B — "পুরো inventory manage করতে চায়" (proper POS user)
- POS দিয়ে বিক্রি + proper purchase entry, batch সহ।
- **App features:** দ্রুত বিক্রি (POS grid + photo), ক্রয় এন্ট্রি (draft/খসড়া status সহ — আধা-আধা রেখে পরে শেষ করা যায়), purchase-এ attachment + **স্মার্ট স্ক্যান** (supplier bill-এর ছবি তুললে AI auto-detect করে item পড়ে নেয়), স্টক adjust/transfer, ব্যাচ picker।
- **Hook:** *"কোম্পানির বিলের ছবি তোলেন — পণ্য নিজে নিজে ঢুকে যাবে। হাতে টাইপ করার যুগ শেষ।"*

### Persona C — Pharmacy owner
- সব Persona B + expiry/batch/prescription।
- **App features:** মেয়াদ/এক্সপায়ারি tracking (dashboard "মেয়াদ শেষ" card), ব্যাচ-ভিত্তিক স্টক, **প্রেসক্রিপশন স্মার্ট স্ক্যান** (ছবি → AI পড়ে → কোর্সের দিন ধরে cart-এ add, RX-required ওষুধে prescription gate), প্রেসক্রিপশন history।
- **Hook:** *"প্রেসক্রিপশনের ছবি তুলুন — কোন ওষুধ কত দিনের, অ্যাপ নিজেই বুঝে নেবে।"*

### Persona D — Multi-staff owner
- মালিক + শিফট-ভিত্তিক কর্মচারী।
- **App features:** আলাদা অ্যাকাউন্ট (owner/staff role), staff-এ limited view (পাওনা/লাভ লুকানো), shift-ভিত্তিক বিক্রির হিসাব, day closing।
- **Hook:** *"কর্মচারী দোকান চালাবে, হিসাব দেখবেন শুধু আপনি।"*

---

## 2. Reports → Persona mapping

| Report | কার জন্য | কী দেখায় |
|---|---|---|
| আজকের হিসাব / Day report | সবার | দৈনিক বিক্রি, বিল সংখ্যা, বাকিতে বিক্রি, লাভ |
| Sales report (web) | B, C | Revenue trend, avg invoice, collected vs due |
| Product profit | B, C | কোন পণ্যে কত লাভ — কোনটা বেশি রাখা উচিত |
| প্রতি invoice-এ লাভ | B | কোন বিক্রিতে কত লাভ হলো (sales list-এ profit column — **gap: UI-তে আরও visible করা যায়**) |
| Parties & Due | A, B | কার কাছে পাবো, কাকে দেবো |
| Expense report | সবার | খরচের ধরন-ভিত্তিক হিসাব |
| Low stock / Expiring | B, C | স্টক কম + মেয়াদ অ্যালার্ট |
| VAT report | বড় ব্যবসা | compliance |
| Product batch view | B, C | প্রতি batch-এর স্টক/দাম/সাপ্লায়ার — **কম দামে কোন supplier দিয়েছে identify করা যায়** (batch cost compare) |

**Report-related marketing idea:** *"কোন supplier সস্তা দেয়, কোন ওষুধে লাভ বেশি — ডেটাই বলে দেবে।"* — purchase analytics + batch price comparison নিয়ে একটা আলাদা content করা যায়।

---

## 3. Feature wishlist status (user ideas vs app)

| আইডিয়া | Status | কোথায় |
|---|---|---|
| শুধু হিসাব (no stock) | ✅ আছে | তালি খাতা mode |
| তাড়াতাড়ি sale → day end মেলানো | ✅ আছে | কুইক সেল + দিন বন্ধ |
| Purchase draft খসড়া | ✅ আছে | ক্রয় এন্ট্রি draft status |
| Bill attachment + auto-detect | ✅ আছে | স্মার্ট স্ক্যান (AI bill OCR) |
| Prescription → auto-detect → cart | ✅ আছে | Rx Smart Scan + POS prescription picker |
| Batch details + batch-wise graph | ✅ আছে | ব্যাচস স্ক্রিন + product detail |
| Cheapest supplier identify | 🟡 আংশিক | batch cost compare দিয়ে হয়; dedicated "best price" view হলে stronger |
| Per-invoice profit in list | 🟡 আংশিক | ডেটা আছে (profit report), sales list-এ column করা যায় |
| Invoice → WhatsApp share + print | ✅ আছে | invoice screen share/print |

**সিদ্ধান্ত:** নতুন feature build না করেই এগুলো নিয়ে কনটেন্ট বানানো যায় — ভিডিওতে "আছে" বললে সত্যিই দেখানো যায়।

---

## 4. Content ideas — Pharmacy ads

1. **মেয়াদ শেষ hook** — *"প্রতি মাসে কত টাকার ওষুধ মেয়াদ শেষ হয়ে ফেলে দেন?"* → expiry card + products shot
2. **স্টক শেষ hook** — *"কাস্টমার এসে জানেন ওষুধ নেই"* → low-stock badge/alert
3. **কোম্পানি/ডিলার হিসাব** — *"ACI, Square-এর rep কত নিলো কে জানে?"* → suppliers screen
4. **দুই শিফট দুই কর্মচারী** — *"সকালে রহিম, রাতে করিম — কে কত বিকলো?"* → users page + owner/staff contrast
5. **প্রেসক্রিপশন scan (hero demo)** — ছবি → cart auto-fill — সবচেয়ে strong pharmacy demo
6. **Bill scan** — *"কোম্পানির চালানের ছবি = ক্রয় এন্ট্রি শেষ"*
7. **খাতা-দেনা WhatsApp reminder** — *"কাকা পরে দেবেন — অ্যাপ মনে করিয়ে দেবে"*

## 4.5. তালি খাতা / Simple Mode — promotion concepts

**Positioning:** "POS software" শব্দটা ছোট দোকানদারকে ভয় দেখায়। এই mode-এর promo খাতা language-এ হবে — পাবো/দেবো/জমা/খরচ। Target: mudi, tea stall, tailor, saloon, hardware, chotpoti stand — যে কোনো ছোট দোকান যারা smartphone চালায় কিন্তু "software" ভাবেন complicated.

1. **"খাতাই অ্যাপ" (positioning concept)**
   - খাতা-র ভাষাই অ্যাপ: পাবো/দেবো/জমা। খাতা বন্ধ → অ্যাপ খোল — একই জিনিস, নিরাপদে।
   - Hook: *"এতদিন খাতায় লিখতেন — এবার ফোনে। একই হিসাব, বই ছাড়া।"*

2. **"তাড়াহুড়ায় বিক্রি, রাতে মিল" (quick-sale + day-close story)**
   - কাস্টমার দাঁড়িয়ে, entry-র সময় নেই → কুইক সেলে শুধু টাকাটা ঢুকাও → রাতে "দিন বন্ধ"-এ সব মিলে যাবে।
   - Hook: *"ভিড়ের সময় entry করার সময় কোথায়? বিক্রি করে যান — রাতে হিসাব নিজে মিলে যাবে।"*
   - Shots: কুইক সেল → দিন বন্ধ → ক্যাশ বক্স

3. **"মোবাইল চালালেই পারবেন" (low-tech reassurance)**
   - বয়স্ক দোকানদারদের fear কাটানো — বড় বাটন, সব Bangla, training লাগে না।
   - Hook: *"অ্যাপ চালাতে জানতে হয় না — খাতা লিখতে জানলেই হবে।"*

4. **"ফোন হারালে খাতা হারায় না" (trust/safety)**
   - খাতা বই ভিজে/পড়ে/হারায় — অ্যাপের ডেটা ক্লাউডে। Offline-ও চলে, net এলে sync।
   - Hook: *"খাতাটা পানিতে ভিজে গেলে? অ্যাপে সব টিকে থাকে।"*

5. **"দিনশেষে ২ মিনিটে হিসাব" (time-saving)**
   - রাতে দোকান বন্ধের আগে এক ঘণ্টা খাতা মেলানো → দিন বন্ধে ২ মিনিট।
   - Hook: *"রাতে খাতা মেলাতে ঘণ্টা লাগে? দুই মিনিটে শেষ করুন।"*

6. **"স্টক না চাইলে খুলতেই হয় না" (differentiator)**
   - অন্য POS-এ প্রতি বিক্রিতে পণ্য/স্টক select করতে হয় — এখানে শুধু টাকা ঢুকালেই হিসাব হয়। পরে চাইলে পুরো POS mode-এ যাওয়া যায়।
   - Hook: *"আজ শুধু হিসাব, কাল পুরো ব্যবসা — আপনার গতিতে।"*
   - Growth story: simple → full POS upgrade path (ভবিষ্যতে lock-in angle)

7. **Shop-type montage series**
   - একই খাতা demo — বিভিন্ন দোকানের footage/shot দিয়ে: mudi, tailor, tea stall, saloon, easybike garage।
   - Hook: *"ছোট দোকান যেকোনো ধরনের হোক — হিসাব একইভাবে সহজ।"*

8. **"বাকি মনে করায় অ্যাপ" (কখা focus)**
   - পাবো/দেবো লিস্ট + WhatsApp রিমাইন্ডার — এটা আবারো strongest khata feature।
   - Hook: *"কার কাছে কত পাবেন — মনে রাখার দায়িত্ব অ্যাপের।"*

## 5. Formats

- Before/After reel (খাতা vs অ্যাপ), 15-20s
- Weekly feature teaser (1 feature = 1 video, 20-30s)
- Day-in-the-life (সকালে dashboard → রাতে day closing)
- Carousel: "খাতা vs ব্যবসা ঘর" ৪-৫ slide
- Real owner testimonial 30s (যদি পাওয়া যায় — strongest)
- FAQ post: "ফার্মেসির জন্য POS — ৫টা প্রশ্ন"

## 5.5. User guideline / tutorial video series — "ব্যবসা ঘর শিখুন"

Promotion-এর বাইরে onboarding/tutorial কনটেন্ট। Format: প্রতি ভিডিও **একটাই কাজ**, ৪৫-৯০ সেকেন্ড, intro card (লোগো+টাইটেল) → numbered step overlay → outro। Voiceover না হলেও Bangla text overlay যথেষ্ট। YouTube playlist + app-এর help-এ link।

**সিরিজ ১ — শুরু করুন (Getting Started)**
1. লগইন — ফোন+পাসওয়ার্ড, OTP/PIN লগইন, ফিঙ্গারপ্রিন্ট চালু
2. দোকান সেটআপ — নাম, শাখা, ইনভয়েস-এ লোগো/ঠিকানা
3. প্রথম পণ্য যোগ — ছবি, দাম, স্টক, ব্যাচ/মেয়াদ
4. কাস্টমার ও সাপ্লায়ার যোগ
5. কর্মচারী অ্যাকাউন্ট — staff role বানানো, লগইন দেওয়া
6. সহজ ভিউ (তালি খাতা) চালু/বন্ধ — কার জন্য কোনটা

**সিরিজ ২ — প্রতিদিনের কাজ (Daily ops — সবচেয়ে important)**
7. কুইক সেল — শুধু টাকা ঢুকিয়ে বিক্রি
8. POS দিয়ে বিক্রি — পণ্য → কার্ট → পেমেন্ট → ইনভয়েস
9. ইনভয়েস প্রিন্ট + WhatsApp শেয়ার
10. বাকিতে বিক্রি ও বাকি আদায় (+ WhatsApp রিমাইন্ডার)
11. ক্রয় এন্ট্রি — খসড়া, পেমেন্ট, বিলের ছবি (স্মার্ট স্ক্যান)
12. খরচ যোগ
13. দিন বন্ধ — দিনশেষে টাকা মেলানো

**সিরিজ ৩ — ফিচার ডিপ-ডাইভ**
14. প্রেসক্রিপশন স্মার্ট স্ক্যান (pharmacy)
15. ব্যাচ ও মেয়াদ ট্র্যাকিং
16. রিপোর্ট — আজকের হিসাব, লাভ, দেনা-পাওনা
17. স্টক কম/শেষ অ্যালার্ট
18. MFS ও মোবাইল রিচার্জ
19. অর্ডার → কোটেশন → ডেলিভারি ফ্লো
20. অফলাইনে চলা ও সিংক

**সিরিজ ৪ — কর্মচারীদের জন্য (staff training)**
21. Staff-এ কী দেখা যায়/কী লুকানো থাকে
22. Staff হিসেবে একটা দিন — সেল, বাকি আদায়, দিন বন্ধ

**Priority (starter pack — প্রথম ৫টা বানালেই onboarding চলবে):** #1 লগইন → #3 পণ্য যোগ → #8 POS বিক্রি → #10 বাকি আদায় → #13 দিন বন্ধ = "আপনার প্রথম দিন" playlist।

**Production:** emulator-এ `adb shell screenrecord` দিয়ে real UI record → ffmpeg-এ intro/outro card + step text overlay + (optional) voiceover। 9:16 vertical।

## 6. Practical notes

- CTA সবসময় রাখো: "আজই ডেমো নিন" + WhatsApp নম্বর।
- Pharmacy audience-এ **মেয়াদ + কোম্পানির টাকা** — দুইটা pain point সবচেয়ে বেশি react করবে।
- Persona split-এর সুবিধা: একই ভিডিও ৩ ভাবে cut করা যায় — A version (শুধু হিসাব), B version (inventory), C version (pharmacy) — ভিন্ন audience-এ ভিন্ন ad.
- Screenshots: modi dokan = `modi-dokan/` (21টা), pharmacy = `01-13` + `web_01-05`; `build_video.py` SEGS list বদলে নতুন video render করা যায়।

## Video pipeline

```bash
cd pos/_shots && python build_video.py   # SEGS list edit → re-render → _video/*.mp4
```
