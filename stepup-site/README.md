# StepUp — AI 창업 로드맵 코치 (프론트엔드)

문화예술 분야 청년 창업가를 위한 AI 사업계획서 로드맵 코치 서비스의 프론트엔드 디자인입니다.
아이디어 발굴부터 단계별 사업계획서 작성, 정부지원사업 자동 매칭까지의 화면을 담고 있습니다.

## 화면 구성

| 파일 | 화면 | 설명 |
|------|------|------|
| `index.html` | 랜딩 페이지 | 히어로 · 창업 로드맵 카드 · 3대 핵심 동력 · 철학 가이드 · CTA |
| `dashboard.html` | 대시보드 | 로드맵 사이드바 · 현재 상태 · 다음 과제 · 추천 지원사업 |
| `workshop.html` | 로드맵 작업실 | 현재 단계 작업 · 실시간 지원사업 매칭 (3컬럼) |
| `step-detail.html` | 단계 상세 | TPCS 프레임워크 + AI 초안 생성 인터랙션 |

페이지는 상단 네비게이션과 버튼으로 서로 연결되어 있습니다.
`index → dashboard(시작하기) → step-detail(작업 시작) → workshop(다음 단계)`

## 실행 방법

빌드·설치가 필요 없는 **순수 정적 HTML + 인라인 스타일 + 바닐라 JS**입니다.

```bash
# 로컬에서 바로 열기
open index.html

# 또는 정적 서버
npx serve .
# python3 -m http.server
```

### GitHub Pages 배포
Settings → Pages → Branch: `main` / root 로 설정하면 공개됩니다.

## 디자인 시스템

| 토큰 | 값 | 용도 |
|------|-----|------|
| Navy | `#2F3E72` | 로고 · 제목 · 주요 버튼 |
| Indigo | `#5A5BD6` | AI · 강조 · CTA · 활성 메뉴 텍스트 |
| Lavender | `#ECECFB` | 활성 메뉴 배경 · 뱃지 |
| Green | `#15A06B` | 지원사업 · 진행 · 완료 |
| Red | `#DC4444` | 마감 임박(D-day) |
| Page BG | `#F5F6F8` | 페이지 배경 |
| Card border | `#E8EAEE` | 카드 테두리 |

- 타입: **Pretendard** (Korean), CDN 로드
- 톤: 창업 입문자에게 부담 없는 깔끔한 제품 UI

## 참고 (Claude Code 작업 시)

- 모든 스타일은 **인라인 `style`** 으로 작성되어 있습니다. 컴포넌트화/CSS 분리는 필요에 따라 진행하세요.
- 아이콘은 인라인 **SVG** 입니다.
- `step-detail.html` 의 "AI 초안 생성" 버튼은 데모용 목업 인터랙션(미리 정의된 텍스트 표시)입니다. 실제 LLM·RAG 연동 지점입니다.
- 아바타/이미지는 플레이스홀더입니다.

---

© 2026 StepUp. Culture & Arts Entrepreneurship Support Platform.
