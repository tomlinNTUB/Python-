# A05-7 list的unpacking


## (1) 程式範例
``` python
#---------------------------
# 生成一個list
#---------------------------
mylist = [k for k in 'ABCDEFGHIJ']

print('原始list:', mylist)

#---------------------------
# 將mylist切成
# 前面1個元素, 及剩餘的list
#---------------------------
a, *b = mylist

print('unpacking後:')
print(a)
print(b)
```


### 測試
``` python
>> 原始list: ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J']
>> unpacking後:
>> A
>> ['B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J']
```




## (2) 程式範例
``` python
#-------------------------------------
# 生成一個list
#-------------------------------------
mylist = [k for k in 'ABCDEFGHIJ']

print('原始list:', mylist)

#-------------------------------------
# 將mylist切成
# 前面1個元素, 剩餘的list, 最後1個元素
#-------------------------------------
a, *b, c = mylist

print('unpacking後:')
print(a)
print(b)
print(c)
```


### 測試
``` python
原始list: ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J']
unpacking後:
A
['B', 'C', 'D', 'E', 'F', 'G', 'H', 'I']
J
```
