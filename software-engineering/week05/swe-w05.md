## 프로젝트 팀 구성

* 2단계 구조

* 계층적 구조

* 민주적 팀 구성

## 스케줄링

* 프로젝트 완성을 위해 **수행되어야 할 작업**을 나열한 후 **연관 관계와 순서에 따라 기간 별로 나타내는 것**
* WBS : 프로젝트 중 수행되어야 하는 작업들을 파악

### WBS (Work Breakdown Structure)

![image-20210609150354033.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210609150354033.png?raw=true)

* 프로젝트를 **탑다운 방식으로 세분화**하여 프로젝트의 **단위 작업에 대해 파악**하는 기법
* 프로젝트 팀이 수행할 작업을 인도물 중심으로 분할한 **계층 구조 체계**
* 프로젝트의 전체 범위를 **산출물 중심의 트리 구조**로 나타냄, 아래로 갈수록 작업들이 **점차적으로 상세히 정의**



## 프로젝트 산정

* 프로젝트 수행에 필요한 규모(Size), 공수(Effort), 비용(Cost) 등을 **정량적으로 예측**하는 것
* 방법
  * **경험적 방법** - 델파이 기법
  * **크기 중심 방법** - LOC, COCOMO
  * **기능 중심 방법** - 기능점수(FP)로 측정

### 델파이(Delphi) 기법

* **경험적 산정**, 전문가들의 의견이나 판단을 종합하여 예측

#### 산정 프로세스

![image-20210405104541686.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210405104541686.png?raw=true)

### LOC(Lines Of Code)

* **크기 중심적 산정**, 프로그램 코드 **라인의 수**를 통해 산정

#### 산정 프로세스

1. 전체 프로그램을 **모듈 별로 분할**

2. 모듈 별로 **규모 추정** 및 총 **규모 계산** (경험을 토대로 LOC 추정)

   추정 LOC: EV = (opt + 4m + pess) / 6

   * Vopt: 낙관적 LOC, Vm: 보통 LOC, Vpess: 비관정 LOC

3. **경험적** 데이터를 이용한 **개발 비용 및 개발 노력 추정**

   * 프로젝트 비용: **총 LOC * LOC 당 비용**(경험적 데이터)
   * 개발 노력: **총 LOC / 생산성** -> Man-Month (생산성: 한달에 얼마나 코드를 짤지)

### COCOMO(Constructive Cost Model)

개념: LOC 기반의 경험적 산정 모델, **경험적으로 추출된  상수와  LOC를 사용**

오래된 기법이기 때문에 현재는 부정확

### FP(Function Point 기능 점수)의 개요

* 의미 

* 장점
  * 기술, 환경, 능력에 독립적
  * 프로젝트 초기에 규모 산정 가능

* 단점
  * 주관적인 자료를 바탕으로 하기 때문에 신뢰도가 떨어질 수 있음

#### FP 측정 프로세스

![image-20210405111707017.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210405111707017.png?raw=true)

#### 1.측정 유형의 결정

* 개발 프로젝트 기능 점수 (DFP): 신규 개발시
* 개선 프로젝트 기능 점수 (EFP): 기존 시스템의 개선시
* 어플리케이션 기능 점수 (AFP): 기존 기능의 크기 측정

![image-20210405112101199.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210405112101199.png?raw=true)

#### 2. 측정 범위와 어플리케이션 경계 식별

#### 3.데이터 기능 측정

* 데이터 기능
  * **내부 논리 파일 (ILF)**: 측정 대상 app 내부에서 유지 (DB)
  * **외부 연계 파일** **(EIF)**: 외부에서 유지 ex) 결제 처리에 필요한 은행정보
* ILF와 EIF의 측정 (간이법에선 상용X, 상세법에서는 사용)
  * **RET: 디비의 테이블 갯수**
  * **DET: 디비의 칼럼 갯수**
* 미리 정의된 복잡도와 기여도 Metric에 적용하여 ILF와 EIF의 값을 산정

#### 4.트랜잭션 기능 측정

* 사용자에게 **제공하는 기능의 크기**를 측정

* 트랜잭션 기능
  * **외부 입력(EI: External Input)**
  * **외부 출력(EO: External Output)**
    * 사용자의 **요구를 처리**하고 출력 (필드를 합치는 등)
  * **외부 조회(EQ: External in Inquiry)**
    * 처리 로직을 포함하지 않음, 어떠한 변경도 없이 그냥 출력

* EI, EO, EQ의 측정 (상세법에서는 사용)
  * **FTR**: 참조되는 ILF 또는 EIF
  * **DET**: 사용자가 식별가능한 필드
  
  ![image-20210611120126843.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210611120126843.png?raw=true)
  
* 미리 정의된 복잡도와 기여도 Metric에 적용하여 값을 선정

#### 5.**미조정 기능점수(UFP)**

* **데이터기능점수 + 트랜잭션 기능 점수**
* **ILF, EIF, EI, EO, EQ**의 가중치를 모두 더한 것

![image-20210611120802384.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210611120802384.png?raw=true)

#### 6.조정 인자(VAF)

* **app의 특성 및 영향을 주는 요인에 따라** 기능 점수를 조정할 인자를 설정
* 프로그램 복잡도 및 난이도가 올라갈 수록 보정계수가 높아짐

#### 7.조정기능점수 

* **UFP * VAF**

------

reference

- 상명대학교 한종대교수님 소프트웨어공학 수업