# 이미 있는 코드에 함수형 사고 적용하기

```javascript
function figurePayout(affiliate) {
  var owed = affiliate.sales * affiliate.commission;
  if(owed > 100)
    sendPayout(affiliate.bank_code, owed); // 이 코드만 액션일까요?
}

function affiliatePayout(affiliates) {
  for(var a = 0; a < affiliates.length; a++)
    figurePayout(affiliate[a]);
}

function main(affiliates) {
  affiliatePayout(affiliates);
}
```



\=> 위의 있는 코드를 가지고 생각해본다.

```javascript
sendPayout(affiliate.bank_code, owed);
```

해당 코드는 액션이다. 실제 돈을 송금하는 시점이나 횟수가 중요하기 때문.

송금하는 시점의 금액 액수, 그리고 첫번째 송금하는 것과 두번째 송금하는게 남은 잔액이 다를거고 등등..



그런데 문제는 액션에 해당하는 함수가 있다면 <mark style="background-color:green;">관여된 모든 곳들로 전염병</mark> 퍼뜨리듯 퍼진다는 점이다.



### 액션은 코드 전체로 퍼집니다.

액션은 사용하기 참 어렵습니다. 액션을 부르는 함수가 있다면 그 함수도 액션이 됩니다. 또 그 함수를 부르는 다른 함수도 역시 액션이 됩니다. 이런 식으로 작은 액션 하나가 코드 전체로 퍼져 나갑니다.



그렇다면 어떻게 사용해야하나요 ?



### 액션은 다양한 형태로 나타납니다.

<mark style="background-color:green;">함수형 프로그래머는 액션을 관리하는 법을 배웁니다.</mark>

아래는 액션의 다양한 종류들

* 함수호출
* 메서드 호출
* 생성자
* 표현식
* 상태

### 액션을 잘 사용하기 위한 방법

1. 가능한 액션을 적게 사용합니다.
2. 액션은 가능한 작게 만듭니다.
3. 액션이 외부 세계와 상호작용하는 것을 제한할 수 있습니다.
4. 액션이 호출 시점에 의존하는 것을 제한합니다.



### 결론&#x20;

<mark style="background-color:green;">액션을 통해 계산으로 만드는 계획</mark>을 실행할 수 있습니다.
