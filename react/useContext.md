# useContext

## 설명

props 전송없이도 하위 component들에게도 state값들을 똑같이 공유할 수 있음.

---

## 예제

### 기본

```javascript
App.js;

// 변수를 선언 후 사용 expoprt 시킨다
export const stockContext = React.createContext();

function App() {
  const [stockText, stockTextChange] = useState([10, 11, 12]);

  // html로 stockContext.Provider 만들어준다
  // value 사용할 state를 바인딩 해주면된다
  return (
    <stockContext.Provider value={stockText}>
      <GoodsList
        goods={goods}
        goodsTotal={goodsTotal}
        moreGoods={moreGoods}
        moreButtonShow={moreButtonShow}
      ></GoodsList>
    </stockContext.Provider>
  );
}
```

```javascript
goodsList.js;

// App.js에서 export한 변수를 impoprt 시킨다
import { stockContext } from "../App";

function App() {
  const testContext = useContext(stockContext);

  console.log(testContext)(
    // 결과값
    3
  )[(10, 11, 12)];
}
```
