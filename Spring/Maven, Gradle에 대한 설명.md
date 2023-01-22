- Ant

  이 빌드 툴을 사용하기 전에는 Apache Ant를 사용했었습니다. Java와 같이 플랫폼에 독립적인 특징을 가지고 있고, xml 스크립트로 관리를 했습니다. 하지만 자동으로 라이브러리를 업데이트 해주는 기능이 없기 때문에 jar 파일을 직접 다운받아 관리를 해야 한다는 불편함이 있었습니다. 현재는 레거시 시스템에만 Ant를 사용하고 있습니다.

- Maven

  Maven은 이런 Ant의 단점을 보완했습니다. Java Build Tool로써 자동으로 라이브러리와 의존성을 관리해 줍니다. Ant와 동일하게 xml 스크립트로 이루어져 있고, Pom.xml 파일로 의존성을 관리합니다. 
  ```
  <dependency>
  <groupId>org.project</groupId>
  <artifactId>reusable-test-support</artifactId>
  <version>1.0</version>
  <classifier>tests</classifier>
  </dependency>
  ```
  위와 같은 아티팩트 구조로 의존성을 관리할 수 있는 스크립트를 작성하면 Maven Central Repository에서 아티팩트에 맞는 라이브러리를 자동으로 다운로드 해줍니다.

- Gradle

  Gradle은 Groovy 문법을 사용하기 때문에 가독성 측면에서 Maven보다 뛰어나다고 할 수 있습니다. 요즘 Gradle을 많이 선호하는 이유는 `스크립트가 비교적 간결`하고 `빌드 속도`에서 Maven보다 `우수`하다는 결과<a href="https://gradle.org/maven-vs-gradle/">(결과보기)</a>가 있기 때문입니다. 또한 Gradle은 `멀티 모듈 빌드` 기능을 지원하기 때문에 한 프로젝트 안에서 여러 모듈이 개발되는 환경일 때 중복 설정을 하지 않아도 됩니다.