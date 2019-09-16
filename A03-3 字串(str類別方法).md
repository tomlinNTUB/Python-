# A03-3 字串(str類別方法)


### (1) 常用的str類別方法
```
lower()
upper()

endswith()
startswith()

isalnum()
isalpha()
isdecimal()
isdigit()
islower()
isnumeric()
isspace()
isupper()

find()
join()
replace()
split()
```

### (2) 程式範例
``` python
#----------------------------------------
# 輸入字串, 進行字串處理.
# 測入測試:
# We love the Earth, it is our planet.
#----------------------------------------

# 輸入英文內容字串
s = input('請輸入字串: ')

# 印出原始字串內容及型態
print('內容:', s)

# 字串小寫轉大寫, 大寫轉小寫
s1 = s.upper()
s2 = s.lower()

# 印出轉換後的字串
print('轉成大寫: ', s1)
print('轉成小寫: ', s2)
```
