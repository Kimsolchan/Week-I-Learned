# [스파르타코딩클럽] 웹개발 종합반 - 1주차
## Javascript(자바 스크립트) 기초
### 자바스크립트란
- 프로그래밍 언어 중 하나로, 브라우저가 알아들을 수 있는 언어
```
클라이언트 -> 서버로 요청

서버 -> 클라이언트(HTML+CSS+Javascript를 보내준다)

== 브라우저는 Javascript만 알아듣는가? ==
HTML 안에 파이썬 , Java 같은 언어를 써서 줘도 되자만
"역사적인 이유 & 이미 만들어진 표준"이기 때문에, 모든 브라우저는 기본적으로 
Javascript를 알아듣게 설계되어있고, 모든 웹서버는 HTML+CSS+Javascript를 주게 되어있다. 
```
### 자바 스크립트 맛보기
- 함수 작성

![01](https://user-images.githubusercontent.com/108924832/197788440-65f6fa92-ed2c-4755-b35b-68800d7d2f5e.PNG)

- 결과

![02](https://user-images.githubusercontent.com/108924832/197790433-9724dbac-3703-4a9f-99a4-a61363b503ee.PNG)

## Javascript 기초 문법 배우기(1 ~ 4)
크롬 개발자 도구 > console 창에서 입력한다.
```
크롬 개발자 도구 콘솔창
> 웹 페이지에서 빠르게 자바스크립트를 테스트해볼 수 있게, 개발자들을 위해 만들어둔 도구
  새로고침하면 모두 사라진다.
```
- HTML 파일에 작성한 script 는 웹페이지 > 검사(개발자 도구) > console 과 동일하다

- console 창
    - windows : F12
    - macOs : alt(option) + command + i

![01](https://user-images.githubusercontent.com/108924832/198389177-1c62b344-813c-4882-acdf-15b9d516c8be.PNG)

console.log(변수)
```
console.log(변수) 는, 콘솔 창에 괄호 안의 값을 출력해줍니다.

console.log(변수1,변수2) 로 여러 변수를 한번에 출력할 수도 있다.

console.log("Hello World!");
Hello World!
```
### 프로그래밍 언어를 배울때 중요한 부분
- 변수
    - 값을 담는 것
- 자료형
    - 자료 형태의 모든 것(숫자형, 문자열...)
- 조건문
    - 조건A가 참(true)이면 ~ or 거짓(false)이면 ~
- 반복문
    - 프로그램을 반복해서 실행시키는 것
- 함수
    - 어떤 일을 수행한 다음 그 결과물을 보여주는 것

### 변수 & 기본 연산

![01](https://user-images.githubusercontent.com/108924832/197795016-43e4cf5b-3ba0-4b7c-9116-5b95b5cc199c.PNG)

### 리스트 : 순서를 지켜서 가지고 있는 형태

![01](https://user-images.githubusercontent.com/108924832/198376596-80ac28ff-3d02-4ea3-9c72-d36840357364.PNG)

![02](https://user-images.githubusercontent.com/108924832/198376651-512c6a85-080c-409b-8aa2-b4f0f9d9edbd.PNG)

### 딕셔너리 : 한 쌍의 키(key) 와 벨류(value)를 가지고 있는 형태

![02](https://user-images.githubusercontent.com/108924832/198374419-050e05f2-d97a-444f-87c6-b71dbf2bb607.PNG)

### 리스트와 딕셔너리의 조합
- 장점 : 순서를 표시할 수 있으며 정보를 묶을 수 있다.

한 상점에서 손님의 이름 , 전화번호를 저장하려 할 때 , 변수만 사용해보았다.
```
let customer_1_name : '자바'
let customer_1_phone = '010-1234-1234'
let customer_2_name : '파이썬'
let customer_1_phone = '010-5678-5678'
.
.
.
알아보기 어렵고 , 데이터의 양이 지나치게 많아진다.
```
리스트와 딕셔너리를 적절하게 사용하면 다루기도 쉬울뿐더러, 보기도 간단해진다.
```
== 딕셔너리로 고객정보 관리 ==
let customer_1 = {'name':'자바','phone':'010-1234-1234'}
let customer_2 = {'name':'파이썬','phone':'010-5678-5678'}

== 리스트로 고객정보를 순서대로 담아보기 ==
let customer_info = [
    {'name':'자바','phone':'010-1234-1234'},
    {'name':'파이썬','phone':'010-5678-5678'}
]

== 고객정보 추가 ==
let new_customer_info = {'name':'자바스크립트','phone':'010-2534-2537'}
customer_info.push(new_customer_info)
customer_info
.
.
. 
0: {name: '자바', phone: '010-1234-1234'}
1: {name: '파이썬', phone: '010-5678-5678'}
2: {name: '자바스크립트', phone: '010-2534-2537'}
```

### 기본 함수들
사칙연산 외에도 , 기본적으로 제공하는 여러 함수들이 존재한다
- 나눗셈의 나머지 구하기(%)
```
let a = ;
let b = 7;
a % b
6
```
- 특정 문자로 문자열을 나누기(split)
```
== 사용1 ==
let email = 'kim@naver.com';
let result = email.split('@')
result
['kim', 'naver.com']

== 사용2 ==
let result2 = result[1].split('.')
result2
['naver', 'com']

== 사용3 ==
email.split('@')[1].split('.')[0]
'naver'
```

### 함수
- 기본 문법
```
// 함수 만들기
function 함수명(사용할 변수들) {
  명령문(명령문은 순차적으로 작성)
}

// 함수 사용하기
함수이름(필요 변수들);
```
- 사용 예시
```
== 두 수를 더하는 add 함수 만들기 ==
function sum(num1 , num2){
    return num1 + num2;
}

== add 함수 사용하기 ==
sum(4,8);
12
```

### 조건문
- if , else , else if(중첩 사용 가능)
```
if(조건1){
  조건1의 결과가 참(true)일 경우 메세지 출력
}else if(조건2){
  조건 1의 결과가 거짓(false)이고 조건2의 결과가 참(true)일 경우 메세지 출력
}else{
  조건1 , 조건2의 결과가 거짓(false)일 경우 메세지 출력
}
```
- 사용 에시 
```
== 성인 or 학생을 알려주는 함수 ==
let age = 20;

if(age >= 20){
    console.log('성인')
} else {
    console.log('청소년')
}
성인

== 숫자가 자연수면서 홀수 or 짝수인지 알려주는 함수 ==
if(num < 0){
    console.log(num + '은 음수')
}else if(num % 2 == 1){
    console.log(num + '은 홀수')
}else{
    console.log(num + '은 자연수면서 짝수')
}
100은 자연수면서 짝수
```
### 반복문
- 반복문 이해하기
```
for(let i = 0; i <= 100; i++){
  console.log(i)
}

1. i는 0부터 시작된다.
2. i가 100보다 작거나 같을 때까지
3. i를 출력한다.
4. 반복문이 한번 돌면(i를 한번 출력하면) i 는 1 증가한다.
> i가 조건에 맞지 않을 경우 반복은 종료된다.
```

- 사용예시
```
0부터 5까지 출력해보기
== 반복문 사용X ==
console.log(0)
console.log(1)
console.log(2)
console.log(3)
console.log(4)
console.log(5)

== 반복문 ==
for(let i = 0; i <= 5; i++){
  console.log(i);
}
0
1
2
3
4
5
```
반복문은 주로 리스트와 함께 사용된다.
```
== 반복문을 리스트와 함께 사용하기 ==
for(let i = 0; i < pepole.length; i++){
    console.log(pepole[i]);
}
짱구
철수
유리
맹구
훈이

== 반복문을 딕셔너리가 들어간 리스트와 함께 사용하기 ==
let test = [
    {'name':'짱구','score':'100'},
    {'name':'철수','score':'80'},
    {'name':'맹구','score':'50'},
    {'name':'훈이','score':'40'}
]

for(let i = 0; i < test.length; i++){
    if(test[i]['score'] < 70){
        console.log(test[i]['name']);
    }
}
맹구
훈이
```

## 자바스크립트 연습하기
- 미세먼지 미세먼지(IDEX_MVL)의 값이 40 미만인 구 이름(MSRSTE_NM)과 값을 출력하기
- 서울시 미세먼지 값
```
let mise_list = [
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "도심권",
    MSRSTE_NM: "중구",
    PM10: 22,
    PM25: 14,
    O3: 0.018,
    NO2: 0.015,
    CO: 0.4,
    SO2: 0.002,
    IDEX_NM: "좋음",
    IDEX_MVL: 31,
    ARPLT_MAIN: "O3",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "도심권",
    MSRSTE_NM: "종로구",
    PM10: 24,
    PM25: 18,
    O3: 0.013,
    NO2: 0.016,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 39,
    ARPLT_MAIN: "PM25",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "도심권",
    MSRSTE_NM: "용산구",
    PM10: 0,
    PM25: 15,
    O3: 0.012,
    NO2: 0.027,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "점검중",
    IDEX_MVL: -99,
    ARPLT_MAIN: "점검중",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서북권",
    MSRSTE_NM: "은평구",
    PM10: 36,
    PM25: 14,
    O3: 0.019,
    NO2: 0.018,
    CO: 0.5,
    SO2: 0.005,
    IDEX_NM: "좋음",
    IDEX_MVL: 42,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서북권",
    MSRSTE_NM: "서대문구",
    PM10: 28,
    PM25: 9,
    O3: 0.018,
    NO2: 0.015,
    CO: 0.6,
    SO2: 0.004,
    IDEX_NM: "좋음",
    IDEX_MVL: 37,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서북권",
    MSRSTE_NM: "마포구",
    PM10: 26,
    PM25: 8,
    O3: 0.012,
    NO2: 0.021,
    CO: 0.5,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 36,
    ARPLT_MAIN: "NO2",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동북권",
    MSRSTE_NM: "광진구",
    PM10: 17,
    PM25: 9,
    O3: 0.018,
    NO2: 0.016,
    CO: 0.6,
    SO2: 0.001,
    IDEX_NM: "좋음",
    IDEX_MVL: 31,
    ARPLT_MAIN: "O3",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동북권",
    MSRSTE_NM: "성동구",
    PM10: 21,
    PM25: 12,
    O3: 0.018,
    NO2: 0.017,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 33,
    ARPLT_MAIN: "PM25",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동북권",
    MSRSTE_NM: "중랑구",
    PM10: 27,
    PM25: 10,
    O3: 0.015,
    NO2: 0.019,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 34,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동북권",
    MSRSTE_NM: "동대문구",
    PM10: 26,
    PM25: 9,
    O3: 0.016,
    NO2: 0.017,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 34,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동북권",
    MSRSTE_NM: "성북구",
    PM10: 27,
    PM25: 8,
    O3: 0.022,
    NO2: 0.014,
    CO: 0.5,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 37,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동북권",
    MSRSTE_NM: "도봉구",
    PM10: 25,
    PM25: 12,
    O3: 0.024,
    NO2: 0.011,
    CO: 0.3,
    SO2: 0.002,
    IDEX_NM: "좋음",
    IDEX_MVL: 41,
    ARPLT_MAIN: "O3",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동북권",
    MSRSTE_NM: "강북구",
    PM10: 30,
    PM25: 15,
    O3: 0.022,
    NO2: 0.02,
    CO: 0.4,
    SO2: 0.002,
    IDEX_NM: "좋음",
    IDEX_MVL: 39,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동북권",
    MSRSTE_NM: "노원구",
    PM10: 21,
    PM25: 14,
    O3: 0.017,
    NO2: 0.016,
    CO: 0.4,
    SO2: 0.004,
    IDEX_NM: "좋음",
    IDEX_MVL: 36,
    ARPLT_MAIN: "PM25",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서남권",
    MSRSTE_NM: "강서구",
    PM10: 36,
    PM25: 16,
    O3: 0.021,
    NO2: 0.013,
    CO: 0.4,
    SO2: 0.004,
    IDEX_NM: "좋음",
    IDEX_MVL: 42,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서남권",
    MSRSTE_NM: "구로구",
    PM10: 23,
    PM25: 10,
    O3: 0.022,
    NO2: 0.016,
    CO: 0.3,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 37,
    ARPLT_MAIN: "O3",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서남권",
    MSRSTE_NM: "영등포구",
    PM10: 29,
    PM25: 15,
    O3: 0.01,
    NO2: 0.022,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 41,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서남권",
    MSRSTE_NM: "동작구",
    PM10: 29,
    PM25: 15,
    O3: 0.012,
    NO2: 0.023,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 41,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서남권",
    MSRSTE_NM: "관악구",
    PM10: 27,
    PM25: 12,
    O3: 0.012,
    NO2: 0.022,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 37,
    ARPLT_MAIN: "NO2",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서남권",
    MSRSTE_NM: "금천구",
    PM10: 25,
    PM25: 15,
    O3: 0.015,
    NO2: 0.02,
    CO: 0.4,
    SO2: 0.004,
    IDEX_NM: "좋음",
    IDEX_MVL: 43,
    ARPLT_MAIN: "PM25",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "서남권",
    MSRSTE_NM: "양천구",
    PM10: 0,
    PM25: 14,
    O3: 0.016,
    NO2: 0.017,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "점검중",
    IDEX_MVL: -99,
    ARPLT_MAIN: "점검중",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동남권",
    MSRSTE_NM: "강남구",
    PM10: 31,
    PM25: 16,
    O3: 0.018,
    NO2: 0.018,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 39,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동남권",
    MSRSTE_NM: "서초구",
    PM10: 34,
    PM25: 13,
    O3: 0.024,
    NO2: 0.019,
    CO: 0.3,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 41,
    ARPLT_MAIN: "PM10",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동남권",
    MSRSTE_NM: "송파구",
    PM10: 25,
    PM25: 6,
    O3: 0.014,
    NO2: 0.025,
    CO: 0.4,
    SO2: 0.003,
    IDEX_NM: "좋음",
    IDEX_MVL: 42,
    ARPLT_MAIN: "NO2",
  },
  {
    MSRDT: "201912052100",
    MSRRGN_NM: "동남권",
    MSRSTE_NM: "강동구",
    PM10: 24,
    PM25: 14,
    O3: 0.016,
    NO2: 0.02,
    CO: 0.4,
    SO2: 0.002,
    IDEX_NM: "좋음",
    IDEX_MVL: 39,
    ARPLT_MAIN: "PM25",
  },
];
```
- 반복문
```
== 반복문 ==
for(let i = 0; i < mise_list.length; i++){
  if(mise_list[i]['IDEX_MVL'] < 40){
  let gu_name = mise_list[i]['MSRSTE_NM'];
  let gu_mise = mise_list[i]['IDEX_MVL'];
  console.log(gu_name , gu_mise);
  }
}
.
.
.
중구 31
용산구 -99
서대문구 37
마포구 36
광진구 31
성동구 33
중랑구 34
동대문구 34
성북구 37
강북구 39
노원구 36
구로구 37
관악구 37
양천구 -99
강남구 39
강동구 39
```
