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
      + %s 字串
      + %d 十進
      + %x 十六進
      + %o 八進
      + %f 十進浮點
      + %e 指數
      + %g 十進浮點
      + %% 常數
      + 用法::'%s' % (cat)
    + 新式：{}與format()
      + 'The {} is in the {}.'.format(thing, place)
    + 最新式：f-strings 
      + python 3.6以上
      + f'The {thing} is in the {place}'
      + python 3.8以上  除錯用 : f'{thing =}, {place =} 連同變數印出來

#### Ch06 用while與for來執行迴圈
  >  
1. 用while來重複執行
2. 用break來取消
3. 用continue來跳過
4. 用else來檢查break
5. 用for與in來迭代
6. 用range()來產生數字序列
   + for x in range(0,3)
   + for x in range (2, -1, -1)  2到0
   + list( range(0,11,2) ) 0到10間偶數

#### Ch07 tuple與串列
1. 用逗號與()來建立
   + aaa = ('bbb')
   + aaa = 'bbb'
   + 拆包 a,b,c = aaa
2. 用tuple()來建立
