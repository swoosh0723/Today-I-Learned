# Array.prototype.findIndex()

## 설명

**`array.findIndex()`**  
 주어진 판별 함수를 만족하는 배열의 **_첫 번째 요소_**에 대한 **_인덱스_**를 반환합니다.  
 만족하는 요소가 없으면 -1을 반환합니다.

---

## 예제

### 기본

```javascript
const numberArrary = [1, 2, 5, 100, 20];

const test1 = numberArrary.findIndex((e) => e > 1);
const test2 = numberArrary.findIndex((e) => e > 10);
const test3 = numberArrary.findIndex((e) => e === 20);
const test4 = numberArrary.findIndex((e) => e === 11);

// 결과값
test1: 1;
test2: 3;
test3: 4;
test4: -1;
```
