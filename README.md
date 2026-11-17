# 하우스링 (HOUSE RING) 대표 홈페이지 — v2

`index.html` 파일 하나로 동작하는 반응형 원페이지 사이트입니다. 서버·빌드 없이 열리고, GitHub Pages · Cloudflare Pages · Netlify 에 폴더째 올리면 바로 공개 주소가 생깁니다.

## v2에서 바뀐 것

- 담당자 실명을 모두 빼고 **하우스링(HOUSE RING)** 브랜드와 대표 상담 번호 `010-4825-7879` 로 통일 (본문·상담 카드·푸터·메타태그·구조화 데이터까지)
- 세컨하우스(모듈러) 시작가를 **10평 기준 3,900만 원부터**(CUBE 10)로 수정
- 전시장 섹션을 **“사진과 영상만 보고 속지 마세요”** 초대 메시지로 개편 + 넓은 주차장 · 커피 · 직접 체험 포인트
- 전시 모델 3종(CUBE 10 · NEST 12 · LUNA HIGH 21)과 **무료 출장 견적** 신청 동선 추가
- **현장 한눈에 비교** 표, **채널**(유튜브·블로그·인스타), **방문 예약 달력** 섹션 추가

## 파일 구성

```
houseling-site/
├── index.html                    # 전체 페이지 (HTML + CSS + JS 포함)
├── assets/                       # 로고 이미지 5종
├── tools/shoot.py                # 헤드리스 Chromium 렌더링 점검 + 섹션 스크린샷 촬영
└── README.md
```

로고는 `downloads/1792904790437.jpg` 원본에서 배경(베이지)을 제거하고 네이비·금색으로 정리해 만든 파일입니다. 원본은 `assets/logo-original.jpg`에 그대로 보관했습니다.

## 사진 (`assets/photos/`)

| 파일 | 쓰이는 곳 | 원본 출처 | 비고 |
|---|---|---|---|
| `showroom.jpg` | 전시장 섹션(프레임) | 자사 블로그 `blog.naver.com/yummyapt` (파주 전시장 공개 글) | 실사진 |
| `cube-10.jpg` | 전시 모델 01 | 부경아리아 공식 홈페이지 (`sites.google.com/view/house-ring`) | 모델 이미지 |
| `nest-12.jpg` | 전시 모델 02 | 부경아리아 공식 홈페이지 | 모델 이미지 |
| `luna-high-21.jpg` | 전시 모델 03 | 부경아리아 공식 홈페이지 | 모델 이미지 |
| `teluce.jpg` | 용인 고림동 텔루체 카드 | 자사 블로그 `blog.naver.com/yummyapt` | 실사진 |
| `greendel.jpg` | 파주 그린델 2차 카드 | 자사 블로그 `blog.naver.com/yummyapt` | 실사진 |
| `lancity.jpg` | 서동탄역 랜시티 카드 | 서동탄역 랜시티 공식 홈페이지 `aptgio.co.kr` | 조감도 |

- 모두 가로 1200px 이하로 줄이고(작은 원본은 그대로) JPEG 품질 84로 최적화했습니다. 총 672KB.
- 외부 URL을 직접 불러오지 않고(`hotlink` 없음) 전부 로컬 파일입니다. GitHub Pages·Cloudflare Pages에 폴더째 올리면 그대로 동작합니다.
- 카드에는 `object-fit: cover` + 어두운 그라데이션 오버레이를 써서 비율이 깨지지 않고, 카드 코드·배지 글자가 사진 위에서도 읽힙니다.
- **아직 일러스트로 남은 카드**: 양평 서종 풀바베큐 세컨하우스, 광주 목현동 비에스애비뉴 — 공개된 실사진을 확보하지 못해 기존 라인 일러스트를 유지했습니다. 해당 현장 사진을 주시면 `assets/photos/seojong.jpg`, `bs-avenue.jpg`로 넣고 카드만 바꾸면 됩니다.

## 로컬에서 보기

`index.html` 을 더블클릭하면 브라우저에서 바로 열립니다. (인터넷 없이도 표시됩니다. 외부 폰트·이미지 불러오기 없음)

> 채널 섹션의 영상 카드는 **공개 주소(https)에서 열면 그 자리에서 유튜브 재생목록이 재생**되고, 파일로 바로 열었을 때는 유튜브 채널이 새 창으로 열립니다. (file:// 에서는 유튜브 임베드가 동작하지 않습니다.)

## 무료로 공개하기

**GitHub Pages**
1. GitHub에 새 저장소 생성 (예: `housering-site`, Public)
2. `houseling-site` 폴더 안의 `index.html`, `assets`, `README.md` 를 저장소 루트에 업로드
3. 저장소 → Settings → Pages → Branch: `main` / `/ (root)` 선택 → Save
4. 1~2분 뒤 `https://아이디.github.io/housering-site/` 주소로 공개됨

**Cloudflare Pages**
1. Cloudflare 대시보드 → Workers & Pages → Create → Pages → Upload assets
2. `houseling-site` 폴더를 그대로 업로드 → 배포

나중에 `housering.co.kr` 같은 도메인을 붙이면 주소를 그대로 쓸 수 있습니다.

## 바꿔 넣을 곳 (검색해서 찾으면 됩니다)

| 항목 | 위치 | 현재 상태 |
|---|---|---|
| 전화번호 | `tel:+821048257879` / `010-4825-7879` | 하우스링 대표 상담 번호 |
| 문자 문의 | `sms:+821048257879` | 문자 앱으로 내용 전송 |
| 카카오톡 채널 | `.kakao-note` 문구 | 채널 개설 전이라 "준비 중" 표기 |
| 현장 사진 | `assets/photos/` + `.card-visual` 안의 `img.photo` | 전시장·모델 3종·텔루체·그린델·랜시티는 실사진, 서종·비에스애비뉴는 일러스트 유지 |
| 가격·세대수 | 각 카드의 `.specs`, `.price-band`, `.model` | 확인된 정보만 기재 (CUBE 10 3,900만 원~ / LUNA HIGH 21 1억 760만 원) |
| 지도 링크 | `#showroom` 의 네이버·카카오맵 링크 | 주소 검색으로 연결 |
| 채널 링크 | `#channel` 의 `.ch-item`, `.sns` | 하우스링 유튜브 5개 · 네이버 블로그 2개 · 인스타그램 |
| 방문 예약 | `#booking` 달력·시간대·문자 링크 | `sms:+821048257879` 로 내용 전송 |

## 채널 링크 (확인 완료)

- 유튜브 메인 — 하우스링 모듈러 전원주택 타운하우스: https://www.youtube.com/channel/UCv1LuKEOIRZm-u71nhofMwA
- 부경아리아 파주전시장: https://www.youtube.com/channel/UCGw0eGE1WyVHrMNPFaYJp4Q
- 텔루체타운하우스: https://www.youtube.com/channel/UCKnVgPLCCxq4bYGz_bbiJZg
- 용인 고림동 텔루체타운하우스: https://www.youtube.com/channel/UCK6nJl5qJ906ED_bkiESrlQ
- 파주그린델타운하우스: https://www.youtube.com/channel/UCv0OI5yg0yETDd20zSluVLw
- 네이버 블로그: https://blog.naver.com/yummyapt · https://blog.naver.com/teluceyongin
- 인스타그램: https://www.instagram.com/pajucountry_house/

## 이번 시안에 넣은 내용

- 파주 교하 전시장(부경아리아) — “사진과 영상만 보고 속지 마세요” 초대 섹션 + 전시 모델 3종 + 무료 출장 견적
- 주요 현장 5곳: 용인 고림동 텔루체 · 파주 그린델 2차 · 서동탄역 랜시티 · 양평 서종 풀바베큐 · 광주 목현동 비에스애비뉴
- 사업 분야 6개 (모듈러 전시·시공 / 분양 대행·마케팅 / 토지 매매 / 건축·인허가 / 세컨하우스·수익형 / 2026년 12월 부동산 중개 예정)
- 상담 절차 4단계, 상담 폼(문자 전송), 모바일 하단 고정 전화·문자 바
- 현장 한눈에 비교표, 채널(유튜브·블로그·SNS), 방문 예약 달력(날짜·시간대·문자 예약)

## 확인되지 않아 넣지 않은 것

방문자 수, 확정 수익률, 분양 완료 세대수, 영업시간, 사업자등록번호 등 확인되지 않은 수치는 넣지 않았습니다. 상담 폼과 방문 예약은 서버 없이 문자 앱으로 내용을 넘기는 방식이라 개인정보가 사이트에 저장되지 않습니다. NEST 12 가격은 확인된 금액이 없어 “가격 상담 안내”로 두었습니다.
