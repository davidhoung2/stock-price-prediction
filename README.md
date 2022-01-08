# stock-price-prediction開發過程: 

Dataset 

-----------------------------------------------------------------------------------------------------------------	
catch from kaggle  

分析: 

------------------------------------------------------------------------------------------------------------------- 

Closing price v/s time	 

 ![下載](https://user-images.githubusercontent.com/51390009/148638357-b496dbc3-3a50-4138-bed7-fba024a41c96.png)


Daily Return 百分比直方圖 
![下載 (1)](https://user-images.githubusercontent.com/51390009/148638430-53295bd3-64f6-4493-9bf0-3ccf3f94b460.png)

股票 daily returns 的相關性 

![下載 (2)](https://user-images.githubusercontent.com/51390009/148638434-04369fae-e657-43df-ad07-6b256e550e46.png)

從上圖可以看出，Amazon和google的股票日收益率相關性最強 

Risk v/s Expected Returns 

從上圖可以看出，Tesla的預期收益最高，風險係數最高。 google的預期回報最低，風險因素最低。 
![下載 (3)](https://user-images.githubusercontent.com/51390009/148638444-eea3511a-42b9-47d4-9843-ac7141fee5b3.png)

Deep learning Model 

----------------------------------------------------------------------------------------------------------------- 

Model 

 
![下載 (4)](https://user-images.githubusercontent.com/51390009/148638448-e4791b31-0a7c-45b9-894f-980be1d823c2.png)

我們使用訓練數據集記錄訓練模型，然後用它來預測下一周的收盤值（i.e.一周的下五個值由五個工作日組成） 

網絡輸入層的輸入數據形狀為 (5, 1)，表示使用時間序列的前五個值（i.e.一周的數據）作為輸入。僅考慮數據的一個屬性（即收盤值）。 

Custom Learning Rate 
![下載 (5)](https://user-images.githubusercontent.com/51390009/148638455-059284db-83e7-462d-9f88-43217ddae3eb.png)


 

Result 

Blue: training 

Orange: testing 

Green : prediction 

Netflix 
![下載 (6)](https://user-images.githubusercontent.com/51390009/148638464-f677b67e-c626-497a-802e-364d7c9f1b63.png)


	RMSE: 17.904191193967847  

	MAPE: 2.22996091648307 % 

 

Amazon 
![下載 (7)](https://user-images.githubusercontent.com/51390009/148638468-4a667a29-72e7-4219-8165-124bd00f7cab.png)

	RMSE: 104.9740532443128  

	MAPE: 2.4166268304806455% 

 

Telsa 
![下載 (8)](https://user-images.githubusercontent.com/51390009/148638475-1490f0fe-3e76-4990-a6bb-0b5d7148cc77.png)

	RMSE: 29.76287513978468 

	MAPE: 3.2131938232249864% 

 

Google 
![下載 (9)](https://user-images.githubusercontent.com/51390009/148638477-7aee0936-8548-497d-8be0-c989fbfa636b.png)

	RMSE: 77.6125292803508 

	MAPE: 2.155821981127189% 

 

More details: 

https://github.com/davidhoung2/stock-price-prediction 
