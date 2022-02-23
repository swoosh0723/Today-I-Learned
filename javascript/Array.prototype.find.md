# Array.prototype.find()

## 설명

**`array.find()`**  
 메서드는 주어진 판별 함수를 만족하는 **_첫 번째 요소의_** 값을 반환합니다. 그런 요소가 없다면 undefined를 반환합니다.

---

## 예제

### 기본

```javascript
const nike = [
  {
    name: "airmax",
    quantity: 2,
  },
  {
    name: "jordan",
    quantity: 0,
  },
  {
    name: "airforce",
    quantity: 5,
  },
];

const result = nike.find((item) => {
  return item.quantity > 1;
});

// 결과값
{ name: 'airmax', quantity: 2 }
```

`return item.quantity > 1;` airmax, airforce 해당되지만  
`find()`는 **첫 번째 요소**의 값만 반환
