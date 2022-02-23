# useParams

## 설명

useParams을 이용해 동적 라우팅 하는방법

---

## 예제

### 기본

1. App.js Route에 id값을 지정해준다

```javascript
<Route exact path="/detail/:id"></Route>
```

2. component에 useParams import

```javascript
import { useParams } from "react-router-dom";
```

3. component에서 useParams 사용

```javascript
const { id } = useParams();

/detail/119

119는 위에 {}에 들어간다
```

4. 상품id값과 파라미터와 맞추려면

```javascript

const goodsItem = props.goods.find((item)=>{
  return item.id = id
})

- 3번에서 입력한 파라미터와 props.goods의 id값을
- find()를 사용하여 비교하여 goodsItem으로 반환

const goodsItem = props.goods[119]
```

5. component에 data 바인딩

```javascript
<>
  <Brand>{props.goods[119].brand}</Brand>
  <Name>{props.goods[119].name}</Name>
  // // // // // 같은것 // // // // //
  <Brand>{goodsItem.brand}</Brand>
  <Name>{goodsItem.name}</Name>
</>
```
