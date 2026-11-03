# Third-party software notices / 외부 구성요소 고지

Ultra PNG Studio V2.2 is released under **GNU AGPL-3.0** (see `LICENSE`).
This notice distinguishes separately licensed components; it does not relicense them.

## 1. IMG.LY Background Removal

- Package: `@imgly/background-removal`
- Version: `1.7.0`
- License: GNU Affero General Public License (AGPL-3.0)
- Copyright: IMG.LY GmbH and respective contributors
- Source: https://github.com/imgly/background-removal-js
- Package: https://www.npmjs.com/package/@imgly/background-removal
- License text: `LICENSE` (AGPL-3.0)
- Loaded dynamically from: `https://cdn.jsdelivr.net/npm/@imgly/background-removal@1.7.0/dist/index.min.mjs`
- Model/runtime assets: `https://staticimgly.com/@imgly/background-removal-data/1.7.0/dist/`

Original upstream package code is not copied into this repository; the browser requests it from the CDN when AI removal is invoked. Upstream includes additional third-party components (see upstream `ThirdPartyLicenses.json`).

## 2. Microsoft ONNX Runtime Web

- Package: `onnxruntime-web`
- Version: `1.21.0`
- License: MIT
- Copyright: Microsoft Corporation and contributors
- Source: https://github.com/microsoft/onnxruntime
- License text: `docs/ONNX-Runtime-MIT.txt`
- CDN imports: `https://cdn.jsdelivr.net/npm/onnxruntime-web@1.21.0/dist/`

## 3. AI model and transitive dependencies

- Model configured by this app: `isnet_fp16` (IMG.LY's published model assets)
- The upstream IMG.LY package's third-party license information includes ONNX Runtime Web (MIT), ISNET (MIT), lodash-es (MIT), ndarray (MIT), and zod (MIT):
  https://unpkg.com/@imgly/background-removal@1.7.0/ThirdPartyLicenses.json
- These are external, demand-loaded resources, not redistributions within this ZIP.

## 4. Fonts / 글꼴

No font binaries are distributed with Ultra PNG Studio. Its selectable local system fonts and user-imported files are loaded locally in the browser. Users should obtain individual fonts from their legitimate publishers and follow the publisher's terms; the user is responsible for the permitted use of any selected font.

## 5. Network and privacy / 네트워크·개인정보

Normal image editing is local in the browser. AI processing is also browser-based, but AI runtime code, WASM and model assets may be fetched from the external CDN providers listed above, so browsers contact those providers. This project does not supply an image-upload server. Do not claim the entire application works fully offline on first AI use.
