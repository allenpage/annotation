# @RequestMapping


URL을 매핑해주는데 도움을 주는 어노테이션!
클래스와 메소드에 사용할 수 있다.



RequestMapping은 3가지로 나뉜다.

- 클래스 레벨
    - 클래스 하위 메소드들은 어노테이션에서 작성한 URL을 기준으로, 하위 URL을 입력할 수 있다. (생략이 가능하다!)
        - /클래스URL/하위URL ...

- 메서드 레벨
    - 작성한 URL로 접근할 수 있도록 한다.
    - value = {"/var1", "/var2"} 으로 등록하면 같은 URL은 동일한 수행할 수 있다.

- HTTP 상태코드 매핑
    - 클래스 레벨에 RequestMapping을 하여
    - 메소드에 어노테이션으로 method = RequestMethod.GET과 같이 해당 메소드는 GET만 접근할 수 있도록 지정한다.
    - REST API를 만드는데 참 편해보임!



## 결론
RequestMapping은 URL을 매핑해주는데, 다양하게 활용할 수 있어보인다.
특히 HTTP 상태코드를 매핑하여 REST API를 설계하는데 명확하게 구분하고 작성하는데 도움이 될 것 같다.





## 추후 수정할 것 및 궁금한 것
예제 추가