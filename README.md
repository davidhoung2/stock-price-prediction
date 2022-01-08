# stock-price-prediction開發過程: 

Dataset 

-----------------------------------------------------------------------------------------------------------------	
catch from kaggle  

分析: 

------------------------------------------------------------------------------------------------------------------- 

Closing price v/s time	 

 ![下載](https://user-images.githubusercontent.com/51390009/148638357-b496dbc3-3a50-4138-bed7-fba024a41c96.png)


Daily Return 百分比直方圖 

股票 daily returns 的相關性 

 

從上圖可以看出，Amazon和google的股票日收益率相關性最強 

Risk v/s Expected Returns 

從上圖可以看出，Tesla的預期收益最高，風險係數最高。 google的預期回報最低，風險因素最低。 

Deep learning Model 

----------------------------------------------------------------------------------------------------------------- 

Model 

 

我們使用訓練數據集記錄訓練模型，然後用它來預測下一周的收盤值（i.e.一周的下五個值由五個工作日組成） 

網絡輸入層的輸入數據形狀為 (5, 1)，表示使用時間序列的前五個值（i.e.一周的數據）作為輸入。僅考慮數據的一個屬性（即收盤值）。 

Custom Learning Rate 

分頁符號
 

----------------------------------------------------------------------------------------------------------------- 

 

Result 

Blue: training 

Orange: testing 

Green : prediction 

Netflix 

RMSE: 17.904191193967847  

MAPE: 2.22996091648307 % 

 

Amazon 

	RMSE: 104.9740532443128  

MAPE: 2.4166268304806455% 

 

Telsa 

	RMSE: 29.76287513978468 

MAPE: 3.2131938232249864% 

 

Google 

	RMSE: 77.6125292803508 

MAPE: 2.155821981127189% 

 

More details: 

https://github.com/davidhoung2/stock-price-prediction 
