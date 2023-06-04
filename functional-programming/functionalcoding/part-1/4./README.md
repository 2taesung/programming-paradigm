# 4. 액션에서 계산 빼내기

* 순수 함수 만들기
* 테스트하기 쉽고 재사용성이 좋은 코드를 만들기 위한 함수형 기술
* 액션에서 계산으로 빼내는 방법



'액션'은 순수함수로 이루어지고 이 순수함수는 테스트하기 쉽고 재사용성이 좋다. 그러므로 액션에서 최대한 계산으로 빼내는 '리팩터링'이 중요하고 방법을 연습한다.





<details>

<summary>실습 소스코드</summary>

```javascript
var shopping_cart = []; // 장바구니 제품과 금액 합계를 담고 있는 전역변수
var shopping_cart_total = 0; // 장바구니 금액 합계를 담고 있는 전역변수

function add_item_to_cart(name, price) {
  shopping_cart.push({
    name: name,
    price: price,
  });
  calc_cart_total();
}

function calc_cart_total() {
  shopping_cart_total = 0;
  for(var i = 0; i < shopping_cart.length; i++) {
    shopping_cart_total += item.price;
  }
  set_cart_total_dom(); // 금액 합계를 반영하기 위해 DOM 업데이트
}
```

</details>



### 무료 배송비 계산하기, 세금 계산하기

#### 새로운 요구사항

* 구매 합계 20달러 이상이면 무료 배송이라는 뱃지 표시
* 판매 금액에 10% 세금

#### 절차적인 방법으로 구현하기

###
