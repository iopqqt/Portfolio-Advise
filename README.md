# 投資組合權重服務
這個專案主要會藉由投資人輸入期望報酬以及股票代號，並用蒙地卡羅法模擬效率前緣，來可視化投資人所選股票的投資組合，最後輸出最佳化後的投資組合比例。

## 開發背景
過去投資組合都是輸入股票代碼產生年化報酬風險，再給予投資人一個最佳的配置比例，即是最小變異投資組合。最小變異投資組合(Minimum Variance Portfolio,MVP)，
MVP的設定是在最小風險下能夠獲得的最大報酬。但是如果今天投資人本身可以承受更多風險呢? 或是投資人想要獲得更多報酬的話，他想知道自己應該承受多少風險呢?
   
為了更實際運用這個理論，我們使用蒙地卡羅法去模擬50,000次的投資組合，再透過投資人給予的年化報酬以及股票代碼，
我們就可以提供投資人他所應該承擔的風險以及他應該花多少比例去購買這些股票。

## 理論背景
### 效率前緣
投資組合追溯到1952年Harry Markowitz提出的現代投資組合理論(Modern Portfolio Theory,MPT)，而其中出現的最佳投資組合指的就是效率前緣(Efficient Frontier)。
效率前緣是在預期報酬相同情況下，風險最低的投資組合所形成的一條曲線，也是所有配置中最佳的一系列組合，其中，風險最低的投資組合就是上面提及的MVP。

### 蒙地卡羅
蒙地卡羅(Monte Carlo)，透過機率隨機生成的方式，產生足夠用來模擬現實遇到的各種的情況，以及讓使用者一目了然目前的狀況。
首先，我們先創造一系列介於0~1之間的Uniform distribution U(0,1)   
![image](https://github.com/user-attachments/assets/2ce2cb8d-6305-4b72-ab51-cdf3fb40f33d)  
再來因為投資組合權重最後需要加總為1(限制式)  
![image](https://github.com/user-attachments/assets/c2511c9b-5870-4122-a319-ef8e4d6637b2)   
所以我們要把所有隨機生成的數值加總當成樣本總數(分母)、隨機數值當成樣本(分子)，這就是我們隨機生成的權重    
![image](https://github.com/user-attachments/assets/817812bc-6b8c-4956-842b-e171719f9a18)  

## Install


## Usage


## Contributing



## Reference
詳細Markowitz最小變異投資組合
https://ch-hsieh.blogspot.com/2017/03/markowitz.html
