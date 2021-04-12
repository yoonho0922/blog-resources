## 프로젝트의 정의

### 정의

- 프로젝트는 **유일한** 제품이나 서비스를 만들기 위해 수행되어야 할 **일시적인** 행동

### 프로젝트의 구성 요소

- 목표, 비용, 관리자, 참여자, 기간, 기술, 고객

## 소프트웨어 프로젝트

### 소프트웨어 개발의 시작

- 조직이 요구사항에 맞는 프로그램을 획득(Acquire)할 필요가 생겼을 때
  - 시중에 나와있는 프로그램 구입
  - 소프트웨어 개발 전문 업체에 의뢰
  - 직접 개발

### 소프트웨어 개발

- 발주자(고객)가 요구사항을 주면 수주자(개발자)가 요구사항에 맞는 프로그램을 개발

## 소프트웨어 프로젝트 프로세스

### 소프트웨어 제품 구상

- 발주자
  - 소프트웨어 제품의 구상 및 가치를 검증
  - 제품의 투자 대비 효과를 예측하고, 사업에 미치는 영향을 파악
  - 제품의 기능상, 성능상 요구사항들을 정의

### 소프트웨어 제안 요청서 (RFP: Requers for Proposal) 배포

- 개발 회사들에게 제안 요청서를 발송 (개발을 맡아줄 회사를 찾는 과정)

### 제안서 제출

### 제안서 심사

### 계약서 작성

### 프로젝트 시작 및 수행

- 마일스톤(이정표) 별로 별로 또는 발주자의 참여 필요 시 회의를 갖고 요구사항 변경 등 중요한 사항 협의

### 프로젝트 종료 및 제품 인도

## 소프트웨어 프로젝트의 성공요소

### 성공요소

![1.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week03/1.png?raw=true)

- 예상 비용을 초과하면 실패한 프로젝트

## 소프트웨어 프로젝트의 잘못된 통념

![swe-w03-2.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week03/swe-w03-2.png?raw=true)

(브룩스의 법칙 : 도중에 개발자를 투입해도 개발 속도가 늘기는 커녕 줄어듬)

## 프로젝트 관리

### 정의

- 프로젝트의 요구사항을 만족시키기 위해 지식, 기술, 툴 및 기법을 프로젝트 활동에 적용하는 것

### 프로젝트 프로세스

![swe-w03-3.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week03/swe-w03-3.png?raw=true)

착수

계획

- 프로젝트가 수행해야 할 목표 및 범위를 달성하기 위해 필요한 행동 방침을 계획

실행

통제

- 프로젝트가 계획대로 잘 수행되고 있는가를 주기적으로 검토
- 프로젝트 목표를 달성하는 데 필요하면 시정 조치를 취할 수 있도록 함

종료

### PMBOK의 프로젝트 관리 영역

![swe-w03-4.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week03/swe-w03-4.png?raw=true)

## 프로젝트 성공을 돕는 지침서

프로젝트를 잘 하는 조직은 어떻게 알 수 있을까?

## CMM (Capability Maturity Model)

### CMM의 등장

- 프로젝트 관리의 중요성 인식, 카네기멜론 대학에 SEI 설립 : 소프트웨어공학 전문연구소
- SW-CMM 개발
  - SEI에서는 개발 조직 프로세스의 성숙도에 따라 저민적 개선을 제시하는 SW-CMM을 개발
  - 성숙도가 높은 조직이 성숙도가 낮은 조직보다 높은 품질의 소프트웨어를 생산할 수 있다는 것 (CMM은 역량이 얼마나 성숙한지를 나타냄)

### 성숙도의 따른 조직의 비교

![swe-w03-5.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week03/swe-w03-5.png?raw=true)

## CMMI (Capability Maturity Model Integrate)

여러 종류의 CMM을 합쳐 기존의 문제점을 해결. 단계별로 인증을 해줌.

### CMMI의 5단계 소프트웨어 프로세스 성숙도

![swe-w03-6.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week03/swe-w03-6.png?raw=true)

- 단계를 나눠서 조직의 역량을 점진적으로 높일 수 있음.

### CMMI의 단계별 특성

1단계: 초기(Initial)

- 조직에 정의된 프로세스가 거의 없음, 계획 없이 코딩과 시험에 집중
- 뛰어난 사람 몇에 의해 프로젝트의 성공이 좌우됨
- 능력은 조직이 아닌 개인의 특성

2단계: 관리(Managed)

- 기본적인 프로젝트 관리 프로세스가 설정됨
- 프로젝트의 중간 산출물에 대한 통제가 가능
- 이전의 성공한 프로젝트에 근거하여 새로운 프로젝트 관리가 이루어짐

3단계:  정의(Defined)

- 표준과 일관성 있는 프로세스
- 조직 전체에 걸쳐 SW의 개발 및 유지에 관한 표준 프로세스가 문서화되고 통합되는 단계
- 조직의 소프트웨어 프로세스 활동에 대한 책임이 있는 팀이 구성

4단계: 정량적관리(Quantitatively Managed)

- 정량적 프로젝트 관리를 시행
- 조직의 표준 프로세스가 안정화됨

5단계: 최적화(Optimizing)

- 조직은 지속적인 프로세스 개선을 추진

## ISO 12207

### 소개

- 소프트웨어 생명주기 공정 표준
- SW 개발을 위한 일관적이고 체계적인 구조(framework)를 제공하기 위하여 제정
- CMM은 미국, ISO는 국제표준

### 구성

기본 생명주기 프로세스

지원 프로세스

조직 생명주기 프로세스

(이하 생략)

------

reference

- 상명대학교 한종대교수님 소프트웨어공학 수업
