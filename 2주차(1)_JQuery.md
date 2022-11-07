# [스파르타코딩클럽] 웹개발 종합반 - 2주차
## 2주차 : 배울 것
### jQuery

HTML 파일을 받았다고 가정 , Javascript로 다시 서버에 데이터를 요청하고 받는 방법을 배운다.

jQuery를 이용해 Javascript로 HTML을 쉽게 제어하고, 

Ajax를 이용해 다시 서버에 데이터를 요청하고 받아본다.

![01](https://user-images.githubusercontent.com/108924832/198628843-81545cd0-b75a-473c-899b-365be5852dce.PNG)

## Javascript 복습 - 홀짝 판별 onclick 함수 만들기
- 짝/홀수 판단하는 방법
```
let number = 4;
// 2로 나눴을 때 나머지 : 0
console.log(number % 2);

let number2 = 5;
// 2로 나눴을 때 나머지 : 1
console.log(number2 % 2);
```
### HTML 코드
- 웹페에지를 열고 버튼을 누르면 화면에 홀수 or 짝수 를 알려주는 메세지(alert) 를 띄운다.

![01](https://user-images.githubusercontent.com/108924832/198640681-130cf381-e58f-42d5-b717-bbad785b0e13.PNG)

### 결과

![01](https://user-images.githubusercontent.com/108924832/198642180-bc5ba8b2-f7bc-4dd9-ac5b-14e2404a86fe.PNG)

![02](https://user-images.githubusercontent.com/108924832/198642324-bc61b323-9923-43e9-a868-552250e9c964.PNG)

### Javascript 만으로 충분할까?
- 만약 버튼의 색깔을 바꾸고 싶다면?
- div 박스를 하나 감추고 싶다면?

자바스크립트만으로도 가능하지만 어렵다, 그래서 jQuery가 필요한 것이다.

## JQuery 시작하기
### jQuery 란?
- HTML의 요소들을 조작하는, 편리한 Javascript를 미리 작성해둔 것(라이브러리 라고 부름)
```
Javascript로도 모든 기능(예 - 버튼 글씨 바꾸기 등)을 구현할 수는 있지만 단점이 있다.

1. 코드가 복잡해진다.
2. 브라우저 간 호환성 문제도 고려해야한다.
> jQuery라는 라이브러리가 등장하게된 이유
```
