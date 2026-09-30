# ZEROXAND 웹사이트

- 법인: ZERO X AND PTE. LTD. (UEN 202138132M, ACRA 등록, SSIC 58201)
- 도메인: zeroxand.com (구매 전)
- 배포: Vercel 예정 — 정적 `index.html` + `assets/` (빌드 설정 불필요)
- 디자인: ChatGPT 시안(다크/레드, Classified 컨셉) 채택 — `DESIGN_PROMPT.md`로 의뢰

## 확정 사항
- 대표 이메일: baht@0xand.com
- Ragnarok Monster World: 직접 개발 및 퍼블리싱, 글로벌 서비스 2024~2025
- 언어: 영문 단일

## Vercel 배포
정적 사이트라 빌드 단계 없음. `main`에 push하면 Vercel이 자동으로 다시 배포하고, 다른 브랜치나 PR은 미리보기 URL이 생긴다.

1. Vercel → Add New → Project → `baht-mania/zeroxand-web` Import
2. Framework Preset: **Other** / Build Command: 비움 / Output Directory: 비움(루트)
3. Deploy → `zeroxand-web.vercel.app`에서 확인
4. 도메인 구매 후 Project → Settings → Domains에 `zeroxand.com`, `www.zeroxand.com` 추가 → Vercel이 알려주는 DNS 값(A / CNAME)을 도메인 업체에 입력
5. `vercel.json`: `assets/` 캐시(7일), 기본 보안 헤더

## Project X 아트
폴더: `assets/project-x/` (원본 PNG는 vault `04. 자료/ragnarok monster world - Google 검색/무제 폴더/`, 웹용 WebP로 변환)

| 파일 | 용도 |
|---|---|
| `bg.webp` | Project X 섹션 전체 배경 (어둡게 오버레이) |
| `char-01~05.webp` | 캐릭터 쇼케이스 큰 이미지 + 썸네일 |

- 캐릭터 이름은 `index.html`의 `data-name`과 `aria-label` 값 수정 (01 Sera · 02 Izuna · 03 Roha · 04 Nut · 05 Sion)
- 캐릭터 교체·추가 시 16:9 일러스트 그대로 넣으면 됨. 썸네일 얼굴 위치는 `object-position`으로 조정

## 히어로 배경 영상
폴더: `assets/video/` (원본: vault `04. 자료/ragnarok monster world - Google 검색/영상/new/`)

| 파일 | 원본 | 용도 |
|---|---|---|
| `px-teaser-01.mp4` / `-480.mp4` | Teaser_new.mp4 (23MB) | 1번째 재생 (데스크톱 4.3MB / 모바일 1.8MB) |
| `px-teaser-02.mp4` / `-480.mp4` | Teaser3.mp4 (8.7MB) | 2번째 재생 (데스크톱 3.7MB / 모바일 1.6MB) |
| `px-teaser-poster.jpg` | Teaser_new 첫 프레임 | 로딩 전·동작 줄이기·데이터 절약 모드일 때 표시 |

- H.264, 소리 없음, 15초. 두 영상을 번갈아 재생하고 오른쪽 아래 버튼으로 일시정지
- vault `.gitignore`가 `*.mp4`를 막으므로 이 폴더 영상은 `git add -f`로 커밋
- 인코딩: `ffmpeg -i in.mp4 -an -c:v libx264 -preset slow -crf 26 -movflags +faststart -vf scale=1280:720 out.mp4` (모바일은 `-crf 28 -vf scale=854:480`)
