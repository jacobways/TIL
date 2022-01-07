## backtick을 활용한 코드 표시
- 형태
```
```프로그램명
코드 내용```
```

- 주의 사항 : 프로그램 명을 기재하지 않으면 컬러가 아닌 흑백으로 표시됨

![logo](https://user-images.githubusercontent.com/80403988/136531547-2361d5f1-24bb-4028-a06a-e4ce012f7c2c.png)

<img width="887" alt="스크린샷 2021-10-14 오전 1 04 17" src="https://user-images.githubusercontent.com/80403988/137171683-fbb45d64-9d40-45f2-ad4d-85481fae5857.png">

<img width="796" alt="스크린샷 2021-10-20 오후 1 11 43" src="https://user-images.githubusercontent.com/80403988/138027186-fedb6fa9-1f2f-4f5c-a573-536c2a8331fb.png">

<img width="800" alt="스크린샷 2021-10-20 오후 2 39 10" src="https://user-images.githubusercontent.com/80403988/138034439-6cc1a208-7c93-4701-84a1-9ffc86517a0e.png">

<img width="400" alt="스크린샷 2021-10-20 오후 6 09 38" src="https://user-images.githubusercontent.com/80403988/138064375-4bda5d15-eefb-413d-87d6-1c1f0d543ec5.png">

- API

<img width="700" alt="스크린샷 2021-10-25 오후 1 52 52" src="https://user-images.githubusercontent.com/80403988/138636598-8c8c8aad-1839-411b-9326-a8c914968b84.png">

<img width="700" alt="스크린샷 2021-10-25 오후 1 53 04" src="https://user-images.githubusercontent.com/80403988/138636602-c8961b10-d2cb-4a12-987d-ccbbf801ea5b.png">

<img width="700" alt="스크린샷 2021-10-25 오후 1 53 14" src="https://user-images.githubusercontent.com/80403988/138636608-17c7e50a-6a69-4867-a7da-a9aa9aa80a15.png">

<img width="700" alt="스크린샷 2021-10-25 오후 1 53 33" src="https://user-images.githubusercontent.com/80403988/138636613-1fd60f13-dbd9-4859-a31a-e25c639df8d5.png">

<img width="700" alt="스크린샷 2021-10-25 오후 1 53 43" src="https://user-images.githubusercontent.com/80403988/138636619-e31e8830-891e-424f-93e7-e4cc5fb3ff30.png">

![hometownalba](https://user-images.githubusercontent.com/80403988/141236509-0747eebd-3a81-45dd-b403-222a0e1d5801.png)



```html

  <body>
    <div id="root"></div>
    
    <script type="text/javascript" src="//dapi.kakao.com/v2/maps/sdk.js?appkey=API키&libraries=services"></script>
    
  </body>


```

```js
import React, { useEffect } from "react";
const { kakao } = window;

export default function Map() {

  useEffect(()=>{
    let mapContainer = document.getElementById('map') // 지도를 표시할 div 
    
    // 지도의 옵션 설정
    let mapOption = { 
        center: new kakao.maps.LatLng(33.450701, 126.570667), // 지도의 중심좌표
        level: 3 // 지도의 확대 레벨
    };
  
    // 지도를 표시할 div와  지도 옵션으로  지도를 생성합니다
    var map = new kakao.maps.Map(mapContainer, mapOption); 
  }, [])

  return(
    <div
    id="map"
    style={{
      width: "80%",
      height: "80%",
    }}
    ></div>
  )
}
```



```js
useEffect(()=>{

  axios.get( DB에서 일자리 데이터 불러오기 )

  .then( 기준에 따라 데이터 필터링 )

  .then ( //지도 API 기능 활용

    지도 화면에 띄우기

    지도 이동 이벤트 등록

    렌더링 시점에 지도 위치 지정

    검색 기능 입력

    반복문 : 일자리별 마커 표시하기

    마커에 이벤트 등록하기

  )
}, [지도 위치, 일자리 지원, 데이터 필터링 기준, 검색 키워드])

return (
  필터링 된 데이터 목록에 띄우기
  지도 표시하기
)
```

```js
var iwContent = `
<div>회사명 : ${data.companyName}</div>
<div>근무시간 : ${data.time}</div>
<div>월급 : ${data.monthlyWage}</div>
<button onclick="${eventHandler}">지원하기</button>
`

let infowindowClick = new kakao.maps.InfoWindow({
  content: iwContent,
  removable: true,
});
```

```js
var iwContent = `
<div>회사명 : ${data.companyName}</div>
<div>근무시간 : ${data.time}</div>
<div>월급 : ${data.monthlyWage}</div>
<button onclick="eventHandler">지원하기</button>
<script>
  function eventHandler () {
    console.log('인포윈도우 클릭이벤트')
  }
</script>
`

let infowindowClick = new kakao.maps.InfoWindow({
  content: iwContent,
  removable: true,
});
```

```js
var iwContent = `
<div>회사명 : ${data.companyName}</div>
<div>근무시간 : ${data.time}</div>
<div>월급 : ${data.monthlyWage}</div>
<button id="button">지원하기</button>
<script>
  button.onclick = function () {
    console.log('인포윈도우 클릭이벤트')
  }
</script>
`

let infowindowClick = new kakao.maps.InfoWindow({
  content: iwContent,
  removable: true,
});
```



```js
let iwContent = document.createElement("div")

let companyName = document.createElement("div")
companyName.textContent = `회사명 : ${data.companyName}`

let time = document.createElement("div")
time.textContent = `근무시간 : ${data.time}`

let monthlyWage = document.createElement("div")
monthlyWage.textContent = `예상 월급여 : ${data[i].monthlyWage}`

let btn = document.createElement("button");
btn.textContent = `지원하기`;
btn.onclick = eventHandler;

iwContent.append(
  companyName,
  time,
  monthlyWage,
  btn
);

let infowindowClick = new kakao.maps.InfoWindow({
  content: iwContent,
  removable: true,
});
```

```js
kakao.maps.event.addListener(map, "dragend", function () {
  // 지도 중심좌표를 얻어옵니다
  let latlng = map.getCenter();
  setApplyLocation([]);
  setSearchLocation("");
  setMapLocation([latlng.Ma, latlng.La]);
});
```

```js
if (mapLevel <= 4) {
  return res.data.data.filter(job => {
    return (
      parseFloat(job.latitude) >= mapLocation[0] - 0.009 &&
      parseFloat(job.latitude) <= mapLocation[0] + 0.009 &&
      parseFloat(job.longitude) >= mapLocation[1] - 0.011 &&
      parseFloat(job.longitude) <= mapLocation[1] + 0.011
    );
  });
} else if (mapLevel === 5) {
  return res.data.data.filter(job => {
    return (
      parseFloat(job.latitude) >= mapLocation[0] - 0.0225 &&
      parseFloat(job.latitude) <= mapLocation[0] + 0.0225 &&
      parseFloat(job.longitude) >= mapLocation[1] - 0.0275 &&
      parseFloat(job.longitude) <= mapLocation[1] + 0.0275
    );
  });
} else if (mapLevel === 6) {
  return res.data.data.filter(job => {
    return (
      parseFloat(job.latitude) >= mapLocation[0] - 0.045 &&
      parseFloat(job.latitude) <= mapLocation[0] + 0.045 &&
      parseFloat(job.longitude) >= mapLocation[1] - 0.055 &&
      parseFloat(job.longitude) <= mapLocation[1] + 0.055
    );
  });
} else if (mapLevel >= 7) {
  return res.data.data.filter(job => {
    return (
      parseFloat(job.latitude) >= mapLocation[0] - 0.09 &&
      parseFloat(job.latitude) <= mapLocation[0] + 0.09 &&
      parseFloat(job.longitude) >= mapLocation[1] - 0.11 &&
      parseFloat(job.longitude) <= mapLocation[1] + 0.11
    );
  });
}
```

```js
if (지원/취소 state) {

  // 지원/취소 한 일자리로 지도 이동
  
} else if (검색 state) {

  // 검색 위치로 지도 이동
  
} else {

  // 마우스 드래그된 위치로 지도 이동
  
}
```

### 와이어프레임

<img width="258" alt="스크린샷 2021-11-21 오전 1 31 24" src="https://user-images.githubusercontent.com/80403988/142734149-1ea1d714-eda5-44e6-8204-5d6936bd6083.png">

<img width="256" alt="스크린샷 2021-11-21 오전 1 31 30" src="https://user-images.githubusercontent.com/80403988/142734151-55a21cb7-6513-4362-8b8a-c6a94e8d2717.png">

<img width="256" alt="스크린샷 2021-11-21 오전 1 31 37" src="https://user-images.githubusercontent.com/80403988/142734155-a3ed0e2a-8c5b-4073-ab4a-856b7e3b4664.png">

<img width="258" alt="스크린샷 2021-11-21 오전 1 31 43" src="https://user-images.githubusercontent.com/80403988/142734158-bc87f0a3-01e2-4d39-a360-d55d4660d1aa.png">

<img width="257" alt="스크린샷 2021-11-21 오전 1 31 52" src="https://user-images.githubusercontent.com/80403988/142734161-8d1f0d46-830f-4820-8b46-4f8fe0231120.png">

<img width="255" alt="스크린샷 2021-11-21 오전 1 31 59" src="https://user-images.githubusercontent.com/80403988/142734164-2dd9f57f-725c-457c-be75-1374dacb3944.png">

<img width="259" alt="스크린샷 2021-11-21 오전 1 46 57" src="https://user-images.githubusercontent.com/80403988/142734409-b1f22e5c-6770-4c62-843c-b70d783805d2.png">

<img width="258" alt="스크린샷 2021-11-21 오전 1 47 05" src="https://user-images.githubusercontent.com/80403988/142734414-66fe4a40-7800-419c-91e5-8a46fd5a344d.png">

## UI 디자인

<img width="381" alt="스크린샷 2021-11-21 오전 1 50 26" src="https://user-images.githubusercontent.com/80403988/142734538-97df50f3-c650-41c2-8b24-633ef481eb15.png">
<img width="374" alt="스크린샷 2021-11-21 오전 1 50 31" src="https://user-images.githubusercontent.com/80403988/142734539-07806bf8-332c-4415-ad1b-ca74e7c64bfd.png">
<img width="361" alt="스크린샷 2021-11-21 오전 1 50 40" src="https://user-images.githubusercontent.com/80403988/142734540-5df391e3-93e6-45fc-b20e-ee0f0f4ab2f4.png">
<img width="350" alt="스크린샷 2021-11-21 오전 1 50 50" src="https://user-images.githubusercontent.com/80403988/142734541-80e0a3fc-6d62-4399-98fd-e8c1e871faa4.png">
<img width="339" alt="스크린샷 2021-11-21 오전 1 50 55" src="https://user-images.githubusercontent.com/80403988/142734542-d67b2788-7be3-4bda-9f9f-14770bddd066.png">
<img width="329" alt="스크린샷 2021-11-21 오전 1 50 59" src="https://user-images.githubusercontent.com/80403988/142734543-169822f3-3c95-4736-afe5-0b69a311987d.png">
<img width="344" alt="스크린샷 2021-11-21 오전 1 51 05" src="https://user-images.githubusercontent.com/80403988/142734544-5914e8e9-6c04-4db0-85fe-a7b0a5c5ccca.png">
<img width="347" alt="스크린샷 2021-11-21 오전 1 51 18" src="https://user-images.githubusercontent.com/80403988/142734545-7a5029e7-3d07-467b-a1f4-4e2491d79ac8.png">
<img width="388" alt="스크린샷 2021-11-21 오전 1 51 29" src="https://user-images.githubusercontent.com/80403988/142734546-35560b33-3842-42e6-85f0-7a73f39d6a5d.png">

<img width="600" alt="스크린샷 2021-11-25 오후 2 32 04" src="https://user-images.githubusercontent.com/80403988/143385187-c39ded55-f7e9-404d-b6ff-fe67f22d74e3.png">
<img width="600" alt="스크린샷 2021-11-25 오후 2 31 48" src="https://user-images.githubusercontent.com/80403988/143385190-88ab7ecd-740d-4186-9347-3136d0180b36.png">
<img width="600" alt="스크린샷 2021-11-25 오후 2 31 28" src="https://user-images.githubusercontent.com/80403988/143385192-34982003-0376-4332-92e7-020e08e2ba82.png">
<img width="600" alt="스크린샷 2021-11-25 오후 2 32 17" src="https://user-images.githubusercontent.com/80403988/143385194-adc74688-642a-4cbd-bdc9-466f9ee88894.png">

<img width="1384" alt="스크린샷 2022-01-07 오전 12 53 09" src="https://user-images.githubusercontent.com/80403988/148411016-14b2af21-dbc8-42e8-a9cc-cf4d34b62e86.png">

<img width="518" alt="스크린샷 2022-01-07 오전 1 17 32" src="https://user-images.githubusercontent.com/80403988/148414574-a0ead091-8728-4bc4-a977-1b094b69340b.png">

<img width="149" alt="logo" src="https://user-images.githubusercontent.com/80403988/148485067-99b8c156-f4ba-4886-8918-f9c7832581de.png">
