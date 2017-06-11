## পপুলেশন ও স্যাম্পল

এ দুটো যথাক্রমে Census এবং Sample এর প্রতিশব্দ। এখানে আবার এই প্রসঙ্গ আনার কারন হচ্ছে, যখন Sample নিয়ে কাজ করতে হবে তখন Sample Variance জানতে হবে যা কিনা Population নিয়ে কাজ করার সময়কার সাধারণ Variance থেকে ভিন্ন।

N সংখ্যক স্যাম্পল নিয়ে কাজ করার সময় Sample Variance বের করার সূত্রে ভগ্নাংশের নিচে মোট এলিমেন্ট \(গোটা পপুলেশন\) সংখ্যা না হয়ে N-1 হবে। আর স্বভাবতই Sample Standard Deviation হবে ওই Sample Variance এর Square Root.

![](https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bequation%2A%7D%0APopulation%20%5C%2C%20Variance%2C%20%5C%2C%20%5Csigma%20%5E%202%20%3D%20%5Cfrac%7B%5Csum%20%28x-%5Cmu%29%20%5E%202%7D%7BN%7D%0A%5Cend%7Bequation%2A%7D&mode=display "$$\begin{equation\*}
Population \, Variance, \, \sigma ^ 2 = \frac{\sum \(x-\mu\) ^ 2}{N}
\end{equation\*}$$")



![](https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bequation%2A%7D%0ASample%20%5C%2C%20Variance%2C%20%5C%2C%20S%20%5E%202%20%3D%20%5Cfrac%7B%5Csum%20%28x-M%29%20%5E%202%7D%7BN-1%7D%0A%5Cend%7Bequation%2A%7D&mode=display "$$\begin{equation\*}
Sample \, Variance, \, S ^ 2 = \frac{\sum \(x-M\) ^ 2}{N-1}
\end{equation\*}$$")



দু ক্ষেত্রেই![](https://render.githubusercontent.com/render/math?math=Standard%20%5C%2C%20Deviation&mode=inline "$Standard \, Deviation$")যথাক্রমে![](https://render.githubusercontent.com/render/math?math=%5Csigma&mode=inline "$\sigma$")এবং![](https://render.githubusercontent.com/render/math?math=S&mode=inline "$S$")

**এ অবস্থায় আরেকটি উদাহরণ দেখে নেই,**

```
incomes = np.random.normal(100.0, 50.0, 10000) # সেন্টার ভ্যালু 100, স্ট্যান্ডার্ড ডেভিয়েশন 20, ডাটা পয়েন্ট 10000 টি

plt.hist(incomes, 50)
plt.show()
```

  


![](data:image/png;base64,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%0A)

```
incomes.var() # Variance
```

```
2483.8524780006833
```

```
incomes.std() # Standard Deviation
```

```
49.838263192056395
```

## 



