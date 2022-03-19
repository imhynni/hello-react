# React 정리

## react 사용하기

### react import

- react를 import하면 react object에 접근 가능
- React JS : 어플리케이션이 인터랙티브하도록 만들어주는 라이브러리. 엔진과 같은 역할.
- React-dom : library 또는 package. 모든 react element들을 HTML body에 두는 역할.

### Vanilla JS vs React JS

- 바닐라 JS : HTML -> JS 순서
- 리액트 JS : JS -> HTML 순서

## JSX

- JS를 확장한 문법
- HTML과 흡사한 문법으로 React 요소를 만들 수 있게 해줌
- 하지만 브라우저는 JSX 문법을 이해하지 못함
- Babel을 사용하면 JSX문법을 브라우저가 이해할 수 있는 형태로 변환해줌
- 컴포넌트를 다른 컴포넌트 안에 넣기 위해서는 컴포넌트들을 함수로 만들어주어야 한다. (() => () : arrow function)
- 주의할 점 : 내가 만든 컴포넌트는 반드시 대문자로 시작해야 한다. 렌더링할 때 html 태그로 혼동하지 않도록!

## State

- state : 데이터가 저장되는 곳
- React.userState()는 [data, modifier]을 반환한다. 두번째 요소는 첫번째 요소인 data를 변경해주는 function이다.
- 배열 값을 가져올 때는 const [counter, setCounter] = React.userStater() 형태로 사용.(function 이름은 보통 set\_\_\_ 이다.)
- modifier에 의해 state, 즉 어플리케이션의 data가 변경되면 새로운 state 값을 가지고 컴포넌트 전체가 재생성되고 리렌더링된다.
- React.js는 똑똑해서, 실제로 바뀌는 부분만 바뀌게 된다. (불필요한 리렌더링은 하지 않는다)
- set 함수에서 현재 state를 바탕으로 다음 state를 계산하고 싶다면, 함수를 전달해주자.(예기치 못한 곳에서 값이 업데이트되어 혼동되는 것을 방지)
