# Simple Radio / 小小收音電台

## 題目發想動機
  現在資訊科技發達，網路也使得人們取的資訊的難易度大幅的下降，不管是取得產品，產品資訊，又或者是瞭解到新事物，是非常容易的，也因為這樣，許多設備也漸漸的被淘汰，像是卡帶式錄影帶，ＣＤ，ＤＶＤ，收音機等等。然而雖然汰舊換新是自然也是必然的現象，不過不管是時代過季的產品，又或者是陳出推新的商品，都有應該被保留的權利。

  家中有一位年邁的奶奶，他是我從小到大最好的朋友，因為時代進步迅速，像是電腦，平板，手機，奶奶是不會使用的，對老人家來說，這些設備都太新了，根本學不來，這些陳出推新的商品中，電視是他老人家的好朋友，家中年輕人都在外拚命工作，小朋友也都在外地讀書，看電視變成他日常消耗時間的一大部分，雖然電視節目多元，身邊沒有人陪他說說話，我想奶奶的內心也是相當寂寞的。

  近期奶奶因為身體不好，視力已受到影響，看東西變得非常的不清楚，所以在下午的時光奶奶都會收聽收音機來度過他的下午時光，不過老人家聽到電台那些油嘴滑舌的主持人，都會廣告商品與藥品，奶奶也都會受到他們的影響而購買了一些來路不明或者是不知道在幹嘛的藥品，令家裡的人非常擔心，怕老人家購買來路不明的要亂吃，而把自己的身體搞壞了，在這學期的LSA課程有學到了raspberry pi 的應用，想利用這塊pi版，架設一個小小的基地台，裡面可以放置奶奶想聽的音樂，並跟他說這是我這個孫子為他設計的一個電台，希望老人家可以收聽這個電台，這樣不僅是可以讓他聽到想要的音樂，也可以預防奶奶去聽那些賣藥電台。

  不僅僅這樣，在特定的節日，知道奶奶會收聽的時間，也可以預先錄製一段語音，祝福他生日快樂或者跟他說一些內心話，給她大大的驚喜。

  實作嘗試使用 Raspberry Pi 實作小小廣播電台，放置在家中，給家中的人都可以聆聽。

## 實作材料
| 材料名稱 | 取得來源 | 價格 |
| --- | --- | ---: |
| Raspberry Pi | 課堂提供  | NT$0 |
| 電料線材    |展瑩贊助     | NT$0 |
| webcam      |茂權贊助      | NT$0 |
| 杜邦線      |金華電子零件  | NT$75|
| 收音機      |全國電子      | NT$350|  
|焊接設備      |MOLi | NT$0  |
|熱縮套       |五金行       | NT$25 |


## 使用的現有軟體與來源
  - raspberry pi 廣播設定與下載
    - http://gsyan888.blogspot.tw/2013/03/raspberry-pi-pifm-fm-transmitter.html
    - 
  - Turning the Raspberry Pi Into an FM Transmitter
    - http://www.icrobotics.co.uk/wiki/index.php/Turning_the_Raspberry_Pi_Into_an_FM_Transmitter
  -標題為Microphone 部分，設定麥克風
    https://wolfpaulus.com/journal/embedded/raspberrypi2-sr/

## 實作過程（碰到哪些問題、如何解決）
  - 一開始的發想購買零件路途坎坷
  - Raspberry Pi一直當機，網路環境不好
  - 無法上網，網路環境設定很久
  - 安裝檔案後執行錯誤無法修復，重灌Raspberry Pi
  - 麥克風有執行卻無法錄音
  - 收音音頻訊號不好(接收範圍只有10cm)
  - 錄音變狂派音了...

## 運用哪些與課程內容中相關的技巧
  - Linux 基本觀念和指令
  - 接網路線，檢查網路設定
  - 製作天線解決訊號問題

## 組裝過程及製作教學

### 天線
  1. 先拿取到一條AWG線（約12~18mm）
  2. 把一條母頭的杜邦線剪斷，留下母頭部分並留約一公分長度的線絲
  3. 用和接棒把AWG線與杜邦線母頭的線絲焊接
  4. 等待焊接點降溫以後，使用熱縮套把焊接觸進行連接

### 收音機
  1.打開收音機
  2.轉到所設置的頻道
  3.開始收聽播放音樂

### Raspberry Pi
  1.Raspberry Pi下建立一個新資料夾
     ```
    sudo mkdir Pifm
    ```

## 操作教學
  1. 在raspberry pi底下輸入下載檔案
  ˋˋˋwget http://www.icrobotics.co.uk/wiki/images/c/c3/Pifm.tar.gz ˋˋˋ
  2.建立一個新的目錄（Pifm）並移到目錄底下，解壓縮
  ˋˋˋmkdir Pifm
    cd Pifm
    tar zxvf ../Pifm.tar.gz
  ˋˋˋ
  3.執行播放程序
    ˋˋˋsudo ./pifm sound.wav ˋˋˋ
## 工作分配表
  - 天線製作：琨柏
  - 軟體設定與環境建置：琨柏、俞蓁
  - 簡報製作、報告：琨柏、俞蓁
  - 文件製作：琨柏、俞蓁
  - 過程鼓勵與幫助師：BlueT、李悅、展瑩


