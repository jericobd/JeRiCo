# JeRiCo অ্যান্ড্রয়েড অ্যাপ

এটি আপনার ওয়েবসাইট (https://www.jericobd.xyz) কে মোবাইল অ্যাপে রূপান্তর করার Android Studio প্রজেক্ট।

## অ্যাপের ফিচার
- সম্পূর্ণ ফুল-স্ক্রিন ওয়েবসাইট (কার্ট, লগইন, অর্ডার সব আগের মতোই কাজ করবে)
- নিচে টেনে রিফ্রেশ (pull-to-refresh) ও লোডিং বার
- ব্যাক বাটনে আগের পেজে যাওয়া
- ইন্টারনেট না থাকলে সুন্দর অফলাইন পেজ
- কল (tel:), ইমেইল ও WhatsApp লিংক ফোনের অ্যাপে খোলে
- Facebook / YouTube / TikTok / Twitter লিংক বাইরের অ্যাপে খোলে
- ফাইল আপলোড (রেজিস্ট্রেশন ফর্মের জন্য) ও ডাউনলোড সাপোর্ট

## APK বানানোর দুইটি উপায়

### উপায় ১: Android Studio দিয়ে (কম্পিউটারে)
1. https://developer.android.com/studio থেকে Android Studio ইনস্টল করুন
2. **Open** দিয়ে এই ফোল্ডারটি খুলুন, Gradle Sync শেষ হওয়ার অপেক্ষা করুন
3. মেনু: **Build > Build Bundle(s) / APK(s) > Build APK(s)**
4. `app/build/outputs/apk/debug/app-debug.apk` ফোনে পাঠিয়ে ইনস্টল করুন

### উপায় ২: GitHub দিয়ে (কম্পিউটারে কিছু ইনস্টল ছাড়াই)
1. github.com এ বিনামূল্যে একটি অ্যাকাউন্ট ও নতুন repository খুলুন
2. এই ফোল্ডারের সব ফাইল (`.github` ফোল্ডারসহ) upload করুন
3. **Actions** ট্যাবে গিয়ে **Build APK** চালান (Run workflow)
4. কয়েক মিনিট পর সেখান থেকে `JeRiCo-APK` ডাউনলোড করুন

## Google Play Store এ দিতে চাইলে
- Android Studio তে **Build > Generate Signed App Bundle / APK** দিয়ে signed AAB বানাতে হবে
- Google Play Developer অ্যাকাউন্ট লাগবে (এককালীন $25)
- Play Store নিয়ম অনুযায়ী Privacy Policy পেজ থাকা দরকার

## নিজের মতো বদলানো
| কী বদলাবেন | কোথায় |
|---|---|
| অ্যাপের নাম | `app/src/main/res/values/strings.xml` |
| রঙ | `app/src/main/res/values/colors.xml` |
| আইকন / লোগো | Android Studio: File > New > Image Asset |
| ওয়েবসাইট URL | `MainActivity.kt` এর `HOME_URL` |
| ভার্সন নম্বর | `app/build.gradle.kts` এর `versionCode` / `versionName` |
