# Guardian

## 8/15 (회의)
  - 공업지역이 확진자수가 많다. 외국인 확진자수가 많다. 유흥가
  - 연휴패턴, 데이터 변수가 어떤의미인지 불명확 (GRP)
  - 목표 : 추석기간(9.30 - 10.4) 동안 확진자 수 예측
  - 돌발감염 (집단감염), 지난 추석기간 유동인구 데이터와 어린이날 유동인구 데이터를 비교, 역귀향
  - 
  - 유동인구 예측 -> 유동인구에 따른 확률 예측
  - 확진자 : 병원 가서 확진판정 받은 사람
  - 잠복기간 1-2주
  - 추석기간 확진자수 통계는 2주전(9.16-9.22) 의 감염자수 예측

  - 정책 - 지역별 감염확률 예측 통해 위험지역 알림 서비스, (고양시에 코로나 의심환자가 많이 유입되었습니다! 사회적 거리두기, 마스크 착용), (코로나 주의보 발령, 코로나 경보 발령 지역 한정)

## 8/17 (승호형)
  - 목표 : 추석기간(9.30 - 10.4) 동안 확진자 수 예측
    ==> 이 의미가 불명확함 : 추석기간에 집계 되는 수. 
        즉, 추석 이전 또는 당일 발병해서 검사받는 인원(검사 시간 : 24h)  

 - 가설 정리 
1. 공업 지역 확진자 발생수 : 안산, 화성, 평택 중 평택에 다수 발생
   -> 대기업 공장 위치 파악 필요. 
   -> 타지역에 비해 공업지역에서 확진자 수가 많다?? 
   -> 지역별 공장 수, 공장 밀도, 대기업 및 중소기업 공장 비율, 확진자 소속 비교
2. 외국인 확진자 수(노동자, 여행자 모두 합산) 및 해외유입 인원 
3. 지역별 유흥가 밀집도(술동네, 빨간 동네)
4. 2020년 1월부터 9월 까지의 연휴 기간 및 휴가기간 파악
   (설날, 어린이날,여름휴가 등등) 
5. 돌발 집단 전염 제외한 확진자 수 기반으로 예측 후 돌발 집단 전염 더하기
6. 확진자의 소속이 거주지 등록 기준이면 귀향인원과 역귀향에 의한 전염 구분??  
7. 정보 통신 업체(네비 정보, 위치기반 정보), 
   교통, 관광 관련 공공기관(교통 유동량)
    (지하철 유동 인구, 출퇴근, 교통중심지(역,터미널))
8. 확진자 기준 : 병원 가서 확진 판정 받은 사람
9. 전염 날짜를 알면(잠복 기간 1~2주) 추석 확진자 예측 가능
   -> 2주전 상황에서 예측 시작?? 
10. 데이터 변수 파악 필요(불명확한 변수 다수 - GRP...)

* 한번 더 생각
  - 날씨에 따른 유동 인구 증감소 여부
종교에 따른 날짜별(주말) 유동인구 증감소 및 돌발 집단 전염 여부
연령대,성 별 구분 유흥가(2,30대), 공업(2,30대) 등등
추석은 민족 대이동 -> 경기도 유동인구 + 전국단위 유동인구 필요 (코로나19로 이동율 감소 여부 예측)
각 지역 인구 밀도와 확진자 수를 퍼센트로 비교해 보기
마스크 쓰고 일하기 쉬운 직업과 어려운 직업 비교(확진자 수, 사무원과 현장직 등) 
데이터 관련 사이트(kaggle 등)에서 관련 정보 구하기
Plague.Inc 라는 게임 모델과 비슷한 예측은 어떨까?
  (각 지역 특성 별 가중치 x 인구수에 비례) / 
  (돌발집단 전염 후 경계도 상승 ->  전염율 감소) 
  (무증상자 -> 전염율 증가) 등등

- 정책 제언  
지역별 감염확률 예측 통해 위험지역 알림 서비스
(고양시에 코로나 의심환자가 많이 유입되었습니다! 사회적 거리두기, 마스크 착용)
(코로나 주의보 발령, 코로나 경보 발령 지역 한정)

- 기본 데이터(경기도확진환자_연습용 (이하 db1)) 변수 파악
연번	: db1 식별 번호
확진자 : 타 데이터 연번	
성별
나이(만)	
연령대	
확진일자 : 병원에서 확진 받은 날짜	
증상발현일 : 확진자가 병증을 인식한 날짜	
무증상/조사중	
경기번호 : 경기도에서 따로 지정한 번호 (지역-숫자)	
지역 : 지역 구분(큰 지역은 나눈 듯)	
재검출 : 최초 확진 날짜 이후 재검출 날짜	
감염경로 : 불명확, 해외유입, 대규모 집단 감염 구분	
GRP	: group(?)의 약어 인듯 한데 의미 불분명
구분2 : 접촉자의 타지역에서 감염 된 여부	
구분 : Primary(일종의 root 인듯(?)) 와 접촉자 구분	
지역 (group) : ?
지역 + 시 : ? 지역 구분
확진일-증상발현일 : 확진자가 병증을 인식한 날짜와 확진 판정 받기 까지의 기간
무증상자수 : 무증상 여부

## 8/18 (동현)
fbprophet 패키지로 시계열 예측 기본 모델 만들기
