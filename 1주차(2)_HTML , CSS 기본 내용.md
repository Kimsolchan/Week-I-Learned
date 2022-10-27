# [스파르타코딩클럽] 웹개발 종합반 - 1주차
## HTML , CSS 기본 내용
- HTML : 웹페이지의 뼈대
- CSS : HTML을 꾸미는 것

### HTML
- HTML은 구역과 텍스트를 나타내는 코드
- HTML은 크게 head와 body로 구성됨
- head안에는 페이지의 속성 정보를, body안에는 페이지의 내용을 담는다.
- head 안에 들어가는 대표적인 요소들: meta, script, link, title 등

**자주 쓰이는 태그(tag)들**

![100](https://user-images.githubusercontent.com/108924832/196955613-a7564fc1-e72e-47e4-b57f-2da4953abc4f.PNG)
이 외에도 아주 많으며 , 필요할 때마다 찾아서 사용한다고 한다.

**결과**

![01](https://user-images.githubusercontent.com/108924832/197727407-a38ad867-1ebc-46e1-acc4-a70432ce618d.PNG)


## Quiz_간단한 로그인 페이지 만들기
- HTML 코드

![100](https://user-images.githubusercontent.com/108924832/196960632-bafced8b-40be-4319-b9d1-e18f1075b2bc.PNG)

- 결과

![200](https://user-images.githubusercontent.com/108924832/196960831-87529f44-737b-45c7-a44b-1684c0903d93.PNG)

## CSS 기초
### 1. HTML 부모-자식 구조 살펴보기
- html 태그는, **'누가 누구 안에 있느냐'** 를 이해하는 것이 가장 중요하다.
    - a 를 감싸고 있는 태그가 바뀌면, 그 안의 내용들도 모두 영향을 받는다

![CSS 기초](https://user-images.githubusercontent.com/108924832/196961999-619567d8-dfcf-4543-972b-2db380334c68.PNG)
-  빨간색 div를 가운데로 옮기면, 내용물인 초록/파란 div도 모두 함께 이동한다.
    - 박스를 옮기면 안의 내용물도 함께 옮겨지는 것과 같은 원리
- 초록 div의 글씨색을 바꾸면, 나는버튼1의 글씨색도 바뀐다
### 2. CSS 기초
- css 사용법
```
<head>
  <style>
    여기서 CSS를 사용
   </style>
</head>

==사용 예시 id값이 'mytitle' 인 태그에 스타일을 적용==
 <head>
  <style>
    .mytitle{
      이곳에 스타일 적용
    }
   </style>
</head> 
```
- .mytitle : mytitle라는 클래스를 가리킨다 는 의미며 {}를 사용한다
- 자주 사용되는 CSS
```
== 배경관련 ==
background-color
background-image
background-size

== 사이즈 ==
width
height

== 폰트 ==
font-size
font-weight
font-family
color

== 간격 ==
margin
padding
```
### 자주 쓰이는 CSS 연습하기(1)
- 자주 쓰이는 CSS
```
h1, h5, background-image, background-size, background-position
color, width, height, border-radius, margin, padding

== margin과 padding 의 차이점 ==
margin  : 바깥 여백을 주는 것
padding : 내 안쪽 여백을 주는 것
-> div에 색깔을 넣고, 직접 사용해서 차이를 비교해보기 
```
- HTML 코드

![01](https://user-images.githubusercontent.com/108924832/197728788-089afeec-38b1-4886-b2b4-81cb122a1f07.PNG)

- 결과

![02](https://user-images.githubusercontent.com/108924832/197728874-bee45d64-ad98-472c-b5ff-7c923fa0b5b9.PNG)


### 자주 쓰이는 CSS 연습하기(2)
- 로그인 화면을 웹페이지 중앙으로 위치 옮겨보기
```
CSS : 에 width를 주고, margin: auto를 사용
-> 안될 경우 : display:block을 추가
```
- HTML 코드

![01](https://user-images.githubusercontent.com/108924832/197732204-4446c83b-5d91-4feb-a40b-7f2e323f00ba.PNG)

- 결과

![02](https://user-images.githubusercontent.com/108924832/197732268-c8de0a0c-2b20-4fa7-a4b4-2c7144720c8e.PNG)

## 폰트, 주석, 파일분리
### 1. 구글 웹폰트 입히기
- 구글 웹폰트
```
https://fonts.google.com/?subset=korean
```

- 적용시킬 폰트 클릭

![01](https://user-images.githubusercontent.com/108924832/197764884-23782c6c-de5f-4069-add0-a4d9ccd2a947.PNG)

- link 부분 복사

![02](https://user-images.githubusercontent.com/108924832/197765691-ac5c7640-4276-4f1a-b5af-f78fd9757f1d.PNG)

- HTML 적용

![01](https://user-images.githubusercontent.com/108924832/197766260-e1c5f37b-4b90-46e8-be21-d5b914cc36e8.PNG)

- CSS 복사

![02](https://user-images.githubusercontent.com/108924832/197767055-5ac3706c-575b-4af0-bb00-773b38aa8996.PNG)


- HTML에 CSS적용

![03](https://user-images.githubusercontent.com/108924832/197767105-549f7f01-8aba-4716-a8d3-df01f5b86383.PNG)
```
* : 모든 태그에 적용시키겠다는 의미 
```

- 결과(구글폰트 'Jua' 폰트로 폰트 스타일이 변경되었다)

![04](https://user-images.githubusercontent.com/108924832/197767285-947a43ae-7d82-472d-b12a-9285f15691f0.PNG)

### 2. 주석(Comment)
```
주석을 적용시키면 브라우저/컴퓨터 는 코드를 읽지 않으므로 프로그램에 영향을 주지 않는다.
```
- 주석은 언제 사용하나?
```
1. 필요없어진 코드를 삭제하는 대신 임의로 실행되지 않게 할 때 
2. 코드에 대한 설명을 적어 다른 사람이 코드를 읽을때 가독성을 높힐 때
```

### 3. CSS 파일 분리
```
HTMl 파일에 있는 <style> ~ </style> 부분이 너무 길어지면, 

보기가 불편하므로 따로 CSS 파일을 만들어 파일을 분리할 수 있다.

CSS 파일을 따로 불러올 경우, HTML에 적용시키기 위해서는 import 과정이 필요하다.
```

- 따로 분리된 HTML , CSS

![01](https://user-images.githubusercontent.com/108924832/197770585-a9371550-fd7d-43af-93b4-cce16630840f.PNG)

- HTML 파일에 CSS를 적용

![02](https://user-images.githubusercontent.com/108924832/197770632-0a0e1c18-82e9-4314-8697-cb00ea10ebd7.PNG)

## bootstrap(부트스트랩)
```
미적 감각을 살려서 디자인된 CSS를 미리 모아둔 것

CSS를 다룰 줄 아는 것과, 미적 감각을 발휘하여 만드는 것은 다르기 때문에, 
현업에서는 미리 완성된 부트스트랩을 가져다 쓰는 경우가 많다.
```

### 1. bootstrap - 시작 템플릿

![10](https://user-images.githubusercontent.com/108924832/197774025-4b8b9875-da12-4a25-b2ba-77e1e405d65a.PNG)


### 2. bootstrap - 컴포넌트5.0
```
https://getbootstrap.com/docs/5.0/components/buttons/
```

버튼을 아름답게 꾸며주는 부트스트랩 사이트로 접속된다.

### 3. 적용시킬 코드 복사(Primary 버튼을 적용시켜보겠다.)

![01](https://user-images.githubusercontent.com/108924832/197773467-89c88000-796e-4687-8676-dfc4f98097f3.PNG)


### 4. bootstrap - 시작 템플릿 페이지에 그대로 적용시킨다

![10](https://user-images.githubusercontent.com/108924832/197773721-dbf0117c-98ef-48cc-bf61-db290cbe43e2.PNG)


### 결과

![05](https://user-images.githubusercontent.com/108924832/197773366-1560c06c-e764-4c0e-acb9-c138addbb6d0.PNG)

## CSS 꿀팁 한번 더 배우기
- HTML 코드
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS 꿀팁</title>
    <!--  구글 폰트 불러오기  -->
    <link href="https://fonts.googleapis.com/css2?family=Gowun+Dodum&display=swap" rel="stylesheet">
    <style>
        /* 모든 태그에 글씨체 적용 */
        * {
            font-family: 'Gowun Dodum', sans-serif;
        }

        .mytitle {
            background-color: greenyellow;
            /* width: 100%; : 내 브라우저 화면을 100% 라 가정하고 '얼만큼 채울건지' 를 뜻함  */
            width: 100%;
            height: 200px;
            /* linear-gradient(0deg, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), : 이미지 어둡게 적용 */
            background-image: linear-gradient(0deg, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),url("https://movie-phinf.pstatic.net/20210715_95/1626338192428gTnJl_JPEG/movie_image.jpg");
            background-position: center;
            background-size: cover;

            color: white;

            /* 네 줄 세트 : 영역 안에 있는 모든 내용들을 가운데 정렬하겠다 */
            display: flex;
            flex-direction: column; /* colum : 세로 정렬 / row : 가로 정렬  */
            justify-content: center;
            align-items: center;
        }

        /* .mytitle > button : mytitle 이라는 클래스 이름을 가진 태그 안에 있는 버튼 태그에 스타일 적용 */
        .mytitle > button {
            width: 200px;
            height: 50px;

            background-color: transparent; /*transparent : 투명색 */
            color: white;
            border-radius: 50px; /*border-radius : 모서리 라운드 적용 */

            border: 1px solid white; /* 선 굵기가 흰색이고 실선이란 의미 */

            margin-top: 10px; /* 위쪽 여백 적용 */
        }

        /* 버튼에 마우스를 올리면(hover) 굵어지는 이펙트 적용 */
        .mytitle > button:hover {
            border: 2px solid white;
        }
    </style>
</head>
<body>
<div class="mytitle">
    <h1>내 생의 최고의 영화들</h1>
    <button>영화 기록하기</button>
</div>
</body>
</html>
```

- 결과

![01](https://user-images.githubusercontent.com/108924832/197779224-2a724e87-8975-42ef-a154-0a6ccc5fb273.PNG)