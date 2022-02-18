# useState

## 설명

변수 대신 사용하는 데이터 저장공간  
useState()를 이용해 만들어야함  
`const [data, dataChange] = useState(initialData)`  
최초로 랜더링 될 때 `data`는 `initialData`와 동일

---

### state의 장점

- 웹이 App처럼 동작하게 만들고 싶어서
- state는 변경되면 HTML이 자동으로 재렌더링 됩니다
- 그냥 변수로 데이터 만들고 사용하면 새로고침을 해야함
- !!새로고침없이 스무스하게 만들고싶다!!! useState
- 자주 바뀌는, 중요한 데이터는 변수 말고 state로 저장해서 사용

---

### 예제

#### 기본

```javascript
const [data, dataChange] = useState(["0", "1", "2"]);
```

#### deep copy

**deep copy**를 해야한다. (react의 대원칙: immutable data)

```javascript
const [data, dataChange] = useState(["0", "1", "2"]);

const newData = [...data];
newData.push("3");
dataChange(newData);
```
