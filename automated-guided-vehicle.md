#AGV 發展現況

這邊整理的是近幾年來 ( 2016前 )  AGV ( Automated Guided Vehicle ) 在大型工廠、物流中心、倉儲管理等應用案例與技術探討，這裡不會提到早期傳統軌道式、導引線式、磁條式，特定路線設計的AGV。

主要針對正在發展中的移動式機器人 ( Mobile Robot ) 使用Laser、3D Sensor、Lidar、RFID等技術達到自主定位導航，以SLAM ( Simultaneous Localization and Mapping ) 為基礎的AGV發展現況。 

- - -
## 基於Tag(RFID or 2D Bar codes)+Lidar(IR)AGV
在2013年時 Amazon 展示了 Kiva robots once the marvel of warehouses everywhere，倉儲機器人，採用於地面貼上Tag作為AGV的定位與路徑規劃，透過AGV前方的IR Sensor偵測障礙物，由中央監控平台管理所有的AGV，規劃移動路徑與工作排程，每個Tag所貼的位置距離依據AGV的大小為單位佈建，採取如棋盤格座標方式定位 

每次所移動的距離與轉彎的角度都是固定的(如等距等速與自轉180度或90度)。
Tag的建置僅要求工廠或倉儲的地面需平整，避免移動過程起伏導致定定位錯誤或移動過程偏離。 
在佈建Tag的過程必不是整個場域都建置，會依據移動位置的複雜度與同一時間AGV移動的數量來做調配規劃。

![AGV1](image/agv1.png)
![AGV1](image/agv2.png)

針對上述的介紹，接著說明目前這類技術的AGV公司與相關硬體規格

### -[Amazon Kiva](https://www.amazonrobotics.com/ )
**關於 Kiva 5大重點**

• 客製化Kiva可移動的貨架高度 ( shelves )

• 使用2D QR codes佈建於地面定位基準點 ( known as "fiducials" )

• 內建重量偵測、雷射掃描與其他sensor

• 能移動到貨架下方直接抬起行動

• 多台Kiva移動時之路線規劃 ( Complex and robust software system ) 

<iframe width="560" height="315" src="https://www.youtube.com/embed/z_R8feyCu-M" frameborder="0" allowfullscreen></iframe>

在Kiva的前方有10組的單點紅外線陣列模組以及最下方有條壓力感知器，負責做前方障礙物偵測避障，但在線上資料中沒有提到當出現障礙物時，或是有人員移動經過等，Kiva會如何排除這類問題。 
在Kiva的核心有兩組鏡頭，一組是看地面的Bar code 偵測掃描做路徑規劃與定位、而另一組是裝置上方掃描貨架底部bar code的資訊，如下圖所示。 

在針對Bar code的條碼辨識採用了ADI ADSP-BF548處理器，在晶片中做影像處理，提高在移動過程中辨識的速度 

![AGV1](image/agv3.png)

Kiva目前有提供兩種載貨規格(1)貨架長框在60~100cm的可負重約1000 pounds(430KG)，(2)較大的貨架可自訂，可負重約3000 pounds(1200KG)。在移動速度上約在1.3m/second 
建構場域約：600~6000坪 
建構AGV成本每台約在100~150萬台幣 
- - -
### -[上海快仓智能](http://www.flashhold.com/)
採用跟Kiva類似的技術 

• 每台AGV 約50萬台幣，包含軟體系統價格。 

• 特別提到快速充電與換電池 

• 移動速度一樣在1.5m/s 

• 支援的貨架規格 90×90cm 和 120x120cm， 

• 負重約在300到900kg 

• 整合了中央控制與通訊，負責AGV調度、控制，AGV間的通訊， 

• 官方提到智能倉儲系統，基於據分析的隨機存儲，基於搜索引擎的命中算法，基於資源與任務的智能調度。
![AGV1](image/agv4.png)
![AGV1](image/agv5.png)

- - -
### -[Cainiao菜鳥網絡](https://www.cainiao.com/)
這是在今年中國智能倉儲管理會議中Cainiao所展示的完整物流管理平台，在1分11秒鐘展示他們強大火力再AGV導入應用上成果，多台協同搬運、避障、排隊的展現。 

詳細技術細節與規格無提供，這是由阿里巴巴所投資成立的智能物流管理研發從物到人的Total Solution 