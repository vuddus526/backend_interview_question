# backend_interview_question
백엔드 개발자로서 꼭 알아야 하는 개념을 이해하고 정리하는 공간입니다

# CS면접 관련지식

## 자바
<details>
<summary>Override 와 Overload 를 설명해주실 수 있을까요?</summary>
<div markdown="1">
오버라이딩은 부모 클래스의 메서드를 자식 클래스에서 재정의 해서 사용하는 기술입니다

오버로딩은 같은 이름의 메서드를 매개변수의 유형과 개수를 다르게 해서 여러 개 가지는 기술입니다
</div>
</details>

<details>
<summary>Annotation이란 무엇이고 구체적으로 어떤 것이 있는지 예시를 들어 설명해주실 수 있을까요?</summary>
<div markdown="1">
사전적 의미로 주석을 뜻합니다 즉 프로그램에게 추가적인 정보를 제공해주는 메타데이터라고 볼 수 있습니다
예를들어 컴파일러에게 문법상 에러를 체크 해도록 정보를 제공하고 특정 역할을 수행하게 지정할 수 도 있습니다
</div>
</details>

<details>
<summary>JVM 이란 무엇이고 왜 필요한지 설명해주실 수 있을까요?</summary>
<div markdown="1">
한마디로 정의해보자면 OS에 종속받지 않고 CPU가 자바를 인식하고 실행할 수 있게 해주는 가상 컴퓨터입니다
한번 쓴 것은 어디서든지 읽혀야한다 라는 철학으로 만들어진 자바이다 컴파일된 뒤 바이트코드로 변형된 자바를
어느 OS든 사용할 수 있게 하기 위해 JVM이 필요하다고 생각합니다

일반 프로그램들은 OS에 종속되어있어 OS가 바뀌면 그 OS에 적용하기 위해 많은 노력이 필요한데
자바 프로그램은 JVM이라는 가상 컴퓨터를 중간에 끼워 사용하기에 JVM만 OS에 맞춰 바꿔주면
자바 소스코드를 컴파일러가 JVM이 인식할 수 있는 자바 바이트 코드로 변환해서 넘겨주고 
이를 JVM에서 바이너리 코드로 바꿔 OS가 이해할 수 있게 해석해줍니다
</div>
</details>

<details>
<summary>Java가 컴파일되는 과정은 어떻게 되는지 설명해주실 수 있을까요?</summary>
<div markdown="1">
개발자가 자바로 코드를 작성하면 자바 소스코드 파일인 .java 파일이 만들어지고
이를 자바 컴파일러가 컴파일해서 바이트코드 파일인 .class 파일을 만듭니다
이를 JVM 클래스 로더에게 전달해 검증해서 JVM 메모리에 올리게 되고 실행 엔진에 의해 실행됩니다
이때 인터프리터나 JIT 컴파일러에 의해 바이너리 코드로 변환된다고 설명드릴 수 있습니다
</div>
</details>

<details>
<summary>JVM의 스택과 힙메모리 영역에 대해 아는 만큼 설명해주실 수 있을까요?</summary>
<div markdown="1">
스택은 자바 프로그램이 컴파일 되어 생성되는 바이트 코드가 아닌 실제 실행할 수 있는
기계어로 작성된 프로그램을 실행시키는 영역입니다 각종 형태의 변수나 스레드나 메서드의 정보를 저장합니다

힙메모리는 객체를 저장하는 공간으로서 new 연산자로 생성되는 객체와 배열을 저장합니다
</div>
</details>

<details>
<summary>클래스와 인스턴스의 차이에 대해 설명해주실 수 있을까요?</summary>
<div markdown="1">
클래스는 변수와 메서드의 집합 이고 쉽게 말해 설계도와 같다고 볼 수 있습니다
인스턴스는 그런 클래스를 바탕으로 소프트웨어 세계에 구현된 구체적인 실체라고 볼 수 있습니다
oop의 관점에서 보자면 객체가 메모리에 할당되어 실제 사용될때 인스턴스라고 할 수 있습니다
</div>
</details>

<details>
<summary>Garbage Collector의 역할, 원리, 알고리즘에 대해 아는 만큼 설명해주실 수 있을까요?</summary>
<div markdown="1">
가비지 컬렉터는 JVM의 Heap 영역에서 동적으로 할당했던 메모리 영역 중 필요 없게 된 메모리를 주기적으로 삭제하는 프로세스를 말합니다
이는 순회를 통해 메모리가 어떤 객체를 참조하고 있는지 마킹하고, 참조하고 있지 않은 메모리들을 제거하는 방식을 진행됩니다
이러한 과정을 Mark And Sweep 알고리즘이라고 부릅니다
</div>
</details>

<details>
<summary>Java Map의 내부 구현은 어떻게 이루어져 있을지 추측해보실 수 있을까요?</summary>
<div markdown="1">
// 추후 내용 더 추가예정
</div>
</details>

<details>
<summary>JVM 구조에 대해서 설명해주세요</summary>
<div markdown="1">
JVM의 구조는 클래스 로더(Class Loader), 실행 엔진(Execution engine), 실행 데이터 영역(Runtime Data Area), 가비지 컬렉터 (Garbage Collector)등으로 이루어져 있습니다

- 클래스로더는 동적으로 클래스를 로딩해주는 역할을 하는데 class파일을 묶어서 JVM이 운영체제로부터 할당받은 메모리 영역인 Runtime Data Area로 적재합니다
- 실행엔진은 클래스 로더에 의해 실행 데이터 영역의 Method Area에 배치됩니다 그리고 배치된 바이트코드를 실행하는 역할을 합니다
- 가비지컬렉터는 더는 사용하지 않는 메모리를 자동으로 회수해줍니다 heap메모리 영역에 생성된 객체들 중에 참조되지 않은 객체들을 탐색 후 제거하는 역할을 하며
해당 역할을 하는 시간은 정확히 언제인지 모릅니다 가비지컬렉터 역할을 하는 스레드를 제외한 나머지 모든 스레드들은 일시정지 상태가 됩니다
- 실행 데이터 영역은 메서드영역, 힙영역, 스태경역, 네이티브메서드 스택영역으로 구성되어있습니다
</div>
</details>

<details>
<summary>객체지향프로그램이란 무엇인가요?</summary>
<div markdown="1">
<p>프로그래밍에서 필요한 데이터를 추상화 시켜 (클래스로)</p>
<p>상태(변수) 와 행위(메서드)를 가진 객체(인스턴스 화)를 만들고</p>
<p>그 객체들 간의 유기적인 상호작용을 통해 로직을 구성하는 프로그래밍 방법이다</p>
</div>
</details>

<details>
<summary>객체지향이 지향하는 바 무엇인가요?</summary>
<div markdown="1">
<p>쉽게 정의하면 객체지향은 의존성 관리라고 말할 수 있습니다</p>
<p>객체지향으로 의존성을 관리함으로써 변경 영향을 최소화하고 객체마다 독립적인 개발이 가능해집니다</p>
<p>이로인해 유지보수성과 확장성을 가질 수 있습니다</p>
</div>
</details>

<details>
<summary>객체 지향 프로그래밍 했을때의 장점 / 단점 무엇인가요?</summary>
<div markdown="1">
<p>장점</p>
<p>코드 재사용이 용이하다 (상속을 통해 확장하거나 클래스 이용)</p>
<p>유지보수가 좋다 (클래스 내부의 변수, 메서드를 수정하면되기에)</p>
<p>대형 프로젝트에 적합하다 (API별로 나눠서 업무 분담이 쉽기 때문에)</p>
<p>단점</p>
<p>처리 속도가 상대적으로 느리다</p>
<p>설계시 많은 시간과 노력이 필요하다</p>
<p>객체가 많으면 용량이 커질 수 있다</p>
</div>
</details>

<details>
<summary>객체지향 프로그래밍 4대 특징은 무엇인가요?</summary>
<div markdown="1">
<p>캡슐화</p>
<p>데이터와 코드의 형태를 외부로부터 알 수 없게 하고
데이터의 구조와 역할, 기능을 하나의 캡슐 형태로 만드는 것이다</p>
<p>추상화</p>
<p>공통의 속성이나 기능을 묶어 이름을 붙이는 것이다</p>
<p>객체지향 관점에서 클래스를 정의하는 것이다</p>
<p>상속화</p>
<p>부모 클래스에 정의된 변수 및 메서드를
자식 클래스에서 상속받아 사용하는 것이다</p>
<p>다형성</p>
<p>다양한 형태로 표현이 가능한 구조를 말한다</p>
<p>오버로딩, 오버라이딩을 예로 들 수 있다</p>
</div>
</details>

<details>
<summary>객체지향 프로그래밍 5대 원칙은 무엇인가요?</summary>
<div markdown="1">
<p>1) 단일 책임 원칙</p>
<p>한 클래스는 하나의 책임만 가져야한다</p>
<p>ex) 사람 클래스는 사람의 역할만 충실히 한다</p>
<p>2) 개방 폐쇄 원칙</p>
<p>확장에는 열려있고 변경에는 닫혀 있어야 한다</p>
<p>ex) 기능을 더 추가는 할 수 있어도 바꾸는건 함부로 못한다</p>
<p>3) 리스코프 치환 원칙</p>
<p>상위 타입의 객체를 하위 타입의 객체로 치환해도
상위 타입을 사용하는 프로그램은 정상적으로 작동해야 한다</p>
<p>ex) 어떤 메서드에 Item 이라는 상위 타입으로 받고 있는데
apple 이라는 하위 타입으로 바뀌어 넘어와도 동작해야한다</p>
<p>4) 인터페이스 분리 원칙</p>
<p>인터페이스는 그 인터페이스를 사용하는
클라이언트를 기준으로 분리해야한다</p>
<p>ex) 3명의 클라이언트가 하나의 인터페이스를 상속받기보다
각 클라이언트 별로 인터페이스를 분리해야한다</p>
<p>5) 의존 역전 원칙</p>
<p>추상화에 의존해야 하고 구체화에 의존하면 안된다</p>
<p>ex) 자동차가 스노우 타이어(구체화)에 의존하는게 아니라
타이어(추상화)에 의존해야하는 것이다</p>
</div>
</details>

<details>
<summary>getter, setter를 사용하는 이유는 무엇인가요?</summary>
<div markdown="1">
<p>객체의 무결성을 보장하기 위해 사용한다</p>
<p>무결성은 데이터의 정확성과 일관성을 유지하고 보증하는 것이다</p>
<p>정확성은 중복이나 누락이 없는 상태이고
일관성은 원인과 결과의 의미가 연속적으로 보장되어 변하지 않는 상태이다</p>
<p>getter는 필드의 값을 숨긴채 값을 꺼낼 수있고
setter는 필드를 private로 만들어 외부 접근을 제한하고
setter로 값을 받아 가공해 넣을 수 있다</p>
<p>그러나 무분별한 setter는 무결성을 해칠 수 있기에 사용하지 말아야한다</p>
<p>builder 패턴이나 개방폐쇄원칙으로 처리해야한다</p>
</div>
</details>

<details>
<summary>Error와 Exception의 차이를 설명하시오</summary>
<div markdown="1">
<p></p>
</div>
</details>

<details>
<summary>hashMap과 hashtable의 차이를 설명하시오</summary>
<div markdown="1">
<p></p>
</div>
</details>

<details>
<summary>String, StringBuffer, StringBuilder의 차이를 설명하시오</summary>
<div markdown="1">
<p></p>
</div>
</details>

<details>
<summary>쓰레드 동기화란 무엇인가요</summary>
<div markdown="1">
<p></p>
</div>
</details>

<details>
<summary>제네릭이 무엇인가요</summary>
<div markdown="1">
<p></p>
</div>
</details>

<br>

## 스프링
<details>
<summary>DI와 IoC에 대해 아는 만큼 설명해주실 수 있을까요?</summary>
<div markdown="1">
DI는 의존성 주입으로 스프링에서 외부(컨테이너) 에서 객체를 생성 후 주입 시켜주는 방식입니다

IOC는 제어의 역전으로 메서드나 객체의 호출 작업을 개발자가 아닌 외부(컨테이너) 에서 결정되는 것을 의미합니다
</div>
</details>

<details>
<summary>MVC 모델이란 무엇인지 설명해주실 수 있을까요?</summary>
<div markdown="1">
모델, 뷰, 컨트롤러의 약자이며 개발을 할 때 3가지 형태로 역할을 나누어 개발하는 방법론입니다
모델의 경우 무엇을 할 것인지 정의하는 부분인데 사용자가 입력한 데이터나 사용자에게 출력할 데이터를 다룹니다
뷰는 사용자에게 시각적으로 보여지는 부분을 담당하고 컨트롤러는 사용자로부터 받은 데이터를 모델에 넘겨주거나
모델로 부터 받은 데이터를 뷰에 넘겨주는 역할을 합니다
역할을 분리해서 개발을 하다 보니 확장성이나 유연성이 증가하는 효과를 가질 수 있습니다
</div>
</details>

<details>
<summary>Spring Security의 구조와 JWT 발급 과정에 대해 설명해주실 수 있을까요?</summary>
<div markdown="1">
// 추후 내용 더 추가예정
</div>
</details>

<details>
<summary>Spring bean container 생성부터 스프링 종료까지의 사이클에 대해 알려주실 수 있을까요? @PostConstruct, @PreDestroy 어노테이션의 역할도 함께 알려주시면 좋습니다</summary>
<div markdown="1">
가장 먼저 스프링 컨테이너 생성이 되고 컴포넌트 스캔을 통해 스프링 빈이 생성되어 컨테이너에 싱글톤으로 관리됩니다
이후 코드에 작성된 의존 관계를 토대로 스프링 컨테이너에서 의존성 주입을 진행합니다
이 과정들이 완료되면 초기화 콜백이 동작하게 됩니다
똑같이 종료 직전에도 소멸 콜백이 동작하고 스프링이 종료하게 됩니다

@PostContruct는 객체 생성 후 별도의 초기화 작업을 위해 실행하는 메서드 위에 선언합니다
@PreDestroy는 스프링 컨테이너에서 스프링 빈(객체)을 제거하기 전에 해야할 작업이 있을 때 메서드 위에 선언합니다

@PostConstruct와 @PreDestroy로 초기화 콜백과 소멸 콜백을 동작시킬 수 있습니다. 최신 스프링에서 가장 권장하는 방법입니다. 또한 스프링 종속적인 기술이 아니라 자바 표준이기에 다른 컨테이너에서도 동작하고 컴포넌트 스캔과 잘 어울린다는 장점이 있습니다
</div>
</details>

<details>
<summary>AOP, Interceptor, Filter 의 차이점, Request가 들어올때 거치는 순서, 각 역할들의 장점을 설명해주실 수 있을까요?</summary>
<div markdown="1">
요청에 따른 실행 순서는 Filter → Interceptor → AOP → Interceptor → Filter 순으로 진행됩니다

Filter(필터)는 말그대로 요청과 응답을 거른뒤 정제하는 역할을 합니다
서블릿 필터는 DispatcherServlet 이전에 실행이 되는데 필터가 동작하도록 지정된 자원의 앞단에서 요청내용을 변경하거나, 
여러가지 체크를 수행할 수 있습니다
Interceptor(인터셉터)는 요청에 대한 작업 전/후로 가로챈다고 보면 됩니다
필터는 스프링 컨텍스트 외부에 존재하여 스프링과 무관한 자원에 대해 동작합니다
하지만 인터셉터는 스프링의 DistpatcherServlet이 컨트롤러를 호출하기 전, 후로 끼어들기 때문에 스프링 컨텍스트(Context, 영역) 내부에서 Controller(Handler)에 관한 요청과 응답에 대해 처리합니다 
AOP는 Interceptor나 Filter와는 달리 메소드 전후의 지점에 자유롭게 설정이 가능합니다
Interceptor와 Filter는 주소로 대상을 구분해서 걸러내야하는 반면
AOP는 주소, 파라미터, 애노테이션 등 다양한 방법으로 대상을 지정할 수 있기에
로깅, 에러처리와 같이 비즈니스 로직에서 세밀한 조정이 필요할 때 주로 사용합니다
</div>
</details>

<details>
<summary>필터와 인터셉터 차이가 무엇인가요?</summary>
<div markdown="1">

</div>
</details>

<br>

## 데이터베이스
<details>
<summary>인덱스란 무엇이고 일반적인 원리는 어떠한지 설명해주실 수 있을까요?</summary>
<div markdown="1">
데이터베이스 테이블에 대한 검색 성능의 속도를 높여주는 자료구조입니다
특정 컬럼에 인덱스를 생성하면 해당 컬럼의 데이터들을 정렬하여 별도의 메모리 공간에
데이터의 물리적 주소와 함께 저장을 합니다 이렇게 인덱스를 생성해놨다면
앞으로 쿼리문에 where 조건을 주면 옵티마이저가 판단해서 생성된 인덱스에 접근하게됩니다
인덱스에 접근하게되면 인덱스에 저장되어있는 데이터의 물리적 주소로 가서 데이터를 가져오는
방식으로 검색 속도의 향상을 시킬 수 있는 원리입니다
</div>
</details>

<details>
<summary>모든 요소에 인덱스를 걸지 않는 이유는 무엇일까요?</summary>
<div markdown="1">
인덱스를 항상 정렬된 상태로 유지해야 하기 때문에 추가, 수정, 삭제 와 같은 작업 수행시 추가작업이 필요해 집니다
그래서 데이터 검색이 빨라지는 대신 데이터에 한 추가, 수정, 삭제에 대한 연산 속도는 오히려 느려지게 되고
인덱스 관리를 위한 별도의 저장공간을 추가로 필요해 오히려 독이 될 수 있어 모든 요소에 인덱스를 걸지 않습니다
</div>
</details>

<details>
<summary>복합 인덱스란 무엇인지 원리를 설명해주실 수 있을까요?</summary>
<div markdown="1">
복합 인덱스란 두 개 이상의 컬럼을 합쳐서 인덱스를 만드는것을 말합니다
// 추후 내용 더 추가예정
</div>
</details>

<details>
<summary>트랜잭션이란 무엇이고 원자성, 일관성, 고립성, 지속성이란 무엇인지 설명해주실 수 있을까요?</summary>
<div markdown="1">
데이터베이스의 상태를 변환시키는 논리적 기능을 수행하기 위한 작업의 단위입니다
원자성은 트랜잭션의 연산은 데이터베이스에 모두 반영되거나 전혀 반영되지 않아야하는 특징입니다
일관성은 트랜잭션이 그 실행을 성공적으로 완료하면 언제나 일관성있는 데이터베이스 상태를 유지해야하는 특징입니다
고립성은 어느 하나의 트랜잭션이 실행중에 다른 트랜잭션의 연산이 끼어들 수 없다는 특징입니다
지속성은 성공적으로 완료된 트랜잭션의 결과는 영구적으로 반영되야 한다는 특징입니다
</div>
</details>

<details>
<summary>정규화란 무엇이고 대표적인 장점과 단점은 무엇이 있을까요?</summary>
<div markdown="1">
DB 테이블 간에 중복된 데이터를 허용하지 않아 무결성을 유지할 수 있게하는 처리를 말합니다
장점으로는 이상현상을 제거 할 수 있습니다
단점으로는 테이블 분해로 인해 조인 연산이 발생해 응답 시간이 느려질 수 있습니다
</div>
</details>

<details>
<summary>RDBMS, NoSQL, in memory 에대해</summary>
<div markdown="1">
RDBMS

- 관계형 데이터베이스입니다

- 예로 MySQL, Oracle, MSSQL, PostgreSQL이 있습니다

- 효율적, 안정적, 안전한 데이터 저장소입니다

- 대용량 데이터를 영구적으로 저장, 관리, 접근할 수 있습니다

- 테이블마다 스키마를 정의해야합니다

- SQL을 통해 요청을 처리합니다

- 성능을 높이려면 하드웨어를 높은 성능으로 교체해야 합니다

- 높은 성능의 하드웨어는 가격이 비싸 RDBMS의 성능을 높이거나 확장하는게 어렵습니다

NoSQL
- RDBMS의 확장성 문제를 해결하기 위해 나왔습니다

- 예로 MongoDB, Redis, hBase가 있습니다

- 비교적 저렴한 가격으로 성능을 높일 수 있습니다

- RDBMS처럼 여러 테이블을 사용하는게 아닌 큰 테이블 하나만을 사용합니다

- SQL 질의문을 사용하지 않습니다

- 구조 변경이 용이하고, 데이터 형식이 다양하며 바꾸기가 쉽습니다

- 정확성 보다 데이터 양이 중요해 빅데이터에 사용합니다

- 자주 변경되는 데이터를 저장하거나 다양한 유형의 데이터를 처리하는데 적합하다

In-memory database
- Key-value형의 NoSQL이다

- RAM에 모든 데이터를 보유하고 있는 데이터베이스이다

- DB 응답속도가 떨어지는 문제를 해결할 수 있는 대안이다

- 전형적인 디스크 방식은 쿼리를 수행하지만 in-memory는 메모리상에 색인을 넣어 필요한 모든 정보를 메모리상의 인덱스를 통해 빠르게 검색 가능하다

- 휘발성이라 DB 서버 전원이 갑자기 꺼지면 데이터들이 삭제된다

- 그래서 날아가도 되는 임시 데이터에 주로 쓰인다
</div>
</details>

<details>
<summary>DB를 사용하는 이유</summary>
<div markdown="1">
파일 단위로 저장할 때 데이터 종속성 문제와 중복성, 데이터 무결성 문제 떄문에
DB를 사용하여 무결성을 보장하고 프로그램으로 구현해야 했던 것들을
SQL 쿼리문으로 간단하게 수행이 가능해 지기 때문이다
</div>
</details>

<details>
<summary>이상현상이란?</summary>
<div markdown="1">
테이블내의 데이터들이 불필요하게 중복되어
테이블을 조작할 때 발생하는 데이터 불일치 현상입니다

이상현상에는 삽입이상, 삭제이상, 갱신이상이 있는데
삽입이상은 의도하지 않는 데이터가 같이 삽입되는 것이고
삭제이상은 의도와 다른 값들도 연쇄 삭제되는것을 뜻하고
갱신이상은 일부 튜플만 갱신되어 모순이 발생되는것을 뜻합니다 
</div>
</details>

<details>
<summary>Redis가 무엇인가요?</summary>
<div markdown="1">
<p>Redis는 REmote Dictionary Server의 약자로 오픈소스 DBMS입니다</p>
<p>NoSQL DBMS로 분류되며 In-Memory 기반의 Key-Value 구조를 가진 DBMS입니다</p>
</div>
</details>

<details>
<summary>캐싱이 무엇인가요?</summary>
<div markdown="1">
<p>캐시란 한번 조회된 데이터를 미리 특정 공간에 저장해 놓고</p>
<p>똑같은 요청이 발생하게 되면 서버에게 다시 요청하지 말고</p>
<p>저장해놓은 데이터를 제공해서 빠르게 서비스를 제공해주는것을 말합니다</p>
</div>
</details>

<details>
<summary>캐시미스, 캐시히트 가 무엇인가요?</summary>
<div markdown="1">
<p>캐시미스는 메모리에 찾고자 하는 데이터가 없어서 디스크에 조회 할때를 의미하고</p>
<p>캐시히트는 메모리에 찾고자 하는 데이터가 있을때를 의미합니다</p>
</div>
</details>

<details>
<summary>Redis의 작동원리 및 프로젝트에 왜 사용했는지?</summary>
<div markdown="1">
먼저 저희 프로젝트에서는 클라이언트 들에게 산을 추천해주는 태그라는 기능이 있는데
이 태그안의 산들은 모든 유저에게 중복되고 반복적으로 보여주어야하는 목록입니다
이때 같은 값을 계속해서 DB에서 불러와야하니 성능저하가 발생할것이라 판단해
캐싱을 이용해서 처리하고자 Redis를 사용하여 처리했습니다 동작 방식으로는
먼저 A라는 클라이언트가 태그를 누르면 먼저 Redis에 와서 캐싱된 내용이 있는지 확인 후 없다면 DB에 접근해서 쿼리를 이용해서 값을 가져오게되고 그 값을 Redis에 저장하고
클라이언트에 보여주게 됩니다
두번째로 B라는 클라이언트가 태그를 누르면 Redis에 와서 캐싱된 내용이 있으니
바로 클라이언트에게 보여지게 됩니다
이를 JMeter를 통해 확인한 결과 30%정도의 성능 개선을 경험 했습니다
</div>
</details>

<details>
<summary>Redis 와 Memcached의 차이와 왜 Redis를 썼는지에 대해서 설명해주세요</summary>
<div markdown="1">
Memcached와 Redis 둘다 key-value 를 기반으로 둔 NoSQL 입니다
하지만 Memcached의 대부분의 기능을 Redis로도 커버가 가능하고
Redis는 list, hash, set 등 다양한 자료구조를 제공하여
데이터 조작에 편리성이 있습니다 이러한 이유로 Redis를 사용하였습니다
</div>
</details>

<details>
<summary>왜 RDB를 썼나요?</summary>
<div markdown="1">
<p>저희 프로젝트에서는 각 요소별로 연관관계를 맺어줘야하는 상황이 많이 있어
RDB가 더 맞다고 판단해서 사용하였습니다</p>
</div>
</details>

<details>
<summary>NoSQL은 언제 쓰나요?</summary>
<div markdown="1">
스키마에 구애받을 필요가 없어 데이터를 편하게 밀어 넣어두고 쓰기 편해
중간 분석 데이터나 최종적으로 사용할 데이터를 넣어두는 용도로 많이 사용합니다
</div>
</details>

<details>
<summary>MySQL을 왜썼나요? 다른 선택지는 없었나요?</summary>
<div markdown="1">
비교적 설치와 관리가 쉽고 안정성을 가지고 있으며 레퍼런스가 많았습니다
또한 저희가 진행하는 작은 프로젝트 단위에 더 적합하다 생각했습니다
</div>
</details>

<details>
<summary>MySQL과 postgreSQL 차이</summary>
<div markdown="1">
MySQL은 설치와 관리과 비교적 쉽고, 빠르며 안정성을 가진 데이터베이스입니다
postgreSQL은 복잡한 쿼리와 대규모 데이터베이스를 다룰 수 있는 기능이 풍부한 데이터베이스입니다
</div>
</details>

<details>
<summary>커밋, 롤백 이 무엇인가요?</summary>
<div markdown="1">
커밋 : 모든 작업을 정상적으로 처리하겠다고 확정하는 연산 입니다
롤백 : 트랜잭션 과정 중 문제가 생겼을때 처리를 시작하기 이전 상태로 되돌리는 연산 입니다
</div>
</details>

<details>
<summary>수직적 확장, 수평적 확장이 무엇인가요?</summary>
<div markdown="1">
<p>수직적 확장이란 단순히 데이터베이스의 성능을 업그레이드 시키는것입니다</p>
<p>수평적 확장이란 더 많은 서버가 추가되고 데이터베이스가 전체적으로
분산되는것을 의미합니다</p>
</div>
</details>

<br>

## JPA
<details>
<summary>JPA란 무엇인가요?</summary>
<div markdown="1">
<p>JPA는 자바 진영의 ORM 기술 표준으로 사용되는 인터페이스 모음입니다</p>
<p>DB와 객체지향 개발을 연결해주어
두 분야의 개발이 독립적으로 이루어 질 수 있게</p>
<p>해주는 역할을 하며 쿼리를 직접 작성하지 않아도 되어
유지보수와 생산성을 높일 수 있습니다</p>
<p>따라서 객체 중심적인 개발을 할때 사용합니다</p>
</div>
</details>

<details>
<summary>JPA의 장점/단점</summary>
<div markdown="1">
<p>객체 모델을 이용하여 비즈니스 로직을 구성하는데만 집중이 가능합니다</p>
<p>쿼리를 직접 작성하지 않아서 생산성과 유지보수성이 올라가고</p>
<p>특정 데이터베이스에 종속되지 않다는 장점이 있습니다</p>
<p>단점으로는 개발자가 의도하지 않은 자동으로 생성된 쿼리로 인해</p>
<p>성능이 저하될 수 있고 복잡한 상황에서는 직접 쿼리를 쓰는게</p>
<p>나을 수 있는것이 단점이라고 볼 수 있습니다</p>
</div>
</details>

<details>
<summary>영속성 컨텍스트란 무엇인가요?</summary>
<div markdown="1">
<p>엔티티를 영구 저장하는 환경이라는 뜻입니다</p>
<p>애플리케이션과 데이터베이스 사이에서
객체를 보관하는 가상의 데이터베이스 같은 역할을 합니다</p>
<p>엔티티 매니저를 통해 엔티티를 저장하거나 조회하면</p>
<p>엔티티 매니저는 영속성 컨텍스트에 엔티티를 보관하고 관리합니다</p>
</div>
</details>

<details>
<summary>플러시는 무엇인가요?</summary>
<div markdown="1">
<p>영속성 컨텍스트의 변경 내용을 데이터베이스에 반영하는것 입니다</p>
<p>영속성 컨텍스트의 엔티티를 지우는 것이 아니라</p>
<p>변경 내용을 데이터베이스에 동기화 하는 것입니다</p>
</div>
</details>

<details>
<summary>Hibernate는 무엇인가요?</summary>
<div markdown="1">
<p>JPA 구현체의 한 종류입니다</p>
<p>JPA가 DB와 자바 객체를 매핑하기 위한 인터페이스이고</p>
<p>Hibernate는 이를 구현한 라이브러리입니다</p>
</div>
</details>

<details>
<summary>Spring Data JPA는 무엇인가요?</summary>
<div markdown="1">
<p>JPA를 편하게 쓰기 위한 모듈입니다</p>
<p>엔티티매니저가 아닌 레포지토리를 정의하여 사용합니다</p>
<p>물론 레포지토리 내부적으로는 엔티티매니저를 사용합니다</p>
</div>
</details>

<details>
<summary>JPA는 언제 필요하고 언제 필요하지 않은지 설명해주실 수 있을까요?</summary>
<div markdown="1">
JPA는 자바 진영의 ORM 기술 표준으로 DB와 객체지향 개발을 연결해주어 두 분야의 개발이 독립적으로 이루어질 수 있게 해줍니다
이로 인해 쿼리를 직접 작성하지 않아도 되어 유지 보수와 생산성을 높일 수 있습니다
하지만 복잡한 조회가 필요한 상황에는 JPA보다는 쿼리를 직접 작성하는 것이 적합하여 필요하지 않습니다
</div>
</details>

<details>
<summary>ORM이란 무엇인가요?</summary>
<div markdown="1">
<p>객체와 관계형 데이터베이스의 데이터를 자동으로 매핑(연결)해주는 것을 말합니다</p>
<p>이를 이용해 패러다임 불일치를 개발자 대신 해결해줍니다</p>
</div>
</details>

<details>
<summary>JPA의 더티 체킹이란 무엇인가요?</summary>
<div markdown="1">
jpa에서 트랜잭션이 끝나는 시점에 변화가 있는 모든 엔티티 객체를 DB에 자동 반영 시켜주는 것을 말합니다
원리를 살펴보자면 jpa에서 엔티티를 최초 조회한 상태를 스냅샷으로 만들어두게 되고
트랜잭션이 끝나는 시점에 이 스냅샷과 비교해서 다른점이 있다면 update query를 DB로 전달합니다
이는 영속성 컨텍스트가 관리하는 엔티티에만 적용된다는 점도 유의해야 합니다
</div>
</details>

<details>
<summary>N+1 문제의 발생 이유와 해결 방법에 대해 설명해주실 수 있을까요? 해결 방법은 3가지 이상 말씀해주시면 좋습니다</summary>
<div markdown="1">
연관 관계에서 발생하는 이슈로 연관관계가 설정된 엔티티를 조회할 때 조회한 갯수보다 쿼리가 더 나오는 것이다
JPA가 JPQL을 분석해서 SQL을 생성할 때는 글로벌 fetch 전략을 참고하지 않고 오직 JPQL자체만을 사용하고
지연로딩을 해도 하위 엔티티를 가지고 작업하면 추가 조회가 발생합니다
이를 해결하기 위해 fetch join을 이용해 DB에서 데이터를 가져올 때 처음부터 연관된 데이터까지 가져오게 하는 방법이 있습니다
그러면 SQL문으로 inner join 구문으로 변경되어 실행합니다
또는 EntityGraph 어노테이션을 사용하거나 Batch Size를 1000으로 설정해 in 절로 쿼리를 발생시키는 방법이 있습니다
</div>
</details>

<details>
<summary>즉시로딩과 지연로딩은 각각 언제 사용하면 좋은지 설명해주실 수 있을까요?</summary>
<div markdown="1">
즉시로딩의 경우 참조객체와 항상 함께 불러오면 좋은 엔티티에 적용하면 좋습니다
예를들어 게시글과 작성자를 보면 게시글을 불러올때 항상 저자의 이름을 불러와야하기에 적합합니다

지연로딩의 경우 참조객체가 존재하지만 필요한 시점에만 사용하고 싶을때 사용한다고 볼 수 있습니다
</div>
</details>

<details>
<summary> </summary>
<div markdown="1">

</div>
</details>

<br>

## 운영체제
<details>
<summary>프로세스와 스레드를 비교하여 설명해주실 수 있을까요?</summary>
<div markdown="1">
프로세스는 컴퓨터 메모리(Ram)에 적재되고 CPU 자원을 할당받아 프로그램이 실행되고 있는 상태를 말합니다
스레드는 프로세스 내에서 실행되는 흐름의 단위라고 볼 수 있습니다
</div>
</details>

<details>
<summary>동기와 비동기를 비교하여 설명해주실 수 있을까요?</summary>
<div markdown="1">
동기는 동시에 일어난다를 의미합니다 요청과 요청에 대한 결과가 동시에 일어난다는 것을 뜻합니다
예시로 은행이 있는데 A라는 계좌에서 송금을 했을때 B라는 계좌에서 받았다는 응답을 해줘야
A계좌에서 돈을 마이너스하고 B계좌에 플러스 할 수 있어 이런 상황을 동기식(블록 상태)이라 표현합니다

비동기는 동시에 일어나지 않는다를 의미합니다 요청과 요청에 대한 결과가 따로 일어난다는 것을 뜻합니다
예시로 시험날이 있는데 학생이 문제를 풀고 제출을하고 선생님은 받아서 체점을하고 결과를 보냅니다
이때 학생은 시험지가 돌아오기를 기다리고 있을 필요없이 집에가도 되고 선생님은 내일 채점해도 되고 이렇게 
서로 작업이 분리되어 있기에 처리하는 시간이 일치하지 않아도 되는 이런 상황을 비동기식(논블럭 상태)이라 표현합니다
</div>
</details>

<details>
<summary>동시성과 병렬성을 비교하여 설명해주실 수 있을까요?</summary>
<div markdown="1">
동시성은 하나의 프로세스에 멀티 스레드를 이용해서 여러 작업이 동시에 실행되고 있는 것처럼 구현되는 것입니다
예를들어 커피 추출구가 하나인 커피머신이 여러 종류 커피의 재료를 바꿔가며 동시에 만드는것으로 볼 수 있습니다

병령성은 멀티프로세스를 이용해서 여러 작업이 실제로 동시에 실행되는 것입니다
예를들어 커피 추출구가 여러개인 커피머신이 여러 종류 커피를 각각의 재료를 이용해 동시에 만드는것으로 볼 수 있습니다
</div>
</details>

<details>
<summary>싱글스레드와 멀티스레드가 무엇인가요?</summary>
<div markdown="1">

</div>
</details>

<br>

## 네트워크
<details>
<summary>HTTP에 비해 HTTPS가 더 안전한 원리를 설명해주실 수 있을까요?</summary>
<div markdown="1">
HTTP를 SSL 프로토콜 위에서 돌아가도록 하여 클라이언트와 서버가 주고받는 데이터를 암호화 하기에 더 안전하다고 할 수 있는데 원리를 알아 보자면
1) 서버가 공개키와 개인키를 생성하고 서버 내 사이트의 각종 정보와 자신의 공개키를 인증기관에 전달해 SSL 인증서 생성을 요청합니다
2) 인증기관에서 인증기관의 개인키로 암호화해서 사이트에 해당하는 SSL 인증서를 생성해 사이트로 발급해줍니다
3) 서버는 인증기관의 개인키로 암호화된 SSL 인증서를 클라이언트에게 전달합니다
4) 클라이언트는 인증기관에서 공개중인 공개키를 가져와 SSL 인증서를 복화해서 확인하고 서버의 공개키를 얻습니다
5) 얻은 서버의 공개키로 대칭키를 암호화해서 서버에 전송하고 서버는 개인키로 복호화해서 대칭키를 얻습니다
6) 이로써 클라이언트와 서버는 대칭키를 이용해서 암호문을 주고 받습니다
</div>
</details>

<details>
<summary>TCP 3 way handshake란 무엇인지 설명해주실 수 있을까요?</summary>
<div markdown="1">
OSI 7계층증 4계층인 전송계층에서  서버와 클라이언트를 연결하는데 필요한 프로세스 이고
연결지향적인 특성을 갖게 해주는 과정을 뜻합니다
데이터를 주고받기 전에 서버와 클라이언트가 확인 패킷을 3단계로 교환하여 연결을 맺습니다
</div>
</details>

<details>
<summary>TCP 와 UDP 를 비교하여 설명해주실 수 있을까요?</summary>
<div markdown="1">
먼저 TCP는 인터넷상에서 데이터를 메세지의 형태로 보내기 위해 IP와 함께 사용하는 프로토콜입니다
IP가 데이터의 배달을 하면 TCP는 패킷을 추적 및 관리 합니다
TCP는 연결형 서비스로 신뢰성을 보장하기에 파일전송 같은 신뢰성있는 전송이 필요할 때 사용됩니다

UDP는 데이터를 데이터그램 단위로 처리하는 프로토콜 입니다
UDP는 비연결형 서비스로 신뢰성이 없기에 실시간 서비스 같은 신뢰성보다 연속성이 중요한 서비스에 사용됩니다
</div>
</details>

<details>
<summary>HTTP란 무엇인가요?</summary>
<div markdown="1">

</div>
</details>

<br>

## 자료구조/알고리즘
<details>
<summary>배열, 링크드리스트를 비교하여 설명해주실 수 있을까요?</summary>
<div markdown="1">
배열은 인덱스를 사용하여 값에 바로 접근할 수 있습니다
값을 삽입하거나 삭제하려면 해당 인덱스 주변에 있는 값을 이동 시키는 과정이 필요해 삽입과 삭제가 어렵습니다
배열의 크기는 지정할 수 있는데 한 번 선언하면 크기를 늘리거나 줄일 수 없습니다

리스트는 인덱스가 없어 값에 접근하려면 Head 포인터 부터 순서대로 접근해야 해서 값에 접근하는 속도가 느립니다
포인터로 연결되어 있어 데이터를 삽입하거나 삭제하는 속도가 빠릅니다
리스트의 크기는 정해져 있지 않으며 크기가 변하기 쉬운 데이터를 다룰 때 적절합니다
포인터를 저장할 공간이 필요하므로 배열보다 구조가 복잡합니다
</div>
</details>

<details>
<summary>시간복잡도와 공간복잡도가 무엇인지 설명해주실 수 있을까요?</summary>
<div markdown="1">
시간복잡도는 특정 알고리즘이 어떤 문제를 해결하는데 걸리는 시간을 의미합니다

공간복잡도는 작성한 프로그램이 얼마나 많은 메모리를 차지 하느냐를 분석하는 방법입니다
</div>
</details>

<details>
<summary>스택, 큐에 대해 설명해주실 수 있을까요?</summary>
<div markdown="1">
스택은 책상에 책을 쌓는 것처럼 차곡차곡 쌓아 올린 형태를 가진 자료구조입니다
책이 쌓인 것을 상상해보면 알겠지만 정해진 방향으로만 삽입, 삭제를 할 수 있습니다
LIFO 방식으로 가장 마지막에 삽입된 데이터가 가장 먼저 삭제된다는 특징을 가집니다

큐는 길게 줄을 서서 기다리는 사람들의 형태를 가진 자료구조입니다
줄을 서있는 모습을 상상해보면 알겠지만 한쪽 방향에서만 삽입 한쪽 방향에서만 삭제를 할 수 있습니다
FIFO 방식으로 가장 먼저 삽입된 데이터가 가장 먼저 삭제된다는 특징을 가집니다

스택의 실제 활용예시는 웹브라우저 뒤로가기 버튼이 있습니다

큐의 실제 활용예시는 프린트 출력인데 가장 먼저 인쇄를 눌러 대기열에 오른 프린트가 먼저 출력한다는걸 들을 수 있습니다
</div>
</details>

<details>
<summary>이분탐색이 무엇이고 시간복잡도는 어떻게 되며 그 이유는 무엇인가요?</summary>
<div markdown="1">
이분탐색이란 정렬된 리스트에서 탐색 범위를 절반씩 줄여가며 값의 위치를 찾는 알고리즘입니다
// 추후 내용 더 추가예정
</div>
</details>

<details>
<summary>트리, 그래프를 비교하여 설명해주실 수 있을까요?</summary>
<div markdown="1">
트리는 그래프에 포함되며 둘 다 노드와 노드간 연결하는 간선으로 구성된 자료구조 입니다
먼저 트리는 두 개의 노드 사이에 반드시 1개의 경로만을 가지며 사이클이 존재하지 않는 방향 그래프입니다
루트와 부모 노드를 가지는 특징이 있으며 회사의 조직도가 트리의 대표적인 예시라고 할 수 있습니다
그래프는 노드 사이에 둘 이상의 경로가 가능하며 순환, 비순환 사이클이 존재하며 방향, 무방향 둘 다 가능합니다
루트나 부모-자식 개념이 없으며 지하철 노선도가 그래프의 대표적인 예시라고 할 수 있습니다
</div>
</details>

<details>
<summary>포트폴리오에서 시간복잡도를 낮춘 사례가 있다면 설명해주실 수 있을까요?</summary>
<div markdown="1">
// 추후 내용 더 추가예정
</div>
</details>

<details>
<summary> </summary>
<div markdown="1">

</div>
</details>

<br>

## 보안/암호
<details>
<summary>CORS란 무엇이고 어떻게 허용할 수 있나요?</summary>
<div markdown="1">
출처가 다른 자원들을 공유할 수 있도록 해주는 보안 정책입니다
예를 들어 프론트엔드에서 백엔드 자원에 접근할 수 있게 허용해주는 개념이고
허용해주는 방법은 클라이언트의 요청하면 서버는 Access-Control-Allow-Origin 헤더에
요청 출처를 담아 응답하거나 * 로 설정해 응답하면 됩니다
</div>
</details>

<details>
<summary>사용자 패스워드를 전송하고 보관하는 방법을 설명해주실 수 있을까요?</summary>
<div markdown="1">
해시 함수를 이용해서 패스워드를 해싱처리를 하는데 이때 암호화된 패스워드를 다이제스트라고 합니다
하지만 다이제스트는 원문에 대해 항상 같은 값을 얻기 때문에 해커들에게 금방 해킹될 위험이 있습니다
이를 보완하고자 해시함수를 여러 번 수행하거나 솔트라는 기법을 이용해 원문에 임의의 문자열을 덧붙여서
DB에 보관할 수 있습니다
</div>
</details>

<details>
<summary>Base64 인코딩이란 무엇인가요?</summary>
<div markdown="1">
바이너리 데이터를 ASCII 문자로 이루어진 텍스트로 변경하는 인코딩 이라고 할 수 있습니다
바이너리 데이터가 정확히는 8비트 로 이루어져있는데 base64 즉 문자 64개로 모든 문자열을 표현하고자 하면
2에 6승 해서 6비트가 필요합니다 그래서 8비트와 6비트의 최소 공배수인 24비트씩 끊어서 인코딩합니다
</div>
</details>

<details>
<summary>JWT에 대해 설명해주실 수 있을까요? 구체적으로 JWT를 어디서 처리하는지, 어떠한 방식으로 검증하는지, 재발급 방식과 주기는 어떻게 처리하는지, 다른 API 서비스 호출 시 어떻게 잡아서 인증 처리하는지 말씀해주시면 좋습니다</summary>
<div markdown="1">
Json 포맷을 이용하여 사용자에 대한 속성을 저장하는 Claim 기반의 Web Token입니다
Header 에는 토큰 타입과 해시 알고리즘의 종류가 담겨있으며
Payload에는 사용자 권한 정보와 데이터 조각 Claim이 담겨 있습니다
Signature 에는 헤더, 페이로드를 Base64 URL-safe 인코드를 한 이후 헤더에 명시된 해시함수를 적용하고
개인키(Private Key)로 서명한 전자서명이 담겨있습니다
로그인 요청 시 access, refresh 토큰을 발급하여 클라이언트에 전달합니다
클라이언트는 서버로부터 받은 JWT를 로컬 스토리지에 저장하며 API를 서버에 요청할때 Authorization 헤더에 Access Token을 담아서 보냅니다
이 때 서버는 클라이언트가 Header에 담아서 보낸 JWT가 내 서버에서 발행한 토큰인지 일치 여부를 확인합니다
만일 access 토큰의 시간이 만료되면 클라이언트는 refresh token을 이용해 access토큰을 재발급 해줍니다
</div>
</details>

<details>
<summary>쿠키가 무엇인가요?</summary>
<div markdown="1">
<p>key-value 형식의 문자열 덩어리이다</p>
<p>클라이언트가 웹사이트 방문시 그 사이트가 사용하고 있는 서버를 통해</p>
<p>클라이언트의 브라우저에 설치되는 작은 기록 정보 파일이다</p>
<p>1) 브라우저(클라이언트)가 서버에 요청(접속)을 보낸다</p>
<p>2) 서버는 요청에대한 응답을 작성할 때 클라이언트 측에 저장하고 싶은 정보를
응답 헤더의 set-cookie에 담는다</p>
<p>3) 이후 클라이언트가 요청을 보낼때 마다 매번 저장된 쿠키를 요청헤더의 cookie에 담아 보낸다
서버는 쿠키에 담긴 정보를 바탕으로 해당 요청의 클라이언트가 누군지 식별한다</p>
<p>단점</p>
<p>보안에 취약하다</p>
<p>용량 제한이 있어 많은 정보를 못담는다</p>
<p>브라우저간 공유가 불가능하다</p>
</div>
</details>

<details>
<summary>세션이 무엇인가요?</summary>
<div markdown="1">
<p>쿠키의 보안 이슈나 민감한 인증 정보를 브라우저가 아닌 서버측에 저장하고 관리한다</p>
<p>서버의 메모리에 저장하기도 하고 서버의 로컬 파일이나 DB에 저장하기도 한다</p>
<p>핵심은 클라이언트에게 보내지말고 서버에서 관리한다는것이다</p>
<p>1) 유저가 웹사이트에서 로그인하면 세션이 서버 메모리(혹은 DB) 상에 저장된다
이때 세션을 식별하기 위해 session id를 기준으로 정보를 저장한다</p>
<p>2) 서버에서 브라우저에 쿠키에다가 session id를 저장한다</p>
<p>3) 브라우저는 해당 사이트에 대한 모든 request에 session id를 쿠키에 담아 전송한다</p>
<p>4) 서버는 클라이언트가 보낸 session id와 관리중인 session id를 비교해 인증해준다</p>
<p>단점</p>
<p>해커가 session id 자체를 탈취하여 클라이언트인척 위장하면 한계가 있다</p>
<p>요청이 많아지면 서버에 부하가 심해진다</p>
</div>
</details>

<details>
<summary>토큰이 무엇인가요?</summary>
<div markdown="1">
<p>클라이언트가 서버에 접속하면 서버에서 인증되었다는 의미로 토큰을 부여한다</p>
<p>이 토큰은 유일해서 클라이언트가 또 다시 서버에 요청을 보낼때 요청 헤더에 심어 보낸다</p>
<p>그럼 서버는 클라이언트로 부터 받은 토큰을 서버에서 제공한 토큰과 일치 여부를 체크해서
인증과정을 처리하게 된다</p>
<p>기존 세션은 DB에 세션정보를 가지고 있어야하고 이를 조회하는 과정이 필요해 부하가 심해지는데</p>
<p>토큰은 세션과 달리 서버가 아닌 클라이언트에 저장되기 때문에 서버 부담이 줄어든다</p>
<p>토큰은 앱과 서버가 통신할때 많이 쓰인다</p>
<p>왜냐하면 웹에는 쿠키와 세션이 있지만 앱에는 없기 때문이다</p>
<p>1) 사용자가 아이디 비밀번호로 로그인 한다</p>
<p>2) 서버측에서 사용자에게 유일한 토큰을 발급한다</p>
<p>3) 사용자는 서버측에서 받은 토큰을 쿠키나 스토리지에 저장해두고
서버에 요청을 할 때마다 해당 토큰을 http 요청 헤더에 포함시켜 전달한다</p>
<p>4) 서버는 전달받은 토큰을 검증하고 요청에 응답한다
토큰에는 요청한 사람의 정보가 담겨있어 서버는 DB를 조회하지 않고 누가 요청하는지 안다</p>
<p>단점</p>
<p>payload 자체는 암호화 되지 않기 때문에 유저의 중요한 정보는 담을 수 없다</p>
<p>토큰을 탈취당하면 대처하기 어렵다</p>
</div>
</details>

<details>
<summary>JWT가 무엇인가요?</summary>
<div markdown="1">
<p>JWT는 JSON Web Token 이라는 인증에 필요한 정보들을 암호화시킨 JSON 토큰을 의미한다</p>
<p>JWT 기반 인증은 JWT 토큰을 HTTP 헤더에 실어 서버가 클라이언트를 식벽하는 방식이다</p>
<p>JSON 데이터를 Base64를 통해 인코딩하여 직렬화 한것이다</p>
<p>토큰 내부에는 위 변조 방지를 위해 개인키를 통한 전자서명도 들어있다</p>
<p>1) 사용자가 ID, PW를 입력하여 서버에 로그인 인증을 요청한다</p>
<p>2) 서버에서 클라이언트로부터 인증 요청을 받으면 header, payload, signature를 정의한다
각각 base64로 한 번 더 암호화하여 JWT를 생성하고 쿠키에 담아 클라이언트에게 발급한다</p>
<p>3) 클라이언트는 받는 JWT를 로컬 스토리지에 저장한다 (쿠키에 해도됨)
API를 서버에 요청할 때 Authorization header에 Access Token을 담아 보낸다</p>
<p>4) 서버는 header에 담아서 보낸 JWT가 내 서버에서 발행한 토큰인지 일치 여부를 확인한다
일치하면 인증 아니면 통과안해준다
인증이 되었으면 payload에 들어있는 유저의 정보들을 select해서 클라이언트에게 준다</p>
<p>5) 만약 클라이언트가 요청했는데 엑세스토큰이 만료되면 리프래시 토큰으로 재발급 받는다</p>
<p>토큰의 진짜 목적은 정보 보호가 아닌 위조 방지이다</p>
<p>장점</p>
<p>데이터 위변조를 막을 수 있다</p>
<p>별도의 저장소가 필요없다</p>
<p>OAuth의 경우 소셜계정을 이용하여 다른 웹서비스에서도 로그인을 할 수 있다</p>
<p>모바일 환경에서도 잘 동작한다</p>
<p>단점</p>
<p>토큰 자체에 정보를 담고 있어 양날의 검이다</p>
<p>patload 자체는 암호화 된 것이 아니라 탈취하여 디코딩하면 데이터를 볼 수 있다</p>
</div>
</details>

<br>

## 기타
<details>
<summary>Call by reference란 무엇이고 보통 어떻게 쓰이나요?</summary>
<div markdown="1">
참조에 의한 호출로서 값을 전달하는 대신 주소 값을 전달하는 방식을 의미합니다
보통 swap하는 상황에서 쓰이는데 자바로 예를 들자면 stack 영역에서 변수의 값을 아무리 바꿔도
기존 변수에 변화를 주지 못하지만 객체의 value값을 가리키고 즉 주소를 가리킨 상태에서 값을 바꾸면
기존 변수에 변화를 줄 수 있어 이렇게 사용한다고 말씀드릴 수 있습니다
</div>
</details>

<details>
<summary>웹 통신의 큰 흐름 https://www.google.com/ 을 접속할 때 일어나는 일</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>restful API란 무엇인가요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>에자일이란 무엇인가요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>MSA 아키텍처에 대해 아는데로 설명하시오</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>CI / CD란 무엇인가요?</summary>
<div markdown="1">
<p>CI는 지속적인 통합이라고 해서 개발자가 동시에 코드 작업을 할때</p>
<p>변경된 내용이 정기적으로 빌드 및 테스트를 거쳐 공유 레포지토리에 병합되는 것을 뜻합니다</p>
<p>CD는 지속적인 배포라고 해서 CI를 통해 빌드된 결과물을 프로덕션으로 배포하는 작업을 자동화 하는 것입니다</p>
</div>
</details>

<details>
<summary>CI / CD 툴은 어떤걸 사용했나요? 왜 사용했나요? 다른 대안은 없었나요?</summary>
<div markdown="1">
<p>깃허브 액션을 사용했습니다</p>
<p>젠킨스나 트레비스 씨아이와 같은 다른 툴들도 있었지만</p>
<p>깃허브와 바로 연동할 수 있고 상대적으로 설정도 간편하며</p>
<p>저희 프로젝와같이 작은 규모일때 조금 더 맞다고 판단해서 깃허브 액션을 이용했습니다</p>
</div>
</details>

<details>
<summary>swap 메모리란 무엇인가요?</summary>
<div markdown="1">
<p>스왑메모리는 메모리가 부족할 경우 하드디스크의 일부 공간을 활용하여
작업을 도와주는 공간을 의미합니다</p>
<p>하드디스크 일부를 사용하다보니 RAM처럼 빠르지는 않지만
실제 메모리보다 더 많은 공간을 사용할 수 있습니다</p>
</div>
</details>

<details>
<summary>어떤 배포 방식을 사용했고 왜 사용했나요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>다운타임은 무엇인가요?</summary>
<div markdown="1">
<p>버전1이 8081 포트에서 돌아가고 있는 중에</p>
<p>버전2를 만들어 8081 포트에 올려 돌리려하면</p>
<p>기존의 버전1 프로세스를 종료해야합니다</p>
<p>이때 버전1이 종료되고 버전2가 실행되는 그 사이</p>
<p>즉 유저가 서비스를 이용할 수 없는 시간을 뜻합니다</p>
</div>
</details>

# 인성면접 관련질문
<details>
<summary>1분 자기소개를 해보세요</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>개발자로서 본인의 장단점과 근거가 되는 경험을 말씀해주실 수 있을까요?(협업 능력 제외)</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>개발자가 되기로 한 이유에 대해 말씀해주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>가장 인상 깊게 읽었던 책과 그 이유에 대해 알려주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>즐겨 보는 테크 유튜버나 뉴스레터가 있다면 알려주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>삶에서 중요하게 생각하는 가치가 있다면 무엇인가요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>최근에 본 기술 아티클에 대해 설명해주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>즐겁고 행복했던 경험을 하나 이야기해주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>힘들고 쉽지 않았지만 극복한 경험을 하나 이야기해주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>우리 회사에 지원한 동기를 말씀해주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>앞으로 3개월, 6개월, 1년 동안 어떤 것을 공부할 계획인지, 그리고 그러한 계획을 세운 이유는 무엇인지 알려주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary>재미있게 공부한 알고리즘이 있다면 설명해주실 수 있을까요?</summary>
<div markdown="1">

</div>
</details>

<details>
<summary> </summary>
<div markdown="1">

</div>
</details>
