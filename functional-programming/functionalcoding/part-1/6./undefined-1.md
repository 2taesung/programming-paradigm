# '얕은 복사', '깊은 복사' 활용

![](<../../../.gitbook/assets/image (17).png>)&#x20;



* 얕은 복사 : '얕은' 은 해당 층만의 복사라는 뜻이다. 그러므로 해당 층이 아닌 앞뒤로 레이어가 다른 데이터들은 얕은 복사로 연동된다.
* 깊은 복사 : 말 그대로 깊은 복사 레이어 상관 없이 해당 모든 것을 복사하는 것을 말한다. 그러므로 유기적으로 원본데이터와 연동 되는게 없다.

얕은 복사는 객체나 배열의 값을 복사하는 것이 아니라, 원본 객체나 배열의 참조만을 복사하는 것이다. 이것은 원본 객체나 배열이 변경될 경우, 복사된 객체나 배열 역시 함께 변경된다는 문제가 있다. 반면 깊은 복사는 객체나 배열의 값을 완전히 새로운 메모리 공간에 복사하는 것이다. 이러한 방식으로 복사된 객체나 배열은 원본 객체나 배열의 변경과 무관하게 독립적으로 동작한다.





### js 에서 깊은 복사 하는법



**JSON.parse()와 JSON.stringify()**

JSON.parse()와 JSON.stringify() 메소드를 사용하여 객체나 배열을 깊은 복사할 수 있다. 이 방식은 객체나 배열을 JSON 형태의 문자열로 변환한 후 다시 객체나 배열로 변환하는 방식으로 동작한다.



```javascript
const obj1 = { a: 1, b: { c: 2 } };
const obj2 = JSON.parse(JSON.stringify(obj1));

obj2.b.c = 3;

console.log(obj1); // { a: 1, b: { c: 2 } }
console.log(obj2); // { a: 1, b: { c: 3 } }

```

![](<../../../.gitbook/assets/image (7).png>)



\=> json 함수를 사용할 경우 문제가 발생할 수 있다.

JSON 객체를 이용한 깊은복사는 의도하지 않은 결과를 불러올 수 있습니다. JSON에서 사용 가능한 자료형은 number, string, boolean, object, array, null 입니다. 객체의 프로퍼티의 타입이 function일때 JSON.stringify를 쓸 때 undefined로 변환이이 되고, NaN은 null로 변환이 이루어집니다. 마찬가지로 다른 타입의 자료들도 변환이 되기때문에 유의해야합니다



고로 loadash를 써야함...

[https://velog.io/@th0566/Javascript-%EC%96%95%EC%9D%80-%EB%B3%B5%EC%82%AC-%EA%B9%8A%EC%9D%80-%EB%B3%B5%EC%82%AC](https://velog.io/@th0566/Javascript-%EC%96%95%EC%9D%80-%EB%B3%B5%EC%82%AC-%EA%B9%8A%EC%9D%80-%EB%B3%B5%EC%82%AC)

