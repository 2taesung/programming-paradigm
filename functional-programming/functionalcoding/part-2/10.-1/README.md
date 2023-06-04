# 10. 일급 함수 1

<mark style="background-color:green;">코드의 냄새</mark>와 <mark style="background-color:green;">중복</mark>을 없애 추상화를 잘할 수 있는 리펙터링 두가지 방법



\*코드의냄새: 함수 이름에 있는 암묵적 인자

일반적으로 작명하는 함수명은 우리가 추구하는  일급함수를 만드는데&#x20;

필수적으로 잡아내야하는 <mark style="background-color:green;">'암묵적 인자'</mark>를 찾는 멋진 단서가 된다.



### 리펙터링

&#x20;1\. 암묵적 인자를 드러내기

암묵적 인자가 일급 값(명시적 인자)이 되도록 합니다.

2.함수 본문을 콜백으로 바꾸기

