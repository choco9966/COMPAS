## 주제 : 화재발생 예측모델 개발 

기간 :  2019년 10 월 14 일 ~ 2019년 12 월 13 일

결과 

![rank](https://drive.google.com/uc?export=view&id=1xSoM7x1lpwUMd6gO0RAka0BBhppH4kTi)

### 폴더 구조

```
.
├── code
│   └── 화재예측과제_KernelSource.ipynb
│   └── 화재예측과제_Report.HTML
├── Experience
```

### 실행 환경

- python3.6 

### 필요 라이브러리

결과가 lightgbm과 scikit-learn 버전에 따라 달라지니 아래의 버전으로 재현해야 합니다. 

- LightGBM 2.3.0
- pandas 0.25.1
- numpy 1.16.4
- Scikit-learn: 0.21.3 

### 전처리 

- 건물 승인일자 : 년도, 이상치를 맞춰줌 
- 결측치 처리 : 시간대를 기준으로 평균을 넣어줌 
- 빌딩 용도 분류 : bldng_us으로 bldng_us_clssfctn 채워 넣음. 

### 피쳐 설명

- null information : 건물정보에서 결측치의 수
- 행정 구역 : 행정 구역을 단계별로 분리 
- 빌딩 id : 건물, 건축, 토지 면적, 지역등을 사용하여 같은 건물을 판단. 

### 모델 설명

- LightGBM
