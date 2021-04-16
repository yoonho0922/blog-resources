## 프로젝트 팀 구성

* 2단계 구조

* 계층적 구조

* 민주적 팀 구성

## 프로젝트 산정

### 델파이(Delphi) 기법

의미 : 경험적 산정, 전문가들의 의견이나 판단을 종합하여 예측

산정 프로세스

![image-20210405104541686.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210405104541686.png?raw=true)

### LOC(Lines Of Code)

의미 : 크기 중심적 산정, 프로그램 코드 라인의 수를 통해 산정

산정 프로세스

1. 전체 프로그램을 모듈 별로 분할
2. 모듈 별로 규모 추정 및 총 규모 계산 (경험을 토대로 LOC 추정)
3. 경험적 데이터를 이용한 개발 비용 및 개발 노력 추정
   * 생산성 (LOC / Man-Month: 한 사람이 한달에 짜는 코드)을 이용해 추정
   * LOC당 비용 (경험적 비용 / LOC) -> 프로젝트 비용:  LOC * (LOC당 비용)

### COCOMO(Constructive Cost Model)

개념: LOC 기반의 경험적 산정 모델, 경험적으로 추출된  상수와  LOC를 사용

오래된 기법이기 때문에 현재는 보통 부정확.



### FP(Function Point 기능 점수)의 개요

의미: 

장점:

단점: 주관적인 자료를 바탕으로 하기 때문에 신뢰도가 떨어질 수 있음

### FP 측정 프로세스

![image-20210405111707017.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210405111707017.png?raw=true)

1.측정 유형의 결정

* 개발 프로젝트 기능 점수 (DFP)
* 개선 프로젝트 기능 점수 (EFP)
* 어플리케이션 기능 점수 (AFP)

![image-20210405112101199.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week05/image-20210405112101199.png?raw=true)

 3.데이터 기능 측정

* 데이터 기능
  * 내부 논리 파일 (ILF): 측정 대상 app 내부에서 유지
  * 외부 연계 파일 (EIF): 외부에서 유지 ex) 결제 처리에 필요한 은행정보
* ILF와 EIF의 측정 (상세법에서는 사용)
  * RET: 디비의 테이블ㅇㅇㅇㅇ 갯수
  * DET: 디비의 칼럼 갯수

4.트랜잭션 기능 측정

* 사용자에게 제공하는 기능의 크기를 측정
* 트랜잭션 기능
  * 외부 입력(EI: External Input)
  * 외부 출력(EO: External Output)
  * 외부 조회(EQ: External in Inquiry)
* EI, EO, EQ의 측정 (상세법에서는 사용)
  * FTR
  * DET

5.미조정 기능점수(UFP)

* 그냥 더한 것: 데이터기능점수 + 트랜잭션 기능 점수

6.조정 인자(VAF)

* app의 특성 및 영향을 주는 요인에 따라 기능 점수를 조정할 인자를 설정

7.조정기능점수

* UFP * VAF

------

reference

- 상명대학교 한종대교수님 소프트웨어공학 수업