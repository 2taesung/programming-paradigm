# 테스트하기 쉽게 만들기

### 지금 코드는 비즈니스 규칙을 테스트하기 어렵습니다.

테스트를 만드는 과정은

1. 브라우저 설정하기
2. 페이지 로드하기
3. 장바구니에 제품 담기 버튼 클릭
4. <mark style="background-color:green;">DOM이 업데이트될 때까지 기다리기</mark>
5. <mark style="background-color:green;">DOM에서 값 가져오기</mark>
6. 가져온 문자열 값을 숫자로 바꾸기
7. 예상하는 값과 비교하기



### 테스트 개선을 위한 제안

* 'DOM 업데이트'와 '비즈니스 규칙'의 분리
* 전역변수가 없어야 합니다.
