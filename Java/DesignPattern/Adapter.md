# Adapter 패턴
## 무언인지?
- 제공된 것 (클래스, 라이브러리) 을 포장하는 것
- 제공된 것이 검증된 것이나 변경이 불가능 한 경우 
     - COMS 코드를 고쳐야 할 때?
- 인터페이스가 있어야 하는 이유?
    - 관리 측면에서 어댑터 클래스가 늘어 났을 때 인터페이스가 변경 되면 여러 어댑터에 강제적으로 구현을 요구하기 때문에 유지가 가능하다.
    - 어댑터를 바꿔야 하긴 한다!