# A10-2 讀入CSV檔再排序

## (1) 程式範例
``` python
#---------------------------------------
# 讀入CSV檔的格式
# 序號(0), 性別(1), 國文(2), 英文(3), 
# 數學(4), 社會(5), 自然(6), 作文(7)
#---------------------------------------

# 在with指令包含的範圍中, 開啟的檔案以file變數表示
with open('scores.csv', 'r', encoding='UTF-8') as file:
    # 設定輸出list
    output=[]

    # 逐行處理讀入的資料
    for data in file.readlines():
        # 刪除前後空白, 以逗號分隔資料項目
        data=data.strip()
        items=data.split(',')

        # 各個資料項目存入各變數中
        no = int(items[0])
        gender = items[1]
        chi = int(items[2])
        eng = int(items[3])
        mat = int(items[4])
        soc = int(items[5])
        nat = int(items[6])
        lec = int(items[7])

        # 將資料加入輸出list
        output.append([no, gender, chi, eng, mat, soc, nat, lec]) 

# 排序(以國文及英文成績排序, 由大至小)
output.sort(key=lambda x:(x[2], x[3]), reverse=True)

# 輸出資料
for data in output:
    print(data)
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

### 測試(畫面輸出)
``` python
[186, '女', 60, 46, 60, 44, 44, 10]
[234, '女', 60, 46, 51, 44, 43, 10]
[296, '女', 60, 43, 48, 48, 39, 10]
[304, '男', 60, 39, 51, 46, 41, 10]
[9, '男', 56, 60, 30, 48, 41, 8]   
[82, '女', 56, 60, 49, 46, 52, 6]
[98, '女', 56, 60, 40, 46, 46, 10]
[167, '女', 56, 56, 42, 55, 41, 10]
[273, '女', 56, 56, 41, 43, 41, 8]
[104, '女', 56, 52, 42, 41, 43, 10]
[133, '女', 56, 52, 40, 50, 42, 8]
[134, '男', 56, 52, 50, 39, 43, 8]
[130, '女', 56, 51, 35, 48, 49, 8]
[113, '女', 56, 49, 45, 50, 39, 10]
[209, '女', 56, 46, 51, 46, 52, 8]
[201, '女', 56, 43, 55, 52, 47, 8]
    .
    .
    .
[318, '女', 32, 43, 55, 50, 44, 8]
[182, '女', 31, 56, 60, 46, 52, 8]
[275, '女', 31, 46, 60, 40, 40, 8]
[396, '女', 29, 49, 55, 43, 38, 8]
[342, '女', 27, 56, 48, 44, 46, 8]
[284, '女', 25, 46, 60, 44, 46, 8]
``` 
