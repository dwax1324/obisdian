무엇이 성공적인 테스트 스위트를 만드는가 ? 
1. 개발 주기에 통합되어 있다
2. 코드 베이스에서 가장 중요한 부분을 테스트한다
3. 최소한의 유지비로 최대의 가치를 끌어낸다
가치있는 테스트 식별하기, 더 가치있는 테스트 작성하기

좋은 설계 없이 좋은 테스트 코드는 없다. <- 이 책 전반적으로는 설계에 대한 내용을 다룬다

코드는 건들면 건들수록 엔트로피가 증가하여 복잡해진다. 꾸준한 리펙터링이 필요하고, 테스트는 안전망 역할을 한다.
애플리케이션과 테스트 코드는 모두 자산이 아니라 부채다.

코드 커버리지가 낮은건 분명히 안좋은 것이지만, 높다고 해서 좋은건 아니다. 

좋은 테스트랑 좋지 않은 테스트를 구별할 줄 알아야한다.

켄트백의 tdd

고전파와 고전파 <- 무엇이 단위를 의미하는지에 대한 관점과 테스트 대상 시스템의 의존성 처리 방식에 영향을 미침
고전파는 단위가 아니라 단위 테스트를 서로 분리해야한다고 한다. 테스트 대상 단위는 동작 단위다. 공유 의존성만 대역으로 교체해야 한다. 공유 의존성이란 테스트가 서로의 실행 흐름에 영향을 미치는 수단을 제공하는 의존성이다. 바텀업
런던파는 테스트 대상 단위(보통 단일 클래스)를 서로 분리해야 한다고 한다. 불변 의존성을 제외한 모든 의전송을 대역으로 대체한다. 탑다운

코드 조각을 단위테스트할 수 없다는 것은 코드에 문제가 있다는 사실을 알려주는 강한 징후다. 

aarange, act, assert <- AAA패턴 <- GWT(Given When Then과 비슷)

GWT를 써라
GWT만 써라.(GWGWT 이런식으로 반복 X)
테스트내 if문을 피하라 <- 최대한 간단한게 작성해라
준비 구절이 큰 경우 <- 비공개 메서드 ㄸ도는 별도의 팩토르 클래스로 도출해라. 준비 구절 코드 재사용에 도움이 되는 두 가지 패턴으로 오브젝트 마더와 테스트 데이터 빌더가 있다.
실행 구절은 한 줄로 작성하라 <- 단일 작업을 수행하는데 두 개의 메서드 호출이 필요하면 어카죠? API에 문제가 있다는 뜻이다

불변 위반 invariant violation <- 1. 상품을 구매한다 2. 재고 수량이 줄어든다. 라는 메서드들이 있을 때 1을 호출하고 2을 호출하지 않으면 모순이 생김
캡슐화 <- 잠재된 모순으로부터 코드를 보호
불변 위반을 초래할 수 있는 잠재적인 행동들은 제거해야한다
단일 동작은 여러 결과를 초래할 수 있고. 모두 검증하는 게 좋다..

테스트픽스처 <- 테스트 실행 대상 객체, 테스트 실행하기 전에 고정된 상태 유지, 동일한 전제조건



