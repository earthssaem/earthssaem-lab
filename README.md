# EARTHSSAEM LAB · 연경쌤의 지구과학 수업 도구

고등학교 지구과학 수업용 웹앱을 모아 소개하는 개인 허브페이지입니다.
빌드 과정 없이 `index.html` 한 파일로 동작하며, GitHub Pages와 Vercel에서 그대로 배포할 수 있습니다.

## 앱 추가 방법

`index.html` 하단 `<script>` 안의 `APPS` 배열에 객체 하나를 추가하면 카드가 자동으로 생성됩니다.

```js
{
  title: '웹앱 제목',
  type: 'concept',            // concept(개념 탐구) / data(데이터 분석) / game(게임·복습)
  description: '한두 문장의 설명', // " / "를 넣으면 데스크톱 4열 카드에서 그 위치에서 줄바꿈
  subjects: [
    { name: '통합과학', year: '2022' },
    { name: '지구과학', year: '2022' },
  ],
  url: 'https://example.vercel.app/',
  icon: 'fossil',             // <symbol id="icon-fossil"> 의 "fossil" 부분
},
```

아이콘은 같은 파일의 `<svg>` 심볼 모음에 `<symbol id="icon-이름">`을 추가하고 `icon` 값에 그 이름을 적으면 됩니다.
