# DataScience


### 프로젝트로 배우는 데이터 사이언스 ###

* 사이킷런 ( https://scikit-learn.org/stable/ )
**  Classification / Regression
** Classification(분류) - 물건을 구매할 것인지 아닌지, 광고를 클릭할 것인지 아닌지, 공장의 제품이 불량이다 아닌다, 고객에게 대출을 해줘도 된다 안된다, 고객 상담 시 배송 문의 인지 상품 문의인지

  
** Regression(회귀) - 물건을 구매한다고 했을때 얼마에 구매를 할 것인지, 광고에 효율을 측정한다면 광고의 효율이 어느정도 나올지 특정 수치로 예측을 할 때 사용한다, 재고량, 판매량, 매출액 예

*** Supervised learning(지도학습) - 정답이 있는 데이터를 맞추는 것
정답을 알고 있는 문제를 풀 때 
(공부)기출문제와 정답을 열심히 풀어서 공부하는 과정이 모델을 만드는 과정과 유사하다.
모델을 만들어서 실제 시험장에 들어가서 시험을 보게 되는 것이 Prediction(예측)에 해당하게 된다.
고객이 과거에 구매한 데이터와 이 고객이 구매한다 안한다에 대한 정답을 알고 있으면 어떤 고객들이 구매한다 안한다 모델이 학습을 할 수 있을 것이다. 새로운 고객이 들어왔을 때 이 고객은 구매할 것이다. 하지 않을 것이다.라고하면은 만약에 구매한다고하면 적절한 상품을 추천을 하고 구매하지않을 거 같다한다면 구매할 수 있도록 유도하는게 머신러닝을 통해서 우리가 추가적인 액션 플랜을 짜 볼 수 있다.
예측을 하게 되는데 이렇게 예측을 한 것이 과연 얼마나 맞는 예측인지 확인이 필요할 것이다. 만약 우리가 시험을 본다 기출문제와 정답을 가지고 공부를 했다 그 다음 공부한 것을 바탕으로 시험을 보고 채점을 해서 정답을 맞춰볼때 이 과정을 Evaluation이라고 한다.

Training Data와 Training Labels(정답 데이터)를 가져와 학습을 해서 모델을 만드는 과정을 Traning

Training 한 것을 일반화하는 과정을 Prediction, Evaluation해서 평가까지 하게 된다. 

clf = RandomForestClassifier() //대표적인 Tree 모델에 해당
clf.fit(X_train, y_train) //문제와 정답을 넣어주었다고 보면 된다.  이것을 가지고 학습(기출문제와 유사하다)

y_pred = clf.predict(X_test) //실제로 시험보는 과정
clf.score(X_test, y_test)  //문제를 푼 것을 바탕으로 채점을 한다.




** Clustering / Dimensionality reduction
** Clustering(군집) - (쇼핑몰)고객이 어떤 고객의 군집이 있는지

**** Unsupervised learning(비지도 학습) - 정답이 없는 데이터를 예측 
pca = PCA() //차원 축소 기법 중 하나
pca.fit(X_train)
X_new = pca.transform(X_test) // 원하는 차원으로 축소해줘서 머신러닝의 피처로 사용하거나 시각화하여 사용하기도 한다. 


Training Data를 바탕으로 모델 생성 -> 고객을 군집화하여 마케팅
차원 축소 기법
Unsupervised learning을 통해서 처리해준 데이터를 다시 Supervised learning 피쳐로 다시 사용하기도 한다. 


*Basic API(조리도구의 사용법)
** estimator.fit(X,[y]) **
- 지정해줄 수 있는 모델을 의미
- RandomForest 모델 등.. 학습을 하게 된다. X 값은 필수이지만 y값이 선택인 이유는 Unsupervised learning의 경우에는 정답 값이 들어가지 않기 때문 
- estimator.predict- Classification, Regression, Clustering
- estimator.transform - Preprocessing, Dimensionality reduction, Feature selection, Feature extraction


* Cross-validation
- 모델이 얼마나 좋은 성능을 내는지 알아보는 것
clf = SCV 
clf.fit(X_train, y_train)
y_pre = clf.predict(X_test)


* Grid Searches
- 파라미터를 지정했을때 그리드 안에 있는 점수만 찾을 수 있을 것이다.
- 안에 있는 것을 찾기 위해서 Random서치할 것이다. 













