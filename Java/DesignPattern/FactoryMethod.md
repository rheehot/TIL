# Factory Method 패턴

## 질문
1. 왜 new가 아니라 외부에서 만드는가?
    - 책 속의 예제로는 이해하기 힘들다.
    - 2번의 답을 참고
2. Factory 클레스가 왜 있는 것인가? 
    - Factory를 하위에서 만들어 상위 클래스에게 주면 인스턴스를 수시로 만들어서 쓸 수 있기 때문이다.
    - 이를 의존성 주입 (dependency injection)이라고 한다.
    - 추상화 계층 유지, 같은 계층 끼리는 적어도 하위를 보고 있으면 안된다
