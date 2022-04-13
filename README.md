# 디자인패턴

---
- 디자인패턴이란?
- 디자인패턴의 종류
- 디자인패턴 조사(Prototype Pattern, Bridge Pattern, Command Pattern, Singleton Pattern)
- 참조

---
## 디자인패턴이란?

디자인 패턴이란 기존 환경 내에서 반복적으로 일어나는 문제들을 어떻게 풀어나갈 것인가에 대한 일종의 솔루션 같은 것입니다. 디자인 패턴 계의 교과서로 불리는 [GoF의 디자인패턴]에서는 객체지향적 디자인 패턴의 카테고리를 "**생성 패턴(Creational Pattern)**", "**구조 패턴(Structural Pattern)**", "**행동 패턴(Behavioral Pattern)**" 3가지로 구분하고 있습니다.

 ![pattern](https://user-images.githubusercontent.com/97214187/163108956-0f014826-a261-4e3a-a9b8-71e56a9971ee.png)


디자인 패턴은 설계자로 하여금 재사용이 가능한 설계는 선택하고, 재사용을 방해하는 설계는 배제하도록 도와줍니다.   
또한 패턴을 쓰면 이미 만든 시스템의 유지보수나 문서화도 개선할 수 있고, 클래스의 명세도 정확하게 할 수 있으며, 객체 간의 상호작용 또는 설계 의도까지 명확하게 정의할 수 있습니다.     
간단하게 말해서 디자인 패턴은 설계자들이 "**올바른**" 설계를 "**빨리**" 만들 수 있도록 도와줍니다.
&nbsp;정말 여러가지 패턴이 있지만 golang에서 사용하기 좋은 디자인 패턴이 무엇이 있을까? 상황에 따른 디자인 패턴을 사용하려면 정말 깊게 알아야 할 것 같습니다.  

---
## 디자인 패턴의 종류
---
### 생성패턴 (Creational Patterns)

#### 생성패턴이란?
성패턴은 객체의 생성에 관련된 패턴으로 객체의 생성절차를 추상화하는 패턴이다.  
객체를 생성-합성하는 방법 / 객체의 표현방법과 시스템을 분리한다.  

#### 생성패턴 특징
생성패턴은 시스템이 어떤 구체 클래스(구체적인 클래스)를 사용하는지에 대한 정보를 캡슐화한다.&nbsp;&nbsp;
생성패턴은 이들 클래스의 인스턴스들이 어떻게 만들고 어떻게 서로 맞붙는지에 대한 부분을 완전히 가린다.&nbsp;&nbsp;
즉, 객체의 생성과 조합을 캡슐화해 특정 객체가 생성되거나 변경되어도 프로그램 구조에 영향을 크게 받지 않도록 유연성을 제공한다.&nbsp;&nbsp;

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

#### 행동패턴 종류
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
### 1. (Prototype Pattern)
프로토타입 패턴은 원형이 되는 인스턴스를 사용해 새롭게 생성할 객체의 종류를 명시하여 새로운 객체가 생성될 시점에 인스턴스의 타입이 결정되도록 하는 패턴입니다.

#### 적용 가능한 경우
코드가 복사해야 하는 구현 클래스에 의존하지 않아야 하는 경우 프로토타입 패턴을 사용할 수 있습니다.
이 경우는 코드가 인터페이스를 통해 써드파티 코드와 함께 작동할 경우 많이 발생합니다.
객체를 초기화 하는 방식만 다를뿐 서브클래스의 수를 줄이려는 경우 프로토타입 패넡을 사용할 수 있습니다.

#### 장점
구현 클래스에 직접 연결하지 않고 객체를 복사할 수 있습니다.
프로토타입이 미리 정의되어 있기 때문에 중복되는 초기화 코드를 제거할 수 있습니다.
복잡한 오브젝트를 보다 편리하게 만들수 있습니다.

#### 단점
순환 참조가 있는 복잡한 객체를 복제하는 것은 매우 까다로울 수 있습니다.

#### 예제
prototype 패턴은 매번 객체를 새로 생성하기보다는 original 객체를 복사해서 필요한 부분만 수정해서 사용하는 패턴이다.
1. 복제할 객체 생성 프로세스가 복잡할 때 프로토타입 패턴을 사용
2. 새 인스턴스를 처음부터 만드는 대신 개체의 복사본이 만들어 지므로 데이터베이스 작업과 같은 새로운 개체를 생성하는 동안 관련된 비용이 드는 작업 방지  

```
type Address struct {
	City          string
	AddressNumber uint
}

type Person struct {
	Name    string
	Address *Address
}

```
이러한 구조체를 만들었을때  
```
alex := Person{"alex", &Address{"Seoul", 1234}}

	sarah := alex
	sarah.Address.City = "Busan"
	fmt.Println(alex.Address)  // Busan
	fmt.Println(sarah.Address) // Busan
 
```
위처럼 코드 작성시에 Address 포인터 타입이기 때문에 alex의 주소도 Busan으로 바뀌어 버립니다.  

```
func (p *Person) DeepCopy() *Person {
	buf := bytes.Buffer{}
	e := gob.NewEncoder(&buf)
	_ = e.Encode(p)

	decoder := gob.NewDecoder(&buf)
	result := Person{}
	_ = decoder.Decode(&result)

	return &result 
```
여러가지 방법이 있겠지만 gob 패키지를 이용하는 방법으로 예시를 들자면
encoding과 decoding 과정을 거치게되면 포인터 형태로 이루어진 구조체도 deepcopy가 가능합니다.  
```
hyeon := Person{"alex", &Address{"Seoul", 1234},}

	geun := hyeon.DeepCopy()
	geun.Address.City = "Busan"
	fmt.Println(hyeon.Address) // Seoul
	fmt.Println(geun.Address)  // Busan

```
위 코드를 보면 deepcopy가 되어서 geun의 주소는 여전히 seoul로 확인 할 수 있습니다.

---

### 2. (Bridge Pattern)
#### 장점
구현을 인터페이스에 완전히 결합시키지 않았기 때문에 구현과 추상화된 부분을 분리시킬 수 있다.
추상화된 부분과 실제 구현 부분을 독립적으로 확장 할 수 있다.
추상화된 부분을 구현한 구상 클래스를 바꿔도 클라이언트 쪽에는 영향을 끼치지 않는다.
코드의 단위 테스트
Bridge 패턴은 독립적인 테스트가 용이
Bridge 패턴을 사용하지 않는다면, 구현 클래스를 테스트 하기 위해 슈퍼클래스가 필요
구현 클래스의 모의 객체를 만들어, 추상 클래스를 테스트  

#### 단점
여러 플랫폼에서 사용해야 할 그래픽스 및 윈도우 처리 시스템에서 유용하게 쓰인다.
인터페이스와 실제 구현부를 서로 다른 방식으로 변경해야 하는 경우에 유용하게 쓰인다.
디자인이 복잡해진다는 단점이 있다.  

#### 예시
Bridge 패턴은 두 구현체 간의 결합을 제거하기 위해 (decoupling) 사용되는 패턴입니다.

이 패턴의 예제로 컴퓨터와 프린트기의 예제가 많이 사용됩니다.

mac과 windows 컴퓨터가 있고 삼성 프린트기와 HP 프린트기가 있다고 가정해봅시다.

컴퓨터의 종류가 2가지고 프린트기의 종류가 2가지이므로 제일 단순한 방법은 2*2=4 
즉, 4개의 구조체를 만드는 것입니다.  
```
type MacWithSamsungPrinter struct {}
 
type MacWithHpPrinter struct {}
 
type WindowWithSamsungPrinter struct {}
 
type WindowWithHpPrinter struct {}

```
이렇게 생성시에는 상당히 번거럽고 유연하지가 않다  


```
type printer interface {
    printFile()
}
 
 
type computer interface {
    print()
    setPrint(print)
}

```
인터페이스를 2개 만들어 준후

```
type samsungPrinter struct {}
 
func (p *samsungPrinter) printFile() {
    fmt.Println("Printing by a samsung..")
}
 
type hpPrinter struct {}
 
func (p *HpPrinter) printFile() {
    fmt.Println("Printing by a hp..")
}
```
그럼 삼성 프린트기와 HP 프린트기는 위처럼 나타낼 수 있습니다.

```
type mac struct {
    printer printer
}
 
func (m *mac) print() {
    fmt.Println("Print in mac")
    m.printer.printFile()
}
 
func (m *mac) setPrinter(p printer) {
    m.printer = p
}
 
 
 
type windows struct {
    printer printer
}
 
func (w *windows) print() {
    fmt.Println("Print in windows")
    w.printer.printFile()
}
 
func (w *windows) setPrinter(p printer) {
    w.printer = p
}
```
mac과 windows는 위처럼 나타낼 수 있습니다.  
중요한 점은 mac과 windows 구조체는 필드에 printer 인터페이스 타입을 가지고 있습니다.  
그렇기 때문에 프린트기를 동작시킬 수 있으며 printer의 인터페이스 타입만 만족시킨다면 어떤 프린트기든 동작시킬 수 있습니다.  


### 3. (Command Pattern)
요청을 객체의 형태로 캡슐화하여(실행될 기능을 캡슐화함으로써) 사용자가 보낸 요청을 나중에 이용할 수 있도록 매서드 이름, 매개변수 등 요청에 필요한 정보를 저장 또는 로깅, 취소할 수 있게 하는 패턴이다
커맨드 패턴에는 명령(command), 수신자(receiver), 발동자(invoker), 클라이언트(client)의 네개의 용어가 항상 따른다.

#### 장점
커맨드 패턴을 활용하게 요청부와 동작부를 분리시켜주기 때문에 시스템의 결합도를 낮출 수 있으며, 각 객체들이 수정되어도 다른 객체가 영향을 받지 않습니다.
클라이언트와 INVOKER 클래스 간의 의존성이 제거 된다.  
#### 단점 
리시버 및 리시버의 동작이 추가된다면 그 동작에 대한 클래스를 만들어야 하기 때문에, 다소 많은 잡다한 클래스들이 추가된다는 단점이 있습니다.  

### 4. (Singleton Pattern)
싱글톤 패턴은 단 하나의 인스턴스를 생성해 사용하는 디자인 패턴이다.

#### 장점
고정된 메모리 영역을 얻으면서 한번의 new로 인스턴스를 사용하기 때문에 메모리 낭비를 방지할 수 있음
또한 싱글톤으로 만들어진 클래스의 인스턴스는 전역 인스턴스이기 때문에 다른 클래스의 인스턴스들이 데이터를 공유하기 쉽다.
DBCP(DataBase Connection Pool)처럼 공통된 객체를 여러개 생성해서 사용해야하는 상황에서 많이 사용.

#### 단점
싱글톤 인스턴스가 너무 많은 일을 하거나 많은 데이터를 공유시킬 경우 다른 클래스의 인스턴스들 간에 결합도가 높아져 "개방-폐쇄 원칙" 을 위배하게 된다. (=객체 지향 설계 원칙에 어긋남)
따라서 수정이 어려워지고 테스트하기 어려워진다.

---
## 참조
[웹 개발자가 알아야할 7가지 디자인 패턴](https://sangcho.tistory.com/entry/%EC%9B%B9%EA%B0%9C%EB%B0%9C%EC%9E%90%EA%B0%80%EC%95%8C%EC%95%84%EC%95%BC%ED%95%A07%EA%B0%80%EC%A7%80%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4)  
[생성패턴 구조패턴 행위패턴](https://velog.io/@ha0kim/Design-Pattern-%EC%83%9D%EC%84%B1-%ED%8C%A8%ED%84%B4Creational-Patterns)   
[기본기를 쌓는 코딩 블로그](https://jeong-pro.tistory.com)  
