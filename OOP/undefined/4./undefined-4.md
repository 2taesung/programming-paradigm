# 객체지향 설계 기법

1. 책임-주도 설계(Responsibility-Driven Design) 방법은 협력에 필요한 책임들을 식별하고 적합한 객체에게 책임을 할당하는 방식으로 애플리케이션을 설계한다.
2. 디자인 패턴(Design Pattern)은 전문가들이 반복적으로 사용하는 해결 방법을 정의해 놓은 설계 템플릿의 모음이다. 패턴은 전문가들이 특정 문제를 해결하기 위해 이미 식별해 놓은 역할, 책임, 협력의 모음이다.
3. 테스트-주도 개발(Test-Driven Development) 방법이다. 이 방법은 테스트가 중요한게 아니라 설계를 위한 기법이다. 실제 목적은 구체적인 코드를 작성해나가면서 역할, 책임, 협력을 식별하고 식별된 역할, 책임, 협력이 적합한지를 피드백받는 것이다.

### 책임-주도 설계

객체지향 시스템은 역할과 책임을 수행하는 자율적인 객체들의 공동체다. 결국 객체지향 설계란 애플리케이션의 기능을 구현하기 위한 협력 관계를 고안하고, 협력에 필요한 역할과 책임을 식별한 후 이를 수행할 수 있는 적절한 객체를 식별해 나가는 과정.



객체지향 설계의 핵심은 올바른 책임을 올바른 객체에게 할당하는 것이다.



전체 개발 단계에 걸쳐 객체의 역할과 책임, 협력을 도드라지게 만드는 기법과 체계를 따르는 것이 중요하다.



현재 가장 대세는 책임-주도 설계(RDD)



객체가 다른 객체에게 작업을 요청하는 행위를 통해 결과적으로 객체들 간의 협력 관계가 만들어진다. 만약 책임을 여러 종류의 객체가 수행할 수 있다면 협력자는 객체가 아니라 추상적인 역할로 대체된다.



### 디자인 패턴

디자인 패턴은 책임-주도 설계의 결과를 표현한다.&#x20;

반복적으로 발생하는 문제와 그 문제에 대한 해법이 쌍으로 정의됨.

패턴은 반복해서 일어나는 특정한 상황에서 어떤 설계가 왜 더 효과적인지에 대한 이유를 설명.



대표적인 예시는 COMPOSITE 패턴



디자인 패턴은 책임-주도 설계의 결과물인 동시에 지름길.



### 테스트-주도 개발

테스트-주도 개발을 통해 '작동하는 깔끔한 코드(clean code that works)'를 얻을 수 있다.



테스트-주도 개발은 객체가 이미 존재한다고 가정하고 객체에게 어떤 메시지를 전송할 것인지에 관해 먼저 생각하라고 충고한다. 그러나 이 같은 종류의 충고는 역할, 책임, 협력의 관점에서 객체를 바라보지 않을 경우 무의미하다.











