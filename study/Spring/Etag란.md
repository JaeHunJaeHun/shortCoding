# Spring Etag란
### Etag란
- Etag 또는 Entity Tag는 월드 와이드 웹 프로토콜인 HTTP의 일부이다. HTTP가 웹 캐시 유효성 검사를 위해 제공하는 몇가지 메커니즘 중 하나로 클라이언트가 조건부 요청을 할 수 있게 한다.
- Etage는 웹 서버가 URL에서 찾는 리소스의 특정 버전을 할당하는 불투명한 식별자이다. 만약 그 URL의 리소스 표현이 변경된다면, 새롭고 다른 Etag가 할당된다. 이러한 방식으로 사용하는 Etgae는 지문과 유사하며, 한 자원의 두가지 표현이 동일한지 여부를 결정하기 위해 빠르게 비교할 수 있다.
- 웹 서버가 주어진 URL의 콘텐츠가 변경되었는지 알려주고 이를 반환하는 HTTP 응답 헤더
### 사용하는 이유
> 캐시를 사용하면 불필요한 요청을 줄이면서 서버의 부하를 줄일 수 있고, 미리 캐시에 저장해 놓은 값을 사용함으로써 빠른 응답을 할 수 있다.


#### 정리
> HTTP API가 응답했던 결과에 대한 해시값을 만들어 놓고 저장하다가 기존 리소스와 동일한 값(Etage 값)을 가지면 데이터 베이스 조회 없이 응답하는 것
> 조회 했을 때 Etage 값이 다르면 조회하는 일종의 웹 캐싱 방식









[출처] [https://www.notion.so/Spring-Etag-5dd31f9b48c342238dfec60859583243#c156aef1aa3c49e4b2dc4c37b2564e44](https://www.notion.so/Spring-Etag-5dd31f9b48c342238dfec60859583243#c156aef1aa3c49e4b2dc4c37b2564e44)
