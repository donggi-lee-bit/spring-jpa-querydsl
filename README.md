# spring-jpa-querydsl
인프런 김영한님 실전 QueryDsl 강의 연습 레포

## QueryDsl 환경 설정

spring boot 버전 2.6 이상, querydsl 5.0 환경 설정 방법이 다르다. querydsl 설정 시 `annotationProcessor` 사용을 권장하고 있다. 그 이유는
- spring boot가 버전업을 하면서 gradle 도 버전업 하게 되고 그 과정에서 인텔리제이에서 build 시 querydsl Q클래스 생성 문제
  - gradle 로 빌드하면 문제 없지만 intellij idea 로 빌드하면 정상 작동이 되지 않는다고 한다

자세한 내용은 아래 블로그에 자세하게 나와있다

[그레이들 Annotation processor 와 Querydsl](http://honeymon.io/tech/2020/07/09/gradle-annotation-processor-with-querydsl.html)

### 설정 검증 및 확인

검증
- Gradle > build
  - 에러가 난다면 환경 설정에 문제가 있는 것

확인
- build > generated > querydsl
  - Q class 생성되어 있어야함 