리액트 공부 스타트 공부하자!
바닐라Js 리액트사용 비교

암기할 필요 없다. 이해하기
리액트를 import했기 때문에 createElement function을 가진 리액트 object에 접근 가능
const span 그러나 createElement(“span”) 은 반드시 생성하고자 하는 HTML 태그와 똑같아야함

React JS - 어플리케이션이 아주 인터랙티브하도록 만들어주는 library. 엔진과 같다.
React-dom - library 또는 package. 모든 react element들을 HTML body에 둘 수 있도록 해줌.
ReactDOM.render() - render의 의미는 react element를 가지고 HTML로 만들어 배치한다는 것. 즉, 사용자에게 보여준다는 의미
ReactDOM.render(span, span이 가야할 위치)
-> 그래서 보통 body에 id=“root” 만들어서 span을 root 안에 두라고 함

React.createElement("span", {span의 property}, “span의 내용”)
-> property는 class name, id도 가능 style도 가능
-> 참고만 하고 외우지 말기. 이렇게 쓸 일 없음

바닐라JS는 HTML -> JS 순서
리액트는 JS -> HTML 순서

JS가 element를 생성하고 React JS가 그것을 HTML로 번역하는 것
React JS는 업데이트 해야 하는 HTML을 업데이트 할 수 있음.

두 가지 const를 render 하고 싶은 경우 div를 만든다
그리고 React.createElement("div", null, [span, btn]); 와 같이 배열을 만들어서 const를 넣어준다.

property에 eventListener 넣는 것도 가능.
클릭 - {onClick: () => console.log("I'm clicked")}
마우스엔터 - {onMouseEnter: () => console.log("mouse enter")}

혹시 콘솔에 안 뜨는 경우 event listener가 소문자, 대문자로 잘 적혀있는지 확인해 보세요

JSX – 자바스크립트를 확장한 문법
보통의 HTML과 비슷. 그러나 property를 HTML 태그의 속성처럼 적으면 됨
const Title = (
console.log("mouse enter")}>
Hello I'm a span

);
style={{ backgroundColor: "tomato" }} -> 스타일은 {} 2개임
JSX를 브라우저가 온전히 이해하지 못하므로 이해할 수 있게
https://unpkg.com/@babel/standalone/babel.min.js 를 설치해야함
-> JSX로 적은 코드를 브라우저가 이해할 수 있는 형태로 바꿔줌
바벨을 가져온 뒤 script type="text/babel"로 적어줘야 인식함

리액트JS에서 데이터를 저장시켜 자동으로 리렌더링을 일으킬 수 있는 방법
const data = React.useState();를 console.log 시키면
[undefined, f ] -> undefined와 함수가 적힌 배열이 나타남
undefined는 data이고 f는 data를 바꿀 때 사용하는 함수
React.useState() 함수는 초기값을 설정할 수 있음
즉, undefined는 초기값이고 두 번째 요소인 f는 그 값을 바꾸는 함수

배열을 꺼내기
const x = [1, 2, 3]
const [a, b, c] = x;
으로 꺼낼 수 있음
