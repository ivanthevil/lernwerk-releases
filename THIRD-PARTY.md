# Open-Source-Komponenten

Lernwerk ergänzt den lokalen Transkriptionskern um einen Lernserver und eine React-Oberfläche. Weitere Paketversionen und mitgelieferte Lizenztexte liegen unter `assets/licenses/lernwerk` bzw. im Windows-Paket unter `_internal/assets/licenses/lernwerk`. Darunter befinden sich insbesondere die Lizenzhinweise von pypdfium2/PDFium (Apache-2.0/BSD), FastAPI, React, ReportLab, Microsoft MSAL und KaTeX. Die Aussage zu nicht hochgeladenen Audiodateien im folgenden Abschnitt bezieht sich auf TRANSKRIPT; Lernwerk sendet ausgewählten Text und Bilder bei angeforderten KI-Aktionen und Mikrofonton während Sprachgesprächen an OpenAI.

TRANSKRIPT nutzt folgende Komponenten. Die Modelle werden separat heruntergeladen; Audiodateien werden nicht hochgeladen.

| Komponente | Version | Lizenz / Quelle |
| --- | --- | --- |
| whisper.cpp | 1.8.4 | MIT — https://github.com/ggml-org/whisper.cpp/tree/v1.8.4 |
| Windows Vulkan-Build | v1.8.4.1 | Build von jiang1997 — https://github.com/jiang1997/whisper.cpp-release/tree/v1.8.4.1 |
| Whisper-Modelle | quantisiert, siehe core.py | MIT — https://huggingface.co/ggerganov/whisper.cpp und https://github.com/openai/whisper |
| Silero VAD | 6.2.0 | MIT — https://github.com/snakers4/silero-vad und https://huggingface.co/ggml-org/whisper-vad |
| PySide6 / Qt | 6.11.2 | LGPLv3 / GPLv3 / kommerziell; hier LGPL-Komponenten — https://doc.qt.io/qtforpython-6/licenses.html |
| Shiboken6 | 6.11.2 | LGPL — https://code.qt.io/cgit/pyside/pyside-setup.git/ |
| PyAV | 18.1.0 | BSD-3-Clause — https://github.com/PyAV-Org/PyAV |
| FFmpeg (BtbN LGPL shared) | n8.1.2-53-g1005b294ff | LGPLv3+, ohne GPL-Encoder — https://ffmpeg.org/legal.html |
| NumPy | 2.5.3 | BSD-3-Clause — https://github.com/numpy/numpy |
| RapidOCR ONNX Runtime | 1.4.4 | Apache-2.0 — https://github.com/RapidAI/RapidOCR |
| PaddleOCR-Modelle (über RapidAI) | Detektion/Klassifikation PP-OCRv4, lateinische Erkennung PP-OCRv3 | Apache-2.0 — https://github.com/PaddlePaddle/PaddleOCR |
| ONNX Runtime | 1.30.0 | MIT — https://github.com/microsoft/onnxruntime |
| OpenCV-Python | 5.0.0.93 | Apache-2.0; zusätzliche Binärbibliotheken siehe Paketlizenz — https://github.com/opencv/opencv-python |
| Pillow | 12.3.0 | MIT-CMU — https://github.com/python-pillow/Pillow |
| Shapely | 2.1.2 | BSD-3-Clause; GEOS LGPL — https://github.com/shapely/shapely |
| Pyclipper | 1.4.0 | MIT — https://github.com/fonttools/pyclipper |
| Python | 3.12 | PSF — https://www.python.org/downloads/source/ |
| PyInstaller (Packaging) | 6.22.2 | GPL mit Bootloader-Ausnahme — https://pyinstaller.org/en/stable/license.html |

Die originale whisper.cpp-Lizenz liegt im Paket unter `_internal/licenses/WHISPER-LICENSE.txt`. Paketmetadaten einschließlich mitgelieferter Lizenztexte von PySide6, Shiboken6, PyAV und NumPy werden in `_internal` mitgeliefert. Qt/PySide-Bibliotheken liegen als austauschbare DLLs bzw. Module im Paket vor; der Python-Anwendungscode befindet sich im Projektordner. Das Paket ist nicht digital signiert.

Engine-Archiv: `whisper-1.8.4-windows-x64.zip`

SHA-256: `4b1b36343feb55ec3deace6a7dd18cc217f43a55e4ecce76ccd4ee3595c0b642`

Die Downloadquelle und Modelldateien sind im Quellcode festgelegt; Downloads werden vor Verwendung anhand der gespeicherten SHA-256-Prüfsummen validiert. Es werden keine zufälligen neuesten Releases automatisch ausgeführt.

Das OCR-Modell für lateinische Schrift wird mitgeliefert unter `assets/ocr/latin_rec.onnx`.

Quelle: https://www.modelscope.cn/models/RapidAI/RapidOCR/resolve/v3.9.2/onnx/PP-OCRv4/rec/latin_PP-OCRv3_rec_mobile.onnx

SHA-256: `e9d7a33667e8aaa702862975186adf2012e3f390cc0f9422865957125f8071cf`

RapidOCR bringt weitere Detektions-/Klassifikationsmodelle im Python-Paket mit. Lizenztexte der zusätzlich gebündelten Python-Pakete werden über ihre Metadaten mitgeliefert. Ollama und Qwen sind optionale, separat einzurichtende Komponenten und nicht Bestandteil dieses Pakets.

## Bibliotheksquellen und Austausch

Die archivierten Quellen von Qt 6.11.2 (einschließlich Chromium), PySide/Shiboken 6.11.2, GEOS 3.13.1, FFmpeg und seinen Komponenten stehen zusätzlich zum Installer auf https://github.com/ivanthevil/lernwerk-releases/releases/tag/third-party-0.2.0 zum kostenlosen Download. Die Archive enthalten die jeweiligen Lizenztexte, Copyright-Hinweise und Builddateien. Versions- und Prüfsummenlisten liegen bei. Diese Quellen gehören zu den mitgelieferten Bibliotheken, nicht zum Lernwerk-Anwendungscode.

Qt/PySide, Shiboken, FFmpeg und GEOS bleiben dynamisch geladen und austauschbar. Lernwerk schließen und ABI-kompatible eigene Builds im Programmordner unter `_internal/PySide6`, `_internal/shiboken6`, `_internal/av.libs` bzw. `_internal/shapely.libs` ersetzen. Kopien vorher sichern. Änderungen an diesen Bibliotheken und das dafür notwendige Debugging/Reverse Engineering sind nicht beschränkt. Es wird kein Signaturschutz oder anderer Sperrmechanismus für diese Bibliotheken eingesetzt.

Für PyAV wurden ausschließlich die DLL-Importnamen in den Windows-Erweiterungen angepasst: die von delvewheel angehängten Hashnamen wurden durch die unveränderten FFmpeg-ABI-Namen ersetzt. Das mitgelieferte Skript `prepare_lgpl_av.py` im Bibliotheksquellenpaket dokumentiert die reproduzierbare Anpassung. FFmpeg selbst ist der unveränderte LGPL-Shared-Build von BtbN (2026-09-15), ohne libx264/libx265. Die Konfiguration und Buildskripte liegen bei den Quellen. Qt/PySide können aus den offiziellen Quellen mit den beiliegenden Build-Anleitungen erstellt werden; `qtattributionsscanner` erzeugt die weitergehenden Drittanbieterhinweise.

## Windows-Audioaufnahme

PyAudioWPatch 0.2.12.8 (Apache-2.0, mit ursprünglichen PyAudio-Anteilen unter MIT) und PortAudio (MIT), Quelle: https://github.com/s0d3s/PyAudioWPatch/ . Lizenztexte liegen unter assets/licenses/lernwerk/PyAudioWPatch. Die Aufnahme verwendet WASAPI-Loopback des gewählten Wiedergabegeräts.
