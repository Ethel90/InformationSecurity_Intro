## __Internet Security__
- 中間人攻擊(Man-in-the-middle Attack)
    - 指攻擊者冒充受害者與他人的連線，藉此插入受害者的通話連線中，並透過嗅探等方式獲取通話間的資料
- 防火牆設置在router上
- 典型入侵方式
    - 掃描網路來找到
        - 哪些IP正被使用中
        - 電腦主機使用哪種作業系統
        - 監聽主機的TCP或UDP埠(Ports) 哪些被打開(Open)
        - 針對那些被打開的埠來執行`Exploit`scripts指令
        > su -> 管理者權限
    - 利用具有特權指令的管理者帳號“suid” 來存取作業系統的命令列模式(Shell)
    - 從駭客(Hacker)的網頁中下載某些系統程式，使得破解者(Cracker) 有更多的時間來入侵系統而不被發現
    - 找尋系統存在之脆弱點
    - 植入後門程式
- 字典攻擊法(Dictionary Attacks)
> 最常用的暴力攻擊法
- 邏輯炸彈(Logic Bomb)
    - 通常嵌入在正常軟體中
    - 在某些事件發生(點燃導火線)，就突然引爆
- 特洛伊木馬
    - 通常是某些好用的程式中，暗藏會造成傷害或是侵犯對方隱私的功能
    - 駭客可以側錄使用者的密碼，或在系統中開啟一道後門來作為入侵管道
- 電腦病毒生命週期
    - 潛伏階段(Dormant Phase)
    - 繁殖階段 (Propagation Phase) 
    - 觸發階段(Triggering Phase) 
    - 執行階段(Execution Phase)
- 巨集病毒(Macro Virus)
    - 利用軟體提供之巨集功能撰寫而成
    - 與作業平台相互獨立(Platform Independent)
- ITU- T的X.800建議書(Recommendation)，也就是「 OSI安全架構」
    - OSI安全架構提供了規劃安全作業的方法
    - 廠商依據OSI安全架構制訂相關產品及服務的安全功能
> 國際電信聯盟通訊標準部門簡稱ITU-T -> 聯合國所發起的通訊及開放系統網路組織
#### 威脅與攻擊
- 依據RFC 2828文件所定義
- 威脅(Threat)
    - 可能破壞系統安全的情況能力或行為
- 攻擊(Attack)
    - 利用已知的技術，並且有計畫的迴避系統的安全服務
- 主動式攻擊(Active Attacks)
    - 中途竊取(機密性)
- 被動式攻擊(Passive Attacks)
    - 目的在於獲得被傳送的資訊 
    - 主要透過竊聽(Eavesdropping)、監控傳輸(Monitoring)
    - 修改偽造(完整性)、阻斷(可靠性)
- X.800將安全服務分成五個類別
    1. 認證(Authentication)
    2. 存取權控制(Access Control)
    3. 資料完整性(Data Integrity)
    4. 資料機密性(Data Confidentiality)
    5. 不可否認性(Nonrepudiation)

- 對等實體認證( Peer Entity Authentication) 
    - 辨別雙方身份
- 資料來源認證( Data Origin Authentication)
    - 收到資料時確認sender的身分
- 資料完整性
```
- 連接導向(Connection-oriented)的完整性服務
    - 保證收到的訊息如寄送端所送出的內容
    - 沒有任何的複製、增添、修改、重新排列、重播
    - 可以指出包括訊息串流的修改和阻絕服務
- 非連接導向(Connectionless)的完整性服務
    - 僅提供預防訊息修改的保護
```
- 可利用的服務(Availability Service)
    - X.800和RFC2828都將可用性(Availability)定義成系統或系統資源的特性
    - 可用性會根據系統的執行規格而定
    - 遭受攻擊會導致系統失去或減少部分可用性
    > 是一種確保系統可用的防護
- 網路安全模型的目標
    - 可用性
    - 保密性
    - 完整性
    - 確認性
- 常見攻擊模式
    - 中斷：對「可用性」做攻擊
        - e.g. 提款機的線路被中斷後便無進行提款
    - 竊取：對「保密性」做攻擊
        - e.g. 例如利用擷取封包程式來監聽網路上的通訊訊息
    - 竄改：對「完整性」做攻擊
        - e.g. 擷取在網路上的訊息並修改後再傳送出去
    - 偽造：對「確認性」做攻擊
        - e.g. 傳送假的訊息到網路上
- 當事人(Principal)
    - 處理透過網路將訊息從一方被傳送到另一方兩端收送合作交易的人
- 網路安全模型所提供的安全技術可分為兩個重點
    - 傳送的資訊應作安全轉換
    - 機密資訊不被洩露
- 雜湊函式(Hash) -> one way trap door function（不可回推）
#### 常見的惡意程式
- 後門程式
    - 建立祕密通道於電腦系統中，之後再利用一些特別的輸入程序打開通道，便可溜進該電腦系統中
- 細菌
    - 在電腦系統裡面大量的自我複製，企圖大量佔據並消耗系統資源
- 邏輯炸彈
    - 寄生於某程式中，當如特定日期的到來，某種應用程式被使用，或者某些檔案出現等特定條件成立時，便進行破壞
- 守門人防線
    - 第一道防線-使用者的登入及偵測
        - 以密碼為基礎來設計登錄程式以拒絕非法使用者的存取
        - 設計過濾機制來偵測和拒絕蠕蟲、病毒、和其它類似的攻擊
    - 第二道防線-存取控制系統
        - 辨識使用者身份
        - 辨識成功後，給予適當的使用權限
    - 第三道防線-內部控制組成
        - 它是以監控活動和分析資訊的存取，來嘗試測非法入侵者的存在問題
- 閘道防火牆已無法提供足夠的防護來對抗入侵威脅
    - 因為對網路「邊界」的定義已經變得模糊
        - 遠端存取伺服器、點對點連線(Peer to Peer Connection)與無線基地台等都意味著曾經有清楚定義的網路邊界已不存在
### __網路安全機制__
- 網際網路通訊協定(IP)
    - 為非連線(Connectionless)
    - 屬於網路架構第三層（網路層）
    - 為非可靠(Unreliable)的通訊協定
        - 資料(Datagram)傳輸在過程中可能遺失或順序顛倒
        - TCP則是改良這些缺點
- IP層級的安全性的三種安全機制
    - 認證(Authentication)
    - 私密性(Confidentiality)
    - 金鑰管理(Key Management)
- 假冒網路位址(IP Spoofing)
    - 是IP層級常見的攻擊類型
    - 攻擊者利用假造的IP位址在網路上為所欲為
- IPSec
    - 是網際網路工程任務組織(Internet Engineering Task Force, IETF)所制訂之開放標準網路安全協定
    - 為非連線(Connectionless)
    - 位於網路架構的第三層（網路層）
    - 並不使用特定加解密演算法，僅提出一個共同的基礎架構
        - 新的加解密演算法可以輕易套用到IPSec上，保留其彈性
```
IPSec應用：
    - 一家公司與分公司作安全的連線
    - 對遠端進行安全的存取
    - 建立與其他組織相通的外部網路(Extranet)或內部網路(Intranet) 
    - 增強電子商務的安全性
優點：
    - IPSec位於傳輸層(Transport Layer)之下，應用程式感覺不出其存在
    - 將IPSec建置在路由器或是防火牆之中，可以提供很好的安全性
        - 如果防火牆是進入組織內部的唯一管道時且建置IPSec，就不必擔心駭客會繞過防火牆
    - 使用者不知道IPSec的存在，所以不需要額外去教育使用者
    - IPSec可以對每一位使用者提供專屬的安全
```     
> 為何用IPSec? 因為IP不安全，而TCP的成本高。
#### [IPSec兩種安全協定](https://raw.githubusercontent.com/Ethel90/Photo/main/InformationSecurity_Intro/IPSecSecurity.png?token=AOYZYZQ3K5ALR6WDKMSOVDC77EORG)
- 認證標頭(Authentication Header, AH)
    - 是IPSec的兩種安全協定之一
    - 提供IP封包所需的資料`完整性(Integrity)`與`認證性(Authentication)`
    - 主要認證封包標頭是否有遭受竄改或偽裝，其中有『傳輸模式』與『通道模式』兩種封包模式
- 封裝安全承載(Encapsulation Security Payload, ESP)
    - 是IPSec的另一個安全協定
    - 將原IP封包經過加密後，重新封裝成另一個IP封包，以達到資料`私密性`的功能，同樣也有『傳輸模式』與『通道模式』兩種封包模式。
- 安全關聯(Security Association, SA)
    - 介於傳送者與接收者之間的`單向關係(One-way Relation)`
        - 單獨的SA可以實作AH或ESP其中之一
        - 若要同時實作AH及ESP，則必須結合多個SA
        - 位於同一包(Bundle)中的SA，可能在相同或不同的端點結束
    - 可以針對訊息來提供安全服務

    > 『傳輸模式』-> 點對點的確認方式，用來加密以及選擇性的認證IP資料
 ;『通道模式』-> 點對中繼點的確認方式，可以加密整個IP封包
 - IPSec的金鑰管理
    - 通常需要兩對金鑰
        - AH和ESP的每個方向各需要2把金鑰
    - 可以用手動或自動方式管理金鑰
- Oakley金鑰產生協定
    - 是Diffie-Hellman金鑰交換演算法的改良
- ISAKMP(Internet Security Association and Key Management Protocol)
    - 提供金鑰管理的架構(Framework)
    - 定義程序和封包格式來建立、處理、修改、刪除SA
    - 提供五種訊息交換架構(Frameworks)
        - 基本式(Base)
        - 身份保護式(Identity Protection)
        - 只有認證功能式(Authentication Only)
        - 積極式(Aggressive)
        - 資訊性的方式(Informational)
### __網路攻擊模式__
- 阻斷服務式攻擊
    -  送出大量的封包使網路雍塞; 直接攻擊伺服器，將記憶體或硬碟空間佔滿
        - 阻斷服務(Denial of Service, DoS)
            - 是指任何導致伺服器不能正常提供服務的攻擊
        - 分散式服務阻斷式攻擊(Distributed Denial of Service, DDoS)
            - 攻擊端分散在很多的主機上，同時對目標伺服器發動阻斷服務的攻擊
- 傳輸控制協定(TCP)
    - 是連線導向(Connection Oriented)的協定
    - 先建立連線才開始傳遞封包
    - [三向交握(Three-way Handshaking)式](https://raw.githubusercontent.com/Ethel90/Photo/main/InformationSecurity_Intro/Three-way%20handshaking.png?token=AOYZYZQ3VX35S3EWSPZLXCS77ESQ4)建立連線
- TCP SYN Flood攻擊
    - 利用三向交握的弱點
    - 惡意地送出許多TCP SYN封包，但後續沒有回覆確認(ACK)封包
- 來源位址欺騙攻擊(Land Attack)
    - 是TCP SYN Flood攻擊的變形
    - 偽裝成可被伺服器信任(Trusted)的IP位址，再發動攻擊
- UDP Flood的攻擊
    - 利用UDP是非連接導向的弱點
    - 傳送任一埠號(Port)的UDP封包到被攻擊端
錯誤控制協定(Error Control Protocol)
> 一個用來報告錯誤或網路狀態的協定
```
- 監控每個主機(Hosts)或路由器(Routers)上的TCP/IP狀態
- 回報主機與路由器間的錯誤
```
- 網際網路控制訊息協定(Internet Control Message Protocol, ICMP)
    - 用來回報網路間各種可能的錯誤情形
    - 網路指令“Ping”也是一個ICMP封包
    - 會跨越子網路(Subnets)，具有路由(Routing)的功能
```
弱點&攻擊方式：
- 回報偽造的錯誤訊訊息
- 傳送假的控制訊息
```
- ICMP攻擊大致分為
    - 網路監聽(Sniff)
        - ICMP重新導向(ICMP Redirect)
            - 告訴機器向另一個路由器發送資料封包
            - 利用ICMP重新導向方式將封包發送給駭客
            - 獲得訊息封包來達到竊聽
        - ICMP路由器公告(ICMP Router Advertisements)
            > 由路由發現協定(ICMP Router Discovery Protocol, IRDP)缺陷引起
，其功能是為主機自動配置路由器的位址
            - 用偽造的ICMP Router Advertisement訊息，將封包流向導往他處
            - 使用IRDP宣稱自己是預設路由器，獲取傳遞中的訊息封包
    - 阻斷服務式(Denial-of-Service)攻擊
        - Ping到死(Ping of Death)攻擊
            - 在Option Data欄位加入大量資料，形成大型的ICMP封包
            - 使用Ping工具程式，來產生超過IP協定所能允許的最大封包
        - Smurf攻擊
            - 直接對網路進行廣播，產生大量垃圾封包
            - 受害主機一時無法處理大量的封包因而當機 
            - 是Ping-of-Death的另一種變形
- 來源路由攻擊(Source Routing Attacks) , Routing攻擊
    - 對於每個傳送的封包都指定其在網際網路上的送路徑
    - 讓封包遵循一條非預期的路徑而繞過網路上特定的安全檢查機制
    >來源路由(Source Routing)允許封包的發送者指定封包傳送過程必須經過的路徑
- 網域名稱系統 (Domain Name System, DNS)
    - 負責處理“主機名稱”與“IP位址”之間的對應關係 
    - 主機名稱是方便人類的記憶，IP位址卻是電腦實際運作時所使用的
- DNS惡意攻擊
    > 對網域名稱系統發出查詢要求(Query)，而系統會回應一個回答(Answer)
    - 惡意欺騙DNS
        - 修改DNS的回應訊息
    - 利用DNS本身的漏洞
        - 藉由緩衝區溢位(Buffer Overflow)來藉此達到阻斷服務
        - 取得特殊權限能力或修改DNS中的記錄
    - 透過DNS蒐集相關資訊
        - DNS快取中的資料，對於攻擊者是重要的情報
- 緩衝區溢位(Buffer Overflow)
>緩衝區(Buffer)是指在記憶體中宣告一個區域來暫時存放使用者的資料，若使用者在使用緩衝區時，沒有注意其範圍限制，可能造成緩衝區溢位(Buffer Overflow)的問題，而資料溢位後會覆蓋到其他的資料，造成錯誤
```
動態記憶體配置
    - 堆疊(Stack)
    - 堆積(Heap)  -> 比較安全
- 緩衝區溢位的分類
    - 堆疊溢位(Stack Overflow) -> 較常見
        => 輸入大量資料到堆疊中，造成區段錯誤
        - 影響：
            - 系統將堆疊中的內容當成程式碼執行
            - 可以改變程式的執行流程
            - 駭客將後門程式填入堆疊中
    - 堆積溢位(Heap Overflow)
```
- Port Scanning
>網際服務都會有一個預設的連接埠(Port)

    - 不是一個直接攻擊網路漏洞的程式
    - 透過連接埠掃描(Port Scanning)就可以大概知道該主機開啟了那些服務
    - 駭客獲得遠端主機連接埠資訊，即可分析其弱點而入侵
