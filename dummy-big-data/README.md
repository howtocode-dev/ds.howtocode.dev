# বেশি ডাটা নিয়ে কাজ

এখন পর্যন্ত আমরা ম্যানুয়ালি একদম অল্প কিছু ডাটা নিয়ে শুধুমাত্র ম্যাথেমিটিক্যাল টার্ম গুলো বোঝার চেষ্টা করেছি। এখন থেকে আমরা একটু বেশি সংখ্যক ডাটার উপর কাজ করবো যাতে করে ফ্যাক্টর গুলোর সঠিকটা আরও ভালভাবে যাচাই করা যায়। এ জন্য আমরা numpy এর রেন্ডমাইজেশন ফাংশন এর সাহায্য নিয়ে চাহিদা মোতাবেক বিভিন্ন ডাটাসেট বানিয়ে সেগুলোর উপর পরীক্ষা চালাবো।

```text
incomes = np.random.normal(27000, 15000, 10000)
np.mean(incomes)
```

```text
27012.587884334778
```

উপরে আমরা একটা নরমাল ডিস্ট্রিবিউশন তৈরি করেছি যার ডাটাসেট হচ্ছে কিছু লোকের মাসিক ইনকাম। এর সেন্টার মান ঠিক করে দিয়েছি 27000, স্ট্যান্ডার্ড ডেভিয়েশন বলে দিয়েছি 15000 এবং মোট 10000 -টি ডাটা পয়েন্ট তৈরি করতে বলেছি। এই রেন্ডোম ডাটা সেটের mean তথা গড় মান বের করতে আমরা numpy এর mean ফাংশন কল করেছি এবং এর ভ্যালু এসেছে ঠিক 27000 এর মতই।

আর নিচে আমরা উক্ত ডাটা গুলোকে 50 টি সেগমেন্টে ভাগ করে একটা হিস্টোগ্রাম দেখার চেষ্টা করেছি।

```text
plt.hist(incomes, 50)
plt.show()
```

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXoAAAD8CAYAAAB5Pm/hAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAALEgAACxIB0t1+/AAAEfpJREFUeJzt3W+s5Fddx/H3xy5tFZHdpdfNurt1l9ho9AG03mAJxiD1
T7sQtyaIJUaWWrOJVgJiolt5oCQ+aNUINJrChqpbU4VawG5qFetSoj6gsJVS6D96KdTupu0ulVaR
oKl+fTBn7ey6u3fm3pk7956+X8lkzu/8zsyc09/0c8+e38xvUlVIkvr1LbPugCRpugx6SeqcQS9J
nTPoJalzBr0kdc6gl6TOGfSS1DmDXpI6Z9BLUufWzboDAOedd15t37591t2QpDXlnnvu+WpVzS3W
blUE/fbt2zl06NCsuyFJa0qSx0Zp59KNJHXOoJekzhn0ktQ5g16SOmfQS1LnDHpJ6pxBL0mdM+gl
qXMGvSR1blV8M1aatO17//qU9V+59vUr3BNp9pzRS1LnDHpJ6pxBL0mdM+glqXMGvSR1zqCXpM4Z
9JLUOYNekjo3UtAnWZ/k1iQPJXkwyauTbExyZ5JH2v2G1jZJrk+ykOS+JBdNdwiSpDMZdUb/PuBv
q+r7gFcADwJ7gYNVdQFwsG0DXAZc0G57gBsm2mNJ0lgWDfokLwV+BLgRoKr+q6qeAXYB+1uz/cDl
rbwLuKkGPgWsT7J54j2XJI1klBn9DuAY8CdJPpvkg0leDGyqqidamyeBTa28BXh86PGHW50kaQZG
Cfp1wEXADVV1IfAfPL9MA0BVFVDjvHCSPUkOJTl07NixcR4qSRrDKEF/GDhcVXe37VsZBP9Tx5dk
2v3Rtv8IsG3o8Vtb3Qmqal9VzVfV/Nzc3FL7L0laxKJBX1VPAo8n+d5WdQnwAHAA2N3qdgO3tfIB
4C3t0zcXA88OLfFIklbYqNejfxtwc5KzgUeBKxn8kbglyVXAY8CbWts7gJ3AAvCN1laSNCMjBX1V
3QvMn2LXJadoW8DVy+yXJGlC/IUprQn+YpS0dF4CQZI654xea9rpZvqSnmfQ6wXFJSC9ELl0I0md
M+glqXMu3Ui4pKO+OaOXpM4Z9JLUOYNekjpn0EtS5wx6Seqcn7qRzuBM37z1EzlaK5zRS1LnDHpJ
6pxBL0mdM+glqXMGvSR1zqCXpM4Z9JLUOYNekjpn0EtS5/xmrFYVfwNWmryRZvRJvpLk80nuTXKo
1W1McmeSR9r9hlafJNcnWUhyX5KLpjkASdKZjbN086NV9cqqmm/be4GDVXUBcLBtA1wGXNBue4Ab
JtVZSdL4lrNGvwvY38r7gcuH6m+qgU8B65NsXsbrSJKWYdSgL+DvktyTZE+r21RVT7Tyk8CmVt4C
PD702MOtTpI0A6OejP3hqjqS5DuBO5M8NLyzqipJjfPC7Q/GHoDzzz9/nIeqA550lVbOSDP6qjrS
7o8CHwNeBTx1fEmm3R9tzY8A24YevrXVnfyc+6pqvqrm5+bmlj4CSdIZLRr0SV6c5CXHy8BPAF8A
DgC7W7PdwG2tfAB4S/v0zcXAs0NLPJKkFTbK0s0m4GNJjrf/86r62ySfAW5JchXwGPCm1v4OYCew
AHwDuHLivZZWgdMtP/nLU1ptFg36qnoUeMUp6p8GLjlFfQFXT6R3kqRl8xIIktQ5g16SOmfQS1Ln
DHpJ6pxBL0mdM+glqXMGvSR1zqCXpM4Z9JLUOYNekjpn0EtS5wx6SeqcQS9JnTPoJalzBr0kdW7U
34yVNCJ/kESrjTN6SeqcQS9JnTPoJalzBr0kdc6TsdIK8SStZsUZvSR1zqCXpM4Z9JLUuZGDPslZ
ST6b5Pa2vSPJ3UkWknw4ydmt/py2vdD2b59O1yVJoxhnRv924MGh7euA91TV9wBfA65q9VcBX2v1
72ntJEkzMlLQJ9kKvB74YNsO8Drg1tZkP3B5K+9q27T9l7T2kqQZGPXjle8Ffh14Sdt+GfBMVT3X
tg8DW1p5C/A4QFU9l+TZ1v6rw0+YZA+wB+D8889fav+1SvjRQWn1WnRGn+QNwNGqumeSL1xV+6pq
vqrm5+bmJvnUkqQho8zoXwP8VJKdwLnAdwDvA9YnWddm9VuBI639EWAbcDjJOuClwNMT77nWhNPN
9CWtnEVn9FV1TVVtrartwBXAJ6rq54C7gDe2ZruB21r5QNum7f9EVdVEey1JGtlyPkf/G8A7kyww
WIO/sdXfCLys1b8T2Lu8LkqSlmOsa91U1SeBT7byo8CrTtHmm8DPTKBvkqQJ8JuxktQ5g16SOmfQ
S1LnvB69NGN+2UzT5oxekjpn0EtS5wx6SeqcQS9JnTPoJalzBr0kdc6gl6TOGfSS1DmDXpI6Z9BL
UucMeknqnNe60Vj8aUBp7XFGL0mdM+glqXMGvSR1zqCXpM4Z9JLUOYNekjpn0EtS5xYN+iTnJvl0
ks8luT/Ju1v9jiR3J1lI8uEkZ7f6c9r2Qtu/fbpDkCSdyShfmPpP4HVV9fUkLwL+KcnfAO8E3lNV
H0ryfuAq4IZ2/7Wq+p4kVwDXAT87pf5L3fJHwzUpi87oa+DrbfNF7VbA64BbW/1+4PJW3tW2afsv
SZKJ9ViSNJaR1uiTnJXkXuAocCfwJeCZqnquNTkMbGnlLcDjAG3/s8DLJtlpSdLoRgr6qvrvqnol
sBV4FfB9y33hJHuSHEpy6NixY8t9OknSaYx1UbOqeibJXcCrgfVJ1rVZ+1bgSGt2BNgGHE6yDngp
8PQpnmsfsA9gfn6+lj4ETYMXL5P6McqnbuaSrG/lbwV+HHgQuAt4Y2u2G7itlQ+0bdr+T1SVQS5J
MzLKjH4zsD/JWQz+MNxSVbcneQD4UJLfAT4L3Nja3wj8WZIF4F+BK6bQb0nSiBYN+qq6D7jwFPWP
MlivP7n+m8DPTKR3kqRl85uxktQ5g16SOmfQS1LnDHpJ6pxBL0mdM+glqXMGvSR1zqCXpM4Z9JLU
OYNekjpn0EtS5wx6SercWNejlzR7/pasxuWMXpI6Z9BLUucMeknqnEEvSZ0z6CWpcwa9JHXOj1e+
gJ3uY3qS+uKMXpI6Z9BLUucMeknq3KJBn2RbkruSPJDk/iRvb/Ubk9yZ5JF2v6HVJ8n1SRaS3Jfk
omkPQpJ0eqOcjH0O+LWq+uckLwHuSXIn8FbgYFVdm2QvsBf4DeAy4IJ2+yHghnYvaYq8Bo5OZ9EZ
fVU9UVX/3Mr/DjwIbAF2Aftbs/3A5a28C7ipBj4FrE+yeeI9lySNZKw1+iTbgQuBu4FNVfVE2/Uk
sKmVtwCPDz3scKuTJM3AyEGf5NuBjwDvqKp/G95XVQXUOC+cZE+SQ0kOHTt2bJyHSpLGMFLQJ3kR
g5C/uao+2qqfOr4k0+6PtvojwLahh29tdSeoqn1VNV9V83Nzc0vtvyRpEaN86ibAjcCDVfUHQ7sO
ALtbeTdw21D9W9qnby4Gnh1a4pEkrbBRPnXzGuDngc8nubfV/SZwLXBLkquAx4A3tX13ADuBBeAb
wJUT7bEkaSyLBn1V/ROQ0+y+5BTtC7h6mf2SJE2IFzV7AfDiZdILm5dAkKTOGfSS1DmXbqTOeWkE
OaOXpM4Z9JLUOYNekjpn0EtS5wx6SeqcQS9JnTPoJalzBr0kdc6gl6TOGfSS1DkvgdARr1Ip6VQM
+jXIQJc0DoNeeoHyYmcvHK7RS1LnDHpJ6pxBL0mdM+glqXMGvSR1zqCXpM4Z9JLUuUWDPskfJzma
5AtDdRuT3JnkkXa/odUnyfVJFpLcl+SiaXZekrS4UWb0fwpcelLdXuBgVV0AHGzbAJcBF7TbHuCG
yXRTkrRUiwZ9Vf0D8K8nVe8C9rfyfuDyofqbauBTwPokmyfVWUnS+Ja6Rr+pqp5o5SeBTa28BXh8
qN3hVvf/JNmT5FCSQ8eOHVtiNyRJi1n2ydiqKqCW8Lh9VTVfVfNzc3PL7YYk6TSWGvRPHV+SafdH
W/0RYNtQu62tTpI0I0sN+gPA7lbeDdw2VP+W9umbi4Fnh5Z4JEkzsOhlipP8BfBa4Lwkh4HfAq4F
bklyFfAY8KbW/A5gJ7AAfAO4cgp9ljRFXr64P4sGfVW9+TS7LjlF2wKuXm6nJEmT4zdjJalzBr0k
dc6fElzF/G1YSZPgjF6SOueMfhVw5i5pmpzRS1LnnNFLGsmZ/uXpZ+xXN4Ne0rL5JavVzaUbSeqc
QS9JnTPoJalzBr0kdc6gl6TO+ambFeQXoyTNgjN6SeqcQS9JnXPpZgpcopG0mhj0kqbGb8yuDi7d
SFLnDHpJ6pxLN8vgWry0NC7prCxn9JLUOWf0I3DmLmktm0rQJ7kUeB9wFvDBqrp2Gq8jqS8u6UzH
xIM+yVnAHwE/DhwGPpPkQFU9MOnXmjRn7tLq5B+A5ZnGjP5VwEJVPQqQ5EPALmDVB72ktcU/AKOZ
RtBvAR4f2j4M/NAUXgdwFi7p/5t2LizlD8ks/yjN7GRskj3Anrb59SQPr+DLnwd8dQVfbyX0OCbo
c1yOae045bhy3eReYJnP9d2jNJpG0B8Btg1tb211J6iqfcC+Kbz+opIcqqr5Wbz2tPQ4JuhzXI5p
7ehlXNP4HP1ngAuS7EhyNnAFcGAKryNJGsHEZ/RV9VySXwE+zuDjlX9cVfdP+nUkSaOZyhp9Vd0B
3DGN556QmSwZTVmPY4I+x+WY1o4uxpWqmnUfJElT5LVuJKlzXQR9kt9L8lCS+5J8LMn6oX3XJFlI
8nCSnxyqv7TVLSTZO1S/I8ndrf7D7YQySc5p2wtt//aVHOOZnG4sq0WSbUnuSvJAkvuTvL3Vb0xy
Z5JH2v2GVp8k17fx3JfkoqHn2t3aP5Jk91D9Dyb5fHvM9UmyQmM7K8lnk9zetsd+/4z7Hl2BMa1P
cmv7f+rBJK9e68cqya+2994XkvxFknN7OFYjq6o1fwN+AljXytcB17Xy9wOfA84BdgBfYnCC+KxW
fjlwdmvz/e0xtwBXtPL7gV9q5V8G3t/KVwAfnvW4W19OO5bVcgM2Axe18kuAL7Zj87vA3la/d+i4
7QT+BghwMXB3q98IPNruN7Tyhrbv061t2mMvW6GxvRP4c+D2pbx/lvIeXYEx7Qd+sZXPBtav5WPF
4EucXwa+degYvbWHYzXyf4NZd2AKB/WngZtb+RrgmqF9Hwde3W4fH6q/pt3C4MsRx/9o/F+7449t
5XWtXVbBeE85lln3a5E+38bgWkgPA5tb3Wbg4Vb+APDmofYPt/1vBj4wVP+BVrcZeGio/oR2UxzH
VuAg8Drg9qW8f8Z9j67AmF7aQjEn1a/ZY8Xz39bf2P7b3w785Fo/VuPculi6OckvMJglwKkvx7Dl
DPUvA56pqudOqj/hudr+Z1v7WTvdWFal9s/gC4G7gU1V9UTb9SSwqZXHPW5bWvnk+ml7L/DrwP+0
7aW8f8Yd67TtAI4Bf9KWpD6Y5MWs4WNVVUeA3wf+BXiCwX/7e1j7x2pkaybok/x9W187+bZrqM27
gOeAm2fXU51Okm8HPgK8o6r+bXhfDaZCa+YjYEneABytqntm3ZcJWwdcBNxQVRcC/8Fgqeb/rMFj
tYHBhRV3AN8FvBi4dKadWmFr5odHqurHzrQ/yVuBNwCXtDcinPlyDKeqfxpYn2Rd+0s+3P74cx1O
so7BP3GfXvKAJmekS07MWpIXMQj5m6vqo636qSSbq+qJJJuBo63+dGM6Arz2pPpPtvqtp2g/Ta8B
firJTuBc4DsY/AbDuO+fcd+j03YYOFxVd7ftWxkE/Vo+Vj8GfLmqjgEk+SiD47fWj9XoZr12NKE1
uEsZXAZ57qT6H+DEkyePMjhxsq6Vd/D8yZMfaI/5S048QfPLrXw1J56guWXW4259Oe1YVsuNwfrm
TcB7T6r/PU48wfe7rfx6TjzB9+lWv5HB+vGGdvsysLHtO/kE384VHN9ref5k7Fjvn6W8R1dgPP8I
fG8r/3Y7Tmv2WDG4eu79wLe119wPvK2HYzXyf4NZd2BCB3KBwRrZve32/qF972JwRvxhhs7uM/i0
wBfbvncN1b+8vREX2hvhnFZ/btteaPtfPutxLzaW1XIDfpjBP/XvGzpGOxmsex4EHgH+figIwuDH
a74EfB6YH3quX2jHYAG4cqh+HvhCe8wfsoInyjkx6Md+/4z7Hl2B8bwSONSO118xCOo1fayAdwMP
tdf9MwZhveaP1ag3vxkrSZ1bMydjJUlLY9BLUucMeknqnEEvSZ0z6CWpcwa9JHXOoJekzhn0ktS5
/wW/7lnQ5pXvSgAAAABJRU5ErkJggg==
)

```text
np.median(incomes)
```

```text
26976.888137643109
```

অর্থাৎ আবারও প্রমাণ হয় যে - নরমালি ডিস্ট্রিবিউটেড ডাটার ক্ষেত্রে mean, median এবং mode মোটামুটি একই।

**Outlier** হচ্ছে এমন ভ্যালু যেটা আলোচ্য সাধারণ ভ্যালু থেকে যথেষ্ট দুরে বা বাইরে অবস্থান করে। অর্থাৎ উপরের ইনকাম এমাউন্ট গুলোর মধ্যে যদি এমন কোন লোকের ইনকাম যুক্ত করা যায় যার মাসিক আয় 1000000000 তাহলে এটাকে আউটলায়ার বলা হয় এবং এটা অবাঞ্ছিতভাবে mean ভ্যালু বদলে দেয়।

```text
incomes = np.append(incomes, [1000000000])
np.mean(incomes)
```

```text
126999.88789554522
```

কিন্তু এক্ষেত্রেও median সাহায্য করে সঠিক গড় ভিউ পেতে,

```text
np.median(incomes)
```

```text
26977.609357910656
```

আর হ্যাঁ, স্ট্যান্ডার্ড ডেভিয়েশন জানা থাকলে কিন্তু আমরা সহজেই এরকম আউটলায়ার গুলোকে চিহ্নিত করে বাতিল করে দিতে পারি। কারন আমরা জানি সেন্টার ভ্যালু থেকে ২/৩ একক স্ট্যান্ডার্ড ডেভিয়েশনেরও বাইরে পরবে এরকম আউটলারায় গুলো। তাই এগুলোকে আনইউজুয়াল হিসেবে চিহ্নিত করা যায়। z-score এর কথা নিশ্চয়ই মনে আছে এতক্ষণেও।

