## 스케줄링

프로젝트의 완성을 위해 수행되어야 할 작업을 나열한 후 연관 관계와 순서에 따라 기간 별로 나타내는 것

### WBS (Work Breakdown Structure)

의미

* 프로젝트를 탑다운 방식으로 세분화하여 프로젝트의 단위 작업 파악하는 기법
* 인도물 중심으로 분할한 계층 구조 체계 (요구사항 명세서, 설계 문서 등)

![image-20210412092319826.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week06/image-20210412092319826.png?raw=true)

 ## 일정 계획

WBS를 통해 파악된 단위 작업들을 계획

표현 방법

* 차트를 사용
* 종류
  * 퍼트 차트
  * 간트 차트

### 퍼트(PERT) 차트

표기법

* 박스(또는 원): 작업이나 업무
* 선과 화살표: 각 작업간의 순서와 의존성
* 각 작업은 병행적으로 수행될 수 있음

장점

* 작업들 간의 상호의존성 및 프로젝트가 진행되는 다양한 경로 파악 가능

  퍼트차트의 가장 긴 경로(critical chart) 예측 가능

퍼트 차트 용어

* SE(Earlist Start Time): 해당 단위 작업이 가장 빨리 시작할 수 있는 일자
* EF(Earlist Finish)
* LS(Latest Start): 가장 늦게 시작하는 일자 (작업을 망치지 않는 한도 내에서 얼마나 늦게 시작할 수 있나)
* LF(Latest Finish)
* DU(Duration): ES~EF, LS~LF 사이의 작업 기간
* FT(Float Time): LS~ES 사이의 여유 기간

![image-20210412093812876.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week06/image-20210412093812876.png?raw=true)

작성 순서: 경로 작성 -> DU -> ES -> EF -> Latest .. -> FT

* EF = ES + DU
* ES는 자기의 선행작업 EF 중 max값.
* 마지막 단위 작업의 LF는 EF와 같음. (프로젝트 전체가 밀리면 안되기 때문)
* FT = LS - ES
* LF는 다음 작업의 LS 중 min 값.
* (주요 경로를 바탕으로 다른 경로의 FT가 생김.)
* 주요 경로는 계획에 차질이 생기면 바뀔 수 있음

### 간트(Gantt) 차트

퍼트 차트보다 간략해서 소규모 프로젝트 계획에 알맞음

표기법

* 시간 순으로 된 캘린더에 프로젝트 시작 시간과 종료 시간을 막대 형태로 나타냄

장점

* 작업 시작일과 종료일을 분명히 알 수 있음

단점

* 퍼트 차트와 달리 작업간의 의 존성을 보여주지 않음 (original 간트 차트의 경우)

## 프로젝트 통제

### 프로젝트 통제란

* 계획대로 잘 수행되고 있는지 주기적으로 검토

* 목표를 달성하는 데 필요하면 시정 조치를 함

많은 프로젝트가 비용 초과와 일정 지연으로 실패하게 됨

### EVM (Earned Value Management)

(SW 개발에는 잘 통하지 않는 경향이 있음)

의미

* 프로젝트의 일정상태, 비용 상태, 완료된 작업량을 비용화 하여 계획 대비 실적을 비교 및 평가하여 프로젝트의 성과와 진행률을 정량적으로 관리

특징

* 계획 대비 실제 수행의 비교가 가능

* 비용과 시간을 모두 화폐단위로 통합하여 정량화

### EVM의 기본 용어

BCWS (Budgeted Cost of Work Scheduled)

* PV(Planned Value), 계획된 작업량의 계획된 비용
* 일정이 뒤쳐지면 그만큼 손해라고 계산.
* 50을 계획 했는데 70이 걸림 -> 20 오버

**BCWP** (Budgeted Cost of Work Performed)

* EV(Earend Value), 수행한 작업의 계획된 비용
* 작업 완료됐을 때 얻는 값을 기준으로 비용을 계산
* 완료했을 때 100을 얻는데, 50% 완료 -> 50

ACWP (Actual Cost of Work Performed)

* AC(Actual Cost), 수행한 작업의 실제 비용 (실제 돈을 얼만큼 사용했는지)
* 50% 완료했는데 해당 작업의 예산을 다씀  -> 50% 오버



BAC (Budget at Completion)

* BCWS의 합, 전체 작업에 대한 계획된 비요

EAC (Estimate at Completion)

* ACWP + 남은 작업량에 대한 예측된 비용
* 전체 작업이 완료되는데 예측된 실제 비용



### SV (Schdule Variance)

BCWP - BCWS = SV

계획된 작업량과 실제 수행된 작업량의 차이

(마이너스 값은 **일정** 지연을 의미함)

### CV (Cost Variance)

BCWP - ACWP = CV

계획된 비용과 실제 비용의 차이

(마이너스 값은 **비용**초과를 의미함)

![image-20210412103847278.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week06/image-20210412103847278.png?raw=true)

### 성과 지표 (Performance Indices)

SPI (Schedule Performance Index)

* BCWP / BCWS (계획된 작업량 / 실제 작업량)
* SPI < 1 이면 일정 지연을 의미

CPI (Cost Performance Index)

* BCWP / ACWP (계획된 비용 / 실제 비용)

* CPI < 1 이면 비용 초과를 의미

### VAC (VAriance at Completion)

BAC - EAC

값이 마이너스면 **전체 작업이 완료 될 때 비용** 초과를 의미

EAC (Estimate at Completion)

* ACWP + 남은 작업량에 대한 예측된 비용
* ACWP + ((BAC - BCWP)/CPI)

### EVM 그래프

![image-20210412104601995.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week06/image-20210412104601995.png?raw=true)