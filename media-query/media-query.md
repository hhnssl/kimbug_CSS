-   미디어쿼리
    1. 작은 사이즈인 모바일 먼저 시작한다
    2. 크롬 개발자도구의 모바일 버전을 아이폰5/SE로 두고 스타일링 하기(제일 작은 사이즈라서 얘로 성공하면 다른 사이즈에서 웬만해서는 잘 깨지지 않는다고 함)

*   Media Query: 반응형 웹(Responsive Web: 사용자가 접속한 디스플레이 사이즈에 반응함) 위한 CSS
*   반응형 웹을 위한 HTML과 CSS 설정

-   HTML: <meta name="viewport" content="width=device-width" />
    ㄴ 가로길이를 사용자 디바이스 가로 길이에 맞춰라~
-   CSS: @media screen and (min-width: 768px) { }
    ㄴ 나 미디어쿼리 선언할 거고/ 스크린에 관해서 쓸게/ 최소 브라우저 가로 사이즈가 768px 이상에서는 { } 스타일을 적용시켜줘~

*   단위 vh: viewport height
    1vh == 내가 보고 있는 화면(뷰포트 기준)에서 세로 길이의 1%
    100vh == 100%
    (vw도 있음~ 근데 vh를 더 많이 쓴대)
