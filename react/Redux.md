# Redux

## 설명

redux를 사용하는 이유 ?  
props 전송 없이도 모든 컴포넌트들이 state를 사용할 수 있게 만들어준다.

**`Store`**

**`Action`**  
상태에 변화가 필요할 때 발생하는 하나의 객체를 의미합니다. 액션의 이름인 type 필드를 필수로 포함한 구조로 되어 있다.

**`Reducer`**  
변화를 일으켜 새로운 상태를 반환하는 함수입니다. state와 action을 파라미터로 받아옴

**`Dispatch`**  
스토어의 내장 함수이며 액션을 발생시킵니다. 액션 객체를 파라미터로 받아서 호출합니다. dispatch가 호출되면 스토어의 리듀서가 실행되어 새로운 상태를 반환합니다.

**`useSelector`**  
redux의 state조회 (즉, 스토어에 있는 데이터들 조회)

**`useDispatch`**  
생성한 action 실행

---

##

### 기본

```javascript
// index.js
// redux
import { Provider } from 'react-redux'
import { createStore, combineReducers } from 'redux';

const goodsData = [
  {
    id: 0,
    image: "https://image.msscdn.net/images/goods_img/20200918/1611805/1611805_1_500.jpg",
    brand: "무신사 스탠다드",
    name: "무신사 스탠다드 코트",
    content: "Born in France",
    price: 120000,
    rate: "30%",
    stock: 3
  },

  {
    id: 1,
    image: "https://image.msscdn.net/images/goods_img/20210201/1771542/1771542_1_500.jpg",
    brand: "Nike",
    name: "에어포스1",
    content: "Born in Seoul",
    price: 110000,
    rate: "20%",
    stock: 2
  },
]

const basicState = dataGoods;

function reducer(state = basicState, action) {
  if (action.type === "add") {
    return addState;
  } else {
    return state;
  }
}

const basicState2 = true;

function reducer2(state = stateBasic, action){
  return state;
}

const store = createStore(combineReducers({ reducer, reducer2 }))

// Provider로 감싸주고 store를 바인딩 해준다
ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>
}

// component.js
import { useDispatch, useSelector } from 'react-redux'

// useSelector
const cartData = useSelector((state) => state)
const dispatch = useDispatch();

// cartData의 결과값
// index.js에서 선언한 함수 state를 모두가져온다
// {reducer: Array(2), reducer2: true}

// const cartData = useSelector((state) => state.reducer)
// cartData의 결과값
// (2) [{…}, {…}]

<button
  onClick={() => {
    dispatch({ type: "addState" });
  }}
>
  더하기
</button>
```
