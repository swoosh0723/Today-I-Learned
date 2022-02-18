# map

---

## 설명

javascript의 내장함수
map 함수는 파라미터로 전달된 함수를 사용해, 배열 각 요소를 원하는 규칙에 따라 변환한 다음 새로운 배열을 생성  
`arr.map(callbackFunction(currentValue, index, array), thisArg);`
나는 react에서 `map()`을 사용 UI를 만듬

---

### 예제

#### 기본

```javascript
function App() {
  const [title, titleChange] = useState(["제목1", "제목2", "제목3"]);

  return (
    <div className="App">
      // <!-- markdownlint-disable-next-line -->
      {
          title.map((item, i) => {
            <div className="list" key={i}>
              <h3>{item}</h3>
            </div>;
          })
      }
    </div>
  );
}
```
