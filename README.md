# Marketing-Segmentation  
캐글데이터를 활용한 소비자 구분   
Customer Segmentation Using Kaggle Dataset  
  
## 학습환경 (Training Environment)    
* Colab Pro (But Not that important)

## 데이터셋 출처 (Source of Dataset)
* Kaggle Customer Segmentation  
* https://www.kaggle.com/datasets/vetrirah/customer  

* About Dataset  
Context  
An automobile company has plans to enter new markets with their existing products (P1, P2, P3, P4 and P5). After intensive market research, they’ve deduced that the behavior of new market is similar to their existing market.  
Content  
In their existing market, the sales team has classified all customers into 4 segments (A, B, C, D ). Then, they performed segmented outreach and communication for different segment of customers. This strategy has work exceptionally well for them. They plan to use the same strategy on new markets and have identified 2627 new potential customers.   
You are required to help the manager to predict the right group of the new customers.  

## 데이터셋의 특징 (Characteristics of this dataset)
1. Data Leakage가 존재하는 데이터
2. Submission File의 정답 데이터가 모두 'A'로 되어있다.   
  - Data Uploader가 임의로 정답을 채워넣은 것으로 예상된다.
  - 원본 데이터셋 홈페이지에 들어가봤으나, 현재으로는 해당 데이터를 구할 수 없는 상태였다. (대회기간에만 공개)
3. 결론 : 그렇게... 좋은 데이터셋은 아니였다. 그러나 항상 방심하면 안 된다는 것을 다시 깨닫게 해준 대회.  


## 학습 전략 (Training Strategy)
* Sklearn을 이용한 Customer Segentation 
* 여러가지 Encoding, Missing Value 처리를 조합하는 과정에서 Dataset의 특성 파악
* 변수간 상관관계를 고려하여 Feature Selection 진행 (변수를 삭제하는 게 맞을지?)

## 배운 점 (What I learned..)
* EDA의 중요성. Dataset의 ID column을 처음에는 무시했지만, 뭔가 이상해서 다시 보니 trainset의 ID와 testset의 ID가 겹치는 것이 많았다. ID는 같지만 변수의 값은 약간 다른 현상 발견. 다시 말해, Data Leakage 가 존재하는 데이터였다.
* 이에 이에 맞는 처리로 다시 진행, Submission Data를 다시 Inference 한 결과 유의미한 결과 차이를 얻을 수 있었다.
* Pycaret의 사용법
