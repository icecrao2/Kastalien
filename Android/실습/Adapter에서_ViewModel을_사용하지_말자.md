# Adapter에서 ViewModel을 사용하지 말아라
- Adapter는 프래그먼트나 액티비티와 생명주기가 완전히 다르다.
    - 그러므로, Adapter 내부에 ViewModel을 사용하면 사용되는 ViewModel이 꼬일 수 있다.
- Adapter에서는 LiveData 등의 구독 해제 시점이 불명확함
    - Adapter에서 구독을 사용하면 구독 해제 시점이 불명확해져 메모리 누수가 발생할 수 있다.


표현하자면 ViewModel은 Activity와 Fragment에서 사용되도록 설계가 되었다.
그런데, 이것을 역할과 수명주기가 다른 Adapter가 사용하게 되면 ViewModel에서 이상 동작이 발생할 수 있으므로 Adapter에서는 ViewModel 사용을 금지한다