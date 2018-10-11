# test


# 積分関数の計算とプロット
必要なライブラリを下記のようにインポートします．


```python
import numpy as np
from scipy import integrate
import matplotlib.pyplot as plt
```

次に$\int_0^x \frac{4}{1+x^2}$という積分を計算する関数を準備します．


```python
def computePi(x):
    return 4/(1+x**2)
```

次に前処理で作った関数を用いて値を[0,1]の範囲で順次計算していきます．


```python
l = len(x1)
y1= []
for e in range(l):
    x1 = np.linspace(0, 1)
    y1.append(integrate.quad(computePi, 0, x1[e-1])[0])
```

最後に計算したものを関数でプロットします．


```python
# Notebook出力には次の１行が必要
%matplotlib inline

plt.figure(figsize=(8, 6))
plt.plot(x1, y1, label="Int")
plt.title("Int graph")
plt.xlabel("Value")
plt.ylabel("Number")
```




    Text(0, 0.5, 'Number') 

![output_7_1](https://user-images.githubusercontent.com/24654057/46822981-e80aad80-cdc7-11e8-851b-3ed8c1eb40e0.png)