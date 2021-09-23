## 購買書籍備註與參考:https://github.com/madscheme/introducing-python

#### Ch01 初嘗PY
#### Ch02 資料:型態、值、變數與名稱
  >  
1. Python的資料都是物件
2. 型態
3. 可變性-(強定型):物件的型態不可改變
4. 常值
5. 變數-命名規則、保留字
6. 賦值
7. 變數是名稱，不是位置-垃圾回收器
8. 指派給多個名稱
9. 重新指派名稱
10. 複製-如果是陣列，被複製的值會跟著改變。
11. 選擇好的變數名稱
#### Ch03 數字
1. 布林-非0都為True
2. 整數
3. 字面整數
4. 整數運算-//整數捨去(divmod回傳Tuple)
5. 整數與變數
6. 優先順序
7. 底數
   + 二進制(0b,0B)-反bin
   + 八進制(0o,0O)-反oct
   + 十六進制(0x,0X)-反-hex
   + 字元-chr-反ord
8. 型態轉換
9. Int有多大-python3後為任何大小
10. 浮點數-5e1=50.0

#### Ch04 用IF來選擇
1. 用#來註釋
2. 用\來延續一行文字
3. 用if、elif與else來進行比較
4. 什麼是Ture-False明細-(null、空字串、空串列、空字典、空集合)
5. 用in來做多項比較
6. 新功能:我是海象(walrus) name := expression

#### Ch05 文字字串
  >  
1. 用引號來建立-三引號可用再多行字串
2. 用str()來建立
3. 用\來轉義
   + \n 換行
   + \t 對齊文字
   + \' 單引號
   + \\ 反斜線
4. 用 + 來結合
5. 用 * 來重複
6. 用 [] 來取得字元
7. 用slice來取得子字串-offset起始 letters[start : end : step]
8. 用len()取得長度
9. 用split()來拆分-tasks.split(',')
10. 用Join()來結合-aaa_string = ', '.join(aaa_list)
11. 用replace()來替換 - aaa.replace('aaa', 'bbb')
12. 用strip()來剝除 - aaa.strip() 去除空白 - lstrip,rstrip
13. 搜尋與選擇  
    + aaa.find  
    + aaa.index  如不存在會給-1
    + aaa.count  
    + aaa.isalnum 判斷是否只有字母與數字
14. 大小寫
    + aaa.capitalize()  第一字大寫
    + aaa.title() 所有單字第一字大寫
    + aaa.upper()  所有單字大寫
    + aaa.lower()
    + aaa.swapcase() 大小寫對調
15. 對齊方式
    + aaa.center(30)
    + aaa.ljust(30)
    + aaa.rjust(30)
16. 格式化
    + 舊式：％
    + aaa.ljust(30)
    + aaa.rjust(30)
17. 
