# props

## 설명

부모 component에 있는 어떠한 값을 자식 component에 전달할 때 사용

---

### 예제

#### 기본

```javascript
function App() {
  let [title, titleChange] = useState(["제목1", "제목2", "제목3"]);

  return (
    // component 사용시 선언을 해줘야함
    <div>
      <Modal title={title}></Modal>
    </div>
  );
}

function Modal(props) {
  return (
    <div className="modal">
      // 사용시 state 앞에 props를 붙여줘야함
      <h2>제목: {props.title[0]}</h2>
      <p>날짜</p>
      <p>상세내용</p>
    </div>
  );
}
```
