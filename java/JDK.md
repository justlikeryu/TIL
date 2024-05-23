# JDK(Java Development Kit)
> 자바 기반 SW 애플리케이션 개발에 필요한 도구 및 라이브러리 모음을 제공하는 크로스 플랫폼 SW 개발 환경

# JDK의 구성
JDK = JRE(Java Runtime Environment) + Development Tools
<img src="https://github.com/justlikeryu/TIL/assets/111476710/92bf5a29-1d67-416e-9666-c088a59dda4c">
- JRE
  - 자바 프로그램을 실행하기 위해 필요한 SW
  - JVM의 실행 환경을 구현한다.
- 컴파일러(javac)
    - 자바소스 코드를 바이트 코드[^byte]로 컴파일한다.
- 인터프리터/로더(java)
  - 컴파일러가 생성한 바이트 코드를 해석하고 실행한다.
- 아카이버(jar)
  - 클래스 파일과 프로그램 실행에 관련된 파일을 하나의 jar파일로 압축/압축해제한다.
- 그외
[^byte]: JVM이 이해할 수 있는 기계어
