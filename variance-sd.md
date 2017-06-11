## ভ্যারিয়েন্স ও স্ট্যান্ডার্ড ডেভিয়েশন

আমরা আগেই বলেছি ডাটা ডিস্ট্রিবিউশন করাকে স্প্রেড আউট করা বা ছড়িয়ে দেয়াও বলা যায়। সেক্ষেত্রে আমরা জানতে পেরেছি যে নরমালি ডিস্ট্রিবিউটেড ডাটা বা ডাটাকে নরমালি ডিস্ট্রিবিউট করার অনেক সুবিধা আছে। তো, সেই নরমালি ডিস্ট্রিবিউট করার পর যদি পর্যবেক্ষণ করি যে- ডাটা গুলো গড় মান থেকে কতটা ছড়ানো বা এর থেকে কত দুরে অবস্থিত সেক্ষেত্রে যে ফ্যাক্টরটি সম্বদ্ধে জানতে হবে সেটি হচ্ছে উক্ত ডিস্ট্রিবিউশনের ভ্যারিয়েন্স।

ভ্যারিয়েন্স হচ্ছে - উক্ত ডিস্ট্রিবিউশনের mean \(গড়\) মান থেকে প্রত্যেকটি এলিমেন্টের দূরত্বের বর্গের গড়। অর্থাৎ, উপরের sizes অ্যারের ভ্যারিয়েন্স বের করার জন্য আমরা নিচের ফর্মুলা ব্যবহার করতে পারি,

![](https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bequation%2A%7D%0AVariance%2C%20%5C%2C%20%5Csigma%20%5E%202%20%3D%20%5Cfrac%7B%5Csum%20%28x-%5Cmu%29%20%5E%202%7D%7BN%7D%0A%5Cend%7Bequation%2A%7D&mode=display "$$\begin{equation\*}
Variance, \, \sigma ^ 2 = \frac{\sum \(x-\mu\) ^ 2}{N}
\end{equation\*}$$")



যেখানে![](https://render.githubusercontent.com/render/math?math=x&mode=inline "$x$")হচ্ছে এলিমেন্ট এবং![](https://render.githubusercontent.com/render/math?math=%5Cmu&mode=inline "$\mu$")হচ্ছে গড়। আর![](https://render.githubusercontent.com/render/math?math=N&mode=inline "$N$")হচ্ছে মোট এলিমেন্ট সংখ্যা।

![](https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bequation%2A%7D%0AVariance%20%3D%20%5Cfrac%7B%2811.19-1%29%5E2%20%2B%20%2811.19-4%29%5E2%20%2B%20%2811.19-5%29%5E2%20%2B%20%2811.19-6%29%5E2%20...%20%20%2811.19-18%29%5E2%20%2B%20%2811.19-20%29%5E2%7D%7B36%7D%0A%5Cend%7Bequation%2A%7D&mode=display "$$\begin{equation\*}
Variance = \frac{\(11.19-1\)^2 + \(11.19-4\)^2 + \(11.19-5\)^2 + \(11.19-6\)^2 ...  \(11.19-18\)^2 + \(11.19-20\)^2}{36}
\end{equation\*}$$")



আর, স্ট্যান্ডার্ড ডেভিয়েশন হচ্ছে ভ্যারিয়েন্স এর বর্গমূল,

![](https://render.githubusercontent.com/render/math?math=Standard%20%5C%2C%20Deviation%20%3D%20%5Csqrt%7BVariance%7D&mode=inline "$Standard \, Deviation = \sqrt{Variance}$")

নিজে নিজে ক্যালকুলেশনটা করে দেখতে পারেন। আমি numpy এর std ফাংশন ব্যবহার করে তাড়াতাড়ি জেনে নেই স্ট্যান্ডার্ড ডেভিয়েশন কত,

```
np.std(sizes)
```

```
3.9144990061482714
```



## 



