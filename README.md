# test


# �ϕ��֐��̌v�Z�ƃv���b�g
�K�v�ȃ��C�u���������L�̂悤�ɃC���|�[�g���܂��D


```python
import numpy as np
from scipy import integrate
import matplotlib.pyplot as plt
```

����$\int_0^x \frac{4}{1+x^2}$�Ƃ����ϕ����v�Z����֐����������܂��D


```python
def computePi(x):
    return 4/(1+x**2)
```

���ɑO�����ō�����֐���p���Ēl��[0,1]�͈̔͂ŏ����v�Z���Ă����܂��D


```python
l = len(x1)
y1= []
for e in range(l):
    x1 = np.linspace(0, 1)
    y1.append(integrate.quad(computePi, 0, x1[e-1])[0])
```

�Ō�Ɍv�Z�������̂��֐��Ńv���b�g���܂��D


```python
# Notebook�o�͂ɂ͎��̂P�s���K�v
%matplotlib inline

plt.figure(figsize=(8, 6))
plt.plot(x1, y1, label="Int")
plt.title("Int graph")
plt.xlabel("Value")
plt.ylabel("Number")
```




    Text(0, 0.5, 'Number') 

![output_7_1](https://user-images.githubusercontent.com/24654057/46822981-e80aad80-cdc7-11e8-851b-3ed8c1eb40e0.png)