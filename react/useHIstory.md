# useHistory

## 사용방법

1. `npm install react-router-dom` 설치한다
2. `import { useHistory } from 'react-router-dom'` 문서에 import 시킨다

---

## 설명

페이지 이동내역 + 유용한 함수

---

## 예제

### 기본

```javascript
function App() {
  const history = useHistory();

  return (
    <div>
      // 원하는 path로 이동
      <button
        type="button"
        onClick={() => {
          history.push("/");
        }}
      >
        홈화면으로
      </button>
      // 뒤로 이동
      <button
        type="button"
        onClick={() => {
          history.goBack();
        }}
      >
        뒤로가기
      </button>
    </div>
  );
}
```
