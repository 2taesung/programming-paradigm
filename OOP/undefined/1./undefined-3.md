# 객체지향의 본질

* 객체지향이란 시스템을 상호작용하는 자율적인 객체들의 공동체로 바라보고 객체를 이용해 시스템을 분할하는 방법
* 자율적인 객체란 상태와 행위를 함께 지니며 스스로 자기 자신을 책임지는 객체를 의미한다.
* 객체는 시스템의 행위를 구현하기 위해 다른 객체와 협력한다. 각 객체는 협력 내에서 정해진 역할을 수행하며 역할은 관련된 책임의 집합니다.
* 객체는 다른 객체와 협력하기 위해 메시지를 전송하고, 메시지를 수신한 객체는 메시지를 처리하는 데 적합한 메서드를 자율적으로 선택한다.

<mark style="background-color:orange;">=> 근데 결국에는 객체인 class가 메시지에 따라 선택하는게 아니라</mark>

<mark style="background-color:orange;">=> 내가 메시지에 따라 필요한 class의 method를 쓰는게 아닌가 ....?</mark>



### 객체를 지향하라

'언어가 인간의 사고를 지배한다'

눈을 의미하는어휘의 수가 400개라는 에스키모인들이 한국인들보다 빙하 크레바스에 빠질 가능성이 훨씬 적다.



눈을 지칭하는 많은 어휘가 존재하기 때문에 한국인에 비해 눈에 관해 좀 더 상세하고 정확하게 생각할 수 있다는 것.

\=> 결과적으로 이건 과장의 과장이 펙트처럼 전해진 것. 실제로는 2개.



어쨌든 객체지향의 세계에서 클래스(class)는 에스키모인들의 눈과 유사.



초기 객체지향 프로그래밍 언어의 초점은 새로운 개념의 데이터 추상화를 제공하는 클래스라는 빌딩 블록에 맞춰져 있었다. 그러다보니 class에 집중하고 class간의 상속에 집착하고 그러다보니 높은 결합도를 가지며 객체의 캡슐화를 저해하고 클래스를 서로 강하게 결합시킨다.



훌륭한 객체지향 설계자가 되기 위해 거쳐야 할 첫 번째 도전은 <mark style="background-color:green;">'코드를 담는 클래스의 관점에서 메시지를 주고받는 객체의 관점'</mark>으로 사고의 중심을 전환하는 것.



핵심은 <mark style="background-color:green;">'적절한 책임을 수행하는 역할 간의 유연하고 견고한 협력 관계를 구축'</mark>하는 것이다.
