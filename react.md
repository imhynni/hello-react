# React 정리

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
- HTML과 비슷하지만 몇 가지 다른 점 기억하기 : class, for 사용 불가! >> className, htmlFor로 사용

## State

- state : 데이터가 저장되는 곳
- React.userState()는 [data, modifier]을 반환한다. 두번째 요소는 첫번째 요소인 data를 변경해주는 function이다.
- 배열 값을 가져올 때는 const [data, setData] = React.userState() 형태로 사용.
- modifier에 의해 state, 즉 어플리케이션의 data가 변경되면 새로운 state 값을 가지고 컴포넌트 전체가 재생성되고 리렌더링된다.
- React.js는 똑똑해서, 실제로 바뀌는 부분만 바뀌게 된다. (불필요한 리렌더링은 하지 않는다)
- set 함수에서 현재 state를 바탕으로 다음 state를 계산하고 싶다면, 함수를 전달해주자.(예기치 못한 곳에서 값이 업데이트되어 혼동되는 것을 방지)

## Props

- 부모 컴포넌트에서 자식 컴포넌트로 데이터 전송
- props는 전달된 모든 prop을 가지는 오브젝트이며 컴포넌트의 첫번째이자 유일한 인자로 주어진다.
- 컴포넌트를 재사용할 수 있게 됨
- PropTypes를 이용해 prop의 데이터 type이나 필수 여부를 설정해줄 수 있다. (실수로 잘못된 prop을 전달하지 않도록 경고해주는 용도)

## Memo

- 변경되지 않은 컴포넌트들까지 모두 리렌더링되면 성능이 느려질 수 있다. (컴포넌트가 매우 많은 경우)
- Props가 변경되지 않은 컴포넌트는 리렌더링되지 않도록 하기 위해 React memo를 사용할 수 있다.
