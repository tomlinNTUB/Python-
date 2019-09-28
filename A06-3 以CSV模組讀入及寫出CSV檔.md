# A06-3 以CSV模組讀入及寫出CSV檔

### (1) 程式範例
``` python
#---------------------------------------
# 讀入CSV檔的格式
# 序號(0), 性別(1), 國文(2), 英文(3), 
# 數學(4), 社會(5), 自然(6), 作文(7)
#---------------------------------------

# 匯入處理csv檔的模組
import csv

# 在本段程式中, 輸入檔以infile變數表示, 輸出檔以outfile變數表示.
with open('score.csv', 'r', encoding='UTF-8') as infile, open('output.csv', 'w', encoding='UTF-8', newline='') as outfile:
    # 讀入資料, 項目分隔符號是逗號   
    data = csv.reader(infile, delimiter=',')

    # 建立輸出物件
    writer = csv.writer(outfile)

    # 逐行取出資料
    for items in data:
        # 將各個項目存入各變數中
        no = int(items[0])
        gender = items[1]
        chi = int(items[2])
        eng = int(items[3])
        mat = int(items[4])
        soc = int(items[5])
        nat = int(items[6])
        lec = int(items[7])

        # 寫出資料
        writer.writerow([no, chi, eng, mat])     
```

### 輸入資料(score.csv)
``` 
1,男,46,56,42,48,37,10
2,男,48,51,39,48,43,10
3,男,50,52,47,41,42,8
4,女,40,56,45,46,45,8
5,男,43,41,29,35,34,10
6,女,44,52,50,41,46,8
7,女,44,56,47,46,41,8
8,男,50,56,47,46,35,8
9,男,56,60,30,48,41,8
10,男,43,55,49,36,50,10
    .
    .
   (略)
``` 

### 輸出資料(output.csv)
``` python
1,46,56,42
2,48,51,39
3,50,52,47
4,40,56,45
5,43,41,29
6,44,52,50
7,44,56,47
8,50,56,47
9,56,60,30
10,43,55,49
    .
    .
   (略)
``` 
