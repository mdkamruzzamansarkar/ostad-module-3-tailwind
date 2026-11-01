# Module 3 Assignment — সহজ নির্দেশিকা

## কোন ডিজাইনটি করা হয়েছে?

Figma ফাইলে থাকা **বাম পাশের প্রথম ডিজাইনটি** বেছে নেওয়া হয়েছে। দ্বিতীয় ডিজাইনটি অন্তর্ভুক্ত করা হয়নি। পেজের মূল রং, সেকশনগুলোর ক্রম, কার্ড এবং মোবাইল বিন্যাস Figma-তে দেখা ডিজাইন ধরে সাজানো হয়েছে।

## সেকশন ধরে পেজের পরিচয়

1. **Header / Navigation:** Pixelab লোগো, Home, About Us, Our App, Contacts এবং Log In / Sign Up। ছোট স্ক্রিনে মেনু ছোট আইকনে আসে।
2. **Hero:** “We boost growth for your startup business” শিরোনাম, পরিচিতি, Get Started ও Learn More বোতাম, এবং ডান পাশে ছবির জায়গা।
3. **Our Vision & Our Goal:** Graphic Design, Video Editing ও Digital Marketing—তিনটি সার্ভিস কার্ড।
4. **Many Blocks and Components:** বাম পাশে লেখা ও Explore বোতাম, ডানে Figma-র গোলাপি চেয়ার ছবির জায়গা।
5. **What Clients say about us:** ক্লায়েন্টদের মতামত ও ছোট প্রোফাইল-ছবি/অবতারের জায়গা।
6. **Meet The Team:** টিমের সদস্য কার্ড।
7. **Subscribe:** ইমেইল লেখার ঘর ও Subscribe বোতাম।
8. **Footer:** Pixelab নাম, কপিরাইট এবং Framework-এর সংক্ষিপ্ত লেখা।

## ছবির লিংক কোথায় বসাবেন?

`index.html` ফাইলে `PASTE_HERO_IMAGE_URL_HERE` খুঁজে Figma-র প্রথম বড় ব্যক্তির ছবির URL বসান। `PASTE_BLOCKS_IMAGE_URL_HERE`-এর জায়গায় গোলাপি চেয়ারের ছবির URL বসান। উদাহরণ: `src="https://example.com/my-image.png"`। URL না থাকলে ছবির জায়গায় হালকা CSS-ভিত্তিক নমুনা দেখা যাবে। টিম ও testimonial-এর জন্য আপাতত রঙিন initials ব্যবহার করা হয়েছে; আসল ছবি পেলে সেগুলিও `<img>` দিয়ে বদলানো যাবে।

## Laptop-এ কীভাবে খুলবেন?

1. ZIP ফাইলটি Extract / Unzip করুন।
2. Extract করা `ostad-module-3` ফোল্ডারটি VS Code-এ খুলুন: **File → Open Folder**।
3. `index.html`-এ পেজের লেখা ও ছবির লিংক সম্পাদনা করুন; `style.css`-এ বিশেষ ডিজাইন অংশ আছে।
4. পেজটি দেখতে `index.html` ফাইলটি Chrome-এ খুলুন। Tailwind CSS ও Google Fonts লোড করার জন্য ইন্টারনেট সংযোগ লাগবে।

## ফাইলগুলোর কাজ

- `index.html` — পেজের HTML কাঠামো ও Tailwind CSS ক্লাস।
- `style.css` — হিরো ছবির fallback, আইকন, কার্ড, চেয়ার/খাম illustration এবং কিছু custom design।

**মাপের কথা:** Figma-র view-only canvas-এ layer-এর সুনির্দিষ্ট Width/Height panel দেখা যায়নি। তাই মূল desktop অনুপাত ধরে `1170px` content width এবং responsive breakpoints ব্যবহার করা হয়েছে; মোবাইলে কার্ডগুলো এক কলামে সাজায়।

## অনুপাত ও মাপ কোথায় বদলাবেন?

`style.css`-এর শেষের দিকে ছবির অনুপাত দেওয়া আছে:

- Hero-র মানুষটির ছবিতে `object-fit: contain` ব্যবহার করা হয়েছে—পুরো ব্যক্তি দেখা যাবে, ছবি কাটা পড়বে না।
- গোলাপি চেয়ারের ছবির বক্স `aspect-ratio: 2/1`—চওড়া ছবির অনুপাত ধরে।
- ছোট testimonial avatar: `46px × 46px`; টিম avatar: `78px × 78px`—দুটিই বর্গাকার ছবি।
- Desktop কনটেন্ট সর্বোচ্চ `1170px`; Tailwind-এর `sm`, `md`, `lg` breakpoint-এ মোবাইল/ট্যাবলেট/ডেস্কটপ অনুযায়ী কলাম বদলায়।

Figma-র view-only ফাইলে নির্দিষ্ট layer নির্বাচন করে Width/Height-এর মাপ পড়া যায়নি। তাই এগুলো স্ক্রিনে দেখা মূল অনুপাতের ভিত্তিতে সেট করা হয়েছে। ছবির আসল URL পেলে উপরের placeholder-এ বসিয়ে একই অনুপাত রেখে দেখা যাবে।
