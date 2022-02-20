# Array.prototype.push()

## 설명

**`array.push()`**  
배열의 **_맨 끝_** 에 값을 추가한다  
배열의 length를 return한다

---

## 예제

### 기본

```javascript
const array1 = [0, 1, 2, 3];

array1.push(4);

// 결과값
[0, 1, 2, 3, 4];
```

### return은 length

```javascript
const sprots = ["soccer", "baseball"];
const total = sprots.push("swimming", "marathon");

// 결과값
console.log(sprots);
["soccer", "baseball", "swimming", "marathon"];

console.log(total);
4;
```

### 두개의 배열 합치기

`apply()`를 사용하여 두개의 배열을 합칠 수 있다

```javascript
const nikeShoes = ["airmax", "air-force1", "jordan"];
const adidasShoes = ["superstar", "Yesszy"];

Array.prototype.push.apply(nikeShoes, adidasShoes);

// 결과값
["airmax", "air-force1", "jordan", "superstar", "Yesszy"];
```
