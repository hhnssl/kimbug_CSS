* Animation
- animation(자연스럽게 애니메이션을 주고 싶을 때) vs trasition(스르륵 전환)
- trasition에 비해 세부 속성이 굉장히 많다
1. property: font-size | background-color 등등. 모두에게 적용하고 싶으면 all
2. duration: 지속 시간. 단위(ms, s ) 1000ms == 1s
3. [timing-function]: 생략 가능. ( ease-in(천천히 바뀌다가 휙 바뀜) | ease-out(휙 바뀌다가 천천히) | ease-in-out(앞 두개 섞인거) | cubic-bezier()<- 곡선 만드는 애. 속도 커스텀 ) 
4. [delay]: 생략 가능. 몇 초 후에 실행할 지
5. iteration-count: 여러번 애니메이션 효과 주기;
(사진 참고)
6. direction: from -> to. alternative를 쓰면 왕복으로 바꿔줌
더 많이 있으니까 MDN CSS animation 찾아봐~

@keyframes name {
  from{ <- 시작. 퍼센트도 가능~ (0% ~ 100%)

  }
  to{ <- 끝

  }
}