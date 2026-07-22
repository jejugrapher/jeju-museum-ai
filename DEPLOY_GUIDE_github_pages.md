# GitHub Pages 배포 가이드 — 우리집 추억! 박물관 추억!

**작성일:** 2026.07.22
**대상 페이지:** 제주민속자연사박물관 어린이 AI 동영상 제작 교육 안내

---

## 1. 업로드할 파일 (이 구조 그대로 올리세요)

```
저장소 루트/
├── index.html                     ← 메인 페이지 (포스터·고래뼈·QR 이미지 내장)
├── robots.txt                     ← 검색엔진용
├── sitemap.xml                    ← 검색엔진용
└── assets/
    ├── artist_sample_video.mp4    ← 작가 예시 영상 (15MB)
    └── og_image.jpg               ← 카카오톡·페북 공유 카드 이미지 (1200×630)
```

- `index.html`은 포스터·고래뼈·QR 이미지가 파일 안에 내장되어 있어 그대로 열립니다.
- `assets/` 폴더는 **반드시 index.html과 같은 위치**에 함께 올려야 영상·공유이미지가 작동합니다.

---

## 2. 저장소(주소) 이름 — 추천

GitHub Pages 주소는 `https://[내 GitHub 아이디].github.io/[저장소 이름]/` 형태로 만들어집니다.
저장소 이름은 영문 소문자 + 하이픈만 사용합니다.

| 저장소 이름 후보 | 완성되는 주소 | 장점 | 단점 |
|---|---|---|---|
| **`jeju-museum-ai`** | `.../jeju-museum-ai/` | 짧고 기억·입력 쉬움. 제주·박물관·AI 성격이 바로 드러남 | 프로그램명이 직접 드러나지 않음 |
| `uri-museum-memory` | `.../uri-museum-memory/` | 프로그램명(우리집 추억) 반영 | 길고 의미 파악이 덜 직관적 |
| `airamedia-museum` | `.../airamedia-museum/` | 작가 브랜드(AIRA) 노출 | 박물관 공식 행사에 개인 브랜드가 앞섬 |

**추천:** `jeju-museum-ai`
**추천 사유:**
- 주소가 짧아 QR·문자·SNS로 공유하기 쉽습니다.
- 제주 / 박물관 / AI 세 키워드가 검색에 잡히기 좋습니다.
- 공식 행사 페이지이므로 개인 브랜드보다 중립적인 이름이 적합합니다.

> **완성 예상 주소:** `https://[내 아이디].github.io/jeju-museum-ai/`
> ⚠ `[내 아이디]` 자리는 실제 GitHub 계정 아이디로 바뀝니다. 아이디를 알려주시면 아래 3-2 항목(주소 넣기)을 제가 대신 완성해 드립니다.

---

## 3. 배포 순서 (클릭 단계)

### 3-1. 저장소 만들기
1. github.com 로그인 → 우측 상단 **+** → **New repository**
2. **Repository name** 칸에 `jeju-museum-ai` 입력
3. **Public** 선택 (Pages는 공개 저장소에서 무료)
4. **Create repository** 클릭

### 3-2. 파일 올리기
1. 만든 저장소 화면에서 **Add file → Upload files** 클릭
2. `index.html`, `robots.txt`, `sitemap.xml` 3개 파일을 끌어다 놓기
3. `assets` 폴더는 폴더째 끌어다 놓기 (또는 `Add file`로 `assets/artist_sample_video.mp4`, `assets/og_image.jpg`를 경로 그대로 업로드)
4. 하단 **Commit changes** 클릭

### 3-3. Pages 켜기
1. 저장소 상단 **Settings** 클릭
2. 좌측 메뉴 **Pages** 클릭
3. **Source** → `Deploy from a branch` 선택
4. **Branch** → `main` 선택, 폴더는 `/ (root)` → **Save**
5. 1~2분 뒤 같은 화면 상단에 주소가 표시됩니다: `https://[내 아이디].github.io/jeju-museum-ai/`

### 3-4. 주소 넣기 (공유 카드 작동용)
`index.html` 상단에 `ID.github.io/jeju-museum-ai` 로 적힌 부분이 4곳 있습니다 (`<!-- 배포 후 변경 -->` 표시).
- `ID` 를 **실제 GitHub 아이디**로 바꾸면 카카오톡·페북에 공유할 때 미리보기 카드(og_image)가 뜹니다.
- `robots.txt`, `sitemap.xml` 안의 `ID` 도 동일하게 바꿔주세요.
- (이 4곳 치환은 아이디만 주시면 제가 완성본으로 만들어 드립니다.)

---

## 4. 공유 미리보기(카카오톡) 최신화

주소를 넣은 뒤 카카오톡·페북 미리보기가 안 바뀌면 캐시를 지워야 합니다.
- 카카오톡: `https://developers.kakao.com/tool/clear/og` 에서 페이지 주소 입력 → 초기화
- 페이스북: `https://developers.facebook.com/tools/debug/` 에서 주소 입력 → **Scrape Again**

---

## 5. 신청 링크에 관한 확인 필요 사항

현재 페이지 안 신청 경로가 **두 가지**입니다. 실제 공식 채널이 무엇인지 확정해 주세요.

1. **공식 배너 QR** → `https://naver.me/56axx2Ow`
   - 첨부해 주신 현수막·배너 PDF의 QR을 스캔하면 나오는 실제 주소입니다. 페이지에 이 QR 이미지를 그대로 넣었습니다.
2. **날짜별 신청 페이지** → `https://www.jeju.go.kr/museum/edu/application/application.htm`
   - 이전에 알려주신 주소입니다. QR 아래 보조 링크로 넣어두었습니다.

두 주소가 같은 곳으로 연결되면 그대로 두면 되고, 하나만 써야 하면 알려주시면 정리하겠습니다.
