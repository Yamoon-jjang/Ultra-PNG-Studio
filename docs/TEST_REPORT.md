# Ultra PNG Studio v2.2 — 테스트 결과 / Validation Report

**검증 일자:** 2026-11-03 · **대상:** `index.html` 포함 V2.2 KO/EN 소스 · **검증 환경:** Linux Chromium 자동화 (Playwright)

## 주요 자동화 결과

| 검사 | 통과 / 전체 | 핵심 내용 |
|---|---:|---|
| 기존 이미지 편집 회귀 | **83 / 83** | 원본 이미지 결과 동일성, 수동 배경 제거 세 방식, 텍스트·투명 이미지, SVG, PNG/JPG 다운로드, 외부 TTF, Undo/Redo/Restore, 모바일 |
| 기존 통합본 경계 사례 | **43 / 43** | SVG viewBox/단일 길이/단위/네임스페이스, 과대 입력, UTF-16 이모지 안전 파일명, AI 오류 및 알림 |
| V2.2 KO/EN·상태 시험 | **49 / 49** | 언어 자동 선택, 수동 스위치, 한국어 입력 보존, 폰트 식별 유지, 영어 오류 메시지, 영어 PNG 저장, Undo/Redo, 화면 폭, 500회 동적 UI 갱신 |
| **합계** | **175 / 175** | 중복되는 핵심 사용자 동작을 다른 조건에서 재확인한 항목 포함 |

추가로 KO/EN 모드의 주요 화면과 오류 상태에서 번역되지 않은 **앱 작성 UI 한글 텍스트 및 접근성 속성**이 남는지 검사했고, 해당 시험 상태에서 검출 항목이 없었습니다. 사용자 텍스트·파일명·폰트 파일명은 번역 대상으로 간주하지 않았습니다.

## v2.2 캔버스 안전 경고 영문 번역 수정 (2026-11-03)

- 작업 이름에 띄어쓰기가 있는 경우 `캔버스 안전 제한` 메시지 일부가 한글로 남던 문제를 수정했습니다. 해당 번역 정규식의 작업 이름 캡처를 `\S+`에서 `.+?`(비탐욕 일치)로 한 곳 변경했습니다.
- Chromium에서 **7개 실제 작업 이름 × 3개 제한 조건 × KO/EN = 42개**, 각 언어 초기 상태와 페이지 오류 = 4개, **KO→EN→KO 활성 경고 전환 = 2개**, 총 **48/48** 추가 회귀 검사 통과.
- 기존 자동화 **83/83 + 43/43 + 49/49**도 수정본에서 재실행하여 통과했습니다. 이번 변경은 한/영 UI 메시지용 정규식에만 한정되며 캔버스 안전 제한, 이미지 처리, 저장, AI 엔진은 변경하지 않았습니다.

## 변경 범위 보존 및 정적 검사

- SVG 입력 처리, 이미지 색상/알파 알고리즘, 출력 렌더링, AI 실행 엔진의 기존 로직은 변경하지 않았습니다. 새로운 언어 레이어는 독립된 후행 `<script>`로 추가했습니다.
- 새 스위치와 스타일을 제외한 앱 UI 구조는 이전 검증된 기준 소스 구조를 유지합니다.
- JS 문법 및 import map JSON 파싱, HTML ID 중복 없음, CSS 문법/블록 균형, 라이선스 및 README 링크, 최종 ZIP의 무결성, 경로 안전성, 20개 파일의 재추출 바이트 일치를 확인했습니다. 재추출된 HTML로 언어 전환·텍스트 PNG·이미지 PNG 저장을 다시 검증한 13개 스모크 시험도 통과했습니다.
- 언어 전환 시 작업을 재시작하거나 업로드된 이미지를 번역·재인코딩하는 기능은 없습니다.
- 사진 편집 및 저장에 사용되는 IMG.LY `1.7.0`, ONNX Runtime Web `1.21.0` 및 AI 모델 `isnet_fp16` 설정은 그대로입니다.

## 자동화에서 확인하지 못한 범위

1. **Windows 실제 Chrome/Edge에서 로컬 `file://` HTML을 직접 실행하는 사용자 테스트.** 컨테이너의 브라우저 접근 정책으로 `file://`와 localhost `page.goto()`가 차단되어, Chromium `set_content()` 방식으로 검증했습니다.
2. **실제 네트워크를 통한 IMG.LY CDN/WASM/모델 다운로드 및 AI 실추론.** AI 처리 성공·실패 상태는 로컬 모의 엔진으로 테스트했습니다.
3. **실제 GitHub Pages HTTPS 배포 후 AI 동작.** 아직 GitHub 저장소/Pages/Release에 게시하지 않았습니다.
4. **실제 기기별 초고해상도 메모리 스트레스.** 크기 제한 로직은 시험했지만 장치별 GPU/메모리 부족을 전부 재현한 것은 아닙니다.
5. **브라우저 재실행 후 언어 선택 저장의 실환경 동작.** 코드에는 localStorage 기반 기억이 구현되어 있지만, 위 테스트 환경에서는 about:blank 저장소 접근이 차단되어 영속성 검증을 수행할 수 없었습니다.

완전 무결성을 보증하는 문서가 아닙니다. 배포 전에 [PC 실사용 체크리스트](TEST_BEFORE_GITHUB_RELEASE.md)를 따라 위 항목을 확인해 주세요.

## English summary

All **175/175 automated checks** passed across original editing regressions (83), SVG/filename/AI boundary conditions (43), and KO/EN UI, state, mobile and accessibility-related behaviors (49). Core rendering and AI integration source were kept intact; the bilingual layer only changes UI presentation. Real Windows `file://` execution, true CDN/WASM/AI inference, persistence across browser restarts and hosted GitHub Pages AI must be verified by the publisher before a final public release.
