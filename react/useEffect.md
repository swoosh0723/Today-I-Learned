# useEffect

## [useEffect란?]

리액트 component는 라이프 사이클이 존재한다.\
'생성(mounting) -> 업데이트(updating) -> 제거(numoutin)'의 생명주기를 갖는다.\
생명주기의 때에 따라 특정 작업을 처리할 수 있다.\
불필요한 updating을 방지할 수 있다.\

## [useEffect 예제]

- useEffect는 mouting, updating마다 실행된다
- component의 다른 부분이 updating도 아래 const = timer는 실행된다
- 불필요하다
- 원하는 것이 updating 될 때만 실행할 수가 있다
- []에는 useEffect가 updating 될 때 실행 조건
- ex) [alert] 해당 state가 변경될 때 (updating 될 때) 실행
- tip. [] 빈칸으로 두면 한 번만 실행되고 끝

```
const [alert, alertChange] = useState(true);

useEffect(() => {
  // mounting 될 때 실행
  // []가 없다면 ... updating 될 때 실행
  const timer = setTimeout(()=>{
    alertChange(false)

    console.log('!!!')
  },2000)


  // return은 numouting 될 때 실행
  return () => {
    clearTimeout(timer);
  }
  // alert가 updating될 때
}, [alert])
```
