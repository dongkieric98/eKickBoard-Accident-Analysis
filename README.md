# 전동 킥보드 사고의 진실: 과장된 공포인가, 실제 위험인가?

## 1. 프로젝트 개요

#### [주제 설명]
- 최근 인터넷에서 '킥보드'라는 단어만 검색해도 뉴스, 인터넷 기사, 그리고 SNS에서 전동 킥보드와 관련된 사고 소식을 쉽게 접할 수 있습니다. 많은 사람들이 전동 킥보드의 등장 이후 사고가 급증했다고 말하며, 이를 도로의 무법자라고 부르기도 합니다. 전동 킥보드가 새로운 교통수단으로 자리잡으며 이용자가 급증한 가운데, 이에 대한 안전성에 대한 논란 또한 커지고 있습니다. 그러나 실제로 전동 킥보드로 인한 사고가 빈번히 발생하는 것일까요? 아니면 단순히 새로운 교통수단에 대한 사회적 관심과 미디어의 집중 보도로 인해 사고가 더 두드러져 보이는 것일까요? 이 프로젝트는 전동 킥보드 사고에 대한 실제 데이터를 분석하여 그 사고 빈도와 특성을 정확히 파악하고자 합니다.

#### [연구 질문]
- 본 프로젝트는 전동 킥보드 사고에 대한 다양한 데이터를 기반으로 아래의 핵심 질문에 대한 답을 찾고자 합니다
1) 전동 킥보드 사고는 다른 교통수단에 비해 얼마나 빈번하게 발생하는가?
2) 전동 킥보드 사고의 사망자수, 부상자수 등 심각도는 다른 교통수단에 비해 어떠한가?
3) 전동 킥보드 사고는 주로 어떠한 경우에 많이 발생하는가?
4) 전동 킥보드 사고를 줄이기 위해서는 어떻게 해야 하는가?

#### [프로젝트 목적]
- 이 프로젝트의 목적은 전동 킥보드 사고에 대한 객관적 데이터를 바탕으로 사고의 실제 빈도와 심각성을 분석하는 것입니다. 이를 통해 전동 킥보드 사고에 대한 대중의 인식과 미디어 보도 내용이 실제 사고 데이터와 어떻게 다른지 파악하고자 합니다. 또한 사고의 발생 빈도와 경향성을 차종, 연령, 계절 등을 기준으로 분석하여, 안전성 문제와 관련된 통찰을 도출하는 것을 목표로 합니다. 이 분석을 통해 정책 입안자나 사용자들이 전동 킥보드의 안전성에 대해 더 나은 결정을 내리는 데 기여하고자 합니다.


<br/></br>
<br/></br>


## 2. 개발환경 (Environment)
- 운영체제 : Window 11 Home
- 개발언어 : Python 3.12.4
- 개발도구 : Jupyter Notebook


<br/></br>
<br/></br>


## 3. 라이브러리 (Library)
- numpy == 1.26.4
- pandas == 2.2.2
- seaborn == 0.13.2
- matplotlib == 3.8.4


<br/></br>
<br/></br>


## 4. 파일 구조
- data
  - raw data/ : 최초 수집 데이터 
    - 차종별 월별 교통사고(2012).csv
    - 차종별 월별 교통사고(2013).csv
    - 차종별 월별 교통사고(2014).csv
    - 차종별 월별 교통사고(2015).csv
    - 차종별 월별 교통사고(2016).csv
    - 차종별 월별 교통사고(2017).csv
    - 차종별 월별 교통사고(2018).csv
    - 차종별 월별 교통사고(2019).csv
    - 차종별 월별 교통사고(2020).csv
    - 차종별 월별 교통사고(2021).csv
    - 차종별 월별 교통사고(2022).csv
    - 차종별 월별 교통사고(2023).csv
    
  - preprocessed data/ : 전처리 후 데이터
    - 연령대별 킥보드 사고건수.csv
    - 차종별 교통사고 유형 건수.csv

  - data_preprocessing.ipynb : 전처리 코드


<br/></br>
<br/></br>
  

## 5. 데이터셋 설명 (preprocessed data)
__1. 차종별 사고 유형과 건수 (2012년 ~ 2023년)__
- 데이터 출처 : 한국도로교통공단

| 컬럼명      | 설명                                          |
|-------------|-----------------------------------------------|
| 발생연도    | 사고가 발생한 연도                            |
| 발생월      | 사고가 발생한 월                              |
| 발생시간    | 사고가 발생한 시간대 (예: 00시, 01시, ..., 23시)|
| 가해자차종  | 사고를 일으킨 차량의 종류 (예: 승용차, 이륜차, 자전거, 전동킥보드 등) |
| 사고건수    | 해당 시간대에 발생한 총 사고 건수             |
| 사망자수    | 해당 시간대에 발생한 사고로 인한 사망자 수     |
| 부상자수    | 해당 시간대에 발생한 사고로 인한 부상자 수     |
| 중상자수    | 해당 시간대에 발생한 중상자의 수              |
| 경상자수    | 해당 시간대에 발생한 경상자의 수              |
| 부상신고자수| 해당 시간대에 발생한 부상 신고자의 수          |



__2. 연령대별 킥보드 사고 건수 데이터 (2017년 ~ 2022년)__
- 데이터 출처 : 공공데이터포털

| 컬럼명      | 설명                                          |
|-------------|-----------------------------------------------|
| 발생연도    | 사고가 발생한 연도                            |
| 나이        | 사고 가해자의 연령대 (예: 19세 이하, 20-29세) |
| 사고건수    | 해당 연령대에서 발생한 전동 킥보드 사고 건수  |
| 사망자수    | 해당 연령대에서 발생한 사고로 인한 사망자 수  |
| 부상자수    | 해당 연령대에서 발생한 사고로 인한 부상자 수  |


<br/></br>
<br/></br>


## 6. 데이터 전처리
#### [컬럼명 통일]
- 각 파일마다 Column명이 달라 통일시키기
<img width="747" alt="image" src="https://github.com/user-attachments/assets/2e06412a-7da9-42aa-b0e9-83b2045fe213">

<br/></br>

#### [각 데이터 구분을 위해 연도 컬럼 추가]
- 각 데이터는 연단위로 수집한 데이터이기에 연도 컬럼이 존재하지 않는다.
- 따라서 이를 그냥 병합할 경우 연도별 데이터를 구분할 수 없기 에 연도와 관련된 컬럼을 추가한다.

<br/></br>

#### [컬럼값 통일하기]
- 동일한 내용을 표현하지만 Column명이 다른 것들을 통일하기
```python
# 불명, 기타, 기타/불명 모두 기타로 통일하기
accident['가해자차종'] = accident['가해자차종'].replace({'불명':'기타', '기타/불명':'기타'})

# 개인형이동장치(PM)을 개인형이동수단(PM)로 통일하기
accident['가해자차종'] = accident['가해자차종'].replace({'개인형이동장치(PM)':'개인형이동수단(PM)'})

# 인덱스 재설정하기
accident = accident.reset_index(drop=True)
```

<br/></br>

#### [연/월 컬럼 생성]
- 연/월을 기준으로 사고건수를 파악하고자 해당 컬럼을 생성
```python
# 연 + 월로 연월 컬럼 생성하기
accident['연월'] = pd.to_datetime(accident['연도'].astype(str) + '-' + accident['발생월'].astype(str), format='%Y-%m')
```

<br/></br>

#### [계절 변수 추가하기]
- 계절에 따른 사고건수를 파악하고자 계절 변수를 생성
```python
# 계절을 판별하는 함수 정의
def get_season(month):
    if month in [3, 4, 5]:
        return '봄'
    elif month in [6, 7, 8]:
        return '여름'
    elif month in [9, 10, 11]:
        return '가을'
    else:
        return '겨울'

# '월' 열을 기반으로 계절 변수 추가
accident['계절'] = accident['발생월'].apply(get_season)
```


<br/></br>
<br/></br>


## 7. 데이터 분석 방법론
#### [연구질문 1,2,3에 대한 분석 방법론]
- 시간 데이터, 범주형 데이터, 수치형 데이터로 나올 수 있는 모든 경우의 수를 시각화하여 파악
![image](https://github.com/user-attachments/assets/d630a8c5-98ad-4872-b6c2-5cc2686ec356)

<br/></br>



<br/></br>
<br/></br>


## 8. 시각화

### [Case 1. 차종별 사고 유형별 건수 분석]

#### [1-1. 차종별 사고 유형별 건수 분석 (승용차 포함)]
<img width="738" alt="image" src="https://github.com/user-attachments/assets/7d79aea6-6133-46d0-bf35-7857914de0f9">

<br/></br>

#### [1-2. 차종별 사고유형별 비율]
<img width="740" alt="image" src="https://github.com/user-attachments/assets/8acc1e84-4dee-4a68-a8ab-331231db5480">


<br/></br>
<br/></br>


### [Case 2. 연도별 사고량 분석]
<img width="740" alt="image" src="https://github.com/user-attachments/assets/5f524b9f-5c68-4afa-88ad-c75ec71b416c">


<br/></br>
<br/></br>


### [Case 3. 월별 사고량 분석]
<img width="738" alt="image" src="https://github.com/user-attachments/assets/d26c6a9f-a4a7-4406-ab50-1835eda51e13">


<br/></br>
<br/></br>


### [Case 4. 연월별 사고량 분석]
<img width="857" alt="image" src="https://github.com/user-attachments/assets/d1eae2ae-5201-45a9-a347-8a428f47553e">


<br/></br>
<br/></br>


### [Case 5. 계절별 사고량 분석]
<img width="825" alt="image" src="https://github.com/user-attachments/assets/0f49d545-d7ed-4379-811b-047bcff88939">


<br/></br>
<br/></br>


### [Case 6. 연도별 차종별 사고량 분석]

#### [6-1. 연도별 차종별 사고 건수]
<img width="824" alt="image" src="https://github.com/user-attachments/assets/3337c6ab-d1e3-4b1b-a29c-bfdd212471ea">

<br/></br>

#### [6-2. 연도별 차종별 사망자 건수]
<img width="822" alt="image" src="https://github.com/user-attachments/assets/6ba3c1ad-a364-48ed-9805-2f7929b7f296">

<br/></br>

#### [6-3. 연도별 차종별 중상자 건수]
<img width="826" alt="image" src="https://github.com/user-attachments/assets/5072f208-922f-43b3-9d25-8a5214a34108">


<br/></br>

#### [6-4. 연도별 차종별 경상자 건수]
<img width="823" alt="image" src="https://github.com/user-attachments/assets/b65a6770-0b7c-44a4-b0a6-5c95382c66f7">


<br/></br>

#### [6-5. 연도별 차종별 부상신고자 건수]
<img width="822" alt="image" src="https://github.com/user-attachments/assets/02d41e7f-f788-4995-a238-6520168d8d63">


<br/></br>
<br/></br>


### [Case 7. 월별 차종별 사고량 분석]

#### [7-1. 월별 사고 건수]
<img width="823" alt="image" src="https://github.com/user-attachments/assets/9a9ef708-e68c-4540-825e-9d4483a7e172">

<br/></br>

#### [7-2. 월별 사망자 건수]
<img width="822" alt="image" src="https://github.com/user-attachments/assets/422296bb-3e30-4885-aa0f-df5682af8d78">

<br/></br>

#### [7-3. 월별 중상자 건수]
<img width="824" alt="image" src="https://github.com/user-attachments/assets/6e37ed3d-9880-4906-a0ca-4985e7e51c6a">

<br/></br>

#### [7-4. 월별 경상자 건수]
<img width="821" alt="image" src="https://github.com/user-attachments/assets/515690fd-879f-49a5-89ff-024bf5f10596">

<br/></br>

#### [7-5. 월별 부상신고자 건수]
<img width="826" alt="image" src="https://github.com/user-attachments/assets/c3928287-2780-4c48-97b4-73ceacab1697">


<br/></br>
<br/></br>


### [Case 8. 계절별 차종별 사고 건수]

#### [8-1. 계절별 차종별 사고 건수]
<img width="823" alt="image" src="https://github.com/user-attachments/assets/212336e8-b0fc-475b-b42d-4dc1bfa45fb1">

<br/></br>

#### [8-2. 계절별 차종별 사망자 건수]
<img width="821" alt="image" src="https://github.com/user-attachments/assets/0e05ff95-1eff-4484-a504-a2b63e7e1653">

<br/></br>

#### [8-3. 계절별 차종별 중상자 건수]
<img width="821" alt="image" src="https://github.com/user-attachments/assets/f790b5f4-f1e3-4acd-b5a5-07dfcc7f04d4">

<br/></br>

#### [8-4. 계절별 차종별 사고 건수]
<img width="821" alt="image" src="https://github.com/user-attachments/assets/2dc3e3d0-a2dd-4337-8b1f-feb201cfe253">

<br/></br>

#### [8-5. 계절별 차종별 사고 건수]
<img width="821" alt="image" src="https://github.com/user-attachments/assets/68081d70-e3c8-48d8-9fd8-fe08ffb71382">

<br/></br>



## 9. 결과 
#### [연구질문1 결과 : 전동 킥보드 사고는 다른 교통수단에 비해 얼마나 빈번하게 발생하는가?] 

<br/></br>

#### [연구질문2 결과 : 전동 킥보드 사고의 사망자수, 부상자수 등 심각도는 다른 교통수단에 비해 어떠한가?]

<br/></br>

#### [연구질문3 결과 : 전동 킥보드 사고는 주로 어떠한 경우에 많이 발생하는가?]

<br/></br>

#### [연구질문4 결과 : 전동 킥보드 사고를 줄이기 위해서는 어떻게 해야 하는가?]


<br/></br>
<br/></br>


## 10. 논의 및 결론


<br/></br>
<br/></br>
