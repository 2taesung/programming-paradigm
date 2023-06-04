# '읽쓰' 분리하기

### 1. 읽기와 쓰기 함수로 각각 분리

(추천하는 방법)

먼저 쓰기에서 읽기를 분리.

'쓰기' 부분을 '카피-온-라이트'를 적용해 '읽기'로 변경



'읽기' 부분인 요소 return 부분을 함수로 분리

```javascript
function first_element(array) {
    return array[0];
}
```



그리고  '쓰기' 부분인 array에서 요소를 제거 부분을 함수로 분리(shift는 그대로 쓰면 됨)

```javascript
function drop_first(array) {
    array.shift()
}
```



읽기와 쓰기를 분리하면 각각 역시 재사용이 가능하기 때문에 추천.



### 2. 함수에서 값을 두 개 리턴

쉽게 생각해 const \[state, setState] = useState();

```javascript
return {
    first: first,
    array: array_copy
}
```



### 3. 이 둘을 조합하는 방법

```javascript
return {
    first: first_element(array),
    array: drop_first(array)
}
```

\=> 사실 이 또한 1번 방법의 활용인셈.
