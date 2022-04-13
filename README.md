# 디자인패턴

---
- 디자인패턴이란
- 디자인패턴의 종류
- 디자인패턴 조사(Prototype Pattern, )
- 참조

---
## 디자인패턴이란

디자인 패턴이란 기존 환경 내에서 반복적으로 일어나는 문제들을 어떻게 풀어나갈 것인가에 대한 일종의 솔루션 같은 것입니다. 디자인 패턴 계의 교과서로 불리는 [GoF의 디자인패턴]에서는 객체지향적 디자인 패턴의 카테고리를 "**생성 패턴(Creational Pattern)**", "**구조 패턴(Structural Pattern)**", "**행동 패턴(Behavioral Pattern)**" 3가지로 구분하고 있습니다.

 

**생성(Creational)패턴**	**구조(Structural)패턴** **행동(Behavioral)패턴**
      Singleton	                Adapter	            Command
   Abstract Factory	          Composite	          Interpreter
    Factory Method	          Decorator	            Iterator
      Builder	                  Facade	             Mediator
     Prototype	               Flyweight	           Memento
                                Proxy	               Observer
                                                      State
                                                     Strategy
                                                 Template Method


디자인 패턴은 설계자로 하여금 재사용이 가능한 설계는 선택하고, 재사용을 방해하는 설계는 배제하도록 도와줍니다. 또한 패턴을 쓰면 이미 만든 시스템의 유지보수나 문서화도 개선할 수 있고, 클래스의 명세도 정확하게 할 수 있으며, 객체 간의 상호작용 또는 설계 의도까지 명확하게 정의할 수 있습니다. 간단하게 말해서 디자인 패턴은 설계자들이 "**올바른**" 설계를 "**빨리**" 만들 수 있도록 도와줍니다.
정말 여러가지 패턴이 있지만 golang에서 사용하기 좋은 디자인 패턴이 무엇이 있을까? 상황에 따른 디자인 패턴을 사용하려면 정말 깊게 알아야 할 것 같습니다.


---
## 디자인 패턴의 종류
---
### 생성패턴 (Creational Patterns)

#### 생성패턴이란?
성패턴은 객체의 생성에 관련된 패턴으로 객체의 생성절차를 추상화하는 패턴이다.
객체를 생성-합성하는 방법 / 객체의 표현방법과 시스템을 분리한다.

#### 생성패턴 특징
생성패턴은 시스템이 어떤 구체 클래스(구체적인 클래스)를 사용하는지에 대한 정보를 캡슐화한다.
생성패턴은 이들 클래스의 인스턴스들이 어떻게 만들고 어떻게 서로 맞붙는지에 대한 부분을 완전히 가린다.
즉, 객체의 생성과 조합을 캡슐화해 특정 객체가 생성되거나 변경되어도 프로그램 구조에 영향을 크게 받지 않도록 유연성을 제공한다.

#### 생성패턴 종류
생성패턴에는 아래와 같은 디자인 패턴이 존재한다.

추상 팩토리 패턴(Abstract Factory Pattern)
: 동일한 주제의 다른 팩토리를 묶어 준다.

빌더 패턴(Builder Pattern)
: 생성(construction)과 표기(representation)를 분리해 복잡한 객체를 생성한다.

팩토리 메서드 패턴(Factory Method Pattern)
: 생성할 객체의 클래스를 국한하지 않고 객체를 생성한다.

프로토타입 패턴(Prototype Pattern)
: 기존 객체를 복제함으로써 객체를 생성한다.

싱글턴 패턴(Singleton pattern)
: 한 클래스에 한 객체만 존재하도록 제한한다.

---

### 구조패턴(structural patterns)

#### 구조패턴 이란?
구조패턴(structural patterns)은 클래스나 객체를 조합해 더 큰 구조를 만드는 패턴이다.
예를 들어 서로 다른 인터페이스를 지닌 2개의 객체를 묶어 단일 인터페이스를 제공하거나 객체들을 서로 묶어 새로운 기능을 제공하는 패턴이다.

#### 구조패턴 특징
서로 독립적으로 개발한 클래스 라이브러리를 마치 하나인 것처럼 사용할 수 있다.
여러 인터페이스를 합성하여 서로 다른 인터페이스들의 통일된 추상을 제공한다.
인터페이스나 구현을 복합하는 것이 아니라 객체를 합성하는 방법을 제공한다.

#### 구조패턴 종류

어댑터 패턴(Adapter Pattern)
: 인터페이스가 호환되지 않는 클래스들을 함께 이용할 수 있도록, 타 클래스의 인터페이스를 기존 인터페이스에 덧씌운다.

브리지 패턴(Bridge Pattern)
: 추상화와 구현을 분리해 둘을 각각 따로 발전시킬 수 있다.

합성 패턴(Composite pattern)
: 0개, 1개 혹은 그 이상의 객체를 묶어 하나의 객체로 이용할 수 있다.

데코레이터 패턴(Decorator Pattern)
: 기존 객체의 매서드에 새로운 행동을 추가하거나 오버라이드 할 수 있다.

퍼사드 패턴(Facade Pattern)
: 많은 분량의 코드에 접근할 수 있는 단순한 인터페이스를 제공한다.

플라이웨이트 패턴(Flyweight Pattern)
: 다수의 유사한 객체를 생성·조작하는 비용을 절감할 수 있다.

프록시 패턴(Proxy Pattern)
: 접근 조절, 비용 절감, 복잡도 감소를 위해 접근이 힘든 객체에 대한 대역을 제공한다.

---

### 행동패턴(Behavioral Patterns)

#### 행동패턴이란?
객체나 클래스 사이의 알고리즘이나 책임 분배에 관련된 패턴이다.
한 객체가 수행할 수 없는 작업을 여러 개의 객체로 어떻게 분배하며 객체 사이의 결합도 최소화에 중점을 둔다.
패턴을 주로 클래스에 적용하는지 아니면 객체에 적용하는지에 따라 구분되는 패턴이다.

행동패턴 종류
행동패턴에는 아래와 같은 디자인 패턴이 존재한다.

책임연쇄 패턴(Chain of responsibility)
: 책임들이 연결되어 있어 내가 책임을 못 질 것 같으면 다음 책임자에게 자동으로 넘어가는 구조이다.

커맨드 패턴(Command Pattern)
: 명령어를 각각 구현하는 것보다는 하나의 추상 클래스에 메서드를 하나 만들고 각 명령이 들어오면 그에 맞는 서브 클래스가 선택되어 실행한다.

인터프리터 패턴(Interpreter Pattern)
: 문법 규칙을 클래스화한 구조를 갖는 SQL 언어나 통신 프로토콜 같은 것을 개발할 때 사용한다.

이터레이터 패턴 (Iterator Pattern)
: 반복이 필요한 자료구조를 모두 동일한 인터페이스를 통해 접근할 수 있도록 메서드를 이용해 자료구조를 활용할 수 있도록 해준다.

옵저버 패턴(Observer Pattern)
: 어떤 클래스에 변화가 일어났을 때, 이를 감지하여 다른 클래스에 통보해준다.

전략 패턴 (Strategy Pattern)
: 알고리즘 군을 정의하고 각각 하나의 클래스로 캡슐화한 다음, 필요할 때 서로 교환해서 사용할 수 있게 해준다.

템플릿 메서드 패턴 (Template method pattern)
: 상위 클래스에서는 추상적으로 표현하고 그 구체적인 내용은 하위 클래스에서 결정된다.

방문자 패턴 (visitor Pattern)
: 각 클래스의 데이터 구조로부터 처리 기능을 분리하여 별도의 visitor 클래스로 만들어놓고 해당 클래스의 메서드가 각 클래스를 돌아다니며 특정 작업을 수행한다.

중재자 패턴 (Mediator Pattern)
: 클래스간의 복잡한 상호작용을 캡슐화하여 한 클래스에 위임해서 처리한다.

상태 패턴 (State Pattern)
: 동일한 동작을 객체의 상태에 따라 다르게 처리해야 할 때 사용한다.

기념품 패턴 (Memento Pattern)
: Ctrl + z 와 같은 undo 기능 개발할 때 유용한 디자인패턴. 클래스 설계 관점에서 객체의 정보를 저장한다.


---
## 디자인 패턴 조사
### 1.(Prototype Pattern)

### 2.

### 3.

### 4.

