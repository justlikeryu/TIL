# JVM(Java Virtual Machine)
> 자바로 작성된 프로그램을 플랫폼에 구애받지 않고 실행할 수 있게 하는 가상 컴퓨터

## JVM 동작 프로세스
<img src="https://github.com/justlikeryu/TIL/assets/111476710/a64bc797-7291-4cad-8f42-3fdb8bc77ea4">

1. 자바 프로그램 실행
2. OS의 가상 머신 프로세스(JVM) 구동
3. 자바 컴파일러가 자바 소스 코드(.java)를 자바 바이트 코드(.class)로 컴파일
4. 클래스 로더가 필요한 클래스를 읽어들이고 컴파일된 자바 바이트 코드를 런타임 데이터 영역에 로드
5. 실행 엔진이 자바 바이트 코드 실행

## JVM 구성요소
- **클래스 로더(Class Loader)**
  - 자바 프로그램이 실행될 때 필요한 클래스 파일을 로드한다.
  - 클래스 파일의 로딩 순서
    - Loading: 클래스 파일을 읽고 해당 바이너리 데이터를 생성해 메소드 영역에 저장한다.
    - Linking: 검증, 준비, 해결을 한다.
      - Verification: 클래스 파일이 올바른 형식인지, 유효한 컴파일러로 생성되었는지 확인한다.
      - Preparation: 정적 변수에 메모리를 할당하고 해당 메모리를 기본값으로 초기화한다.
      - Resoulution: Symbolic references를 direct references로 변경한다.
    - Initialization: 모든 정적 변수는 코드와 static 블록에서 정의된 값으로 할당된다.
- **런타임 데이터 영역(Runtime Data Area)**: 자바 프로그램 실행 중 사용되는 메모리 공간
  - Method: 클래스 정보가 저장된다. 메소드 영역은 JVM당 하나만 존재하며 공유 자원이다.
  - Heap: 객체 정보가 저장된다. 힙 영역은 JVM당 하나만 존재하며 공유 자원이다.
  - Stack: 스레드마다 할당되며 메서드 호출과 관련된 데이터를 저장한다.
  - PC Register: 스레드마다 PC 레지스터가 생성되며 실행 중인 스레드의 실행 명령 주소를 저장한다.
  - Native Method Stack: 스레드마다 네이티브 스택이 생성되며 자바 외의 언어로 작성된 네이티브 언어로 작성된 메서드 정보를 저장한다.
- **실행 엔진(Execution Engine)**
  - 바이트코드 해석기(Bytecode Interpreter): 바이트 코드 명령어를 읽고 해석하여 실행한다.
  - JIT 컴파일러(Just In Time Compiler): 바이트 코드를 네이티브 코드로 변환하여 실행 속도를 향상한다.
  - [가비지 컬렉터(Garbage Collector)](가비지컬렉터.md): 힙 영역에서 더이상 사용하지 않는 객체를 제거하여 메모리 누수를 방지한다.
- **JNI(Java Native Method Interface)**: 자바가 아닌 다른 언어로 만들어진 애플리케이션과 상호 작용할 수 있는 인터페이스를 제공한다.
- **Native Method Libraries**: C, C++로 작성된 라이브러리의 모음이다.