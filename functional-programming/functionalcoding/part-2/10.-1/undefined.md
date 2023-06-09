# 암묵적 인자를 드러내기

### 일급인 것과 일급이 아닌 것을 구별하기

js에서 일급이 아닌 것

* 수식 연산자
* 반복문
* 조건문
* try/catch 블록



### 필드명을 문자열로 사용하면 버그가 생기지 않을까요?

이 문제를 해결하는 방법은&#x20;

1. 컴파일 타입 검사 (ts...?)
2. 런타임 검사



### 객체와 배열을 너무 많이 쓰게 됩니다.

중요한 것은 데이터를 사용할 때 임의의 인터페이스로 감싸지 않고 그대로 사용하고 있다는 점입니다. 인터페이스를 잘 만들면 데이터를 정해진 방법으로만 쓸 수 있습니다.



데이터를 데이터 그대로 사용하는 것의 중요한 장점은 <mark style="background-color:green;">여러 가지 방법으로 해석</mark>할 수 있다는 점입니다.

비교하여 제한된 API로 정의하면 정해진대로만 사용 가능합니다.



이것은 <mark style="background-color:green;">'데이터 지향'</mark>이라는 중요한 원칙입니다.



### 추가 팁

Q. 정적 타입 vs 동적 타입?

어떤 연구에서는 정적 타입 언어와 동적 타입 언어를 구분하는 것보다 소프트웨어 품질을 위해 숙면을 하는 것이 더 중요하다고 합니다.



Q. 모두 문자열로 통신합니다.

오타나 잘못된 문자열로 인한 에러가 종종 발생하는 것도 맞습니다. 하지만 동적 언어로 만든 수십억 이상의 단위의 비즈니스 시스템이 잘 운영되고 있습니다.

정적 타입 언어가 할 수 있는 것은 시스템에 있는 어떤 코드가 가진 타입이 일관되도록 보장해 주는 일입니다.



### 자연스럽게 콜백으로 넘어가기

암묵적인자로 드러내면서 함수가 일반적이게 변화했습니다.

여기에 함수 인자로 함수가 들어가게 되면 '고차 함수'가 됩니다.(forEach)

\=> 이러한 고차함수들을 소개하고 자유롭게 활용하는 것을 유동근씨가 하는 강의인거고



그러면서 이러한 고차함수를 만드는 과정을 '함수 본문을 콜백으로 바꾸기' 방식입니다.

