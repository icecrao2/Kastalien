# Viewmodel은 not null 하게 만들어야 한다.
- Activity든 Fragment든 ViewModel은 not null 하게 사용하는것이 좋다.
    - nullable하게 만들 경우 불필요한 null safe 코드가 발생한다.
    - nullable하게 만들 경우 실제로 null 인 상황이 발생하여 에러가 발생할 수 있다.
    - 그래서 바로 초기화 할 수 없다면 lazy by 를 활용하는것이 가장 좋다.
