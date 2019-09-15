# A01-3 數字運算(使用math模組)


### (1) math模組內常用的常數
```
pi      3.141592…
e       2.718281…
```

### (2) math模組內常用的函式
```
ceil()      
floor()
gcd()
log()
log2()
sqrt()
sin()
cos()
tan()
degrees()
radians()
sin()
cos()
tan()
isfinite()
isinf()
isnan()
```

### (3) 程式範例
``` python
#-----------------------
# 計算圓面積
#-----------------------

# 引用模組
import math

# 輸入圓半徑
r = input('輸入圓的半徑: ')

# 型態轉換
try:
    r = float(r)
except:
    print('請輸入數字資料!')
    exit()

# 計算圓面積, 小數2位, 四捨五入
a = round(math.pi * r**2, 2)

# 印出面積
print('圓面積=', a)
```

### (4) 程式範例
``` python
#-----------------------
# 計算直角三角形的斜邊
#-----------------------

# 引用模組
import math

# 輸入直角三角形的短邊長
a = input('輸入直角三角形的短邊長: ')
b = input('輸入直角三角形的另一個短邊長: ')

# 型態轉換
try:
    a = float(a)
    b = float(b)
except:
    print('請輸入數字資料!')
    exit()

# 計算直角三角形的斜邊, 小數2位, 四捨五入
c = round(math.sqrt(a**2 + b**2), 2)

# 印出斜邊
print('斜邊=', c)
```
