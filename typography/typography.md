-   Typography: 텍스트를 예쁘게 디자인 하는 것
    [1] Essentials

    1. font-size

        - 절대 단위(Absolute unit)
          ㄴ px:

        - 상대 단위(Relative unit)
          ㄴ em: Equal to capital M => 대문자 M 사이즈를 기준으로 하다 == 실제로 적용된 폰트 사이즈
          ex) font-size가 24px일 때, 1em은 24px를, 10em은 240px을 의미한다.
          이것이 의미하는 바는 width를 폰트 크기에 맞출 수 있다는 것?
          .text{ font-size: 24px; }
          .div{ width: 10em; }
          일 때, width의 길이는 240px이 되는 것~

            ㄴ rem: Root em == HTML em - root: HTML 자체를 뜻함
            html{ font-size: 10px}로 정해놓고 다른 태그 꾸밀 때 p{ width: 10rem; font-size: 1.5rem; }과 같이 이용할 수 있다.

    2. line-height: 줄간격. px em rem 단위 동일함. em을 많이 사용함
       p{ font-size: 20px; line-height: 1.5(em);} : 위 아래로 150% 떨어뜨리겠다. 줄간격에서 em 생략하는 것이 관례

    3. letter-spacing: 자간. px과 em만 사용. em을 많이 사용함. em 생략xxxx

        **쉽게 em은 퍼센트라고 생각하면 된다**

    4. font-family: 폰트 서체 표현.
       .text {
       font-family: "Poppins"; <- 포핀스라는 폰트를 적용해라
       font-family: "Poppins", sans-serif; <- 포핀스라는 포핀스를 적용해, 근데 없으면 sans-serif 중에서 암거나 적용해
       font-family: "Poppins", "Roboto", sans-serif; <- 포핀스 적용해, 없으면 로보토로, 그것도 없으면 걍 sans-serif 중 암거나~
       ** serif는 명조체st(삐침이 있는)/ sans-serif는 돋움,고딕체st **

    5. font-weight: 폰트 굵기/ 100단위로 할 것!
       400은 Regular 굵기, 700부터 Bold 굵기

    6. color: 글씨 색

        - color 사용 방식 세가지
            - hex: #0066ff

    -   rgb: rgb(0, 102, 255)
    -   rgba: rgba(0, 102, 255, 1) : a가 1이면 완전 불투명/ 0이면 완전 투명

[2] Etc.. 중요하진 않지만 알아두면 좋은 것

1. text-align: 텍스트 정렬
   left | center | right

2. text-indent: 들여쓰기
   px 단위로. 마이너스도 가능!

3. text-transform: 텍스트 변형
   none | capitalize(모든 단어 첫글자만 대문자로) | uppercase | lowercase

4. text-decoration: 텍스트 줄 꾸밈(like 줄 긋기). 밑줄, 취소선같은 거~. a 태그에 밑줄 없앨 수도 있구
   none | underline | line-through | overline

5. font-style: 문자 기울이기(HTML의 <em>과 같다. 그래서 CSS에서 해제해주기도 함)
   normal | italic | oblique

[3] Web font

-   사용 방법

    1. 갖다 쓴다.
       ex) google font

    2. 직접 제공한다. (자기가 갖고 있는 경우) 82강 8분쯤 참고
       프로젝트가 있는 폴더에 폰트용 폴더 만들고 가지고 있는 폰트 넣는다
       -> css에 @font-face { font-family: '폰트명(내 맘대로 적어도 됨)';
       font-style: normal;
       font-weight: 400;
       src: url(웹폰트가 있는 폴더 경로)}
       -> HTML 또는 CSS import하여 사용!
