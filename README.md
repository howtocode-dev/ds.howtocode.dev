# ভূমিকা

**প্রধান লেখক ও সমন্বয়ক**  
[নুহিল মেহেদী](https://nuhil.net/)

**অন্যান্য লেখক ও কন্ট্রিবিউটরদের তালিকা**  
[বিস্তারিত এখানে](https://github.com/howtocode-dev/ds.howtocode.dev/graphs/contributors?type=a)

**প্রারম্ভিকা**  
খুব সহজ ভাষায় যদি বলা হয় তবে - ডাটা সায়েন্স হচ্ছে এরকম একটা বিশেষ জ্ঞান যার মাধ্যমে বিভিন্ন রকমের, গোছালো বা অগোছালো বিশাল পরিমাণ ডাটা থেকে সঠিক এবং অন্তর্নিহিত ব্যবহার উপযোগী তথ্য বের করে আনা যায় \(এটাকে অনেকেই ডাটা মাইনিং-ও বলে থাকেন\)। পরিসংখ্যান, ডাটা অ্যানালাইসিস ও সে সম্পর্কিত বিভিন্ন মেথডের সমন্বয়ে এমন একটি কনসেপ্ট যার মাধ্যমে কোন ডাটা কালেকশনের মধ্যেকার আসল ঘটনা বা বিষয় বের করে আনা যায়। এই বিজ্ঞান বস্তুত অন্যান্য অনেক ফিল্ড থেকে বিভিন্ন তত্ত্ব এবং টেকনিককে ফলো করে কাজ করে। যেমন - গণিত, পরিসংখ্যান, ইনফরমেশন সায়েন্স, কম্পিউটার সায়েন্স মেশিন লার্নিং, ক্লাস্টার অ্যানালাইসিস, ডাটা মাইনিং, ডাটাবেইজ, ডাটা ভিজুয়ালাইজেশন ইত্যাদি। কঠিন করে বলতে গেলে আরও কঠিন হয়ে যাবে। যেহেতু আমরা এই কোর্সে খুব সহজ ভাষায় ডাটা সায়েন্সের মূল ভিত্তি বিষয়ক কিছু ব্যাসিক টপিকের উপর আলোচনা করবো, তাই গুরুগম্ভীর সংজ্ঞায় না যাওয়াই ভালো। বরং, এই কোর্স থেকে একটা আবছা ধারনা নিয়ে পাঠক নিজে থেকেই পরবর্তীতে বিভিন্ন সোর্স অবলম্বন করে আরও গভীর ভাবে এই বিষয়ে পড়াশুনা করতে পারবেন।

অনেকেই ডাটা সায়েন্টিস্ট এবং পরিসংখ্যানবিদের মধ্যে পার্থক্য করতে চান না। তাই তাদের উদ্দেশ্য একটা মজার সংজ্ঞা এখানে দেয়া যেতে পারে - "Data Scientist: Person who is better at statistics than any software engineer and better at software engineering than any statistician!" :\)

দিন দিন ব্যবসা, বিজ্ঞান, গবেষণা, সমাজ ব্যবস্থা, চিকিৎসা, রাজনীতি, মহাকাশবিজ্ঞান ও অনেক রকম ফিল্ডে ডাটা সায়েন্সের প্রয়োজন বেড়েই চলেছে। প্রয়োজন বাড়লেও অনেক বিশাল পরিমাণ ডাটা নিয়ে কাজ করে যথাযথ ফলাফল বা সিদ্ধান্ত আনার জন্য যে পরিমাণ অভিজ্ঞ লোক প্রয়োজন সেটা বর্তমানে নেই। ডাটা \(বিশেষ করে বিগ ডাটা\) নিয়ে যারা কাজ করেন, তাদেরকে বেশ কয়েকটি ভাগে ভাগ করা যায় যেমন - ডাটা ইঞ্জিনিয়ার, ডাটা সায়েনটিস্ট, স্ট্যাটিসটিসিয়ান, ডাটা অ্যানালিস্ট। অনেকেই ইদানীং মনে করছেন দিন দিন যেভাবে ডাটা বাড়ছে সে অনুযায়ী সেই ডাটা গুলো থেকে যথাযথ প্রায়োগিক ফলাফল বের করে আনার মত উপযুক্ত ডাটা প্রফেশনালের অভাবটাই এখন বড় চ্যালেঞ্জ। ডাটার প্রাপ্তি বা কম্পিউটেশন পাওয়ার চ্যালেঞ্জ এর বিষয় নয়।

আসলেই বিগ ডাটা তৈরি হচ্ছে কিভাবে? খেয়াল করলে দেখবেন - দিন দিন মানুষ সবকিছু ডিজিটালাইজ করে ফেলছে। ফেসবুক স্ট্যাটাস থেকে শুরু করে ফটো, লেখা, খবর। সিনেমা থেকে শুরু করে গবেষণার ফল, জরিপ, বিভিন্ন সেন্সর থেকে প্রাপ্ত তথ্য ইত্যাদি ইত্যাদি। বলে শেষ করা যাবে না। এমনকি, পূর্বের জমা হওয়া অ্যানালগ ডাটা গুলোকেও ডিজিটাল রূপ দেয়া হচ্ছে জোড়ে সোরে। IBM এর গবেষণা মতে, বর্তমান পৃথিবীর শতকরা ৯০ ভাগ ডিজিটাল ডাটা তৈরি হয়েছে মাত্র গত ২/৩ বছরে। তার মানে, এই ডাটা বাড়ার পরিমাণ দিন দিন জ্যামিতিক হারে বাড়তেই থাকবে। এই লিঙ্কের ইনফগ্রোফটি দেখতে পারেনঃ [http://bit.ly/2r4JwYS](http://bit.ly/2r4JwYS) একই সাথে এই বিশাল পরিমাণ ডাটার যথাযথ ব্যবহার নিশ্চিত করতে প্রযুক্তিগত উন্নয়নও হচ্ছে উল্লেখ যোগ্য হারে। যেমন - মেশিন লার্নিং, ডিপ লার্নিং এর মাধ্যমে এরকম বিগ ডাটা গুলোকে সঠিকভাবে ব্যবহার করে ডাটার মধ্যেকার প্যাটার্ন খোজা, ক্লাসিফাই করা, ভ্যালু প্রেডিক্ট করা ইত্যাদি কাজ এখন খুবি স্বাভাবিক। এর মাধ্যমে উক্ত ডাটা সম্পর্কিত ফিল্ড গুলো দ্রুত সিদ্ধান্ত গ্রহণ, ভবিষ্যৎ প্রেডিকশন ও অ্যানালাইসিস এর কাজ করতে পারছে সহজে যেগুলো পক্ষান্তরে উক্ত ফিল্ড গুলোকে উন্নয়নের দিকে নিয়ে যাচ্ছে।

সহজ উদাহরণ দিয়ে বুঝতে চাইলে - ধরুন একটা সুপার শপে প্রতিদিন হাজার হাজার ট্র্যাঞ্জেকশন হয়। আবার সেই কেনা বেচার মধ্যে হাজার হাজার আইটেম বিদ্যমান। আবার মনে করুন, সেই সুপার শপের বিভিন্ন লোকেশনে বিভিন্ন ব্র্যাঞ্চ আছে। সব মিলে প্রতিদিন কয়েক লাখ ট্র্যাঞ্জেকশন ঘটে এই ব্র্যান্ডের মোট বেচাকেনায়। এভাবে কয়েকমাস গেলেই যে পরিমাণ ডাটা এই স্টোরের ডাটাবেইজে তৈরি হয় তা কি নিতান্তই মুনাফা হিসাব করা আর স্টক ম্যানেজ করার মধ্যেই সীমাবদ্ধ থাকবে? যদি তাই হয় তাহলে এতো ডাটার মিস-ইউজ ছাড়া আর কিছুই করা হচ্ছে না। বরং, এই ডাটা গুলোকে যদি সঠিকভাবে পর্যালোচনা করে সেখান থেকে বিভিন্ন মজার তথ্য বের করে আনা সম্ভব হয় তাহলে ওই ব্যবসাকে আরও আধুনিক এবং যুগোপযোগী করা সম্ভব।

একটি উদাহরণ দেয়া যাক - একজন ক্রেতা কোন কোন আইটেম মোটামুটি একই সাথে কিনছেন শুধু এটুকু যদি ট্র্যাক করা যায় তাহলে বড় আকারের সুপার শপে ওই আইটেম গুলো পাসাপাশি সাজিয়ে রাখা যেতে পারে। এতে করে ক্রেতা খুশি হবে এবং বিক্রিও বাড়বে। আবার মনে করুন - অনলাইন স্টোরের ক্ষেত্রে একজন ক্রেতা একবার একটা জিনিষ কিনলে তাকে আরেকটা জিনিষ কেনার জন্য সাজেশন দেয়া। এটা করতে কি কি করা যেতে পারে? ধরুন ওই ক্রেতা একটা মাত্র জিনিষ কিনলো। সাথে সাথে আগের অন্যান্য ক্রেতাদের ডাটা অ্যানালাইসিস করে বের করা সিদ্ধান্তকে আমরা কাজে লাগাতে পারি। আগের অ্যানালাইসিস মোতাবেক আমাদের সিস্টেম জানে যে, বেশিরভাগ ক্রেতাই যখন এই আইটেমটা কিনেছিল তখন তারা আরেকটা আইটেমও কিনেছিল। তো, সেই আইটেমকে সাজেশন হিসেবে দেখানো যেতে পারে এই নতুন ক্রেতার কাছে। এমনকি, যদি কোন ক্রেতা কিছুই না কিনে প্রথমবার একটি সাইট ভিজিট করে সেক্ষেত্রেও আগের অ্যানালাইটিক্যাল বা প্রেডিকশন মডেল বিক্রেতাকে সাহায্য করতে পারে। যেমন - ভিজিটর কোন এলাকা থেকে ভিজিট করছে, তার বয়স কত ইত্যাদি জানা সহজ এবং যদি সিস্টেমের কাছে এরকম কিছু ক্লাসিফিকেশন ডাটা থাকে যে, ওই লোকেশনের, এই বয়সের মানুষ সব চেয়ে কোন জিনিষগুলো বেশি কিনছে তাহলেই হয়ে গেলো। এ তো, গেল খুব সহজ এবং হালকা কিছু উদাহরণ। সঠিকভাবে ডাটা সায়েন্সের প্রয়োগ কল্পনার অতীত ফলাফল এনে দিতে পারে।

**ওপেন সোর্স**

এই বইটি মূলত স্বেচ্ছাশ্রমে লেখা এবং বইটি সম্পূর্ন ওপেন সোর্স । এখানে তাই আপনিও অবদান রাখতে পারেন লেখক হিসেবে । আপনার কন্ট্রিবিউশান গৃহীত হলে অবদানকারীদের তালিকায় আপনার নাম স্বয়ংক্রিয়ভাবে যুক্ত হয়ে যাবে।

এটি মূলত একটি [গিটহাব রিপোজিটোরি](https://github.com/howtocode-dev/ds.howtocode.dev) যেখানে এই বইয়ের আর্টিকেল গুলো মার্কডাউন ফরম্যাটে লেখা হচ্ছে । রিপোজিটরিটি ফর্ক করে পুল রিকুয়েস্ট পাঠানোর মাধ্যমে আপনারাও অবদান রাখতে পারেন । বিস্তারিত দেখতে পারেন এই ভিডিওতে [Video](http://blog.howtocode.dev/?p=32)

> **বর্তমানে বইটির কন্টেন্ট বিভিন্ন কন্ট্রিবিউটর এবং নানা রকম সোর্স থেকে সংগৃহীত এবং সংকলিত।**

  
This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](http://creativecommons.org/licenses/by-nc-nd/4.0/).

