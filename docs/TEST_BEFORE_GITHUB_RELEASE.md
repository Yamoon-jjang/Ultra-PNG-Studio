# Ultra PNG Studio v2.2 — 공개 전 실제 PC 시험 / Pre-release PC Checklist

본 패키지는 자동화 검증을 마친 **GitHub 공개 전 테스트본**입니다. 정상 작동 확인 전에는 Release를 최종 발행한 것으로 안내하지 마세요.

## Windows Chrome / Edge에서 확인

- [ ] ZIP을 풀고 `index.html`을 직접 열어 오류 없이 실행됩니다.
- [ ] 한국어 브라우저는 기본 KO, 영어 브라우저는 기본 EN으로 표시됩니다.
- [ ] 상단 KO / EN 캡슐형 스위치로 전환되며, Ultra Exif Reader의 스위치와 시각적으로 일치합니다.
- [ ] 앱의 메뉴, 3개 작업 모드, 도움말, 알림, 오류 및 상태 표시가 선택 언어로 바뀝니다.
- [ ] 언어를 바꾼 뒤 브라우저를 종료하고 다시 열면 수동 선택이 유지됩니다. (브라우저 정책이 허용할 때)
- [ ] 사용자가 입력한 **한글 텍스트**, 선택한 글꼴 및 이미지 이름은 KO/EN 변경 후에도 바뀌지 않습니다.
- [ ] `배경 제거`: 검정/흰색/컬러 로고를 열고 Smart / Selected Color / Edge-Connected 세 방식을 시험합니다.
- [ ] **실제 AI 배경 제거:** 첫 실행에 외부 라이브러리·WASM·모델이 다운로드되며, 인물/제품 사진의 배경이 실제로 제거됩니다. (모의 시험 아님)
- [ ] AI 다운로드 실패/오프라인 상태에서 한국어와 영어 안내가 이해 가능하게 출력됩니다.
- [ ] `투명 이미지 편집`: 외곽선, 그림자, 회전·반전, 밝기·대비·채도 등을 적용합니다.
- [ ] `텍스트 PNG`: Windows 글꼴을 선택하고 한글/영문 텍스트를 만든 뒤 실시간 수정합니다.
- [ ] 사용자 TTF/OTF/WOFF/WOFF2 폰트를 직접 불러와 적용합니다. ZIP 안에는 글꼴 파일이 없습니다.
- [ ] PNG·미리보기 PNG·흰 배경 JPG·단색 배경 PNG 저장과 저장 파일명을 확인합니다.
- [ ] Undo / Redo / Restore Initial State가 두 언어에서 동일하게 작동합니다.
- [ ] viewBox만 있는 SVG와 한쪽 치수만 있는 SVG가 선명하고 올바른 비율로 표시됩니다.
- [ ] 320px·390px 모바일 폭에서 언어 버튼과 주요 기능이 잘리지 않고 조작할 수 있습니다.
- [ ] 매우 큰 SVG/이미지 입력에서 적절한 크기 제한 메시지가 나오고 편집 중인 이미지가 손상되지 않습니다.

## GitHub 게시 후 확인

- [ ] 저장소 루트에 `index.html`, `README.md`, `LICENSE`, `THIRD_PARTY_NOTICES.md`, `docs/`, `screenshots/`가 있습니다.
- [ ] README 첫 화면의 배너와 세 기능별 스크린샷, KO/EN 비교 이미지가 올바르게 표시됩니다.
- [ ] README/매뉴얼/릴리즈 문서에 **v2.2** 표기가 일관됩니다.
- [ ] GitHub Pages를 활성화한 뒤 HTTPS에서 동일한 3개 모드가 작동합니다.
- [ ] **GitHub Pages에서 실제 AI 배경 제거**를 다시 수행합니다. 로컬 실행의 성공이 HTTPS에서 성공을 보장하지 않습니다.
- [ ] 첫 화면 AGPL 고지 및 저장소의 LICENSE/외부 라이브러리 링크가 유효합니다.
- [ ] Release 태그 `v2.2`, 릴리즈 제목, 배포 ZIP 및 영문/한글 설명이 일치합니다.
- [ ] Release ZIP이 GitHub 저장소의 검증된 `index.html`과 같은 내용인지 SHA256으로 비교합니다.

## English: essential smoke tests

1. Open `index.html` locally with current Chrome and Edge. Confirm the KO/EN capsule, auto-detection and language preference across browser restarts where allowed.
2. Switch languages during image/text editing. Check no user image, filename, font setting, typed characters or undo history are changed.
3. Try manual background removal in all three methods, edit an existing transparent PNG, and create a transparent text PNG with a local font.
4. Export all PNG/JPG variants and verify names and transparency. Try a viewBox SVG and an oversized input.
5. **Perform real first-time IMG.LY AI inference**, including CDN/model download, on local Windows browsers. Repeat after enabling GitHub Pages HTTPS.
6. Verify README images, AGPL notice, manuals, version `v2.2` and release artifacts before publication.

Please report failures with browser/version, operating system, input format, whether the page was opened via `file://` or GitHub Pages HTTPS, and the exact error message. Do not upload personal photos or proprietary font files when filing a public bug report.
