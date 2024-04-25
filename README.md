# 2023_Regional_Public_Safety_Data_Analysis_Competition

### Notice
- 제1회 2023년 지역 치안 안전 데이터 분석 공모전 코드입니다.
  
--------------------------------------------------------------------------------------
### 파일 설명

```치안데이터 코드1(전처리)_올리브통조림.ipynb``` : 전처리 <br/>
```치안데이터 코드2 (예측)_올리브통조림.ipynb``` : 예측 분석 모델 <br/>

--------------------------------------------------------------------------------------

### 분석 설명

성별, 지역, 신고 시간 등의 변수를 활용하여 보이스피싱 예측 모델을 구현함으로써 보이스피싱이 일어날 것을 미리 예측하여 피해를 방지하고자 한다.

1. 보이스피싱 사건을 알아보기 위해 사건종별코드 변수에 중심을 둠
2. 사건종별코드가 보이스피싱:215 == ‘1’ 나머지는 ‘0’으로 변경
3. 보이스피싱에 유의미한 영향을 줄 것이라고 생각되는 날짜와 지역 변수를 가진 새로운 dataframe 생성
4. 대전,세종,충남 지역의 다른 이름의 경찰서들을 ‘대전’,‘세종’,‘충남’ 으로 그룹화
5. 데이터를 train 과 test 로 나눔
6. Logistic Regression, Desicion Tree, RandomForest 작업을 수행

***성능***

- Logistic Regression
| Command    | Description   | Precision| Recall  |
| ---------- | ------------- | -------  | ------- |
| 0.4117     |  0.03429      |  0.0175  |  0.7813 |


- Decison Tree
| Command    | Description   | Precision| Recall  |
| ---------- | ------------- | -------  | ------- |
| 0.4123     |  0.0344       |  0.0176  |  0.7836 |
  
- Random Foreset
| Command    | Description   | Precision| Recall  |
| ---------- | ------------- | -------  | ------- |
| 0.4123     |  0.0344       |  0.0176  |  0.7836 |


- **Note that the details of training configuration which are not mentioned in this document and the comments can be defined yourself.** For example, decide how many epochs you will train the model.

