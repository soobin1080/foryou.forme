
# [ Bixby  캡슐 챌린지 시즌2 ] 포유(for you) - ‘포미(for me)’
------------------------------------------------------------

### 1. 캡슐 소개
----------------
#### “포미는 월경과 관련된 정보를 제공합니다.”

생리 주기 예측 캡슐인 ‘포미’는 사용자의 생리 시작일과 종료일을 기록하여 주기를 계산해주고 다음 생리예정일과 배란일을 알려줍니다. 추가로 사랑일을 기록하면 최근 생리 시작일부터의 사랑일 정보들을 알려줍니다.  
‘포미’는 사용자의 위치 정보를 받아와 공공데이터에 등록된 근처 산부인과와 약국의 정보를 제공해주고, 가는 길과 대표 전화를 알려줍니다.  
‘포미’는 섭취할 식재료가 생리통에 좋은 식재료인지 판단해줄 뿐만 아니라 대표 식재료들을 추천해주고 관련 레시피 영상을 검색하여 알려줍니다.  
‘포미’는 생리통을 완화해줄 수 있는 운동법을 영상으로 알려줍니다.  
‘포미’는 생리대를 주문할 수 있는 구매 링크를 제공해줍니다.  

----------------------------------------------------------------------

### 2. 대표 발화
-----------------
#### 대표 발화#1: 오늘 시작했어/끝났어 (생리 시작일/종료일 저장)  
1. 사용자의 월경 주기를 자동으로 update 함으로써 다음 월경 예정일 예측합니다.  
즉, 20일을 주기로 등록한 사용자의 다음 월경 예정일은 마지막 월경 시작일 + 20일로 나타나게 됩니다.  
2. 사용자가 월경 종료일을 등록하지 않을 것을 대비하여 사용자의 월경 기간을 받아와 자동으로 사용자의 월경 종료일을 등록하게 됩니다. 따라서, 월경 주기 등록 시 종료일이 보여지는 것은 예상 종료일이며, 종료일을 등록 시 사용자의 월경 기간을 자동으로 계산하여 update 합니다.  
3. 2번에 작성한 사항에 따라 '오늘 시작했어' 와 '오늘 끝났어' 라고 발화를 하는 상황에서는 사용자가 월경 기간이 하루로 측정되어 다음 등록 시 동일한 날짜로 등록되는 상황입니다.  
(실제로 하루만 하는 사람이 있기 때문에 예외처리 하지 않았습니다.)  

#### 대표 발화#2: 생리 예정일/배란일 알려줘 (생리 예정일/배란일 정보 제공)
- 먼저 생리 시작일을 등록해야 생리예정일과 배란일 정보를 알 수 있습니다. 또한, 생리 시작일을 등록해야 사랑일을 등록할 수 있습니다.
#### 대표 발화#3: 근처 산부인과(약국) 위치 알려줘 (가는 길/대표 전화)
- 산부인과와 약국에 대한 정보는 공공데이터를 기반으로 하여, 지역으로 검색을 할 때는 정확한 행정구역명으로 검색해야 하고, 시도와 시군구 정보를 모두 입력하여야 합니다. 근처 산부인과와 약국 가는 길과 대표 전화 연결을 위해서는 먼저 사용자가 산부인과와 약국을 선택하여야합니다.
ex) 대전시 유성구 약국 알려줘 / 서울시 종로구 병원 찾아줘
#### 대표 발화#4: 사과 먹어도 돼(생리통에 좋은 식재료인지 판단)
#### 대표 발화#5: 생리통에 좋은 운동 알려줘 (영상)
- 운동, 영상, 자세, 체조 등으로 검색하여야 합니다. (요가는 ‘가’가 조사로 인식되기 때문에 정상적으로 작동하지 않을 수 있습니다.)
#### 대표 발화#6: 생리대 주문해줘 (구매 링크 제공) 

----------------------------------------------------------------------

### 3. 사용자 정보 제공 및 사용 설명
-----------------------------------
본 캡슐에서는 Bixby userID를 이용하여 사용자의 생리일을 저장하고 주기를 예측해주는 캡슐입니다.  
또한, 사용자의 위치정보를 이용하여 공공데이터 기반으로 근처 산부인과와 약국을 찾아주는 캡슐입니다.  

사용자 정보 제공에 대한 동의는 Bixby 기본 정책을 따르며 수집된 사용자 정보는 본 캡슐 외의 다른 매체를 통해 저장 및 공유되지 않습니다.


---------------------------------------------------------
▶개인정보 보호책임자  
성명: 김수빈  
연락처: 010-6800-1080, soobin1080@naver.com  

▶개인정보 보호 담당부서  
부서명: 빅스비 개발팀- Backend  
담당자: 김대래  
연락처: 010-9319-0840, drk0830@naver.com  
