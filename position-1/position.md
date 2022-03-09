-   Position
    : 요소를 원하는 위치에 자유롭게 이동시키기 위한 프로퍼티

*   Position Type (이동시 기준점이 중요하다!)

1. static: 모든 요소의 기본값
2. relative: 이동의 기준이 자기 자신이 본래 있던 자리
   float과 달리 자기 본래 자리를 기억하고 있어서 다른 요소들이 넘보지 않음
3. absolute: float과 매우 비슷!
    1. display: block으로 신분 상승
    2. block인데 길막을 못함 (붕 떠 있기 때문!)
    3. float과 다른 점: float과 달리 inline 요소가 absolute 요소를 인식하지 않음!
    4. 자기가 원하는 기준점(부모 or 부모의부모 or 부모의부모의부모의....)을 고를 수 있다(float은 부모에 종속됨)
       4-1) 선택의 기준: position이 static이 아닌 요소( == 조상의 position: relative | absolute | fixed | sticky 이어야 한다! but relative가 주변 요소에 영향을 끼치지 않기 때문에 relative를 주로 쓴다)
4. fixed: absolute와 모두 동일한 현상이 일어나지만, 자신의 기준점이 *viewport*인 점이 다름!
    - viewport: 브라우저 창의 전체 크기(실제 크기가 아닌 *화면*으로 보이는 크기!)
    - 스크롤 내리면 같이 움직임
5. sticky(지원하는 브라우저가 많이 없기 때문에 스킵~~)

-   이동을 시킬 때는 top: 10px, left: 20px or bottom: 40px, right:60px 과 같이 사용! (생각해보면 너무나 당연한 것임~~)

-   z-index 프로퍼티: position된 요소들의 수직 방향으로써의 위치를 알려줌
    ㄴ 사진 참고하면 짱 쉬움
