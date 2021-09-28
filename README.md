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
1. tuple
   + 用逗號與()來建立
     + aaa = ('bbb')
     + aaa = 'bbb'
     + 拆包 a,b,c = aaa
   + 用tuple()來建立 - 將list轉換成tuple
   + 用 + 來結合Tuple - ('aaa') + ('bbb')
   + 用 * 來重複項目 - (aaa) * 3
   + 比較tuple - a = b
   + 用for與in來迭代 - for word in words
   + 修改tuple - 不可變
2. 串列
   + 用[]來建立
   + 用List()來建立或轉換
   + 用split()和字串來建立 - aaa.split('/')
   + 用[offset]來建立 - aaa[0]
   + 用slice取得項目 - aaa[0:2]
   + 用append()將項目加到尾端 - aaa.append('bbb')
   + 用insert()和offset加入項目 - aaa.insert(2, 'bbb')
   + 用*來重複所有項目
   + 用extend()或+來結合串列  aaa.extend(字串) - 如果用append 會有子串列 非合併
   + 用[offset]改變項目
   + 用slice改變項目
   + 用del和offset來刪除項目 - del aaa[1]
   + 用remove與值來刪除項目 aaa.remove('aaa')
   + 用pop()和offset取出項目並刪除他 aaa.pop() 會彈最後面的FIFO
   + 用clear()刪除所有項目 aaa.clear()
   + 用index()和值來找到項目的offset aaa.index('aaa')
   + 用in來檢測值是否存在  'aaa' in aaa
   + 用count()來計算一個值出現的次數
   + 用join()串列轉換成字串 - ', '.join(marxes)
   + 用sort()或sorted()來排序 
     + sort()可就地排序  aaa.sort()
     + sorted()回傳串列副本 aaa_1 = sorted(aaa)
     + reverse=True
   + 用len() 取得長度
   + 用 = 來賦值
   + 用copy() list() slice來複製
     + aaa = a.copy()
     + aaa = list(a)
     + aaa = a[:]
   + 用deepcopy()來複製東西 - 如第二層需要改變值，需用到此函數
   + 比較串列
   + 用for與in來迭代
   + 用zip()迭代多個序列 平行迭代  可用來直向來製作字典。 dict(zip(english, french))
   + 用生成式來建立串列 
     + number_list = [number-1(運算式) for number(項目) in range(1,6)(可迭代物)]
     + a_list = [number for number in range(1,6) if number % 2 == 1(條件式)]
     + cells = [(row,col) for row in rows for col in cols]
   + 串列的串列
3. tuple vs. 串列 - 前者空間小，後著較好用
4. python沒有tuple生成式 - 產生器生成式(generator)

#### Ch08 字典與集合
1. 字典
   + 用{}來建立
   + 用dict()來建立
   + 用dict()來轉換 -第一個為鍵，第二個為值
   + 用[鍵]來加入或改變一個項目
   + 用[key]或[get]取得一個項目 - aaa.get('aaa')
   + 用keys() 取得所有鍵 - list(aaa.keys())
   + 用values()取得所有值  list(aaa.values())
   + 用items()取得每一對鍵/值  list(aaa.items())
   + 用len()取得長度   len(aaa)
   + 用{**a,**b}來結合字典  -  合併 為淺副本
   + 用update() 結合字典  aaa.update(bbb)
   + 用del和鍵來刪除項目   del aaa['aaa']
   + 用pop()取得並刪除它  aaa.pop('aaa')
   + 用clear()刪除項目
   + 用in來檢測鍵  'aaa' in aaa
   + 用 = 來賦值  aaa['bbb] = bbb_valuse
   + 用copy()來複製
   + 用deepcopy()來複製所有東西
   + 比較字典
   + 用for 與 in 來迭代  for card in aaa or aaa.values()
   + 字典生成式  aaa = {letter: aaa.count(letter) for letter in set(word) if letter in vowels}
2. 集合
   + 無排序
   + 用set()來建立 新增項目用{}
   + 用set()來轉換
   + 用len()取得長度
   + 用add加入項目
   + 用remove()刪除項目
   + 用for 與 in 來迭代
   + 用in來檢測值是否存在
   + 組合與運算子
     + 聯集  a | b
     + 差集  a - b
     + 互斥  a ^ b
     + 子集合 a < b
     + 超集合 a >= b
     + 真超集合  a > b
   + 集合生成式 aaa = {number for number in range(1,6) if number % 3 = 1}
   + 用frozenset()建立不可變集合  frozenset([3,2,1])
   + 截至目前為止的資料結構
   + 製作更大型的資料結構  gps座標

#### Ch09 函式
1. 用def定義函式
2. 用小括號呼叫函式
3. 引數與參數
4. None是有用的
5. 位置性引數 - def menu(wine, entree, dessert): - 缺點常忘記順序
6. 關鍵字引數 - menu(entree='beef',dessert='bagel',wine='bordeaux)
7. 指定預設參數值 - def menu(wine, entree, dessert='pudding) 如有參數根據參數為主，需進行清空動作
8. 用*來炸開/收集位置引數 - def print_args(*args) - tuple
9. 用*來炸開/收集關鍵字引數 - def print_kwargs(*kwargs) -dict
10. 純關鍵字引數 - def aaa(data, *, start=0, end=100) - 單*表示後面變數要用具名引數
11. 可變與不可變引數 - 函數內儘量不要改變引數，需透過return
12. Docstrings - 函數下說明 可使用 ' ' or '''   ''' - 可用help(函數)來看說明
13. 函式是一級公民 - 函式內可再放函式 - aaa(add_args, 5, 9)     
14. 內部函式 - 內部函式自動接上一層變數 
    ``` python
    def aaa(a, b) 
      def bbb(c,d)
        return c + d
      return aaa(a,b)  
    aaa(4,7)
    11
    ```
15. - 
