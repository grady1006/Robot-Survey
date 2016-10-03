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