# MVC(Model-View-Controller) 패턴

> 소프트웨어 설계에서 애플리케이션을 세 가지 주요 구성 요소로 분리하여 모듈성을 높이고 유지보수성을 향상시키는 디자인 패턴
MVC 패턴은 사용자 인터페이스와 비즈니스 로직을 분리하여 코드의 복잡도를 줄이고, 각 구성 요소가 자신의 역할에 집중하도록 설계
> 

### 구성요소

- 모델(Model)
    
    애플리케이션의 데이터와 비즈니스 로직을 담당. 
    데이터베이스와의 상호 작용, 데이터 유효성 검사 등을 처리
    
- 뷰(View)
사용자 인터페이스를 담당. 
모델의 데이터를 사용자에게 보여주는 역할.
- 컨트롤러(Controller)
사용자 입력을 처리하고, 이를 바탕으로 모델과 뷰를 업데이트한다. 
모델과 뷰 간의 흐름을 제어하는 중재자 역할

### MVC 패턴의 장점

- 모듈성: 애플리케이션의 각 구성 요소가 독립적으로 변경될 수 있어 유지보수가 용이
- 재사용성: 모델과 뷰를 분리하여 서로 다른 뷰를 사용해 동일한 모델을 재사용
- 유연성: 애플리케이션의 한 부분을 변경해도 다른 부분에 영향을 최소화

# **전략 패턴 (Strategy Pattern)**

> 정책 패턴이라고 불리기도 함
알고리즘을 캡슐화하여 서로 다른 알고리즘을 객체 간의 교환 가능한 방식으로 사용할 수 있도록 하는 패턴
> 

### 전략 패턴의 장점과 단점

장점

- SOLID원칙의 개방 폐쇄 원칙(OCP)을 지킬 수 있다.
- 새로운 알고리즘을 추가하거나 하나의 알고리즘을 수정하는 데에 있어 유연성과 확장성이 있다.
- 각 알고리즘에 대한 독립적인 테스트가 가능하다.
- 캡슐화로 인한 코드의 재사용성이 증가한다,.

단점

- 각 알고리즘이 별도의 클래스로 구현되어야 하기 때문에 클래스 수가 증가하고 시스템의 복잡도가 증가할 수 있다.
- 런타임에서 객체를 교체하여 실행하면 오버헤드가 발생할 수 있다.

# 이터레이터 패턴(Iterator Pattern)

> 이터레이터(iterator)를 사용하여 컬렉션(Collection)의 요소들에 접근
 내부구조를 노출하지 않고 집합체를 통해 원소 객체에 순차적으로 접근할 수 있는 방법을 제공
> 

### 이터레이터 패턴의 장점과 단점

장점

- 순회할 수 있는 여러 가지 자료형의 구조와 상관 없이 ****Iterator라는 하나의 인터페이스로 순회 가능
- 집합체 내부 구조를 노출하지 않고 순회할 수 있음
- 집합체의 구현과 접근하는 처리 부분을 반복자 객체로 분리해 결합도 줄일 수 있음

단점

- 클래스가 늘어나고 복잡도가 증가

# **MVP 패턴**

> MVC에서 파생된 패턴
C(Controller) → **P(Presenter),** MVC 패턴보다 더 강한 결합을 지닌 디자인 패턴
> 

# **MVVM 패턴**

> MVC에서 파생된 패턴
C(Controller) → **VM(View Model)**
> 

### **뷰 모델**

- 뷰를 더 추상화한 계층
- MVC와 다르게 **커맨드와 데이터 바인딩**을 가지는 것이 특징

뷰와 뷰 모델 사이의 양방향 데이터 바인딩 지원

장점

- UI를 별도의 코드 수정 없이 재사용 가능
- 단위 테스팅이 쉬움
