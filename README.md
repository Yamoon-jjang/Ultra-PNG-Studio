# 🎨 Ultra PNG Studio v2.2

**AI Background Remover · Transparent PNG Editor · Text PNG Maker**

**🇰🇷 한국어 / 🇺🇸 English · One HTML file · No installation**

[📦 **v2.2 다운로드 / Download v2.2**](https://github.com/Yamoon-jjang/Ultra-PNG-Studio/releases/latest) · [🇰🇷 한국어 소개](#korean) · [🇺🇸 English overview](#english) · [📖 사용 설명서 / Manuals](#documentation)

![Ultra PNG Studio v2.2 — Background Remover, Transparent PNG Editor, Text PNG Maker and KO/EN UI](screenshots/00_overview.png)

> **한국어:** 사진의 배경 제거, 투명 이미지 보정, 투명 텍스트 PNG 제작을 하나의 브라우저 앱에서 처리합니다. 설치 프로그램이나 별도의 이미지 업로드 서버가 필요하지 않습니다.
>
> **English:** Remove image backgrounds, edit transparent graphics and create text PNGs in one browser-based app. No installer or separate image-upload server required.

| 🇰🇷 한국어 화면 / Korean UI | 🇺🇸 English interface |
| :---: | :---: |
| ![Ultra PNG Studio landing screen in Korean](screenshots/01_landing_ko.png) | ![Ultra PNG Studio landing screen in English](screenshots/01_landing_en.png) |

<a id="korean"></a>

---

# 🇰🇷 한국어

Ultra PNG Studio v2.2는 **AI·수동 배경 제거**, **투명 이미지 편집**, **텍스트 PNG 제작**을 한곳에서 처리하는 독립 실행형 HTML 이미지 편집 앱입니다. ZIP 압축을 풀고 Chrome 또는 Edge에서 \`index.html\`을 열면 사용할 수 있습니다.

## ✨ 한눈에 보는 세 가지 작업

| ① 배경 제거 | ② 투명 이미지 편집 | ③ 텍스트 PNG |
| :---: | :---: | :---: |
| ![배경 제거 작업 화면](screenshots/02_background_removal_ko.png) | ![투명 이미지 편집 화면](screenshots/03_transparent_edit_ko.png) | ![텍스트 PNG 제작 화면](screenshots/04_text_png_ko.png) |
| AI 자동 제거와 세 가지 수동 제거 방식 | 외곽선·그림자·이미지 효과 | 시스템/사용자 글꼴·실시간 미리보기 |

### ① ✨ AI / 수동 배경 제거

인물·제품·사물 사진의 배경을 제거하거나, 로고와 도안의 단색 배경을 투명하게 만드는 기능입니다.

- **AI 자동 배경 제거:** 브라우저에서 IMG.LY 모델을 사용해 배경을 분리합니다. 최초 AI 실행에는 외부 CDN에서 라이브러리·WASM·모델 파일을 다운로드할 인터넷 연결이 필요합니다.
- **세 가지 수동 제거:** **스마트**, **지정 색상**, **가장자리 연결** 방식 중 이미지 특성에 맞게 선택할 수 있습니다.
- **경계 및 결과 보정:** 페더링과 투명도, 배경색, 출력 영역 등을 조절한 뒤 결과를 확인할 수 있습니다.
- **저장:** 배경 제거 결과를 투명 PNG로 저장하거나 지원되는 배경 채우기·이미지 출력 옵션을 이용할 수 있습니다.

**사용 예:** 프로필 사진, 제품 이미지, 스티커, 배경이 단색인 로고 및 삽화.

### ② 🪄 투명 이미지 편집

배경이 이미 투명한 PNG를 불러와 추가 효과를 적용하고, 필요한 출력 크기와 배치를 정리합니다.

- **테두리와 광원 효과:** 외곽선, 글로우, 그림자의 색상과 크기 등을 조절합니다.
- **기본 이미지 보정:** 밝기·대비·채도 및 이미지 효과를 조절합니다.
- **배치 및 출력:** 회전·반전, 자동 자르기, 정사각형 출력, 타일 미리보기를 사용할 수 있습니다.
- **복구 기능:** **실행취소 / 다시실행 / 처음 상태 복구**로 작업 내용을 관리합니다.

**사용 예:** 투명 로고, 캐릭터 이미지, 아이콘, 썸네일·영상용 오버레이.

### ③ 🔤 텍스트 PNG 제작

텍스트를 원하는 글꼴과 색상으로 구성해 투명 PNG로 내보냅니다.

- **텍스트 설정:** 입력 문구, 글꼴, 크기, 색상, 굵게·기울임을 선택합니다.
- **실시간 미리보기:** 문구나 스타일을 바꾸면서 이미지 결과를 확인할 수 있습니다.
- **글꼴 선택:** Windows 시스템 글꼴과 사용자가 직접 선택한 **TTF / OTF / WOFF / WOFF2** 글꼴을 사용할 수 있습니다.
- **추가 편집과 저장:** 이미지 효과 및 지원되는 PNG 출력·복구 옵션을 사용할 수 있습니다.

**사용 예:** 동영상 자막 그래픽, 타이틀, 썸네일 문구, 로고 텍스트.

## 🌐 한글 / 영어 언어 전환

- 상단의 **KO / EN** 캡슐형 전환 버튼은 [Ultra Exif Reader](https://github.com/Yamoon-jjang/Ultra-Exif-Reader)와 디자인을 통일했습니다.
- 브라우저 언어가 한국어면 KO, 그 외에는 EN을 기본으로 표시합니다. 수동 선택은 브라우저 저장소가 허용하면 다음 실행에도 기억됩니다.
- 작업 중 전환해도 **원본 이미지, 사용자 입력 텍스트, 파일명, 글꼴 내부 값, 실행취소 기록**은 변경하지 않습니다.
- 메뉴, 설정, 툴팁, 상태 메시지, 오류 안내 등을 선택한 언어로 표시합니다.

## 📥 다운로드 및 실행 방법

1. [**GitHub Releases에서 최신 v2.2 ZIP 다운로드**](https://github.com/Yamoon-jjang/Ultra-PNG-Studio/releases/latest)
2. ZIP 압축을 풉니다.
3. **\`Ultra-PNG-Studio/index.html\`**을 Chrome 또는 Edge로 실행합니다.
4. 세 가지 작업 중 하나를 선택해 이미지를 불러오거나 텍스트를 입력합니다.
5. 편집 결과를 확인한 후 해당 모드에서 지원하는 PNG/JPG 형식으로 저장합니다.

별도 설치 프로그램, 계정, 로컬 서버가 필요하지 않습니다. GitHub Pages는 저장소 소유자가 별도로 활성화하면 HTTPS 웹 페이지로도 제공할 수 있습니다.

## 🧰 추가 기능 및 파일 처리

| 항목 | 설명 |
|---|---|
| **SVG 입력** | viewBox만 있는 SVG의 고해상도 처리, 한쪽 크기만 명시된 SVG와 네임스페이스 접두사 SVG 지원 |
| **저장 파일명** | 원본 파일명을 활용하고 한글·이모지 등 유니코드 이름을 안전하게 처리 |
| **투명도와 배경** | 투명 PNG, 단색 배경 출력 및 해당 모드의 JPG 저장 옵션 |
| **이미지 안전 제한** | 매우 큰 캔버스·메모리 요구가 있는 입력은 안전 안내 후 제한될 수 있음 |
| **작업 이력** | 실행취소, 다시실행, 처음 상태 복구 지원 |

## 🔠 글꼴 저작권 및 사용자 글꼴

**GitHub 저장소와 배포 ZIP에는 글꼴 파일을 동봉하지 않습니다.** 저작권·재배포 제한을 피하면서도 글꼴 사용 기능은 유지하기 위한 구성입니다.

- Windows에서 사용할 수 있는 시스템 글꼴을 선택하거나, 앱의 **커스텀 폰트 불러오기**를 통해 직접 보유한 TTF·OTF·WOFF·WOFF2 파일을 선택하세요.
- 사용자는 글꼴마다 다른 **사용 범위, 상업적 이용, 수정·재배포 조건**을 직접 확인해야 합니다.
- 공식 참고 경로: [Pretendard](https://github.com/orioncactus/pretendard) · [네이버 나눔글꼴](https://hangeul.naver.com/font) · [Google Fonts](https://fonts.google.com/)

## 🔒 개인정보, 네트워크 및 AI 사용 시 주의 사항

- 이미지 편집·저장은 브라우저에서 처리하며, 앱 자체적으로 운영하는 **이미지 업로드 서버는 없습니다.**
- AI 자동 배경 제거는 최초 실행 시 **IMG.LY, ONNX/WASM, AI 모델**을 외부 CDN에서 다운로드하므로 인터넷 연결이 필요합니다. 다운로드된 리소스의 캐시 동작은 브라우저 환경에 따라 달라질 수 있습니다.
- 과도하게 큰 이미지와 일부 SVG는 캔버스 크기·메모리 안전 제한에 걸릴 수 있습니다.
- **검증 범위:** Chromium 자동화로 일반 이미지 처리, 파일명·SVG 경계 사례, KO/EN 전환 및 캔버스 경고를 확인했습니다. 하지만 **실제 Windows 로컬 HTML에서의 AI 모델 다운로드·실추론과 GitHub Pages AI 실행은 별도 PC 검증이 필요**합니다.

**📖 자세한 사용법:** [한국어 매뉴얼](docs/manual.md) · [실사용 PC 테스트 체크리스트](docs/TEST_BEFORE_GITHUB_RELEASE.md)

<a id="english"></a>

---

# 🇺🇸 English

**Ultra PNG Studio v2.2** is a **portable, single-file HTML editor** combining **AI/manual background removal**, **transparent-image editing** and **text PNG generation**. Extract the ZIP and open \`index.html\` in Chrome or Edge. No desktop installation or dedicated image-upload server is needed.

## ✨ Three editing modes at a glance

| ① Background Remover | ② Transparent PNG Editor | ③ Text PNG Maker |
| :---: | :---: | :---: |
| ![Background removal interface in English](screenshots/02_background_removal_en.png) | ![Transparent image editor in English](screenshots/03_transparent_edit_en.png) | ![Text PNG maker in English](screenshots/04_text_png_en.png) |
| AI removal and three manual methods | Outlines, shadows and image effects | System/custom fonts and live preview |

### ① ✨ AI & Manual Background Removal

Remove backgrounds from portraits, products and objects, or make flat-color backgrounds transparent in logos and illustrations.

- **AI background removal:** Use the IMG.LY model inside your browser to separate foreground and background. The first AI run requires internet access to download code, WASM and model files from external CDNs.
- **Three manual removal methods:** Choose **Smart**, **Selected Color** or **Edge-Connected** removal depending on the image.
- **Edge and result refinement:** Adjust feathering, transparency, background fill and export-area settings as supported by the mode.
- **Export options:** Save removed-background results as transparent PNGs, or apply supported background-fill and image-output options.

**Ideal for:** Profile pictures, product images, stickers, simple logos and illustrations with plain backgrounds.

### ② 🪄 Transparent PNG Editing

Load an existing transparent PNG, apply finishing effects and prepare the composition for export.

- **Borders and lighting:** Add and customize outlines, glow and drop shadows.
- **Image adjustments:** Fine-tune brightness, contrast, saturation and supported image effects.
- **Layout and sizing:** Rotate or flip, auto-crop transparent margins, use square output and preview tiled backgrounds.
- **History controls:** **Undo / Redo / Restore to Initial State** let you reverse changes and recover the starting image.

**Ideal for:** Transparent logos, character art, icons, thumbnails and video overlays.

### ③ 🔤 Text PNG Maker

Create text graphics with transparent backgrounds, your preferred typography and a live preview.

- **Text styling:** Edit your text, font, size, color, bold and italic options.
- **Live preview:** See the rendered PNG layout update while editing text and style settings.
- **Font support:** Choose available Windows system fonts or import your own **TTF / OTF / WOFF / WOFF2** files.
- **Further editing and export:** Use applicable image effects, PNG export and history controls.

**Ideal for:** Video title cards, subtitle overlays, thumbnail captions and text-based logos.

## 🌐 Korean / English Interface

- The top **KO / EN** segmented switch matches the visual style of [Ultra Exif Reader](https://github.com/Yamoon-jjang/Ultra-Exif-Reader).
- A Korean browser locale selects KO by default; other locales select EN. Your manual preference is remembered for future launches when browser storage permits.
- You can switch languages **without changing the loaded image, user-entered text, filename, internal font values or undo history**.
- Menus, controls, tooltips, status messages and error guidance follow the selected interface language.

## 📥 Download & Run

1. [**Download the latest v2.2 ZIP from GitHub Releases**](https://github.com/Yamoon-jjang/Ultra-PNG-Studio/releases/latest).
2. Extract the archive.
3. Open **\`Ultra-PNG-Studio/index.html\`** in Chrome or Edge.
4. Select a mode, load an image or enter text, and apply your edits.
5. Preview the result and export to a PNG/JPG format supported by the selected mode.

**No installer, account or local server is required.** GitHub Pages hosting is possible if the repository owner enables it separately; this README does not imply that a Pages site is already live.

## 🧰 Additional Features & File Handling

| Feature | Description |
|---|---|
| **SVG import** | High-resolution rendering of viewBox-only SVGs, single-dimension SVGs and namespace-prefixed SVGs |
| **Output filenames** | Source-based filenames, including safe handling of Korean text, emoji and other Unicode characters |
| **Transparency & backgrounds** | Transparent PNGs, solid-background output and mode-dependent JPG options |
| **Image safety limits** | Oversized canvases or memory-intensive inputs may be rejected with explanatory warnings |
| **Edit history** | Undo, Redo and Restore to Initial State |

## 🔠 Custom Fonts & Redistribution

**No font binaries are bundled in the GitHub repository or release ZIP.** This avoids unnecessary third-party redistribution risks while keeping font-import features available.

- Use an available Windows system font or select a font file you legally obtained through **Import Custom Font**.
- Supported imports: **TTF, OTF, WOFF and WOFF2**.
- Check each font provider's separate license for personal use, commercial use, modification and redistribution.
- Official font resources: [Pretendard](https://github.com/orioncactus/pretendard) · [Naver Nanum Fonts](https://hangeul.naver.com/font) · [Google Fonts](https://fonts.google.com/)

## 🔒 Privacy, Network Requirements & AI Limitations

- Editing and exporting images take place in your browser. **The application does not operate its own image-upload server.**
- First-time AI background removal downloads **IMG.LY components, ONNX/WASM resources and model files** from third-party CDNs. Internet access is required, and caching depends on the browser environment.
- Very large images and some SVG inputs can hit canvas-dimension or memory safety limits.
- **Validation scope:** Automated Chromium checks covered core editing, SVG and filename edge cases, KO/EN interface behavior and canvas warnings. **Real AI model download/inference on Windows local HTML and AI operation over GitHub Pages still require separate real-device verification.** Automated results are not a guarantee of live AI execution.

**📖 Detailed guidance:** [Complete English Manual](docs/manual_en.md) · [Pre-release PC Test Checklist](docs/TEST_BEFORE_GITHUB_RELEASE.md)

<a id="documentation"></a>

---

## 📚 문서 / Documentation

| 한국어 | English |
|---|---|
| [🇰🇷 한국어 사용 설명서](docs/manual.md) | [🇺🇸 Complete English Manual](docs/manual_en.md) |
| [📦 v2.2 정식 릴리즈](https://github.com/Yamoon-jjang/Ultra-PNG-Studio/releases/tag/v2.2) | [📦 Official v2.2 Release](https://github.com/Yamoon-jjang/Ultra-PNG-Studio/releases/tag/v2.2) |
| [📝 변경 내용](docs/RELEASE_NOTES_v2.2.md) | [📝 Release Notes](docs/RELEASE_NOTES_v2.2.md) |
| [✅ 테스트 보고서](docs/TEST_REPORT.md) | [✅ Automated Test Report](docs/TEST_REPORT.md) |
| [🧪 PC 실사용 점검](docs/TEST_BEFORE_GITHUB_RELEASE.md) | [🧪 Real-device Test Checklist](docs/TEST_BEFORE_GITHUB_RELEASE.md) |
| [⚖️ 외부 구성요소 고지](THIRD_PARTY_NOTICES.md) | [⚖️ Third-party Notices](THIRD_PARTY_NOTICES.md) |

**라이선스 / License:** [GNU AGPL-3.0](LICENSE) · **개발자 / Developer:** [Yamoon-jjang](https://github.com/Yamoon-jjang)

---

**One Studio · Three Editing Modes · Two Languages**
