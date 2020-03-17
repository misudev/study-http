# :zap: 세번째 모임

<hr>

#### HTTP Client 가 무엇인가요

##### YHJ : HTTP Server 와 통신하도록 도와주는 라이브러리, 통신을 효율적으로 사용할 수 있도록 내부적으로 여러 기능을 제공한다.
##### KYS : 
##### CHH : 
##### KDH : 
##### KDH : 
##### JMS : HTTP Client는 HTTP 프로토콜에 맞게 request를 보내고 response를 받는 작업을 도와주는 라이브러리다.
##### HSM : 

<hr>

## 스터디 진행 내용

1. 두 번째 과제 공유

2. 재밌거나 신기하거나 어려웠거나

3. URLConnection ?

4. HTTP Client 의 역할

5. HTTP Client 에는 어떤게 있을까

6. HTTP Client 를 왜 사용할까? 왜 선택했나?

## :flashlight: 코드 디버깅하기

- 오픈 소스(OkHTTP)를 이용해 클라이언트가 HTTP 로 통신하는 과정을 디버깅해보자
- 높은 버전은 어려우므로 1 버전으로 진행 !

- OkHttp 를 **디버깅**하며 정리한 내용을 한 장의 문서로 만들어 **공유**해보자 !
   - YHJ 
   - KYS
   - CHH
   - KDH
   - KDH
   - JMS
   - HMS

#### 다음을 참고하자

> 괄호() 는 클래스를 의미

1. 클라이언트 생성 (OkHttpClient)
2. 클라이언트 URL 설정 및 초기화 (OkHttpClient -> HttpURLConnectionImpl)
3. 요청 및 응답 처리 (HttpURLConnectionImpl)
   1. httpEngine 초기화
   2. 요청 보내기 (HttpEngine)
      1. 요청 헤더 준비하기
      2. 캐시 판별하기
      3. Socket 생성 (TCP 연결 맺기)
      4. Https 확인하고 SSL 설정하기
      5. RouteSelector 를 이용해 Connection 을 생성
      6. **socket 생성** (Connection)
      7. **socket 연결** (Connection)
   3. 응답 읽기 (HttpEngine)