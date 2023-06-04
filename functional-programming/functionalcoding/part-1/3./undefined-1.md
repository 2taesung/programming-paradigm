# 새로 만드는 코드에 함수형 사고 적용하기

### 쿠폰독의 새로운 마케팅 전략&#x20;

쿠폰독은 쿠폰에 관심 있는 구독자들에게 이메일로 쿠폰을 매주 보내주는 서비스.

쿠폰독은 추천 친구 10명 이상을 추천하면 더 좋은 쿠폰을 보내주려함.



<figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

### 연습문제(액션/계산/데이터)

* 이메일 보내기
* 데이터베이스에서 구독자 가져오기
* 쿠폰에 등급 매기기
* 데이터베이스에서 쿠폰 읽기
* 이메일 제목



### 쿠폰 보내는 과정 그려보기

1. DB에서 구독자 가져오는 것

<mark style="background-color:green;">'시점'</mark>에 따라 구독자는 달라지기 때문에 <mark style="background-color:green;">'액션'</mark>

DB에서 가져온 <mark style="background-color:green;">'구독자 목록'</mark>은 <mark style="background-color:green;">'데이터'</mark>



2. DB에서 쿠폰 목록 가져오기&#x20;

<mark style="background-color:green;">'시점'</mark>에 따라 쿠폰 종류는 달라지기 때문에 <mark style="background-color:green;">'액션'</mark>

DB에서 가져온 <mark style="background-color:green;">'쿠폰 목록'</mark>은 <mark style="background-color:green;">'데이터'</mark>



3. 보내야 할 이메일 목록 만들기

'보내야 할' 이메일 목록은 DB를 가져오는게 아니라.

DB의 구독자 목록(데이터)와 쿠폰 목록(데이터)를 계산(join)시켜 '보내야 할' 이메일 목록을 만든다.

<mark style="background-color:green;">=> 위의 데이터는 시점에따라 바뀌는 것 아님?</mark>



아님. 위의 시점에 의존하는 액션과 데이터도 별개고 이 데이터들로 계산하는 이메일 목록 계획하는 것도 별개임. 왜? 이 계산은 인자로 데이터들을 받는 것일 뿐. 이 데이터들이 없다고 에러가 생기거나 하지 않음.

계산은 input, output이 분명한 순수 함수, 수학 함수 일 뿐이다.

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



4. 이메일 전송하기

'이메일 목록(데이터)'을 참고해 '이메일 전송'



### 이메일 만드는 부분 까보기

* 왜 아직 요청 오지도 않은 보내야 할 이메일 목록을 미리 만들어야하는가?

액션에 해당하는 큰 덩어리에서 쪼개서 계산과 데이터로 최대한 바꿔주는 것.



* 왜 가능한 계산으로 만들어야하는가?

테스트하기 쉽기 때문.



### 추가 팁

* 이것은 계산인가? 같은 input 이면 같은 output인가? ㅇ 호출 횟수가 영향을 주는가 ? x
* 일반적으로 액션도 함수, 계산도 함수 그래서 함수만으로 판단이 불가
* 데이터를 먼저 구현하고&#x20;

