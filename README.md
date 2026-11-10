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

## 베타 웹앱 (나만 보기)

아직 허브에 공개하기 이른 웹앱은 `APPS` 항목에 `beta: true`를 한 줄 추가합니다.

```js
{
  title: '새 웹앱',
  // ...다른 필드는 위와 같음
  beta: true,   // 허브에는 안 보이고 /beta 주소에서만 보임
},
```

- `https://earthssaem-lab.vercel.app/` : 베타 앱이 보이지 않습니다.
- `https://earthssaem-lab.vercel.app/beta` : 베타 앱이 보라색 카드와 BETA 배지로 맨 앞에 보이고(유형과 상관없이 같은 색), 정식 앱도 함께 보입니다.
- `/beta` 주소는 허브 어디에도 링크하지 않으며, 검색엔진에 노출되지 않도록 `noindex`를 붙입니다(`vercel.json`).
- 정식 공개할 때는 `beta: true` 줄만 지우면 됩니다.
- 저장소가 공개되어 있으므로 주소를 아는 사람은 볼 수 있습니다. 비밀번호 같은 접근 제한은 없습니다.
