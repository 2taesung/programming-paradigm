# 메시지와 메서드

### 메시지

사용자에 대한 객체의 독립성과 객체지향 개념을 구현한 초기 언어들의 일부 문법 때문에 객체의 행동을 유발하는 행위를 가리켜 메시지-전송이라고 한다.



메시지를 전송할 때 추가적인 정보가 필요한 경우 메시지의 인자를 통해 추가 정보를 제공할 수 있다.



왕이 전송하는 메시지의 인자를 이용해 '언제'와 '어디서'라는 추가적인 정보를 실어 보낸다.



"모자장수, 증언하라(어제, 왕국)"

메시지 전송은 수신자와 메시지의 조합이다.



근본적으로 메시지의 개념은 책임의 개념과 연결된다.

객체가 수신할 수 있는 메시지의 모양이 객체가 수행할 책임의 모양을 결정한다.

따라서 모자 장수가 메시지를 변경하지만 않는다면 책임을 수행하는 방법을 변경하더라도 왕은 그 사실을 알 수 없다. 이것은 <mark style="background-color:green;">객체의 외부와 내부가 메시지를 기준으로 분리된다는 것을 의미</mark>한다.&#x20;



객체가 제공하는 메시지는 외부의 다른 객체가 볼 수 있는 공개된 영역에 속한다. 메시지를 처리하기 위해 책임을 수행하는 방법은 외부의 다른 객체가 볼 수 없는 객체 자신의 사적인 영역에 속한다.



### 메서드&#x20;

모자 장수가 메시지를 처리하기 위해 내부적으로 선택하는 방법을 메서드라고 한다.



어떤 객체에게 메시지를 전송하면 결과적으로 메시지에 대응되는 특정 메서드가 실행된다.

메시지는 단지 오퍼레이션을 통해 '무엇'이 실행되기를 바라는지만 명시하며, 어떤 메서드를 선택할 것인지는 전적으로 수신자의 결정에 좌우된다.



메시지를 수신한 객체가 실행 시간에 메서드를 선택할 수 있다는 사실은 다른 프로그래밍 언어와 객체지향 프로그래밍 언어를 구분 짓는 핵심적인 특징 중 하나다.



### 다형성 => 스케줄링 기능인데 기기에 따라 다르게 작동

다형성이란 서로 다른 유형의 객체가 동일한 메시지에 대해 서로 다르게 반응하는 것을 의미한다.

다형성을 하나의 메시지와 하나 이상의 메서드 사이의 관계로 볼 수 있다.



'전송 하라'라는 동일한 메시지를 처리하는 방법은 메시지를 수신하는 수신자의 종류에 따라 달라진다.



다형성은 역할, 책임, 협력과 깊은 관련이 있다. 서로 다른 객체들이 다형성을 만족시킨다는 것은 객체들이 동일한 책임을 공유한다는 것을 의미한다.



송신자의 관점에서 다형적인 수신자들을 구별할 필요가 없으며 자신의 요청을 수행할 책임을 지닌다는 점에서 모두 동일하다.



다형성은 메시지 송신자의 관점에서 동일한 역할을 수행하는 다양한 타입의 객체와 협력할 수 있게 한다.



기본적으로 다형성은 동일한 역할을 수행할 수 있는 객체들 사이의 대체 가능성을 의미한다.



대체 가능한 존재라는 사실을 의미한다. 이들이 대체 가능한 이유는 왕의 관점에서 동일한 메시지를 처리할 수 있기 때문이다.&#x20;

예를 들어, 왕의 입장에서 요리사와 앨리스는 모자 장수를 대신해서 증언할 수 있다. 이것은 모자 장수, 요리사, 앨리스가 협력 안에서 대체 가능한 존재라는 사실을 의미한다.



메시지를 처리하는 방법인 메서드는 달라지더라도 말이다.



즉, 다형성은 수신자의 종류를 캡슐화한다.

따라서, 왕에게 영향을 주지 않고도 메시지를 수신할 객체의 타입을 자유롭게 추가할 수 있다.



<mark style="background-color:green;">다형성은 송신자와 수신자 간의 객체 타입에 대한 결합도를 메시지에 대한 결합도로 낮춤으로써 달성</mark>된다. 객체지향이 유연하고 확장 가능하고 재사용성이 높다는 명성을 얻게 된 배경에는 다형성이라는 강력한 무기가 있었기 때문.



### 유연하고 확장 가능하고 재사용성이 높은 협력의 의미

첫째, 협력이 유연해진다.

송신자는 수신자가 메시지를 이해한다면 누구라도 상관하지 않는다.



둘째, 협력이 수행되는 방식을 확장할 수 있다.

'증언하라' 라고 메시지를 기반으로 느슨한 관계만 존재하기 때문에 재판장에 출석하지 않고 동영상만 보내는 객체라도 책임만 완수할 수 있다면 쉽게 수용할 수 있다.



셋째, 협력이 수행되는 방식을 재사용할 수 있다.

협력에 영향을 미치지 않고서도 다양한 객체들이 수신자의 자리를 대체할 수 있기 때문에 다양한 문맥에서 협력을 재사용할 수 있따.



### 송신자와 수신자를 약하게 연결하는 메시지

메시지를 기반으로 한 두 객체 사이의 이 낮은 결합도가 바로 설계를 유연하고 확장 가능하며 재사용 가능하게 만드는 비결이다. 따라서 <mark style="background-color:green;">설계의 품질을 높이기 위해서는 훌륭한 메시지를 선택해야한다.</mark>












