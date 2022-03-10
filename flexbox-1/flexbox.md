-   Flexbox: 정렬의 끝 판 왕

*   사용 방법

1. 나 플렉스 박스 쓸 거야! (선언)
   정렬하고자 하는 요소들의 부모에게 { display: flex | inline-flex; }

    - display는 Box의 Type을 정해주는 CSS 프로퍼티. flex도 Box의 타입!
    - position은 자기 자신 요소한테 썼었지만 flex 박스는 부모에게!

2. 가로 정렬? 세로 정렬?
   { flex-direction: row | row-reverse <- 가로 방향 정렬
   | column | column-reverse; <- 세로 방향 정렬 }

    - Axis(축): 어떤 flex를 사용하면 두 개의 축이 생긴다.
      flex-direction 어떤 값으로 설정 되느냐에 따라 축의 방향이 완전히 달라진다

    <사진 참고>

    - Main axis: flex-direction 의 방향에 따라 생김
    - Cross axis: Main과 정확하게 수직을 이루는 방향으로 생김

    - Main axis를 따라 정렬할 때는 justify-content
    - Cross axis를 따라 정렬할 때는 align-items | align-content
      (align-content를 쓰려면 flex-wrap: wrap이어야 함)

    - align-items 와 align-content의 차이(75강 15분 참고)

    * items: 흐르는 기준이 줄이 나뉠 때 마다 생김 <-- 얘를 많이 씀. 일단 써보고 안되면 content ㄱㄱ
    * content: 무조건 하나의 흐름

3. 무조건 한 줄 안에 다 정렬? or something?
   : 어떻게든 한 줄 안에 다 넣을 것인지 or 상황에 따라 여러 줄에 넣을 것인지 정렬
   { flex-wrap: nowrap | wrap } - nowrap: 감싸지(wrap) 않고 (자식의)사이즈를 줄여서라도 *한 줄*로 정렬 - wrap: 한 줄에 모두 정렬하기에 공간이 넉넉하지 않으면 *여러 줄*로 정렬

---

\*\* flex로 순서 바꾸는 방법 order
: 부모가 {display: flex;}일 때
자식 요소들에게 {order:1; order:2; order: 3;}를 각각 주면
숫자에 따라 자식들의 순서가 바뀐다
