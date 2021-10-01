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
13. 函式是一級公民 - 函式內可再放函式 - 
    ``` python
    def add_args(arg1, arg2):
       print(arg1 + arg2)
    aaa(add_args, 5, 9)
    14
    ``` 
14. 內部函式 - 內部函式自動接上一層變數 
    ``` python
    def aaa(a, b) 
      def bbb(c,d)
        return c + d
      return aaa(a,b)  
    aaa(4,7)
    11
    ```
15. closure - 可以更改或記得函式外面建立的值
    ``` python
    def aaa(saying) 
      def bbb()
        return "we are the knights who say: '%s'" % saying"
      return bbb  
    a = aaa('Duck')
    b = aaa('Hasenpfeffer')
    a()
    we are the knights who say:Duck
    b()
    we are the knights who say:Hasenpfeffer
    ```
16. 匿名函式：lambda - 取代小函式
    ``` python
    def aaa(words, func) 
      for word in words:
        print(func(word))
    stairs = ['thud','meow','thud','hiss']
    def enliven(word):
      return word.capitalize() + '!'
    aaa(stairs,enliven)
    Thud!
    Meow!
    ...
    ```
    ``` python
    def aaa(words, func) 
      for word in words:
        print(func(word))
    stairs = ['thud','meow','thud','hiss']
    aaa(stairs, lambda word: word.capitalize() + '!'
    Thud!
    Meow!
    ...
    ```
17. 產生器(generator) - sum(range(1,101)) - 5050
18. 產生器函式 - 回傳用yield  -  只能使用一次
    ``` python
    def aaa(first=0,last=10,step=1) 
      number = first
        while number < last:
          yield number 
          number += step
    ranger = aaa(1,5)
    for x in ranger:
      print(x)
    1
    2
    3
    4
    ```
19. 產生器生成式 - 類似產生器，只是在小括號，暗中執行yield
    ``` python
    genobj = (aaa((['a','b'],['1','2'])) 
    for thing in genobj:
      pring(thing)
    ('a','1')
    ('b','2')
    ```
20. 裝飾器 - 接收一個函式，並回傳另一個函式
    ``` python
    @_document_it
    def add_ints(a, b):
      return a + b
      
    add ints(3,5)
    start function add_ints
    position arguments: (3,5)
    ...
    ```
21. 名稱空間與作用域 - 全域與區域變數
22. 在名稱內使用_與__  -  使用兩個底線表示保留字串，不可改變  -  aaa.__name__ 
23. 遞迴 - yield from flatten(item) 
24. 非同步函式  -  async , await
25. 例外
26. 用try 和 except來處理錯誤 except exceptiontype as name
27. 製作你自己的例外  Exception

#### Ch10 喔喔 : 物件與類別
1. 物件 - 有屬性跟方法
   + 用class定義類別 class Cat():
   + 屬性 a_cat.age = 3
   + 方法
   + 初始化 def __init__(self):
2. 繼承
   + 從父類別繼承 - class Yugo(Car): 繼承car
   + 複寫方法 - 將Def重寫 - yogo自己的print
   + 添加方法 - 多寫新類別的DEF - yugo多一個功能
   + 用super()來取得父類別的幫助 - 用繼承無法保留父類別的功能 - 如要連動需使用super()
   + 多重繼承 - 方法解析順序 - 祖父、父母、子  往上推
   + Mixin - 輔助類別(helper) class PrettyMixin():
   + 自(self)衛 : 第一個引數為self
3. 屬性存取
   + 直接存取
     + 正確: fowl = Duck('aaa')
     + 錯誤: fowl.name = 'Daphne'
   + getter與setter 屬性的隱私介紹
   + 用來存取屬性的property
     + getter前面加上@property
     + setter前面加上@name.setter
   + 用property回傳算出來的值 
    ``` python
    def Circle(self, radius):
      def __init__(self, radius):
        self.radius = radius
      @property 
      def diameter(self):
        return 2 * self.radius
      c = Circle(5)
      c.radius
      5
      c.diameter   #但不可用c.diameter=20，隱私，會出錯
      10 
    ```
   + 修飾名稱來保護隱私 - fowl.__Duck_name 可以讀取
   + 類別與物件屬性 - 類別不會互相影響
4. 方法型態
   + 實例方法 - self
   + 類別方法 - 影響所有物件 @classmethod - cls.count
   + 靜態方法 - 不影響他的物件@staticmethod
   + 鴨子定型 - 物件導向的多型
   + 魔術方法 - 
     + 比較
       + __eq__ - == 
       + __ne__ - !=
       + __lt__ - <
       + __gt__ - >
       + __le__ - <=
       + __ge__ - >=
     + 算數
       + __add__ - +
       + __sub__ - -
       + __mul__ - *
       + __floordiv__ - //
       + __truediv__  -/
       + __mod__ - %
       + __pow__ - **
     + 其他
       + __str__ 
       + __repr__ 
       + __len__ 
5. 聚合與組合 - duct = Duct(a_bill, a_tail) - duck.about
6. 何時該使用物件或其他東西
   + 當你有很多實例，非常類似方法，但不同屬性時
   + 類別可以繼承，模組不行
   + 只需要使用一個某種東西，模組可能是最好選擇(java singleton)
   + 字典
   + 資料類別(dtaclass)
7. 具名tuple - from collections import namedtuple - Duck = namedtuple('Duck', 'bill tail')
   + 優點為不可變物件
   + 解省空間與時間
   + 句點點標記法取代字典風格
   + 可以當字典使用
8. 資料類別 - @dataclass 
9. Attrs - 主要省略很多魔術方法，attrs，它主要是用來修飾 class 類的，而 attrib 主要是用來做屬性定義的
   + pip3 install attrs cattrs
    ``` python
    from attr import attrs, attrib
 
    @attrs
    class Color(object):
        r = attrib(type=int, default=0)
        g = attrib(type=int, default=0)
        b = attrib(type=int, default=0)
 
    if __name__ == '__main__':
        color = Color(255, 255, 255)
        print(color)
    ```
#### Ch11 模組、程式包與好東西
1. 模組與import陳述式
   + 匯入模組
   + 用其他名稱匯入模組 import fast as f
   + 只從模組匯入你想要的東西 from fast import pick
   + 程式包 - 新增目錄導入
   + 模組搜尋路徑 - import sys - sys.path - sysy.path.insert(0, "/my/modules"
   + 相對與絕對匯入 from .. import rougarou
   + 名稱空間程式包 - 多層目錄命名
   + 模組 vs. 物件 - 模組:導入的變數可以使用並改變，物件的樹性要另外存取
2. Python標準程式庫裡面的好東西
   + 用setdefault()與defaultdict()處裡缺漏的鍵
   + 用counter()來計算項目的數量
   + 用orderedDict()與鍵來排序 - 是用python3.7以前
   + 堆疊 + 佇列 == deque - 回文檢查 - 或使用 slic將字串反過來
   + 用itertools來迭代程式結構
     + clain() 讀取
     + cycle() 重複
     + accumulate() 總和
     + accumulate(字典,函數) 計算
   + 用pprint()印出漂亮的東西
   + 取得隨機值 
     + choice
     + sample
     + randint
     + randrange
     + random
   + 其他的電池
     + pypi
     + github
     + readthedocs
#### Ch12 玩轉資料
1. 文字字串:Unicode
   + python 3 Unicode字串
     + unicodedata.lookup
     + unicodedata.name
     + 'caf\u00e9'
     + 'caf\N{LATIN SMALL LETTER E WITH ACUTE}'
   + UTF-8 - 動態編碼方式  1-4個位元
     + snowman = '\u2603'  #unicode字串
     + len(snowman)    # 1
     + ds = snowman.encode('utf-8')   # unicode字元編碼成byte
     + len(ds)   # 3  b'\xe2\x98\x83
   + 解碼 - place2 = place_bytes.decode('utf-8')
   + HTML實體
     + htmlunescape("&egrave;")
     + html5["egrave"]
     + python 要用 ord取得字元的十進制
   + 標準化
     + eacute1 ='e'         #UTF-8
     + eacute2 = '\u00e9'   #unicode 碼位
     + eacute3 = \'\N{LATIN SMALL LETTER E WITH ACUTE}'  #unicode 名稱
     + eacute4 = chr(233)   #10
     + eacute5 = chr(0xe9)  #16 
2. 文字字串：正規表示式   import re
   + 用match()來確定開頭是否符合  re.match('*Frank', source)
   + 用search()找到第一個符合的對象  re.search
   + 用findall()尋找所有符合的對象  
   + 用split()在符合的地方拆開
   + 用sub()來替換符合的對象
   + 模式:特殊字元
     + . \n 外的字元
     + * 任何
     + ? 可有可無
     + \d 一個數字
     + \w 一個英數
     + \s 空白 
   + 模式:使用說明符 - ^ 開頭 $ 結尾 [] or
   + 模式:指定match()輸出
3. 二進制資料
   + byte與bytearray - bytearray可以更改值 
4. 用struct來轉換二進制資料
5. 用binascii()來轉換byte /字串
6. 位元運算子
#### Ch13 日曆與時鐘
1. 閏年 - isleap
2. datatime模組
   + date
   + time
   + datetime
   + timedelta(days=1)
   + isoformat
   + now
   + combine
3. 使用time模組 import time -絕對時間 - 要使用UTC來取代時區 -struct_time值
4. 讀取與寫入日期與時間 - strftime() - strptime()
5. 所有轉換
#### Ch14 檔案與目錄
1. 檔案輸出與輸入
   + 用open()建立或開啟 - fileobj = open(filename,mode)
     + r 讀取 w寫入 x寫入 a附註
     + t 文字 b 二進制
   + 用print() 寫入文字檔  fout = open('oops.txt', 'wt') - print('xxx', file=fout) - fout.close()
   + 用write()寫入文字檔 fout.write(poem)
   + 用read()、readline()或readlines()讀取文字檔
   + 用write()寫入二進制檔案
   + 用read()讀取二進制檔案
   + 用with自動關閉檔案
   + 用seek來更改位制 - tell回傳目前位位置
2. 記憶體的對應
3. 檔案操作
   + 用exists來檢測是否存在
   + 用isfile()來確認型態
   + copy
   + rename
   + link symlink
   + chomd
   + chown
   + remove
4. 目錄操作
   + midir
   + rmdir
   + listdir 來列出內容
   + chdir 來切換目錄
   + glob來列出相符合檔案
5. 檔名
   + abspath()取得路徑
   + realpath()取得符號連結路徑名稱
   + 用os.path.join鍵裡路徑名稱
   + 使用pathlib
6. BytesIO與StringIO
#### Ch15 時間中的資料:程序與併行處理
1. 程式與程序
   + 說明
     + os.getpid
     + os.getgid
     + os.getcwd
   + 用 subprocess建立程序 .getoutput('date')取得程式輸出
   + 用 multiprocessing來建立程序
   + 用 terminate()終止程序
   + 用 os取得系統
     + os.uname
     + os.getloadave
     + os.cpu_count
     + os.system() 類似終端機輸入命令
   + 用psutil取得程序資訊
     + pip install psutil
     + psutil.cpu_times(True)
2. 命令自動化
   + 呼叫 - pipinstall invoke
   + 並行 
   + 佇列
   + 程序
   + 執行續 - 無法終止，因此多用multiprocessing
   + concurrent.futures - worker - processes - threads
   + 綠色執行與gevent 程式庫是事件式的程式庫
   + twisted 非同步，事件是網路框架
   + asyncio
   + Redis
   + 佇列之外的選項
#### Ch16 盒子資料 : 持久保存
1. 平面文字檔
2. 有填補的文字檔
3. 表格式文字檔
4. CSV
   + XML import xml.etree.ElementTree as et
   + XML安全注意事項 fro deausedxml.ElementTree import parse
   + HTML
   + JSON dumps導入
   + YAML 需用safe_load
   + Tablib 
   + Pandas
   + 組態檔
5. 二進制檔案
   + 有填補的二進制檔案與記憶體對映
   + 試算表
   + HDF5
   + TileDB
6. 關聯資料庫
   + SQL
   + DB-API
   + SQLLITE
   + MYSQL
   + SQLite
   + PostgreSQL
   + SQLAlchemy
   + 引擎層
   + SQL Expression Language
   + Object-Relational Mapper(ORM)
   + 
7. 
