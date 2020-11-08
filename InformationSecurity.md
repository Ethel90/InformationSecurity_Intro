# __資訊安全導論__

## 密碼學
___
- 無條件安全(Unconditionally Secure) 
```
非法使用者不管截獲多少個密文，用盡各種方法仍沒有足夠資訊可以導出明文機密資料
 ```
 - 計算安全(Computationally Secure) 
```
目前或未來預測之科技、以合理之資源設備下，要破解密碼系統需要一段相當長的時間（例如數百年）
 ```
 - 明文(Plaintext)
 ```
傳送方想要接收方獲得的可讀資訊
 ```
- 密文(ciphertext)
```
由明文經過加密演算法產生
```
- 加密(encryption)
- 解密(decryption)

- 秘密分享(secret sharing)
```
以(t,n)來表示
t為授權子集，少於t個人則無法恢復秘密 
n為參與者數目 
```
- 授權(Authorization)
```
依照身份給予適當的權限
```
- 識別（Authentication)
```
確認身份
```
- 防範病毒
  - 專人集中管理
  - 常更新通行碼
  - 不抄襲來歷不明軟體
  - 定期將程式資料備份保存
  - 隔離染病程式
  - 設定檔案為“唯讀”

- 入侵電腦系統的方式
  - 摧毀實體（實體攻擊）
  - 摧毀資訊（邏輯攻擊）
  - 竄改資訊
  - 偷用服務
  - 偷窺
  - 偷用資料
- 主動威脅
```
可感受到被攻擊（e.g. 竄改）
```
- 被動威脅
```
不讓受害者發現自己的機密文件或資料被偷偷送出去（e.g. APT attack）
```
- 偽裝學（藏密學） Steganography
```
將程式碼暗藏在令人料想不到的地方 [如掩護影像(cover image)中]
```
> vital point : image quality & 藏量hiding capacity(embedding efficiency) & security analysis為評量偽裝學的Point
- 可逆式水印技術(reversible)
```
According to image authentication(確認完整性是否有被修改)
```
- LSB replacement
- Cipher Image
```
圖藏圖
```
- 浮水印(Watermark)
  - Privilege information protection
  - Copy right protection
  - Authentication
```
  *Visible watermarking*
- Easy to embed
- Clear to see watermark

  *Invisible watermarking*
- Good visual quality of watermarked image
- Robustness(強韌性) -> copyright protection
```
- 可還原性浮水印reversible watermark(fragile watermark)
```
會嵌入Authentication code
```
- Privilege Information Protection
```
Requirements:
Low distortions causing in the hidden image (good visual quality, hiding capacity)
Reversible or Irreversible
```
** Grayscale image -> Binary image (method: halftone)

- QoS(Quality Of Service)
```
依不同的權限，想有不同的服務品質
```
## 資訊安全
___
- 進階持續性威脅(Advanced Persistent Threat, APT)
```
攻擊特色：
1)針對特定目標
2)低調、隱匿
3)手法多變、客製化

目的：
1)竊取資訊
2)政治因素
3)金錢利益

可能持續幾天，幾週，幾個月，甚至更長的時間。APT攻擊可以從蒐集情報開始，這可能會持續一段時間。它可能包含技術和人員情報蒐集。

e.g. 試圖竊取商業機密可能需要幾個月有關安全協定，應用程式弱點和文件位置的情報收集，但當計畫完成之後，只需要一次幾分鐘的執行時間就可以了。
```
### 駭客入侵程序 ###
___
1. 探勘（Ping）
2. 掃描
3. 分析及準備攻擊
4. 實際攻擊
5. 取得權限（全縣提升或異動、新增帳號）
6. 維持存取（竊取資料）
7. 清除軌跡（刪除或毀壞日誌檔）
___
- 社交工程(Social Engineering)
```
利用人性弱點，應用簡單的溝通和欺騙技倆，以獲取帳號、通行碼、身分證號碼或其他機敏資料
有「後門」-> 被動攻擊(e.g. APT)
```
- 網路釣魚(Phishing)
```
路釣魚電郵假冒可信任的機構，以便竊取用戶的身份憑據。 在下列的例子中，電郵使用了一個常見的網路釣魚手法：要求用戶更新其帳戶資訊。但當點進連結後，進去的卻是「假網站」
```
- 語音網釣(Vishing)
```
使用假冒來電ID顯示，使外觀類似於來自一個值得信賴的組織

e.g. 聲稱是從銀行打來的訊息告訴用戶撥打某支電話號碼以解決其銀行帳戶的問題
```
- 水坑式攻擊(Watering Hole)
```
1. 攻擊者分析攻擊目標經常可能會瀏覽之網站
2. 攻擊者分析網站弱點，並將惡意程式放入網頁中
3. 最終某些攻擊目標的使用者因為瀏覽上述網頁而電腦遭到入侵
```
- 殭屍網路攻擊(Botnet)
```
駭客利用木馬程式控制一群電腦（被動攻擊），用Dos攻擊一台Server（主動攻擊）
```
- 數位鑑識(Digital Forensic)
```
作業階段：
1) 現場蒐證(Identify, Collect)
2) 證據封存及運送(Preserve)
3) 鑑識分析(Analysis)
4) 報告及法院呈現(Present)

分析流程：
1) 鑑識分析開始
2) 製作證據影像檔
3) 復原作業（磁區還原、資料夾還原、特定檔案還原  證據映像檔）
4) 分析作業（檔案特徵值、搜尋關鍵字  揮發性資料、證據映像檔）
5) 數位證據？
6) 製作報告
```
> 揮發性資料
>> 電腦關機時會refresh的資料（日誌檔案、暫存檔或捷徑）

> 非揮發性資料
>> 電腦關機依舊會儲存在內的資料（登入中帳號、網路設定）
## __區塊鏈__
___
> 是一套記錄事實的機制。「區塊」就是帳本的內頁用來記錄交易，且標有頁碼以確保區塊的前後相連。「鏈」是在多位記帳者（礦工）電腦內，保存同一份帳本。每一筆交易都必須由記帳者彼此達成共識，才能確保帳本內容完全同步。若區塊鏈的安全就在於駭客如果想要成功竄改交易紀錄，必須要駭入多台礦工電腦，且掌握`51%` 以上的運算能力。

- 類型
1. 公共鏈（public blockchain）是公開社團（比特幣）
2. 私有鏈（private blockchain）是私密社團
3. 聯盟鏈（consortium blockchain）是介於兩者之間

- 個人數位簽名（digital signature）搭配交易時間戳記（timestamp server），來證明該次交易的唯一性
> Signature 為防止被竄改
- 執行工作量證明(Proof of work, Pow)
  - 礦工挖的為"nonce"，若有挖到則會獲取獎金。是否比他人快挖到要取決於`電腦運算能力`&`運氣`
- 智慧合約
```
藉由編寫程式碼，達成資產交換自動化（程式碼需用以太坊的專用語言Solidity）
以太坊執行的智慧合約他能夠確保程式被貫徹執行，而不受到政府要求下架或駭客惡意攻擊。
```
## 資訊安全基本需求
___
1. 機密性(Confidentiality)
    - 保障資訊不外洩
      - 防止機密資訊洩漏給未經授權的使用者。為確保資料傳輸的隱私，可透過資料加密的程序以達到此目標。
2. 完整性(Integrity)
    - 確保資訊未被篡改
      - 資料內容僅能被合法授權者所更改，不能被未經授權者所篡改或偽造。
      ```
      雜湊函數＆將訊息加密 -> 確保資料能正確無誤的傳送到接收者
      ```
3. 可用性(Availability)
    - 使合法使用者得以正常使用資源
      - 確保資訊與系統持續運轉無誤，以防止惡意行為導致資訊系統毀壞。
4. 不可否認性(Non-repudiation)
    - 確保使用者不可抵賴已做的事，例如網路下單買賣股票
      - 對於傳送方或接收方，都不能否認前進行資料傳輸或接收
      ```
      可以利用數位簽章及公開金鑰基礎架構(Public Key Infrastructure, PKI)對使用者身份及訊息來源做身份驗證及資料來源驗證
      ```
5. 鑑別性(Authentication)
    - 確認與你通訊的對方身份
      - 包括身份驗證及資料來源驗證
6. 存取控制(Access Control)
    - 控制使用權限的範圍，避免未授權者使用資源
      - 根據系統的授權策略，對使用者作授權驗證，以確認是否為合法授權者
- 國際資訊系統安全認證聯盟(International Information Systems Security Certification Consortium(ISC)^2)


## __資訊安全種類__
___
- 硬體安全
  - 遭遇天災人禍，如：硬體毀損、遭竊、遭破壞、停電、水災、風災、地震、炸彈等
- 軟體安全
  - 病毒感染、軟體缺陷等
- 網路及通訊安全
  - 內部網路故障、對外線路故障、資料在傳輸時外洩
- 服務安全
  - 網站遭阻絕服攻擊
- 資料安全
  - 書面資料遺留在桌面上、回收箱、影印機上、板書未清掃、於公共場所交談、電話交談太大聲、資料在機器中被竊取或傳輸時被攔截
- 個人安全
  - 人身安全受威脅、個人隱私權侵犯等

- 無檔案惡意程式(Fileless Malware)
    - 經由文件漏洞攻擊來啟動惡意程式
      - 可能經由傳統方式進入系統，例如經由 JavaScript 或 VisualBasic (VBA) 惡意巨集腳本並內嵌在 Office 文件、PDF 檔案、壓縮檔或看似無害的檔案內部。這些巨集一旦執行，就會運用一些正常的工具 (如 PowerShell) 來進一步啟動、下載和執行更多程式碼、腳本或惡意檔案。這些腳本可利用 `PowerShell` 來讀取並執行本機系統上的執行檔，或者直接執行已經在記憶體中的程式碼。
    - 從記憶體內直接將惡意程式植入系統
      - 通常是直接從記憶體內載入執行，不像其他惡意程式會有寫入硬碟的動作，因而讓防毒軟體很難加以偵測。它也會利用一些正常的系統管理工具和應用程式開發介面 (API)，如：PowerShell、PsExec 與 Windows Management Instrumentation  (WMI) 來入侵正常執行程序的記憶體並取得其權限。
      - 最常見經由記憶體漏洞的攻擊技巧就是所謂的「Reflective DLL 注入」。這是一種將動態連結程式庫 (DLL) 載入某個執行程序當中的技巧，如此就不用將 DLL 寫到磁碟上。

## 資訊安全架構
___
1. 外圍層(Environment Layer)
    - 環境觀點（機房冷氣)
    - 設備的實體安全
2. 外部層(External Layer)
    - 使用者觀點（使用者介面）
    - 通行密碼、生物辨識
3. 中心層(Central Layer)
    - 系統觀點（系統安全的核心、內外部溝通的橋樑）
    - 任意性/強制性控制
4. 內部層(Internal Layer)
    - 資料觀點（牽涉到系統存取與管理資料的方式）
    - 加密解密技術、數位簽章
5. 分析層(Analysis Layer)
    - 管理者觀點（系統的查核與分析）
    - 安全稽核
6. 法律層(Law Layer)
    - 法律觀點（與資安相關之法律與規範）
    - 法律判決
