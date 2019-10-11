# A05-5 由字串切割而成的list


## (1) 字串切割可用以下方式操作

| 操作敘述 | 意義 |
|---------|------|
| s.split() | 將字串s的內容依空白為切割點分切, 成為一個list |
| s.split(k) | 將字串s的內容依k的值為切割點分切, 成為一個list |


## (2) 程式範例
``` python
#----------------------
# 切割字串成為list
#----------------------

# 一個原始字串
s = "With legacies as varied as its adventure landscape and spirited traditions thriving alongside the cream of Asian sophistication, Taiwan is a continent on one green island. Famed for centuries as Ilha Formosa (Beautiful Isle; 美麗島; Měilìdǎo), this is a land with more sides than the 11-headed Guanyin. Towering sea cliffs, marble-walled gorges and tropical forests are just the start of your journey, which could take you as far as Yushan, Taiwan's 3952m alpine roof. In Taiwan you can criss-cross mountains on colonial-era hiking trails or cycle a lone highway with the blue Pacific on one side and green volcanic arcs on the other. And if you simply want a classic landscape to enjoy, you'll find them around every corner. Taiwan is heir to the entire Chinese tradition of Buddhism, Taoism, Confucianism and that amorphous collection of deities and demons worshipped as folk faith. Over the centuries the people have blended their way into a unique and tolerant religious culture that's often as ritual heavy as Catholicism and as wild as Santeria. Taiwanese temples (all 15,000) combine worship hall, festival venue and art house under one roof. Watch a plague boat burn at Donglong Temple, go on a pilgrimage with the Empress of Heaven, study a rooftop three-dimensional mosaic, and learn why a flag and ball have come to represent prayer. 'Have you eaten?' The words are used as a greeting here, and the answer is always 'yes', as there's just too much nibbling to do. Taiwan offers the gamut of Chinese cuisines, some of the best Japanese outside Japan, and a full house of local specialities from Tainan milkfish and Taipei beef noodles to indigenous barbecued wild boar. Night markets around the island serve endless feasts of snacks including stinky tofu, steamed dumplings, oyster omelettes, shrimp rolls and shaved ice. And when you're thirsty you can look forward to juices from the freshest local fruits, local craft beer, aromatic teas and, in a surprising twist, Asia's best gourmet coffee. When I visited Taiwan as a child, the wondrous rocks of Yeliu made an impression. Years later, a fan of director Hou Hsiao-hsien, I went to Jiufen and Fengkuei to see the settings that gave rise to the films I enjoyed, and was bewitched. Now Penghu's windswept islands mesmerise me, as does the taste of musk melons. Taiwan is full of surprises if you know where to look, like the night I waited for a meteor shower in Kenting. I'd expected a crowd to show up, but there wasn't even a hint of a shadow. I was completely alone. Then I looked up – the whole sky was moving. Defying those who said it wasn't in their DNA, the Taiwanese have created Asia's most vibrant democracy and liberal society, with a raucous free press, gender equality, and respect for human rights and, increasingly, animal rights as well. The ancestors are still worshipped, and mum and dad still get their dues, but woe betide the politician who thinks it's the people who must pander, and not him – or her. If you want to catch a glimpse of the people's passion for protest, check out Taipei Main Station on most weekends, or just follow the local news."

# 刪除標點符號
d = ',.;?!'

for k in d:
    s = s.replace(k, '')

# 切割原始字串
v = s.split()

# 印出分割後的list
print(v)
```

### 原始資料
``` 
With legacies as varied as its adventure landscape and spirited traditions thriving alongside the cream of Asian sophistication, Taiwan is a continent on one green island. Famed for centuries as Ilha Formosa (Beautiful Isle; 美麗島; Měilìdǎo), this is a land with more sides than the 11-headed Guanyin. Towering sea cliffs, marble-walled gorges and tropical forests are just the start of your journey, which could take you as far as Yushan, Taiwan's 3952m alpine roof. In Taiwan you can criss-cross mountains on colonial-era hiking trails or cycle a lone highway with the blue Pacific on one side and green volcanic arcs on the other. And if you simply want a classic landscape to enjoy, you'll find them around every corner. Taiwan is heir to the entire Chinese tradition of Buddhism, Taoism, Confucianism and that amorphous collection of deities and demons worshipped as folk faith. Over the centuries the people have blended their way into a unique and tolerant religious culture that's often as ritual heavy as Catholicism and as wild as Santeria. Taiwanese temples (all 15,000) combine worship hall, festival venue and art house under one roof. Watch a plague boat burn at Donglong Temple, go on a pilgrimage with the Empress of Heaven, study a rooftop three-dimensional mosaic, and learn why a flag and ball have come to represent prayer. 'Have you eaten?' The words are used as a greeting here, and the answer is always 'yes', as there's just too much nibbling to do. Taiwan offers the gamut of Chinese cuisines, some of the best Japanese outside Japan, and a full house of local specialities from Tainan milkfish and Taipei beef noodles to indigenous barbecued wild boar. Night markets around the island serve endless feasts of snacks including stinky tofu, steamed dumplings, oyster omelettes, shrimp rolls and shaved ice. And when you're thirsty you can look forward to juices from the freshest local fruits, local craft beer, aromatic teas and, in a surprising twist, Asia's best gourmet coffee. When I visited Taiwan as a child, the wondrous rocks of Yeliu made an impression. Years later, a fan of director Hou Hsiao-hsien, I went to Jiufen and Fengkuei to see the settings that gave rise to the films I enjoyed, and was bewitched. Now Penghu's windswept islands mesmerise me, as does the taste of musk melons. Taiwan is full of surprises if you know where to look, like the night I waited for a meteor shower in Kenting. I'd expected a crowd to show up, but there wasn't even a hint of a shadow. I was completely alone. Then I looked up – the whole sky was moving. Defying those who said it wasn't in their DNA, the Taiwanese have created Asia's most vibrant democracy and liberal society, with a raucous free press, gender equality, and respect for human rights and, increasingly, animal rights as well. The ancestors are still worshipped, and mum and dad still get their dues, but woe betide the politician who thinks it's the people who must pander, and not him – or her. If you want to catch a glimpse of the people's passion for protest, check out Taipei Main Station on most weekends, or just follow the local news.
```


### 測試
``` python
['With', 'legacies', 'as', 'varied', 'as', 'its', 'adventure', 'landscape', 'and', 'spirited', 'traditions', 'thriving', 'alongside', 'the', 'cream', 'of', 'Asian', 'sophistication', 'Taiwan', 'is', 'a', 'continent', 'on', 'one', 'green', 'island', 'Famed', 'for', 'centuries', 'as', 'Ilha', 'Formosa', '(Beautiful', 'Isle', '美麗島', 'Měilìdǎo)', 'this', 'is', 'a', 'land', 'with', 'more', 'sides', 'than', 'the', '11-headed', 'Guanyin', 'Towering', 'sea', 'cliffs', 'marble-walled', 'gorges', 'and', 'tropical', 'forests', 'are', 'just', 'the', 'start', 'of', 'your', 'journey', 'which', 'could', 'take', 'you', 'as', 'far', 'as', 'Yushan', "Taiwan's", '3952m', 'alpine', 'roof', 'In', 'Taiwan', 'you', 'can', 'criss-cross', 'mountains', 'on', 'colonial-era', 'hiking', 'trails', 'or', 'cycle', 'a', 'lone', 'highway', 'with', 'the', 'blue', 'Pacific', 'on', 'one', 'side', 'and', 'green', 'volcanic', 'arcs', 'on', 'the', 'other', 'And', 'if', 'you', 'simply', 'want', 'a', 'classic', 'landscape', 'to', 'enjoy', "you'll", 'find', 'them', 'around', 'every', 'corner', 'Taiwan', 'is', 'heir', 'to', 'the', 'entire', 'Chinese', 'tradition', 'of', 'Buddhism', 'Taoism', 'Confucianism', 'and', 'that', 'amorphous', 'collection', 'of', 'deities', 'and', 'demons', 'worshipped', 'as', 'folk', 'faith', 'Over', 'the', 'centuries', 'the', 'people', 'have', 'blended', 'their', 'way', 'into', 'a', 'unique', 'and', 'tolerant', 'religious', 'culture', "that's", 'often', 'as', 'ritual', 'heavy', 'as', 'Catholicism', 'and', 'as', 'wild', 'as', 'Santeria', 'Taiwanese', 'temples', '(all', '15000)', 'combine', 'worship', 'hall', 'festival', 'venue', 'and', 'art', 'house', 'under', 'one', 'roof', 'Watch', 'a', 'plague', 'boat', 'burn', 'at', 'Donglong', 'Temple', 'go', 'on', 'a', 'pilgrimage', 'with', 'the', 'Empress', 'of', 'Heaven', 'study', 'a', 'rooftop', 'three-dimensional', 'mosaic', 'and', 'learn', 'why', 'a', 'flag', 'and', 'ball', 'have', 'come', 'to', 'represent', 'prayer', "'Have", 'you', "eaten'", 'The', 'words', 'are', 'used', 'as', 'a', 'greeting', 'here', 'and', 'the', 'answer', 'is', 'always', "'yes'", 'as', "there's", 'just', 'too', 'much', 'nibbling', 'to', 'do', 'Taiwan', 'offers', 'the', 'gamut', 'of', 'Chinese', 'cuisines', 'some', 'of', 'the', 'best', 'Japanese', 'outside', 'Japan', 'and', 'a', 'full', 'house', 'of', 'local', 'specialities', 
'from', 'Tainan', 'milkfish', 'and', 'Taipei', 'beef', 'noodles', 'to', 'indigenous', 'barbecued', 'wild', 'boar', 'Night', 'markets', 'around', 'the', 'island', 'serve', 'endless', 'feasts', 'of', 'snacks', 'including', 'stinky', 'tofu', 'steamed', 'dumplings', 'oyster', 'omelettes', 'shrimp', 'rolls', 'and', 'shaved', 'ice', 'And', 'when', "you're", 'thirsty', 'you', 'can', 'look', 'forward', 'to', 'juices', 'from', 'the', 'freshest', 'local', 'fruits', 'local', 'craft', 'beer', 'aromatic', 'teas', 'and', 'in', 'a', 'surprising', 'twist', "Asia's", 'best', 'gourmet', 'coffee', 'When', 'I', 'visited', 'Taiwan', 'as', 'a', 'child', 'the', 'wondrous', 'rocks', 'of', 'Yeliu', 'made', 'an', 'impression', 'Years', 'later', 'a', 'fan', 'of', 'director', 'Hou', 'Hsiao-hsien', 'I', 'went', 'to', 'Jiufen', 'and', 'Fengkuei', 'to', 'see', 'the', 'settings', 'that', 'gave', 'rise', 'to', 'the', 'films', 'I', 'enjoyed', 'and', 'was', 'bewitched', 'Now', "Penghu's", 'windswept', 'islands', 'mesmerise', 'me', 'as', 'does', 'the', 'taste', 'of', 'musk', 'melons', 'Taiwan', 'is', 'full', 'of', 'surprises', 'if', 'you', 'know', 'where', 'to', 'look', 'like', 'the', 'night', 'I', 'waited', 'for', 'a', 'meteor', 'shower', 'in', 'Kenting', "I'd", 'expected', 'a', 'crowd', 'to', 'show', 'up', 'but', 'there', "wasn't", 'even', 'a', 'hint', 'of', 'a', 'shadow', 'I', 'was', 'completely', 'alone', 'Then', 'I', 'looked', 'up', '–', 'the', 'whole', 'sky', 'was', 'moving', 'Defying', 'those', 'who', 'said', 'it', "wasn't", 'in', 'their', 'DNA', 'the', 'Taiwanese', 'have', 'created', "Asia's", 'most', 'vibrant', 'democracy', 'and', 'liberal', 'society', 'with', 'a', 'raucous', 'free', 'press', 'gender', 'equality', 'and', 'respect', 'for', 'human', 
'rights', 'and', 'increasingly', 'animal', 'rights', 'as', 'well', 'The', 'ancestors', 'are', 'still', 
'worshipped', 'and', 'mum', 'and', 'dad', 'still', 'get', 'their', 'dues', 'but', 'woe', 'betide', 'the', 'politician', 'who', 'thinks', "it's", 'the', 'people', 'who', 'must', 'pander', 'and', 'not', 'him', '–', 'or', 'her', 'If', 'you', 'want', 'to', 'catch', 'a', 'glimpse', 'of', 'the', "people's", 'passion', 'for', 'protest', 'check', 'out', 'Taipei', 'Main', 'Station', 'on', 'most', 'weekends', 'or', 'just', 'follow', 'the', 'local', 'news']
```



## (3) 程式範例
``` python
# coding=utf-8

#----------------------
# 切割字串成為list
#----------------------

# 一個原始字串
s = '到越南旅遊，不僅能將一成不變的生活拋諸腦後，還能享受全球一流的服務。越南首都河內終日忙碌。白天熙來攘往，趕着辦事的民眾騎摩托車穿梭街頭；入夜後城市依舊熱鬧，民眾或散步或在街邊隨處可見的咖啡館消磨時光。供奉孔子的文廟建於1070年，不僅是河內最悠久的古蹟之一，也是越南第一所高等學府所在地。這裏坐擁賞心悅目的花園與庭院，是河內人氣最高的旅遊景點。還劍湖位於市中心，附近有劇院，晚上不妨到此觀賞傳統水偶戲，再前往舊城區找家咖啡館歇腳，欣賞街景。1901年興建的大都會飯店呈現法國殖民時期的建築風格，是旅遊河內絕佳的住宿地點。步行就能抵達還劍湖與舊城區，卻又彷彿一片清雅綠洲，遠離兩處景點的熱鬧喧囂。大都會飯店接待過的王室、元首不計其數，默劇大師卓別林、作家格雷安．葛林、搖滾巨星米克傑格都曾在此下榻。飯店裏的俱樂部酒吧每晚都有爵士樂現場演出。此外還有下午茶服務，供應手工糖果、熱巧克力等多種美食。'

# 將標點符號改為特別字元
d = '，。；、'

for k in d:
    s = s.replace(k, '%')

# 刪除字串的最後1個字
s = s[:len(s)-1]

# 切割原始字串
v = s.split('%')

# 印出分割後的list
print(v)
```

### 原始資料
``` 
到越南旅遊，不僅能將一成不變的生活拋諸腦後，還能享受全球一流的服務。越南首都河內終日忙碌。白天熙來攘往，趕着辦事的民眾騎摩托車穿梭街頭；入夜後城市依舊熱鬧，民眾或散步或在街邊隨處可見的咖啡館消磨時光。供奉孔子的文廟建於1070年，不僅是河內最悠久的古蹟之一，也是越南第一所高等學府所在地。這裏坐擁賞心悅目的花園與庭院，是河內人氣最高的旅遊景點。還劍湖位於市中心，附近有劇院，晚上不妨到此觀賞傳統水偶戲，再前往舊城區找家咖啡館歇腳，欣賞街景。1901年興建的大都會飯店呈現法國殖民時期的建築風格，是旅遊河內絕佳的住宿地點。步行就能抵達還劍湖與舊城區，卻又彷彿一片清雅綠洲，遠離兩處景點的熱鬧喧囂。大都會飯店接待過的王室、元首不計其數，默劇大師卓別林、作家格雷安．葛林、搖滾巨星米克傑格都曾在此下榻。飯店裏的俱樂部酒吧每晚都有爵士樂現場演出。此外還有下午茶服務，供應手工糖果、熱巧克力等多種美食。
``` 

### 測試
``` python
['到越南旅遊', '不僅能將一成不變的生活拋諸腦後', '還能享受全球一流的服務', '越南首都河內終日忙碌', '白 
天熙來攘往', '趕着辦事的民眾騎摩托車穿梭街頭', '入夜後城市依舊熱鬧', '民眾或散步或在街邊隨處可見的咖啡 
館消磨時光', '供奉孔子的文廟建於1070年', '不僅是河內最悠久的古蹟之一', '也是越南第一所高等學府所在地', 
'這裏坐擁賞心悅目的花園與庭院', '是河內人氣最高的旅遊景點', '還劍湖位於市中心', '附近有劇院', '晚上不妨
到此觀賞傳統水偶戲', '再前往舊城區找家咖啡館歇腳', '欣賞街景', '1901年興建的大都會飯店呈現法國殖民時期 
的建築風格', '是旅遊河內絕佳的住宿地點', '步行就能抵達還劍湖與舊城區', '卻又彷彿一片清雅綠洲', '遠離兩 
處景點的熱鬧喧囂', '大都會飯店接待過的王室', '元首不計其數', '默劇大師卓別林', '作家格雷安．葛林', '搖 
滾巨星米克傑格都曾在此下榻', '飯店裏的俱樂部酒吧每晚都有爵士樂現場演出', '此外還有下午茶服務', '供應手 
工糖果', '熱巧克力等多種美食']
```

