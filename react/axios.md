# axios

## 설명

> 우선 AJAX?
> AJAX란, javascript의 라이브러리 중 하나.
> 페이지를 **새로고침 없이** 페이지 일부만을 위한 데이터 로드하는 기법
> **자바스크립트를 통해서 서버에 데이터 요청하는 것**  
> `GET`: 지정된 데이터를 요청
> `POST`: 데이터를 서버에 전달

axios는 브라우저, Node.js를 위한 Promise API를 활용하는 HTTP 비동기 통신의 라이브러리
fetch api라브러리가 있지만, react에선 axios를 선호
제일큰 장점은 JSON 형태로 자동 변경해준다.

---

## 사용방법

1. `npm install axios` 설치한다
2. `import axios from 'axios'` 문서에 import 시킨다

---

## 예제

### 기본

- 성공하면 then()
- 실패하면 catch()

```javascript
axios
  .get("URL")
  .then((result) => {
    console.log(result.data);
  })
  .catch(() => {
    console.log("실패함");
  });
```
