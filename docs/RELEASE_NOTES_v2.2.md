# Ultra PNG Studio v2.2 — Release Notes / 릴리즈 안내

> **Release preparation draft (not yet published).** Publish as an official `v2.2` GitHub Release only after Windows Chrome/Edge real-AI and GitHub Pages verification.

## 한국어

**Ultra PNG Studio v2.2**는 브라우저에서 바로 실행할 수 있는 이미지 편집 앱의 **한글·영어 공용 버전**입니다. 배경 제거, 투명 이미지 편집, 투명 텍스트 PNG 제작을 하나의 HTML 파일로 제공합니다.

### v2.2 주요 변경

- **KO / EN 언어 전환:** Ultra Exif Reader와 동일한 캡슐형 KO·EN 스위치 및 선택 강조 디자인을 적용했습니다.
- **완전한 앱 화면 현지화:** 메인 화면, 세 작업 모드, 설정, 툴팁, 상태, 오류 알림, 접근성 레이블을 영어와 한국어로 사용할 수 있습니다.
- **영문 캔버스 경고 보완:** 작업 이름에 공백이 포함되어도 예상 크기·안전 제한 메시지 전체가 영어로 표시됩니다.
- **자동·수동 언어 선택:** 브라우저 언어를 기준으로 기본 선택하며, 사용자가 선택한 언어는 브라우저 저장소가 허용하는 경우 기억됩니다. 작업 중 전환해도 이미지·텍스트·폰트 내부 값·Undo 기록은 변하지 않습니다.
- **기존 기능 보존:** 직전 통합 검증본의 SVG 해상도 처리, 원본 파일명 기반 저장, AI 오류 안내, 수동 제거 3방식, 편집 효과, 실행취소·복구 등을 유지했습니다.
- **저작권·배포 구성:** 글꼴 바이너리 동봉 없음. AGPL-3.0, 외부 라이브러리 라이선스 고지, KO/EN 매뉴얼 및 실제 화면 예제 포함.

### 제공 기능

AI / 수동 배경 제거 · 외곽선 및 그림자 · 투명 PNG 보정 · 텍스트 PNG · 실시간 텍스트 미리보기 · TTF/OTF/WOFF/WOFF2 직접 불러오기 · 회전/반전 · 타일 미리보기 · 자동 자르기 · PNG/JPG 저장 · Undo/Redo/Restore · SVG 지원.

### 다운로드 / 설치

배포 ZIP을 풀고 `Ultra-PNG-Studio/index.html`을 Chrome 또는 Edge로 열면 됩니다. 설치 프로그램이 필요하지 않습니다. GitHub Pages HTTPS 웹 배포도 가능합니다.

**AI 기능 안내:** 최초 AI 배경 제거에는 외부 CDN에서 라이브러리·WASM·모델 다운로드가 필요합니다. 일반 편집 및 수동 제거는 앱 내부에서 처리됩니다. 이미지 파일을 앱 자체 서버에 업로드하지 않습니다.

### 테스트 및 주의 사항

자동화 테스트: 기존 기능 회귀 **83/83**, 추가 경계 사례 **43/43**, 언어 전환·상태·모바일 **49/49** 통과. 실제 Windows 로컬 HTML 실행, CDN AI 모델 다운로드·실추론 및 GitHub Pages에서의 AI 실행은 공개 전 실기기 확인이 필요합니다. 자세한 기록은 `docs/TEST_REPORT.md`를 참고하세요.

---

## English

**Ultra PNG Studio v2.2** introduces a **bilingual Korean/English interface** to the portable, single-file HTML editor for background removal, transparent-image editing and text PNG generation.

### What's new

- **KO / EN language switch** with the same segmented control design as Ultra Exif Reader, including a clear gold active state.
- **Localized interface:** Landing page, three task modes, settings, tooltips, statuses, error notifications and accessibility labels are available in both Korean and English.
- **Canvas warning translation fix:** Safety-limit and expected-size alerts now fully translate even when operation names contain spaces.
- **Automatic locale detection and preference:** Korean browser locales default to KO, other locales to EN, with a manual override remembered when browser storage permits. Switching language does not alter images, input text, font values or editing history.
- **Preserved editing engine:** The proven SVG import behavior, source-based output filenames, detailed AI error messages, manual removal modes, effects, undo/redo and reset logic remain intact.
- **Distribution-ready documentation:** Bilingual README and manuals, updated screenshots, AGPL-3.0 notice, dependency licenses, no bundled font binaries.

### Included features

AI and manual background removal; outlines and drop shadows; image adjustments, flip/rotate, tiled preview, auto-crop and square output; transparent text PNGs with manually imported TTF/OTF/WOFF/WOFF2 fonts; PNG/JPG exports; undo/redo/restore; SVG input support.

### Installation

Extract the ZIP and open `Ultra-PNG-Studio/index.html` in current Chrome or Edge. No installer or server-side image upload is needed. The app can also be hosted on GitHub Pages over HTTPS.

**Network requirement:** First-time AI background removal downloads code, WASM and a model from third-party CDNs. Manual editing and export run locally in the browser.

### Test status and limitations

Automated tests passed: **83/83** baseline regressions, **43/43** boundary cases and **49/49** language / mobile / state checks. Real Windows local HTML execution, real AI CDN/WASM/model inference, and GitHub Pages HTTPS AI functionality were **not** verified in the automation environment. Complete the real-world test checklist before marking this release final.

**License:** [GNU AGPL-3.0](../LICENSE). See [third-party notices](../THIRD_PARTY_NOTICES.md) and [test checklist](TEST_BEFORE_GITHUB_RELEASE.md).
