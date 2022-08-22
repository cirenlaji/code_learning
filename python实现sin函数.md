用泰勒公式

```python
from math import fabs
from math import pi

def sin(x): 
    i=x//(2*pi)
    x=x-2*i*pi
    g = 0
    t = x
    n = 1
    while (fabs(t) >= 1e-15):
        g += t
        n += 1
        t = -t * x * x / (2 * n - 1) / (2 * n - 2)
    return g

ans = sin(1000)
print(ans)
```
