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
<summary> </summary>
<div markdown="1">

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
<summary> </summary>
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
<summary> </summary>
<div markdown="1">

</div>
</details>

<br>

## JPA
<details>
<summary>JPA는 언제 필요하고 언제 필요하지 않은지 설명해주실 수 있을까요?</summary>
<div markdown="1">
JPA는 자바 진영의 ORM 기술 표준으로 DB와 객체지향 개발을 연결해주어 두 분야의 개발이 독립적으로 이루어질 수 있게 해줍니다
이로 인해 쿼리를 직접 작성하지 않아도 되어 유지 보수와 생산성을 높일 수 있습니다
하지만 복잡한 조회가 필요한 상황에는 JPA보다는 쿼리를 직접 작성하는 것이 적합하여 필요하지 않습니다
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
<summary> </summary>
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
<summary> </summary>
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
<summary> </summary>
<div markdown="1">

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
<summary> </summary>
<div markdown="1">

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
