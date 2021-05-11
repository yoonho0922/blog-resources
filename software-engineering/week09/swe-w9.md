### 상위 설계와 하위 설계

상위 설계

* 아키텍처 설계, 예비 설계라고 함
* 소프트웨어 구성 컴포넌트들 간의 관계로 구성된 시스템의 전체적인 구조
* 시스템 구조도, 외부 파일 및 DB 설계도, 화면 및 출력물 레이아웃 등을 포함

하위 설계

* 모듈 설계, 상세 설계라고 함
* 시스템의 각 구성 요소들의 내부 구조, 동적 행위 등을 결정
* 하위 설계 방법
  * 절차기반(Procedure-Oriented), 자료위주(Data-Oriented), 객체지향(Object-Oriented) 설계 방법

![image-20210504141018522.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week09/image-20210504141018522.png?raw=true)

## 설계 프로세스

좋은 설계란

* 요구사항 명세서의 모든 내용을 구현해야 함
* 구현 또는 테스트로 추적이 가능해야 함
* 유지 보수 시 변경이 용이해야 함

설계 방식

* 프로세스 지향 설계 (Process Oriented Design)
* 객체 지향 설계 (Object Oriented Design)

![image-20210504142205248.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week09/image-20210504142205248.png?raw=true)

## 설계 원리

### 추상화

* 의미: 자세한 구현 전에, 상위 레벨에서 제품의 구현을 먼저 생각해보는 것
* 과정 추상화
  * 자세한 단계를 고려하지 않고 상휘 수준에서 수행 흐르만 먼저 설계
* 데이터 추상화
  * 데이터 구조를 대표할 수 있는 표현으로 대체하는 것
  * ex) 날짜 구조를 단순히 "날짜"로 추상화
* 제어 추상화
  * 3-A와 3-B를 “3. 윤년 여부에 따라 요일 계산을 수행한다.”로 추상화 하는 것

예제: 원하는 날짜를 입력으로 받아 요일을 알려주는 만년 달력 프로그램

![image-20210504142718149.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week09/image-20210504142718149.png?raw=true)

### 단계적 분해

의미

* 문제를 사우이 개념 부터 더 구체적인 단계로 불할하는 탑다운 기법의 원리
* 모듈에 대한 구체 설계를 할 때 사용

### 모듈화

모듈의 의미

* 수행 가능 명령어, 자료구조 또는 다른 모듈을 포함하고 있는 독립 단위

특성

* 이름을 가짐
* 독립적으로 컴파일
* 다른 모듈을 사용할 수 있음
* 다른 프로그램에서 사용될 수 있음

## 효과적인 모듈 설계

### 정보 은닉

의미

* 인터페이스를 통해서만 메시지를 전달 할 수 있도록 하는 개념
* 자바에서 private과 public
  * private은 모듈 내에서 사용하기 때문에 바꿔도 다른 모듈에 영향 X

장점

* 모듈의 구현을 독립적으로 맡길 수 있음
* 설계 과정에서 하나의 모듈이 변경되더라도 설계에 영향을 주지 않음

### 모듈의 응집력

의미

* 모듈을 이루는 각 요소들의 서로 관련되어 있는 정도
* **강한 응집력**을 갖는 모듈을 만드는 것이 모듈 설계의 목표

응집력의 종류 (응집력이 약하면 안좋음)

![image-20210504145505604.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week09/image-20210504145505604.png?raw=true)

![image-20210504145427897.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week09/image-20210504145427897.png?raw=true)

### 모듈의 결합도

의미

* 모듈간에 연결되어 상호 의존하는 정도
* **낮은 결합도**를 갖는 모듈(Loosely coupled)을 만드는 것이 목표
* 결합도가 강하면 유지보수가 힘들어짐

모듈간의 의존도(결합도가 강하면 안좋음)

![image-20210504150239629.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week09/image-20210504150239629.png?raw=true)

![image-20210504150411581.png](https://github.com/yoonho0922/blog-resources/blob/master/software-engineering/week09/image-20210504150411581.png?raw=true)

------

reference

- 상명대학교 한종대교수님 소프트웨어공학 수업