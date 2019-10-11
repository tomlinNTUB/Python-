# A06-4 由list建立的set

## (1) 程式範例

``` python
#-------------------
# 一個list
#-------------------
mylist = ['A', 'B', 'D', 'E', 'B', 'E', 'A', 'C']

#-------------------
# 由list生成set
#-------------------
myset = set(mylist)

#-------------------
# 印出
#-------------------
print('list: ', mylist)
print('set:  ', myset)
```


### 測試
``` python
list:  ['A', 'B', 'D', 'E', 'B', 'E', 'A', 'C']
set:   {'D', 'C', 'A', 'B', 'E'}
```



## (2) 程式範例

``` python
#-------------------
# 一個str
#-------------------
s = 'ABDEBEAC'

#-------------------
# 一個list
#-------------------
mylist = [s[i] for i in range(len(s))]

#-------------------
# 由list生成set
#-------------------
myset = set(mylist)

#-------------------
# 印出
#-------------------
print('list: ', mylist)
print('set:  ', myset)
```


### 測試
``` python
list:  ['A', 'B', 'D', 'E', 'B', 'E', 'A', 'C']
set:   {'B', 'C', 'D', 'E', 'A'}
```





## (3) 程式範例

``` python
#-------------------
# 一個原始字串
#-------------------
s = "With legacies as varied as its adventure landscape and spirited traditions thriving alongside the cream of Asian sophistication, Taiwan is a continent on one green island. Famed for centuries as Ilha Formosa (Beautiful Isle; 美麗島; Měilìdǎo), this is a land with more sides than the 11-headed Guanyin. Towering sea cliffs, marble-walled gorges and tropical forests are just the start of your journey, which could take you as far as Yushan, Taiwan's 3952m alpine roof. In Taiwan you can criss-cross mountains on colonial-era hiking trails or cycle a lone highway with the blue Pacific on one side and green volcanic arcs on the other. And if you simply want a classic landscape to enjoy, you'll find them around every corner. Taiwan is heir to the entire Chinese tradition of Buddhism, Taoism, Confucianism and that amorphous collection of deities and demons worshipped as folk faith. Over the centuries the people have blended their way into a unique and tolerant religious culture that's often as ritual heavy as Catholicism and as wild as Santeria. Taiwanese temples (all 15,000) combine worship hall, festival venue and art house under one roof. Watch a plague boat burn at Donglong Temple, go on a pilgrimage with the Empress of Heaven, study a rooftop three-dimensional mosaic, and learn why a flag and ball have come to represent prayer. 'Have you eaten?' The words are used as a greeting here, and the answer is always 'yes', as there's just too much nibbling to do. Taiwan offers the gamut of Chinese cuisines, some of the best Japanese outside Japan, and a full house of local specialities from Tainan milkfish and Taipei beef noodles to indigenous barbecued wild boar. Night markets around the island serve endless feasts of snacks including stinky tofu, steamed dumplings, oyster omelettes, shrimp rolls and shaved ice. And when you're thirsty you can look forward to juices from the freshest local fruits, local craft beer, aromatic teas and, in a surprising twist, Asia's best gourmet coffee. When I visited Taiwan as a child, the wondrous rocks of Yeliu made an impression. Years later, a fan of director Hou Hsiao-hsien, I went to Jiufen and Fengkuei to see the settings that gave rise to the films I enjoyed, and was bewitched. Now Penghu's windswept islands mesmerise me, as does the taste of musk melons. Taiwan is full of surprises if you know where to look, like the night I waited for a meteor shower in Kenting. I'd expected a crowd to show up, but there wasn't even a hint of a shadow. I was completely alone. Then I looked up – the whole sky was moving. Defying those who said it wasn't in their DNA, the Taiwanese have created Asia's most vibrant democracy and liberal society, with a raucous free press, gender equality, and respect for human rights and, increasingly, animal rights as well. The ancestors are still worshipped, and mum and dad still get their dues, but woe betide the politician who thinks it's the people who must pander, and not him – or her. If you want to catch a glimpse of the people's passion for protest, check out Taipei Main Station on most weekends, or just follow the local news."

#-------------------
# 刪除標點符號
#-------------------
d = ',.;?!()'

for k in d:
    s = s.replace(k, '')

#-------------------
# 切割原始字串
#-------------------
mylist = s.split()
print('在list中的單字個數:', len(mylist))

#-------------------
# 印出分割後的list
#-------------------
myset = set(mylist)

#-------------------
# 印出分割後的list
#-------------------
print('在set中的單字個數:', len(myset))
```


### 測試
``` python
>> 在list的單字個數: 535
>> 在set的單字個數: 348
```
