# String.prototype.repeat()

## 설명

```javascript
string.repeat(count);
```

**`count`**  
문자열을 반복할 횟수. 0과 양의 무한대 사이의 정수

---

## 예제

### 기본

```javascript
const text = "apple";

text.repeat(2);

// 결과값
("appleapple");
```

### 예외

`count`는 반드시 양의 정수여야 함  
`count`는 무한대 보다 작아야함

```javascript
const text = "apple";

text.repeat(-2);
text.repeat(1/0));
```
