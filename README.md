# HTML/CSS

1. nav 메뉴들의 max-width:1000px 이므로 section_1, section_3도 max-width:1000px을 줌으로서 화면이 커졌을 경우 라인을 맞춰준다.
2. section_0 에서 p에 div를 감싼 이유는 중앙정렬을 쉽게 하기 위해서이다. div에 height를 3em font-size를 2.5rem으로 줌으로서 글자가 height를 넘어가지 못하게 한다.
3. 제목 부분들은 font-size를 vw로 설명 부분들은 rem으로 주는 이유는 apple 사이트의 디자이너 의도를 따르겠다는 것이다. 따로 정해져 있는 것이 아니다. apple 사이트에서는 제목부분들은 화면에 맞게 커지게 설명 부분들은 고정px로 설정해준다.
4. section.css에 있는 .sticky-element를 적용시키기 위해서는 .scroll--message보다 뒤에 적용되거나 css 우선순위가 높아야한다. 그러므로 .scroll--section .sticky-element{} 이렇게 써주거나 styles.css에서 section.css 순서를 section_0.css보다 뒤로 보낸다.

# 스크롤을 이용한 인터렉션 구현

1. body id값으로 show--scene--0, show--scene--1, show--scene--2, show--scene--3을 js를 이용하여 현재 스크롤 위치에 따라 지정해준다. 그런 다음 body의 id값에 따라 해당 섹션의 .sticky-element을 보여준다.

```
#show__scene--0 .scroll__section--0 .sticky-element,
#show__scene--1 .scroll__section--1 .sticky-element,
#show__scene--2 .scroll__section--2 .sticky-element,
#show__scene--3 .scroll__section--3 .sticky-element {
  display: block;

}
```
