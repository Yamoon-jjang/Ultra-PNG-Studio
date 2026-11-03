# Ultra PNG Studio v2.2 — English User Manual

**Author:** Yamoon-jjang · **Application:** `index.html` · **License:** AGPL-3.0

[한국어 상세 매뉴얼](manual.md) · [README](../README.md)

## 1. What this application does

Ultra PNG Studio is a single HTML app for creating and adjusting transparent PNGs in Chrome or Edge. It has **three task types**: Background Removal, Transparent Image Editing, and Create Transparent Text. It does not require an installer, server-side image uploads, or an account.

- **Background Removal:** Remove a solid-colored background using manual tools, or run AI background removal for complex photos, people and products.
- **Transparent Image Editing:** Add outlines, shadows, color adjustments or transformations to images that already contain transparency.
- **Create Transparent Text:** Turn your own words into transparent PNG images using built-in or manually imported fonts.

The editor can also export a PNG containing the preview background or a JPG composited onto white.

## 2. Run locally, and switch the interface language

1. Download/extract the distribution ZIP and open `index.html` in a recent **Chrome** or **Microsoft Edge** browser.
2. On the landing screen, choose one of the three task cards.
3. Select an image file or enter text, then edit and export.

The top bar contains a **KO / EN** segmented switch, designed to match Ultra Exif Reader. The selected button uses a warm gold highlight. The app starts in Korean when your browser locale begins with `ko`, otherwise English. If supported by your browser, your manual choice is saved using localStorage and restored next time. Browsers may restrict local storage for local files or privacy modes.

Changing the interface language does **not** translate text you typed into the editor, alter any uploaded filename, replace a font family, change your current image, clear the editor history, or rerun the AI model. Only UI text, tooltips, status messages and relevant accessibility labels change.

## 3. Basic controls

- **Task selection / Home:** Return to the three task cards. Starting a new task clears the current editor work, so export first.
- **Choose File / Drop Zone:** Open the picker or drag an image onto the appropriate dashed area. The drop zone accepts images, not folders or documents.
- **Quick Tools:** Enable or disable background removal or shadows without opening the full settings panel.
- **Settings Panel:** Shows task-specific controls. You can collapse it, particularly on a small screen.
- **Preview Background:** View your PNG over a checkerboard, white, black, gray, your own color, or a chosen background image. This is normally a display-only setting unless you explicitly export a preview-background PNG or use solid-background output.
- **Preview Zoom:** Use the zoom slider or activate the canvas zoom mode. Panning and zooming affect only the preview and do not change export resolution.
- **Undo / Redo:** Ctrl+Z, Ctrl+Y (or Ctrl+Shift+Z). Reverses changes to editor settings and relevant image results, within the stored history capacity.
- **Restore Initial State:** Restores the current task's initial image/text source and default editing settings. The action itself can be undone where an earlier state exists.

Tooltips explain the controls when hovered or focused, in the currently selected language.

## 4. Background Removal: manual and AI

Open **Background Removal**, then choose a PNG, JPG/JPEG, WebP, GIF, BMP, SVG or AVIF file that your browser can decode.

### 4.1 Manual background color removal

For logos, text artwork, scanned graphics or products against a flat background, choose **Manual Color Removal**. There are three methods:

1. **Smart:** Estimates transparency from color distance and sensitivity. Best initial choice for simple solid-color backgrounds.
2. **Selected Color:** Removes similar colors throughout the entire image. Use with care if the subject has the same color as the background.
3. **Edge-Connected:** Removes matching areas connected to the outer border while trying to preserve similar colors inside the subject.

Set the **Color to Remove** manually, pick black or white, or use **Auto-Detect Corners** to sample the four corners. Adjust **Detection Sensitivity**, **Full Removal Range**, **Tolerance**, **Edge Feathering**, **Remove Faint Remnants** and **Smooth Edges** as appropriate. The **Preserve Original Colors** option prevents unintended recoloring of your subject.

Manual presets include **Black Background → White Logo**, **White Background → Black Logo**, **Preserve Color Logo**, **Remove Stubborn Remnants**, and **Soft Edges**. These apply manual-mode settings. Presets and engine selection do not delete an already available AI result.

### 4.2 AI automatic background removal

For photographs and complex scenes, select **AI Automatic Removal**, then press **Run AI Background Removal**. The app downloads the IMG.LY AI JavaScript, WASM runtime and model from external CDNs if they are not already available in browser cache. This may take longer on first use. The selected image is processed inside the browser; the application does not upload it to its own image server.

Use **AI Edge Feathering** for smoother semi-transparent borders. After AI completes, the resulting alpha mask is applied to the preview. If you want a flat background rather than transparency, enable **Fill with Solid Color** and choose a color.

**AI failure handling:** The editor provides different guidance for module loading, source-image conversion, model/WASM loading, result decoding, possible memory shortages and offline conditions. These are diagnostic hints, not guaranteed root-cause identification. Try a smaller photo, verify CDN access or use manual removal if needed.

**Not fully offline:** The manual/background editing features work without the AI assets, but the first AI removal requires external network access.

## 5. Transparent Image Editing

Choose **Edit Transparent Image**, then open an existing transparent PNG, WebP, GIF or AVIF that contains an alpha channel. The application checks the image's transparency. If there is no useful alpha channel, it displays a notice and offers to switch to Background Removal while preserving the current image.

The editor offers **Outline / Glow**, **Shadow**, **Visibility Adjustments** (opacity, brightness, contrast and saturation), **Transform** (rotation and horizontal/vertical flip), and **Tiled Preview**. Adjust the settings in the right panel, monitor the result, and save it as PNG or JPG.

Tiled Preview is *only a display preview*. Exporting a transparent PNG normally saves a single image; use the separate preview-background export when you specifically want a preview visualization.

## 6. Create Transparent Text

1. Open **Create Transparent Text**.
2. Enter the words to render. Keep to a maximum of **160 characters** for reliable generation.
3. Choose font size, text color, font family, Bold and Italic settings.
4. Optionally click **Import Custom Fonts** to load local TTF, OTF, WOFF or WOFF2 files. Multiple selection is supported. Fonts remain local and are not included in the ZIP or uploaded. Only the selected custom font is loaded as needed.
5. Press **Create Text PNG**. You can then add outlines, shadows, transformations, and further effects.
6. In the text editor, changes to text, font, size, color and style update the canvas preview live (subject to text-size and canvas safety limits).

The actual font family value used for rendering is not altered when switching between KO and EN, even though visible font labels may be localized. User-entered words are never translated automatically.

## 7. Advanced effects and export settings

**Outline / Glow:** Enable or disable, set stroke width and color, or choose white/black outlines or soft glow. Use it to make logos readable on both dark and light backgrounds.

**Shadow:** Adjust blur, strength, horizontal/vertical offsets and color. Shadows can extend the visible alpha boundary; add crop padding if needed.

**Opacity, Brightness, Contrast, Saturation:** These adjustments apply both to preview and to the exported image.

**Transform:** Rotate or flip the current image. These changes can be undone and redone.

**Auto-Crop Transparent Margins:** Removes unused transparent space around your result. **Crop Padding** retains a margin so strokes/shadows are not clipped. **Make Square** places the result on a square canvas sized to fit the longer side, except when the safety limits require keeping the original aspect ratio.

### Export buttons and names

- **Save Transparent PNG:** Export with alpha preserved where the current result is transparent.
- **Save Preview PNG:** Export what is displayed with the preview background, not a transparent PNG.
- **Save White-Background JPG:** Composite onto white and export as JPG. JPG has no alpha channel.
- **Save Solid-Background PNG:** Appears when flat background fill is enabled.

Filename examples: original `photo.jpg` normally becomes `photo_edit.png` before background removal or `photo_nobg.png` after removal; a transparency edit might become `photo_edited.png` and a flat background `photo_solid_bg.png`. Text PNGs use `text_image.png`. Preview and JPG exports append their relevant suffixes. Invalid filename characters are handled and long Unicode names are truncated without splitting emoji into invalid surrogate halves.

## 8. SVG images and input limits

- A viewBox-only SVG with no explicit pixel dimensions is rasterized using **2048px on the longer side**, preserving its aspect ratio.
- If only width or height is explicitly defined, that dimension is preserved and the other follows the viewBox aspect ratio. CSS absolute units are converted to pixels.
- Namespace-prefixed SVG roots and valid explicit dimensions are supported. The source SVG's XML is not rewritten as part of these adjustments.
- Very large dimensions and expensive pixel operations are checked against canvas safety limits. If blocked, use a lower-resolution input or reduce effects and export size.

TIFF input is deliberately unsupported due to inconsistent browser behavior. Convert TIFF to PNG or WebP first.

## 9. Troubleshooting

| Symptom | What to try |
|---|---|
| AI does not start / model load fails | Check connectivity to `cdn.jsdelivr.net` and `staticimgly.com`, update Chrome/Edge, retry with a smaller image or use manual removal |
| AI reports a possible memory problem | Close other tabs, reduce image resolution, avoid extra heavy effects |
| Wrong pixels disappear in manual mode | Switch to Edge-Connected or Smart, adjust tolerance, use Preserve Original Colors |
| Logo still has colored fringes | Adjust feathering, full removal range, faint-remnant cleanup, or select a better background color |
| Imported font does not show | Verify file format and integrity; try a known compatible TTF; reselect your font file |
| Transparent mode reports opaque image | Switch to Background Removal; simply editing an opaque image cannot invent transparency |
| Output is unexpectedly cropped or huge | Review Auto-Crop, Crop Padding, Make Square and input SVG dimensions |
| KO/EN preference was not remembered | Browser local-file storage or privacy mode may block localStorage; manually switch again |
| Export fails | Reduce image size, disable memory-intensive options, use a modern Chromium-based browser |

## 10. Privacy, licenses, and release testing

The program has no user-image upload endpoint and does not save imported font binaries to the repository or browser persistent storage. Browser-based AI still fetches scripts and model assets from third-party hosts; consult their privacy terms when relevant.

The source is distributed under [GNU AGPL-3.0](../LICENSE), with separate [third-party notices](../THIRD_PARTY_NOTICES.md) for IMG.LY, Microsoft ONNX Runtime Web and model dependencies. Fonts are **not bundled**; users remain responsible for individual font-license restrictions.

Before publishing a public release, test first-time AI model downloads and real inference on Windows Chrome and Edge, plus the same operation on GitHub Pages HTTPS. Automated tests in this package do not replace those real-network checks. See [pre-release checklist](TEST_BEFORE_GITHUB_RELEASE.md) and [test report](TEST_REPORT.md).
