# Iterator 패턴
## 무슨 패턴인가?
- 무엇인가 많이 모여있는 것드르을 순서대로 지정하면서 전체를 검색하는 처리를 실행하기 위한 것
- 클래스와 인터페이스
    - Aggregate: 집합체를 나타내는 인터페이스
        - iterator: 집합체를 하나씩 나열하고, 검색하고, 조사하고 싶을 때 매커니즘을 제공
    - Iterator: 하나씩 나열하면서 검색을 실행하는 인터페이스 (루프 변수와 같은 역할을 수행)
        - next: '다음 요소'를 얻기 위한 메소드
        - hasNext: '다음 요소'가 존재하는지를 조사하기 위한 메소드
## 이 패턴을 왜 쓰는가?
- 구현과 분리해서 하나씩 셀 수 있기 때문이다.
    - 예제 코드에서 사용되고 있는 메소드는 상위의 'hasNext' 와 'next' 뿐이지 Aggregate를 구현한 클래스의 메소드는 전혀 불리고 있지 않음
    - Aggregate를 구현한 클래스 데이터 저장 자료구조를 변경한다 해도 내부 코드만 바뀌지 iterator를 사용하는 부분은 전혀 달라지지 않는다.
    - 재이용성 강조
- 결합을 약하게 해서 부품으로 재이용하기 쉽도록 한다.
    - 구체적인 클래스만을 사용하게 되면 클래스 간의 결합이 강해져서, 부품으로 재이용하기 어렵다.
- '바뀌는 부분을 캡슐화 하라' 라는 중요한 원칙이 존재

## 이 패턴을 어떻게 쓰는가?
1. 집합체에 저장될 단위의 데이터 클래스를 만든다.
2. Aggregate를 구현한 해당 데이터의 집합체 클래스를 만든다.
    1. 데이터를 어떻게 저장할 지 자료구조를 정한다.
    2. 데이터를 삽입, 삭제, 길이 반환 등의 메소드를 정의한다. 
3. 검색 기능을 Iterator 클래스를 구현한다.
    1. Aggregate를 구현한 클래스가 제공하는 매커니즘에 따라 next, hasNext를 구현한다.
4. 외부에서는 Iterator Interface를 이용하여 순회를 한다.

## 예제 형식
### 스터디 교제
### head first design pettern
###  

## 그 밖에 부가적인 내용들
- Iterator 클래스는 자바 기본 클래스 이고 ArrayList에서는 기본적으로 iterator를 제공한다. 
- Iteratble 을 Aggregate라고 볼 수도 있는 것일까?
    - Java Collection을 이 패턴을 이용해서 구현했다고 생각을 해도 되는 것인가?
## 의문점
- getBookAt 메소드가 수정됬을 때 iterator 클래스도 변경되어야 할 상황이 존재할까?
    - index 를 통해서 Book을 리턴하는 동작은 안 변하지 않을까?
- hasNext 가 틀리기 쉬운 이유가 뭘까? 주의해서 작성하지 않으면 최후의 ㅣ1개를 반환하지 못할 위험이 있다는 게 무슨 뜻?

- 효율성 문제
    - Linked List의 get() 함수를 생각, Data structure 를 신경 쓰지 않아도 됨
- 인덱스를 신경쓰지 않는다. 
    - Iterator 가 순서를 보장하는 것은 아니다.
    - 처음 부터 끝까지 한번 순회할 수 있다.
    - 의미만 유지되면 되는 것


- 내용을 한번 훑고
- 왜 이 패턴을 쓰는지 ?