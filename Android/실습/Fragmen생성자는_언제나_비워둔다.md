# Fragment 생성자는 언제나 비워둔다

1. Fragemnt는 외부 요인으로 인해 언제든지 삭제 및 재생성 될 수 있다.
2. 문제는 Fragment가 재생성 될 대 시스템은 기본 생성자를 사용하여 재생성 한다는 것이다.
3. 시스템이 기본 생성자를 통해 Fragment를 생성하는데 만약 생성자 매개변수가 존재한다면 RuntimeException이 발생할 것이다.
4. 그러므로 우리는 Fragment 생성시 데이터 전달을 위하여 생성자 매개변수 말고 Bundle을 사용해야 한다.
5. 생성자처럼 Bundle로 데이터 전송 규격을 정하기 위해서는 팩토리패턴같은 형태가 존재한다.
6. 이것이 Android에서 사람들이 자주 사용하는 Fragment의 newInstance 패턴이다.