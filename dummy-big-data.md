## একটু বেশি ডাটা নিয়ে কাজ

এখন পর্যন্ত আমরা ম্যানুয়ালি একদম অল্প কিছু ডাটা নিয়ে শুধুমাত্র ম্যাথেমিটিক্যাল টার্ম গুলো বোঝার চেষ্টা করেছি। এখন থেকে আমরা একটু বেশি সংখ্যক ডাটার উপর কাজ করবো যাতে করে ফ্যাক্টর গুলোর সঠিকটা আরও ভালভাবে যাচাই করা যায়। এ জন্য আমরা numpy এর রেন্ডমাইজেশন ফাংশন এর সাহায্য নিয়ে চাহিদা মোতাবেক বিভিন্ন ডাটাসেট বানিয়ে সেগুলোর উপর পরীক্ষা চালাবো।

```
incomes = np.random.normal(27000, 15000, 10000)
np.mean(incomes)
```

```
27012.587884334778
```

উপরে আমরা একটা নরমাল ডিস্ট্রিবিউশন তৈরি করেছি যার ডাটাসেট হচ্ছে কিছু লোকের মাসিক ইনকাম। এর সেন্টার মান ঠিক করে দিয়েছি 27000, স্ট্যান্ডার্ড ডেভিয়েশন বলে দিয়েছি 15000 এবং মোট 10000 -টি ডাটা পয়েন্ট তৈরি করতে বলেছি। এই রেন্ডোম ডাটা সেটের mean তথা গড় মান বের করতে আমরা numpy এর mean ফাংশন কল করেছি এবং এর ভ্যালু এসেছে ঠিক 27000 এর মতই।

আর নিচে আমরা উক্ত ডাটা গুলোকে 50 টি সেগমেন্টে ভাগ করে একটা হিস্টোগ্রাম দেখার চেষ্টা করেছি।

```
plt.hist(incomes, 50)
plt.show()
```

![](data:image/png;base64,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%0A/wW/7lnQ5pXvSgAAAABJRU5ErkJggg==%0A)

```
np.median(incomes)
```

```
26976.888137643109
```

অর্থাৎ আবারও প্রমাণ হয় যে - নরমালি ডিস্ট্রিবিউটেড ডাটার ক্ষেত্রে mean, median এবং mode মোটামুটি একই।

**Outlier **হচ্ছে এমন ভ্যালু যেটা আলোচ্য সাধারণ ভ্যালু থেকে যথেষ্ট দুরে বা বাইরে অবস্থান করে। অর্থাৎ উপরের ইনকাম এমাউন্ট গুলোর মধ্যে যদি এমন কোন লোকের ইনকাম যুক্ত করা যায় যার মাসিক আয় 1000000000 তাহলে এটাকে আউটলায়ার বলা হয় এবং এটা অবাঞ্ছিতভাবে mean ভ্যালু বদলে দেয়।

```
incomes = np.append(incomes, [1000000000])
np.mean(incomes)
```

```
126999.88789554522
```

কিন্তু এক্ষেত্রেও median সাহায্য করে সঠিক গড় ভিউ পেতে,

```
np.median(incomes)
```

```
26977.609357910656
```

আর হ্যাঁ, স্ট্যান্ডার্ড ডেভিয়েশন জানা থাকলে কিন্তু আমরা সহজেই এরকম আউটলায়ার গুলোকে চিহ্নিত করে বাতিল করে দিতে পারি। কারন আমরা জানি সেন্টার ভ্যালু থেকে ২/৩ একক স্ট্যান্ডার্ড ডেভিয়েশনেরও বাইরে পরবে এরকম আউটলারায় গুলো। তাই এগুলোকে আনইউজুয়াল হিসেবে চিহ্নিত করা যায়। z-score এর কথা নিশ্চয়ই মনে আছে এতক্ষণেও।

## 



