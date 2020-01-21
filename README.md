파이썬을 이용한 머신러닝 공부를 하려고 합니다.  
과거 캐글 경진대회에서 실제로 사용된 입상자의 코드를 참고하여 실행해볼 예정입니다.  
배우고자 하는 사항을 요약하자면 다음과 같습니다.

- 탐색적 자료분석 코드
- 데이터 다루는 방법 (ex. pandas)
- 데이터 시각화 방법 (ex. matplotlib, seaborn)
- 머신러닝 및 딥러닝을 위한 라이브러리 사용법 (ex. scikit-learn)
- 실제 데이터를 바탕으로 한 머신러닝 파이프라인

사용한 코드는 모두 Window 기반입니다.  모듈설치는 아나콘다 환경을 이용하였습니다.  

## 데이터 준비하기 (머신러닝 탐구생활; 정권우 참고)

### 1. 캐글 홈페이지 회원가입
https://www.kaggle.com/

### 2. 경진대회 선택하고 'Rules' 약관에 동의
예) 산탄데르 제품 추천 경진대회   
https://www.kaggle.com/c/santander-product-recommendation

### 3. kaggle API 설치
```
pip install kaggle
``` 

### 4. kaggle API에 키 등록
kaggle my profile >  ... account > create API token > 다운로드 한 'kaggle.json' 파일을 C:\Users\{user_name}\kaggle\kaggle.json 경로로 이동

### 5. 필요한 데이터 다운로드
kaggle competitions download -c santander-product-recommendation 



## 프로젝트를 위한 가상환경 생성

```
# conda 버전 확인
$ conda --version
# conda 업데이트
conda update
```
```
# 생성
conda create -n 가상환경명  # conda create --name 가상환경명 python=3.6.5 tensorflow keras
# 활성화
activate 가상환경명
# 비활성화
deactivate 
```
```
# 가상환경 목록 확인
$ conda env list
# 가상환경 삭제
conda remove --name 가상환경명 --all
```

Anaconda 가상환경 Spyder IDE 적용
```
conda install -n 가상환경명 spyder
activate 가상환경명
spyder
```

주피터 노트북에 가상환경 추가 
```
# 가상환경 활성화
activate 가상환경명
# 가상환경에서 jupyter notebook 설치
pip install ipykernel
# jupyter notebook에 가상환경 kernel 추가
python -m ipykernel install --user --name 가상환경명 --display-name "가상환경명"
```


