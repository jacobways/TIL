# HTML No.1 : 기본 태그 
*(출처 : Codecademy)

## HTML (Hyper Text Markup Language)
- 웹 페이지와 구조를 만들기 위한 도구

## HTML 요소 (Element)
![HTML 요소](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FAqOHy%2Fbtq3z40Hep8%2FVulCkDWxdwZkSl0Pvx9ep1%2Fimg.png "HTML 요소는 태그, 속성, 내용으로 구성")


1. 태그(Tag)
- 웹 브라우저 화면에 내용을 표시할 수 있도록 도와주는 HTML의 도구
- HTML 문서를 구성하는 기본 단위
- 대부분 오프닝 태그(<tag>)와 클로징 태그(</tag>)로 구성


2. 속성(Attribute)
- '속성 이름'과 '속성 값'으로 구성됨
- 하나의 태그에 1개 이상의 속성을 구현 가능


3. 내용(Contents)
- 오프닝 태그와 클로징 태그 사이에 입력
- 웹 브라우저 화면에 내용이 표시됨



## HTML의 기본 태그와 속성

1. ```<body>```
- 표시되는 모든 콘텐츠는 ```<body>``` 태그 내에 배치되어야 함

2. ```<h1> <h2>, ..., <h6>```
- 제목 및 부제목 태그
- ```<h1>```이 글자 크기가 가장 크고, ```<h6>```이 가장 작음

3. ```<p>```
- 단락(Paragraph) 내용 입력
- ```<p>``` 내용 ```</p>```

4. ```<div>```
- division의 약자
- HTML 요소 그룹화

5. ```<em>```
- 텍스트 스타일링 태그
- 내용 글자 기울어짐
- 사용 예시 : ```<h2>Hello <em>Jacob</em></h2>```

6. ```<strong>```
- 텍스트 스타일링 태그
- 내용 글자 진해짐

7. ```<br>```
- 줄 바꿈 태그 (HTML 코드에서 줄을 바꿔도 브라우저에서 표시되는 내용은 줄이 바뀌지 않음)
- 클로징 태그 없음

8. ```<ul>```
- 순서가 없는 목록 (Unordered List)
- ```<li>``` 태그와 함께 사용
- 사용 예시
```
<ul>
 <li>Apple</li>
 <li>Banana</li>
 <li>Melon</li>
</ul>
```

9. ```<ol>```
- 순서가 있는 목록 (Ordered List)
- ```<li>``` 태그와 함께 사용

10. ```<img>```
- 이미지 삽입 태그
- 클로징 태그 없음
```
<img src="주소" alt="텍스트"/>
```

① src 속성
- src 속성이 반드시 있어야 함
- 속성 값에는 파일이 저장된 로컬 또는 웹 주소 입력

② alt 속성
- 이미지가 웹 페이지에 입력되지 않고 오류가 났을 때, 이미지 대신 alt 속성의 텍스트가 표시됨
- 검색엔진최적화(SEO)에 기여
- 시각 장애용 소프트웨어 사용시 이미지를 글로 읽어줌

11. ```<video>```
- 동영상 삽입 태그
- 오프닝와 클로징 태그 사이 내용 : 동영상 재생이 안 될때만 표시됨 (예시 : Video not supported)

```
<video src="파일명" width="300" height="200" controls>
  Video not supported
</video>
```

① src 속성 : 링크 연결

② 너비(width), 높이(height) 속성 : 브라우저에 표시되는 비디오 크기 설정

③ control 속성 : 브라우저에 재생, 일시중지 등 동영상 컨트롤 버튼이 포함되도록 지시함


## 코드 예시 (출처 : Codecademy)
```
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
    <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" alt="A Brown Bear"/>
    <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls>Video not supported</video>
  </div>
</body>
```

## 코드에 따른 브라우저 표시 화면

<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
    <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" alt="A Brown Bear"/>
    <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls>Video not supported</video>
  </div>
</body>
