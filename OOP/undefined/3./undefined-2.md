# 타입

### 타입은 개념이다.

공학자들은 개념을 대체할 수 있는 좀 더 세련돼 보이는 용어를 수학으로부터 차용해 왔다. 그것은 바로 타입(type)이다.



예를 들어, 이 문제의 개념은 뭐야 ? 라고 하면 객체지향에서는 해당 객체의 타입은 뭐야? 이런식



<mark style="background-color:green;">타입은 개념과 마찬가지로 심볼, 내연, 외연을 이용해 서술할 수 있으며 타입에 속하는 객체 역시 타입의 인스턴스라고 한다.</mark>



타입은 근본적으로 개념과 동일하다고 하더라도 일단 컴퓨터 내부로 들어오는 순간 좀 더 기계적인 의미로 윤색될 수 밖에 없다. 그리고 기계적인 의미는 종종 개발자들의 머리를 혼란스럽게 만든다.



### 데이터 타입

사람이 어떤 일을 수행하기 위해서는 장기 기억 속에 묻혀진 기억의 편린들을 단기 기억 속으로 불러들여야만 하는 것처럼 컴퓨터가 어떤 작업을 수행하기 위해서는 작업에 필요한 데이터를 메모리 안으로 불러들여야 한다. 메모리에 불러들여진 데이터들은 무수히 많은 0과 1로 치장되어 메모리에 저장된다.



실제로 '타입이 없다(Untyped)'라는 말은 메모리 안의 데이터를 다룰 수 있는 단 하나의 타입만이 존재한다는 것을 의미힌다.



애플리케이션 안에서 타입이 없는 메모리 내부의 값을 다루다 보면 수많은 오해와 시행착오에 부딛히게 된다. 메모리 안에 저장된 '10010001'이라는 값은 숫자인가, 문자인가, 아니면 특정한 메모리 상의 주소인가? 혼란은 혼란을 낳고 프로그래머를 정신 착란으로 몰고 가다가 급기야는 데이터를 잘못 사용해서 애플리케이션을 죽음의 길로 몰고 가기도 한다.



<mark style="background-color:green;">결과적으로 타입 시스템의 목적은 데이터가 잘못 사용되지 않도록 제약사항을 부과하는 것이다.</mark>



첫째, 타입은 데이터가 어떻게 사용되느냐에 관한 것이다.



일반적으로 데이터를 이용해 수행할 수 있는 작업은 연산자(operator)라고 한다.



둘째, 타입에 속한 데이터를 메모리에 어떻게 표현하는지는 외부로부터 철저하게 감춰진다.



### 객체와 타입

객체를 타입에 따라 분류하고 그 타입에 이름을 붙이는 것은 결국 프로그램에서 사용할 새로운 데이터 타입을 선언하는 것과 같다.



그렇다면 객체는 데이터인가? 그렇지 않다. 다시 한번 강조하지만 객체에서 중요한 것은 객체의 행동이다. 상태는 행동의 결과로 초래된 부수효과를 쉽게 표현하기 위해 도입한 추상적인 개념일 뿐이다.



객체가 협력을 위해 어떤 책임을 지녀야 하는지를 결정하는 것이 객체지향 설계의 핵심이다.



첫째, 어떤 객체가 어떤 타입에 속하는지를 결정하는 것은 객체가 수행하는 행동이다. 어떤 객체들이 동일한 행동을 수행할 수 있다면 그 객체들은 동일한 타입으로 분류될 수 있다.&#x20;

<mark style="background-color:orange;">=> TS에서 return 값????</mark>



둘째, 객체의 내부적인 표현은 외부로부터 철저하게 감춰진다. 객체의 행동을 가장 효과적으로 수행할 수 만 있다면 객체 내에서 상태를 어떤 방식으로 표현하더라도 무방하다.



### 행동이 우선이다.

객체의 내부 표현 방식이 다르더라도 어떤 객체들이 동일하게 행동한다면 그 객체들은 동일한 타입에 속한다. 결과적으로 동일한 책임을 수행하는 일련의 객체는 동일한 타입에 속한다고 말할 수 있다.



결론적으로 객체의 타입을 결정하는 것은 객체의 행동뿐이다. 객체가 어떤 데이터를 보유하고 있는지는 타입을 결정하는 데 아무런 영향도 미치지 않는다.



동일한 타입에 속한 객체는 내부의 데이터 표현 방식이 다르기 때문에 동일한 메시지를 처리하는 방식은 서로 다를 수밖에 없다. 이것은 다형성에 의미를 부여한다. <mark style="background-color:green;">다형성이란 동일한 요청에 대해 서로 다른 방식으로 응답할 수 있는 능력을 뜻한다.</mark>



따라서 <mark style="background-color:green;">훌륭한 객체지향 설계는 외부에 행동만을 제공하고 데이터는 행동 뒤로 감춰야 한다. 이 원칙을 흔히 캡슐화라고 한다.</mark>



행동에 따라 객체를 분류하기 위해서는 객체가 내부적으로 관리해야 하는 데이터가 아니라 객체가 외부에 제공해야 하는 행동을 먼저 생각해야 한다.



<mark style="background-color:green;">데이터를 먼저 결정하고 객체의 책임을 결정하는 방법은 유연하지 못한 설계라는 악몽을 초래한다. 흔히 책임-주도 설계(Responsibility-Driven Design)라고 부르는 객체지향 설계 방법은 데이터를 먼저 생각하는 데이터-주도 설계(Data-Driven Design) 방법의 단점을 개선하기 위해 고안됐다.</mark>



앨리스가 그들을 동일한 타입으로 분류한 이유는 그들이 동일한 방식에 따라 행동했기 때문이다.




