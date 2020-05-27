# FDA HW3-1 Report
## How did you preprocess this dataset ?
### 檢查有無缺失值
* 用info()看dataset是否有缺失值
### 增加欄位
* 計算 'Close Price' 及 'Volume' 相較於前一天是漲或跌, 在dataset中增加 *'Close Price_move'* 和 *'Volume_move'* 欄位代表漲跌
* 計算前5天 'Open Price' , 'High Price' , 'Low Price' 的平均值, 在dataset中增加 *'Open Price Past mean'*, *'High Price Past mean'*, *'Low Price Past mean'* 欄位代表前5天的平均值, 提供更多參考、判斷的依據
### 資料視覺化
* 畫出各欄位值的折線圖觀察走向
* 畫 *'Close Price_move'* 和 *'Volume_move'* 的變化圖對照比較
### 相關係數
* 列出Close Price分別與其他各feature之間的相關係數
* 列出任兩個features之間的相關係數
### 標準化
* 因為資料中每個欄位的最小值與最大值差距都超過10^2 , 所以嘗試將資料標準化

## Which classifier reaches the highest classification accuracy in this dataset ?
* Why ?
* Can this result remain if the dataset is different ?
### Neural Network的準確率最高
* 因為Logistic Regression是找一條線劃分, 但Neural Network可以用好幾條線劃分, 較容易分得準
* 如果是同種類的dataset, Neural Network仍可較高,  
  但如果是比較單純偏線性的dataset, 則Logistic Regression的準確率未必會較低

## How did you improve your classifiers ?
### 增加能代表過去的資料欄位
* 計算前5天Open Price, High Price, Low Price的平均值, 加入輸入訓練的features
### 調整超參數
* 例如增加hidden layers
### 標準化
* 將資料都標準化後, 對於MLPClassifier的準確率能大幅提昇

## 使用的3種classifiers在實驗中最高的test accracy: 
* **Logistic Regression**: 0.8130081300813008
* **Neural Network**: 0.8292682926829268
* **SVM**: 0.8008130081300813
