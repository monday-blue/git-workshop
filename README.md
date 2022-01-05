
---
# 2021/12/25-26 NodeJS 筆記
---

- 授課教師：
姓名： Ashley (小賴) 賴怡玲     
Email: ashleylai58@gmail.com   

- 共筆與課程資料連結：
  - [12/25  Git Workshop for MFEE22](https://hackmd.io/Ns0AuMFtROOT9E0oSujQ7A)
  - [12/26  NodeJS Workshop for MFEE22 (1)](https://hackmd.io/uCD6ReA5TZ2m-9cgf9v5zw)

  - 作業繳交表:
https://docs.google.com/spreadsheets/d/1CtihKZugWCsyzeFvI1q3EOBCLsCYTI9Wpzm8wB-VwOk/edit?usp=sharing

  - 錄影檔:
https://drive.google.com/drive/folders/1SOEbo95N_LnQeYtim0CvRm3K6saHuiTG?usp=sharing


  - 小賴老師的github：
https://github.com/azole/node-mfee22

- 作業
- [x] 熟悉終端機指令
- [x] 熟悉 git 操作
- [x] 練習 markdown 語法

- [x] 在 github 上建立一個叫做 git-workshop 的 repo
- [x] 至少有要一個 readme.md 記錄 12/25-26 的上課筆記 & 心得
- [x] 請看完 [超級歪-解鎖大腦潛能影片](https://www.youtube.com/watch?v=DgbSc6Ys710) ，建立一個 video.md 的檔案，寫觀影心得
- [ ] 複習 JS 語法，特別 array 的相關函式 (還在緩慢複習中...進度跟不太上QQ)
- [ ] 學習 [ES6 的語法](https://gretema.github.io/javascript/20200504/221423942/) (還在緩慢複習中...進度跟不太上QQ)
- [x] 作業系統複習
- [x] (optional) sum.js 自己做做看測試評估以下四個版本的時間
	- for       (大眾解 XD)
	- 公式解     (靖宇、易澤)
	- recursive (博榆)
	- reducer   (華如）

1/5 (三) 晚上 12點前交

&nbsp;
&nbsp;


---
# 摘要
---

1. Markdown語法 - e.g. HackMD
2. Git相關概念、Terminal(終端機)指令、Git指令
3. JS語法
4. NodeJS介紹與安裝、作業系統概念
5. 書籍與其他重要概念
6. 課後心得

&nbsp;
&nbsp;

---
# Markdown語法 - e.g. HackMD
---

## 一、文字相關

### 1. 標題字

# h1 (下面會自動有一條淡灰線)
## h2 (下面會自動有一條淡灰線)
### h3
#### h4
##### h5
###### h6
&nbsp;


### 2. 內文字
直接打字即可。
&nbsp;

### 3. 文字樣式(行內元素)
＊一個 ---> *斜體*     
＊後加空白 ---> * 可以真的打出＊*     
_不加空白 ---> _斜體_     
＊＊兩個 ---> **粗體**     

&nbsp;

### 4. 引用文字(階層)
加>號
> 引用文字
> 引用文字
> 引用文字

>>  引用文字
>>>  引用文字
&nbsp;

### 5. 換行文字與加空白行
換行：行後加 兩個或多個空白鍵 然後按 enter    
加一個以上的空白行：打html語法 \&nbsp;     

&nbsp;
&nbsp;
       
       
## 二、列點相關
- 第一大點 ( - / ＊ / + )
  - 第一小點（tab鍵或2個空白鍵）
  - 第二小點
	- 第一小小點
	- 第二小小點
- 第二大點
&nbsp;

1. 第一大點
2. 第二大點
   1.第一小點
   2.第二小點 
3. 第三大點

4\. 加 \ 讓數字加點跳脫不轉換成清單
&nbsp;

- [x] checkbox打勾 
- [ ] checkbox不勾
- [ ] checkbox不勾
&nbsp;
&nbsp;


## 三、程式碼相關
### 1. 區塊程式碼加三個\`\`\`後加語法名稱
  
  ```javascript
  function sum( n ) {
    let sum = 0 ;
    for ( let i = 0 ; i <= n ; i++ ) {
        sum = sum + i ;        
    } // for
    return sum ;

  } ;
  
  console.log( sum(1) ) ;  // 1
  console.log( sum(2) ) ;  // 3
  console.log( sum(5) ) ;  // 15
  console.log( sum(10) ) ; // 55
  
  ```
  
### 2. 行內程式碼加\`\`包住
元素`<style></style>`裡面可以加CSS樣式
&nbsp;
&nbsp;


## 四、連結相關
### 1. 超連結
\[連結文字](連結網址)
[Google](https://www.google.com.tw/)

### 2. 圖片連結
\!\[圖片文字](圖片網址 "滑鼠停留文字")
![聖誕節](https://images.unsplash.com/photo-1479722842840-c0a823bd0cd6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2072&q=80 "滑鼠停留文字在此")

### 3. URL
<>     
<https://www.google.com.tw/>

文中 加空白 再打 ＊ 可加連結的文字樣式      
要去youtube *[請點此](https://www.youtube.com/)*     
要去youtube **[請點此](https://www.youtube.com/)**    

&nbsp;


## 五、表格相關

|  tr   |  tr  |
|  ---  | ---  |
|  td   |  td  |
|  td   |  td  |

目前在markdown語法表格無法合併欄

&nbsp;
&nbsp;




---
# Git相關概念、Terminal(終端機)指令、Git指令
---
## 一、Git相關概念
### 1. 分支(branch)
分支主要用來避免自己的程式作業影響到別人在專案中已完成並push或merge到github的主程式碼。

主分支現預設名稱為Main,因之前的預設名稱Master帶有歧視問題(master主要的機器 - slave備份的機器)，修改預設名稱指令為`$ git branch -M (master原名不寫也可以) main` 。     

![Imgur](https://i.imgur.com/WnoFdII.jpg)     
[修改圖片來源](https://www.nobledesktop.com/learn/git/git-branches)

&nbsp;

### 2. Git Flow
Git Flow為專案開發的github分支命名分配與pull、commit方向流程。
下圖的release和master分支為正式專案主幹，通常工程師不會commit到這上面，hotfix為正式版發現緊急bug時分出的修改分支。

develop為主開發分支，工程師通常從develop分支再分出功能與功能更細項(feature)，一項功能寫完後再commit回develop分支。     

Q. feture分支如何切？     
A. 需要團隊討論得到共識。     
     
Q. 多久（寫多少程式）應該 commit (到develop分支) 一次？     
A.「團隊一致性」，原則上是盡量小、但要完整     
-> 建議每天下班前請先 commit 一次(在自己的feature分支)     
	- 看進度     
	- 萬一電腦/人出問題     

而在功能完整要commit到develop分支時，通常不會直接魯莽的就把feature分支merge(merge指令通常不會直接使用)到develop分支，而是先commit後，去github進行pull requests，再請同事主管code review確認後(在此期間可以使用issues功能交流)，從github上按merge按鈕來做confirm merge動作。     
![Git Flow](https://gitbook.tw/images/tw/gitflow/why-need-git-flow/flow.png)
[圖片來源](https://gitbook.tw/images/tw/gitflow/why-need-git-flow/flow.png)

&nbsp;
&nbsp;

## 二、Terminal(終端機)指令

|  MacOS指令   |  作用  |
|  ---  | ---  |
|  cd   |  進入 |
|  cd ．．  |  進入上層 |
|  cd ~  |  進入使用者目錄 (~代表使用者目錄) |
|  pwd   |  顯示現在路徑  |
|  mkdir   |  建立資料夾  |
|  touch   |  建立檔案  |
|  cp   |  複製檔案  |
|  mv   |  移動檔案  |
|  rm   |  刪除檔案  |
|  nano   |  修改檔案內容  |
|  cat  |  顯示檔案內容  |
|  ls  |  列出全部檔案  |
|  ls -a  |  列出全部檔案（包含隱藏檔）  |
|  ls -l   |  以完整格式列出檔案  |
|  ls -al   |  以完整格式列出全部檔案（包含隱藏檔） |
|  clear  |  清除terminal的畫面  |

> ps. 在MacOS的terminal裡，桌面與下載資料夾分別為Desktop與Downloads。

> ps. 在要執行ls指令時，MacOS新系統因安全性設定有改變，會出現Operation not permitted問題，解決方式為： 蘋果圖示 -> 系統偏好設定 -> 安全性與隱私權 -> 隱私權 -> 找到完全取用磁碟 -> 加入terminal應用程式並勾選。

&nbsp;

## 三、Git指令

需至github網站註冊一個github帳號，未安裝git可到官網下載或用Homebrew，git版本更新也可用Homebrew`$brew install git`。然後在github建立一個專案倉庫(repository)。

**1.設定環境變數(在 ~ 設定，不然之後會常出現Permission denied問題)**
|  Git指令   |  作用  |
|  ---  | ---  |
|  git config --global user.name "user" |  設定User訊息 |
|  git config --global user.email "user@gmail.com"  |  設定User訊息 |

**2.初始化資料夾讓git管理**
|    Git指令      |  作用  |
|    ---      | ---  |
|    git init       |  init(initial)，初始化一個資料夾，讓這個資料夾可以被git管理(要cd進入要被git管理的資料夾進行此動作，不然會整個電腦被git控制)，做完後可以看到資料夾有一個隱藏的.git資料夾  |

**3.本地倉庫與遠端倉庫互動的動作**

|  Git指令   |  作用  |
|  ---  | ---  |
|  git add .  |  將所有檔案加入暫存區  |
|  git add 00.js    |  將00.js單一檔案加入暫存區  |
|  git restore --staged 00.js |  反悔git add 00.js到暫存區  |
|  git commit -m "commit註解" / 簡寫 git ci -m "commit註解" |  將檔案加註解並加入儲存庫 |
|  git ci -am "新commit註解"  |  已經git add過的檔案要再次commit  |
|  git restore 00.js |  反悔剛剛的修改  |
|  git status / 簡寫 git st  |  查看git的狀態  |
|  git diff  |  檢視這次修改的差異  |
|  git branch / 簡寫 git br  |  檢視目前分支的狀態，＊為目前所在的分支  |
|  git branch 分支名  |  建立分支與命名  |
|  git switch 欲切換到的分支名  |  切換分支  |
|  git merge feat-login |  把feat-login分支合併進來到你當前所在的分支  |
|  git push -u origin main |  -u設定upstream，來源為遠端倉庫的main，第一次push要這樣下，之後就可以只寫git push  |
|  git pull origin main |  把遠端倉庫的main分支pull下來到本地倉庫並merge到本地工作目錄  |
|  git clone HTTP/SSH連結網址  |  將遠端倉庫的整份專案複製到本地倉庫(要cd進要clone到的資料夾)  |

> ps.現在若有A、B兩分支，若要將A分支merge到B分支，必須先下 git switch B 指令，當前在B分支，然後再下 git merge A 指令，把 A分支 合併進 B分支，但通常merge動作會透過github的pull request進行。

> ps.衝突解決：藍色>>>，綠色<<<

> 本地工作、本地暫存區、本地倉庫、遠端倉庫

![Imgur](https://i.imgur.com/gmn0DaA.png)

&nbsp;

**4.查看相關**
|  Git指令   |  作用  |
|  ---  | ---  |
|  git log  |  查看提交紀錄  |
|  git log 00.js  |  查看00.js的提交紀錄  |
|  git log -p 00.js  |  查看00.js修改細節 |
|  git log --grep="delete"  |  可以針對 commit 訊息做搜尋  |
|  git blame 00.js  |  查看00.js內容是誰編寫的  |


&nbsp;
&nbsp;

---
# JS語法
---

## 一、filter與reduce函式
```javascript=
let data = [
    { id: 1, level: 'A', rate: 1 },
    { id: 2, level: 'B', rate: 3 },
    { id: 3, level: 'C', rate: 4 },
    { id: 4, level: 'D', rate: 2 },
    { id: 5, level: 'E', rate: 1 },   
]

let result = data.filter((item) => item.level === 'A').reduce((acc, item) => acc + item.rate, 0);

console.log(result)
```
```javascript=
let data = [
    { id: 1, title: 'AAAA', price: 100, count: 2 },
    { id: 4, title: 'BBBB', price: 200, count: 1 },
    { id: 6, title: 'CCCC', price: 300, count: 1 },
    { id: 1, title: 'DDDD', price: 500, count: 2 },  
]

let result = data.reduce((acc, item) => acc + item.price * item.count, 0)

console.log(result)
```

 
 
## 二、sum加總功能不同寫法
 我的寫法
```javascript=
function sum(n) {
    let sum = 0 ;
    for(let i = 0; i <= n; i++) {
        sum = sum + i;        
    } // for
    return sum;

  };
  
```
 大部分同學的寫法
```javascript=
function sum(n) {
    let sum = 0 ;
    for(let i = 0; i <= n; i++) {
        sum += i;        
    } // for
    return sum;

  };
  
```
 遞迴(recursive)寫法(博榆)
```javascript=
function sumRecursive(n) {
    // 停止點
    if (n < 1)
        return 0;
    return n + sum(n - 1);
};
```
 reduce寫法(華如)
```javascript=
const sumReducer = (n) => {
  arr = [];
  const reducer = (previousValue, currentValue) => previousValue + currentValue;
  for (i = 1; i <= n; i++) {
    arr.push(i);
  }
  let result = arr.reduce(reducer, 0);
  return result;
};
```
 公式寫法(靖宇)
 ```javascript=
function sumFormula(n) {
  let result = ((1 + n) * n) / 2;
  return result;
};
```
 
 壓力測試寫法
 ```javascript=
console.time('recursive');
for (let i = 0; i < 10000; i++)
    sumRecursive(100);
console.timeEnd('recursive');
```
 Big O
Big O為演算法的效能表示方式     
O(1) > O(log n) > O(n) > O(n^2)
 
&nbsp;
&nbsp;
 
---
# NodeJS介紹與安裝、作業系統概念
---
## 一、NodeJS介紹與安裝
NodeJS可以說是一個執行環境，由Ryan研發，github開源。      
JS在瀏覽器端執行 --> html裡的<script></script>     
JS在伺服器端執行 --> NodeJS (Google Chrome V8 引擎為核心)     
     
nvm指令安裝方式     

&nbsp;

## 二、作業系統(Operating System，OS)概念

### 1. NodeJS特色

- **單執行緒** (一次只能做一件事)
- **非阻塞**
- **非同步 IO** (騙你看起來同時做了很多事，其實同一時間依然只做一件事，只是它偷偷一件事做一點點後，換另一件事做一點點，然後一直切換不同的事做一點點，直到全部的事都做完)
- **事件循環 (event loop)**

### 2. 要點紀錄
- **Process vs Thread (multi-thread)**
- **排程演算法**(作業系統在做的事), **FIFO**(First In First Out), **SJF**(Shortest Job First)
- **Thread pool**
- **Deadlock** (兩precess彼此形成circular waiting的情況，因此processes皆無法繼續執行，導致CPU利用度及產能急速下降)
- **Context Switching** (CPU將執行中的process切換給其他process使用時，必須保存目前執行中process的狀態，並載入欲執行process的狀態資訊)
- **Producer & Consumer** (當Buffer滿時，producer必須等待。當buffer空時，consumer必須等待。採用一個共用變數count來記錄buffer裡item的個數)
- **Race Condition** (共享變數的值會因為Processes執行的順序不同而有所不同)

![Imgur](https://i.imgur.com/wRvqdbG.png)

&nbsp;
&nbsp;

---
# 書籍與其他重要概念
--- 

## 一、書籍
《重構》

“任何一個傻瓜都能寫出電腦可以理解的程式，唯有優秀的程式設計師能寫出讓人讀懂的程式。”     
—M. Fowler (1999)     

《JavaScript大全》犀牛書     

《JavaScript優良部份》蝴蝶書     

《Operating System Concepts》恐龍書     

&nbsp;

## 二、重要概念摘要
(傳統)瀑布式開發 vs SCRUM開發

瀑布式開發：較適合硬體開發。     
SCRUM開發：較適合軟體開發，2-4週一個SPRINT衝刺，planning估點數，daily sync 3問，demo review，反省會議4問。

資料結構 Data Structure (DS)     
演算法 Algorithm (Algo)     
資料庫 Database (DB)     
  正規化 <-- 怎麼設計 table schema     
  （這不是一定非得要遵守的法律，但是我們會盡量遵守，的確有時候會因為一些商業邏輯特殊的設定，會違反正規化）     
網路 Networking     
作業系統 Operating System (OS)     
     
...還有很多來不及寫XD     

&nbsp;
&nbsp;

---
# 課後心得
---  
第一就想先感謝小賴老師的教學，非常能感受到小賴老師的教學熱忱，謝謝老師如此用心教導我們QQ！在平常有正職的情況下，假日還能這麼長時間的教授課程，真的才上一堂課就非常佩服小賴老師，每一句話都包含了大量的資訊(包含講古部分也好多資訊XD)，聽完頭都在冒煙感覺像聽了無數場超值的演講。(其實也想偷偷請教老師是如何維持高能量一整天及保持長時間專注的，因為覺得自己這方面不太行，嘗試改善中未果...。)

非常喜歡也感謝老師願意花時間著重講解許多課內及課外的觀念及程式理解的部分，說來慚愧因為之前的課程還跟不太上，自身理解速度非常非常的慢，還有很多對程式不理解的及需要補足的，所以當然也還談不上舉一反三...，在這一堂課，雖然跟得吃力，對接下來未知的課程難度自己能不能學好也覺得壓力山大 (抱歉，覺得吃力是因為自身聽人說話時，專注度及理解力很容易不足，之前進度又還未完全跟上，是我自身的問題與老師的教學無關～) ，但也開心又有弄懂了一些觀念\＾_＾;/。

課程中發現老師的簡報有幫CPU、記憶體、硬碟做了擬人化對白XD，很喜歡這樣的方式，活潑又有記憶點，又容易理解(雖然老師說這是課程中唯一份簡報XD)，也很感謝老師分享給我們做筆記的方式，雖然自身整理寫筆記的速度也很慢(怎麼什麼都慢@_@;)，但在寫筆記、查資料、補課的過程中，有慢慢理解一些問題，當然也有產生很多問題，之後可能需要再請教小賴老師，希望小賴老師不要覺得煩這麼基礎也在問XD;。

再次謝謝小賴老師的第一堂課，收穫良多！


&nbsp;
&nbsp;
