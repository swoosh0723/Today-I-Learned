# Switch,Route,Link

## 설명

`react-Route-Dom`을 이용하여, 페이지의 로딩 없이, 페이지에 필요한 컴포넌트를 불러와 렌더링 하여 보여주도록 도와줌  
그래서 리액트는 빠르다

**`Switch`**  
여러개 Route가 매칭 되어도 맨 위의 Route 하나만 보여줌

**`Route`**  
페이지 이동 없이 DOM 교체로 페이지 이동된 것처럼  
`exact`: 경로가 정확히 일치 할때만 보여줌

**`Link`**  
`<a>`와 유사하나 `<a>`는 **url** `Link`는 **path** 개념  
랜더링은 `<a>`로 된다

---

## 사용방법

1. `npm install react-router-dom` 설치한다
2. `import { Link, Route, Switch } from 'react-router-dom'` 문서에 import 시킨다

---

## 예제

### 기본

```javascript
function App() {
  return (
    // Switch가 있기때문에 맨 위의 route1만 랜더링 된다
    <Switch>
      <Route exact path="/route1">
        <div>Route1</div>
      </Route>

      <Route exact path="/route2">
        <div>Route2</div>
      </Route>

      <Route exact path="/route3">
        <div>Route3</div>
      </Route>
    </Switch>
  );
}
```
