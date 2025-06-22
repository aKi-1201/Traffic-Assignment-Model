Data Preparation /
===

`Net Pre.ipynb`  路網資料

`OD Pre.ipynb`  旅次資料

`no_left_turn Pre.ipynb`  禁左路口資料

用以將資料轉換為 TNTP 格式 (.dat)

ta /
===
Traffic Assignment

`ta.ipynb` 

指派主程式

ta / 指派結果 /
===

`Correction for TRTS-4S.ipynb`

指派結果校估，

與實際值、CUBE 模擬值相比較

![image](https://github.com/aKi-1201/Traffic-Assignment-Model/blob/main/%E6%A0%A1%E4%BC%B0104%E5%B9%B4%E6%99%A8%E5%B3%B0%E6%8C%87%E6%B4%BE%E6%B5%81%E9%87%8F.png)

![image](https://github.com/aKi-1201/Traffic-Assignment-Model/blob/main/%E6%A0%A1%E4%BC%B0104%E5%B9%B4%E6%98%8F%E5%B3%B0%E6%8C%87%E6%B4%BE%E6%B5%81%E9%87%8F.png)

TRTS-4S 路網編修
===
##新生北路平面 車道數有誤（僅部分拆除路網）

link 6597 -> 6598, 8414 -> 9214

lanes = 2


##中山北路四段 車道數調整（僅全線拆除路網）

link 8342 -> 6675
link 6675 -> 8343
lanes = 4


##新增洲美福國路北出南入匝道節點

link 27278 -> 27609

link 27609 -> 27277

level = 2, class = 9, lanes = 1, S0 = 52


##百齡橋 class 調整

class 27 -> class 26
（省道橋梁分隔車道較寬 -> 車道較窄）


##國一圓山至內湖開放路肩

link 6325 -> 6326

link 6323 -> 6324 

lanes = 3


##基隆路 S0有誤

link 8892 <-> 15321 

S0 = 32


##國一內湖至汐止 車道數有誤

#【北向】

link 6982 -> 6882 -> 6883 -> 5032  lanes = 3

5032 -> 5033  lanes = 5

5033 -> 7193  lanes = 3

#【南向】

link 7192 -> 5022  lanes = 3

5022 -> 5023  lanes = 5

5023 -> 6886 -> 6887 -> 6978  lanes = 3
