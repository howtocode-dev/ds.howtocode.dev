# ভ্যারিয়েন্স ও স্ট্যান্ডার্ড ডেভিয়েশন

আমরা আগেই বলেছি ডাটা ডিস্ট্রিবিউশন করাকে স্প্রেড আউট করা বা ছড়িয়ে দেয়াও বলা যায়। সেক্ষেত্রে আমরা জানতে পেরেছি যে নরমালি ডিস্ট্রিবিউটেড ডাটা বা ডাটাকে নরমালি ডিস্ট্রিবিউট করার অনেক সুবিধা আছে। তো, সেই নরমালি ডিস্ট্রিবিউট করার পর যদি পর্যবেক্ষণ করি যে- ডাটা গুলো গড় মান থেকে কতটা ছড়ানো বা এর থেকে কত দুরে অবস্থিত সেক্ষেত্রে যে ফ্যাক্টরটি সম্বদ্ধে জানতে হবে সেটি হচ্ছে উক্ত ডিস্ট্রিবিউশনের ভ্যারিয়েন্স।

ভ্যারিয়েন্স হচ্ছে - উক্ত ডিস্ট্রিবিউশনের mean \(গড়\) মান থেকে প্রত্যেকটি এলিমেন্টের দূরত্বের বর্গের গড়। অর্থাৎ, উপরের sizes অ্যারের ভ্যারিয়েন্স বের করার জন্য আমরা নিচের ফর্মুলা ব্যবহার করতে পারি,

![$$\begin{equation\*} Variance, \, \sigma ^ 2 = \frac{\sum \(x-\mu\) ^ 2}{N} \end{equation\*}$$](https://render.githubusercontent.com/render/math?math=\begin{equation*}
Variance%2C%20\%2C%20\sigma%20^%202%20%3D%20\frac{\sum%20%28x-\mu%29%20^%202}{N}
\end{equation*}&mode=display)

যেখানে![$x$](https://render.githubusercontent.com/render/math?math=x&mode=inline)হচ্ছে এলিমেন্ট এবং![$\mu$](https://render.githubusercontent.com/render/math?math=\mu&mode=inline)হচ্ছে গড়। আর![$N$](https://render.githubusercontent.com/render/math?math=N&mode=inline)হচ্ছে মোট এলিমেন্ট সংখ্যা।

![$$\begin{equation\*} Variance = \frac{\(1-11.19\)^2 + \(4-11.19\)^2 + \(5-11.19\)^2 + \(6-11.19\)^2 ... \(18-11.19\)^2 + \(20-11.19\)^2}{36} \end{equation\*}$$](https://render.githubusercontent.com/render/math?math=\begin{equation*}
Variance%20%3D%20\frac{%281-11.19%29^2%20%2B%20%284-11.19%29^2%20%2B%20%285-11.19%29^2%20%2B%20%286-11.19%29^2%20...%20%20%2818-11.19%29^2%20%2B%20%2820-11.19%29^2}{36}
\end{equation*}&mode=display)

আর, স্ট্যান্ডার্ড ডেভিয়েশন হচ্ছে ভ্যারিয়েন্স এর বর্গমূল,

![$Standard \, Deviation = \sqrt{Variance}$](https://render.githubusercontent.com/render/math?math=Standard%20\%2C%20Deviation%20%3D%20\sqrt{Variance}&mode=inline)

নিজে নিজে ক্যালকুলেশনটা করে দেখতে পারেন। আমি numpy এর std ফাংশন ব্যবহার করে তাড়াতাড়ি জেনে নেই স্ট্যান্ডার্ড ডেভিয়েশন কত,

```text
np.std(sizes)
```

```text
3.9144990061482714
```

