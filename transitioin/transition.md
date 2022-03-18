* transition(전환;자연스럽게 변하는 효과)
1. property: font-size | background-color 등등. 모두에게 적용하고 싶으면 all
2. duration: 지속 시간. 단위(ms, s ) 10000ms == 1s
3. [timing-function]: 생략 가능. ( ease-in(천천히 바뀌다가 휙 바뀜) | ease-out(휙 바뀌다가 천천히) | ease-in-out(앞 두개 섞인거) | cubic-bezier()<- 곡선 만드는 애. 속도 커스텀 ) 
4. [delay]: 생략 가능. 몇 초 후에 실행할 지

ex)
.box{ 
    transition: font-size 2500ms ease-in;
    /*좀 더 섬세하게 개별적으로 조절하는 법
    transition: font-size 1000ms ease-out, background-color 2000ms cubic-bezier(0.08, 0.57, 0.96, -0.78) 1000ms) <- 이런 식으로 콤마로 구분
    */
}



