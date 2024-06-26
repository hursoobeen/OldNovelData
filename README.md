# 박완서 연구 -박완서 노년소설의 양식을 중심으로-
이 Github 페이지는 "박완서 연구 -박완서 노년소설의 양식을 중심으로-"에서 제시된 데이터 전처리 및 분석 과정을 설명하는 메뉴얼이자 부록이다. 지면의 한계와 디지털인문학 연구의 특성상 연구 전과정을 논문 형태로는 공개하기 어렵기 때문에 이 페이지를 통해 부족한 내용을 채워 연구 재현성을 제고하고자 한다.

## 데이터 안내
- **KCI 논문 서지정보 xlsx**  
  KCI에서 타이틀, 초록, 키워드에 박완서가 포함된 논문을 추출한 결과로, 노년 연구 경향성을 분석하는 데 사용되었다.
- **냄새 문장 xlsx**  
  Gephi 작업을 위해 박완서 전집에서 '냄새'와 관련된 키워드가 들어간 문장을 추출하여 xlsx로 정리한 결과로, 한 문장에서 키워드가 중복 사용된 경우는 횟수를 중복 반영하지 않았다.
- **단어 추이 워드클라우드 jpg**  
  해당 작업을 위해 박완서 전집을 기준으로 텍스트 전처리 과정을 거쳤다. 이후 권별 빈도 상위 30개 단어를 추출하였다.
- **박완서 참고문헌 데이터 xlsx**  
  박완서가 노년과 관련하여 어떻게 표상되고 있는지 확인하기 위해 KCI에서 타이틀, 초록, 키워드에 박완서가 포함된 논문 결과를 추출하였다. 그러나 참고논문 정보는 웹크롤링 과정에서 데이터가 누락되는 경우가 발생한다. 이에 장시간 수작업을 통해 일일이 수집하는 작업이 필요하다. 관련 부분은 상술했듯이 김병준 교수님이 제공해주신 자료를 통해 노년 연구 경향성 분석에 반영할 수 있었다. 김병준 교수님 깃허브 참조(https://github.com/ByungjunKim)

## 코드/폴더 안내
- **KCI_논문 서지정보 코드:**  
'박완서' 연구에서 '노년'이라는 키워드가 어떻게, 어느정도 연구되고 있는지 연구의 빈도 변화와 전체 논문에서의 비중을 확인하기 위한 코드다. 대상은 해외 논문을 제외한 한글로 쓰여진 국내 논문, 주제 분류가 인문학에 대항하는 논문으로 설정하였다.
- **노년 연구 경향성 추출 코드:**  
상술하였듯이 KCI에서 타이틀, 초록, 키워드에 박완서가 포함된 논문 결과를 추출, 이에 더해 박완서를 인용, 피인용 하는 논문을 추출하여 박완서 연구 전반에서 노인이라는 키워드가 어떻게 사용되고 있는지 확인할 수 있는 자료를 추가하고자 하였다. 이에 위 *KCI 논문 서지정보 xlsx*, *박완서 참고문헌 데이터*를 합하여 코드를 작업하였다. 작업 과정에서 먼저 일정 집합으로 키워드를 정리하였다. 논문을 젠더, 전쟁, 가족, 근대화, 노년 등 대표 주제로 집합화한 뒤 각각의 집합에 해당하는 단어를 설정해 분류하는 식이다. 이후 논문 제목, 초록을 통해 시기별로 노년 집합이 차지하는 비중이 어떻게 변하는지, 어떠한 주제와 함께 다루어지는지 등을 가늠해보았다. 전체 연구에서의 비중을 확인하는 만큼 빈도수 계산에서는 중복 횟수를 그대로 반영하였다. 
- **냄새 성질 Gephi 출력 코드:**  
냄새가 어떻한 맥락에서 쓰이는지 확인하기 위해서는 텍스트를 일일이 확인하는 과정이 필요했다. 이에 디지털화한 텍스트에서 냄새에 해당하는 단어 예를 들어 향기,내음,악취 등이 냄새로 검색될 수 있도록 선작업을 시행하였다. 냄새가 포함된 문장을 추출하여 어떠한 대상(subject)을 묘사할 때 쓰였고, 긍정적인 감정으로 쓰였는지 부정적으로 쓰였는지 성격(character)을 확인할 수 있도록 시트를 정리하였다. 이렇게 정리된 *냄새 문장 xlsx*을 Gephi를 통해 시각화하였다.
- **권별 워드클라우드 추출 코드:**  
 빈도수 추출에는 Noun', 'Adjective'만 포함하였으며 불용어 처리는 별도의 파일이 아닌 stopwords로 설정하였다. 이유는 권마다 불용어로 설정해야하는 단어가 다르고, 서사 특성상 빈번하게 쓰였더라고 의미 없는 단어 예를 들어 '버스','강아지' 등을 즉각 확인하며 바로바로 제거하기 위해서다. 따라서 각 권마다 불용어 리스트에 포함된 단어는 상이하다.
  
## 저자
허수빈 성균관대학교 국어국문학과 박사수료, sb_hur@google.com
