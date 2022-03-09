* Box



box-sizing: content-box;
padding의 값을 넣으면 사용자가 원하던 크기에서 벗어나게 됨

box-sizing: border-box;
border까지의 라인을 가로 세로로 보겠다
padding과 border에 얼마를 넣든 자동으로 content 의 크기를 조정해줘서
사용자가 원하는 크기로 완성해준다.


* {
    box-sizing: border-box;
}

ㄴ 필수!!!!!!!






Box Type -> Display: 박스 타입을 결정짓는 css 속성
==> Display에 따라 박스 속성이 달라진다.


[1] Block<- 길막하는 애! (기본 속성)
Block의 성질
1. 따로 width를 선언하지 않은 경우, width는 부모 content width 값과 같음
2. 따로 width를 선언하는 경우, 남은 공간은 margin으로 채운다
3. 다로 부모의 height를 선언하지 않을 경우, 자식 요소들의 height의 합 = 부모의 height가 됨
4. 가로 배치 불편
margin: 0 auto;
ㄴ top 과 bottom은 0, left와 right는 auto;


[2] Inline <- 흐름
: width, height, padding-top/bottom, border-top/bottom, margin-top/bottm 사용 불가!!


Block(면/영역)VS Inline(선/흐름)

[3] Inline block
: Inline처럼 기본적으로는 가로로 흐르는 동시에 Block처럼 영역도 잡을 수 있음







-------------------------------------
Float
1. 어떤 요소가 Float 되면 부모가 그 요소를 잃게 되고, 옆에 있던 요소가 Float된 요소 자리를 빈공간으로 인식하여 차지한다
1-1. overflow: hidden;을 사용하면 부모가 float된 자식의 존재를 다시 인식한다!
2. Float된 요소는 Block 가 된다
Inline/ Inline Block/Block ==> Float 하면 ==> Block
ex) Inline을 Float하면 width, height, padding-top/bottom, border-top/bottom, margin-top/bottm 을 사용할 수 있게 됨! (Block이 됐으니까)
2-2. 단, Float 하면 Display값이 Block이더라도 길막을 못한다! (margin이 자동으로 생기지 않는다는 뜻)
3. Float가 일어나면 Block 박스들은 Float된 요소를 없는 박스 취급한다.
but, Inline 박스들은 플로트의 존재를 안다!
--


****
clearfix: Float으로 인해 망가진 레이아웃을 고쳐주기 위해 탄생한 속성 (clear은 display가 Block인 애들한테만 쓸 수 있다)
1. clear: left ::: Float left된 녀석들이 앞에 있다면 그들의 위치를 정확하게 파악해서 앞으로 영향받지 않을 거야!
2. clear: right
3. clear: both ::: left, right 둘다 알아차려서 영향받지 않겟다!

------
자식 요소가 모두 float되었을 때 부모가 height 가질 수 없으니, 
아무 의미도 없는 div 태그(clear 속성을 탑재한) 같은 것을 가장 밑에 넣어주어서 float된 자식까지 포함한 height 값을 얻을 수 있음
--> HTML에 태그를 넣지 않고 CSS 에서 해주는 방법
:Pseudo Element: HTML에는 존재하지 않는 가상 요소에 clear을 먹임

* 가상 요소 만드는 법
::before <- 가장 첫번째에 가상 요소 삽입
::after <- 가장 마지막에 가상 요소 삽입

예시)
클래스명::after {
  content: '!!!'; <- 필수!
}


* 가상 요소로 clearfix 기법 사용하는 법 예시
.parent::after{
  content: "";
  display: block;
  clear: left;
  /* left | right | both */
}
****
