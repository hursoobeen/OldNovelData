# 박완서 연구 -박완서 노년소설의 양식을 중심으로-
이 Github 페이지는 "박완서 연구 -박완서 노년소설의 양식을 중심으로-"에서 제시된 데이터 전처리 및 분석 과정을 설명하는 메뉴얼이자 부록이다. 지면의 한계와 디지털인문학 연구의 특성상 연구 전과정을 논문 형태로는 공개하기 어렵기 때문에 이 페이지를 통해 부족한 내용을 채워 연구 재현성을 제고하고자 한다.

## 데이터 안내
##### * KCI 논문 서지정보 xlsx  
  KCI에서 타이틀, 초록, 키워드에 박완서가 포함된 논문을 추출한 결과로, 노년 연구 경향성을 분석하는 데 사용되었다.
- 냄새 문장 xlsx  
  Gephi 작업을 위해 박완서 전집에서 '냄새'와 관련된 키워드가 들어간 문장을 추출하여 xlsx로 정리한 결과로, 한 문장에서 키워드가 중복 사용된 경우는 횟수를 중복 반영하지 않았다.
- 단어 추이 워드클라우드 jpg  
  해당 작업을 위해 박완서 전집을 기준으로 텍스트 전처리 과정을 거쳤다. 이후 권별 빈도 상위 30개 단어를 추출하였다.
- 박완서 참고문헌 데이터는 김병준 교수님 깃허브 참조(https://github.com/ByungjunKim)  
  박완서가 노년과 관련하여 어떻게 표상되고 있는지 확인하기 위해 KCI에서 타이틀, 초록, 키워드에 박완서가 포함된 논문 결과를 추출하였다. 그러나 참고논문 정보는 웹크롤링 과정에서 데이터가 누락되는 경우가 발생한다. 이에 장시간 수작업을 통해 일일이 수집하는 작업이 필요하다. 관련 부분은 상술했듯이 김병준 교수님이 제공해주신 자료를 통해 노년 연구 경향성 분석에 반영할 수 있었다.

## 코드/폴더 안내
- KCI_논문 서지정보 코드:  
상술했듯이 '박완서' 연구에서 '노년'이라는 키워드거 어떻게 사용되고 있는지 빈도 변화, 전체 논문에서의 비중 등을 확인하기 위한 코드다. 대상은 해외 논문을 제외한 한글로 쓰여진 국내 논문, 주제 분류가 인문학 논문으로 설정하였다. 
- 냄새 성질 Gephi 출력 코드:
- 노년 연구 경향성 추출 코드:  
  박완서를 인용, 피인용 하는 논문을 추출하여 박완서 연구에서 노인이라는 키워드가 어떻게 사용되고 있는지 확인할 수 있는 자료를 추가하고자 하였다. 이에 KCI 논문 서지정보 xlsx, 김병준 교수님 자료를 합하여 작업을 수행했다. 대표 키워드를 추린 뒤. 논문 제목과, 초록을 통해 각각의 키워드가 시기별로 어떻게, 얼마나 비중 있게 사용되는지 추이를 살펴보고자 했다. 인용 빈도수 계산에서는 중복의 경우를 횟수에 모두 반영하였다. 젠더, 전쟁, 가족, 근대화 등으로 대표 키워드를 분류한 뒤 각각의 키워드에 해당하는 단어를 설정하였다. 이후 노인이 차지하는 중요도가 상승하는지, 하락하는지를 가늠해보았다.
- 권별 워드클라우드 추출 코드:  
  불용어 처리 설명하기
## 저자
허수빈 성균관대학교 국어국문학과 박사수료, sb_hur@google.com
