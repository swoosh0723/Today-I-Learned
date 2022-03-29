# Array.prototype.slice()

## 설명

```javascript
arr.slice([begin[, end]])
```

`slice()` 메서드는 어떤 배열의 `begin`부터 `end`까지(end 미포함)에 대한 얕은 복사본을 새로운 배열 객체로 반환합니다.  
**`원본 배열은 바뀌지 않습니다.`**

- 원본 배열에서 요소의 얕은 복사본을 반환합니다. 원본 배열의 요소는 다음과 같이 반환 된 배열에 복사됩니다
- `String` 및 `Number` 객체가 아닌 문자열과 숫자의 경우 slice()는 문자열과 숫자를 새 배열에 복사합니다. 한 배열에서 문자열이나 숫자를 변경해도 다른 배열에는 영향을 주지 않습니다.
- 새 요소를 두 배열 중 하나에 추가해도 다른 배열은 영향을 받지 않습니다

---

## 예제

### 기본

```javascript
const animals = ["ant", "bison", "camel", "duck", "elephant"];

console.log(animals.slice(2));
// 결과값Array ["camel", "duck", "elephant"]

console.log(animals.slice(2, 4));
// 결과값 Array ["camel", "duck"]

console.log(animals.slice(1, 5));
// 결과값 Array ["bison", "camel", "duck", "elephant"]

console.log(animals.slice(-2));
// 결과값 Array ["duck", "elephant"]

console.log(animals.slice(2, -1));
// 결과값 Array ["camel", "duck"]

console.log(animals.slice());
// 결과값 Array ["ant", "bison", "camel", "duck", "elephant"]
```
