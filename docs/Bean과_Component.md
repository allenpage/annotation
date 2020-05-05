# @Bean과 @Component



Bean과 Component를 배우기전에 Spring Bean을 알아야한다.



* 스프링 빈
  * 재사용되는 객체들을 스프링이 관리해준다.
  * Bean으로 등록된 객체는 **생성과 생명주기**, **의존성 관리**를 받음
* 스프링 빈 컨테이너
  * 등록된 스프링 빈을 인스턴스화
  * 설정 및 의존성 주입을 담당한다.



즉 위와 같은 부분을 스프링에 위임하기 위해서 @Bean과 @Component를 사용한다.

둘의 차이를 알아보자.



## Component

기본적으로 컴포넌트는 Service, Repository, Contoller에 사용됐다.

개발자가 직접 작성한 Class를 Bean으로 등록하는 것이라고 생각할 수 있다.



![](..\img\component.PNG)









## Bean

**@Bean을 사용하려면  클래스 상단에 @Configuration가 필요하다**

개발자가 직접 제어가 불가능한 외부라이브러리 등을 Bean으로 만들때 사용된다.

@Component와 다르게 @Bean은 메소드에 지정을 한다.

Bean의 ID를 설정할 수 있는데, 입력하지않으면 메소드이름이 Bean의 이름으로 등록된다



![](..\img\bean.PNG)





## 결론

간단하게 차이라고하면 **@Component**는 프로그래머가 직접 작성한 클래스를 Spring bean에 등록할 때 사용된다. **@Bean**은 프로그래머가 외부 라이브러리를 가져와 사용할때 Bean에 등록하고 싶을 때 사용된다. 메소드의 리턴타입이 Spring bean에 등록된다.





## 추후 수정할 것 및 궁금한 것

어떤 클래스에 @Component을 달아야할까?

상태가 있는 Component는 사용하면 안된다. > 모든 싱글톤은 Component를 달아도 되지 않을까?

Bean을 활용하는 예제 추가