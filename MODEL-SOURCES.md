# Model sources and attribution

TEUW's language-pack repository contains original TEUW package metadata, command phrase templates, assistant responses, and UI labels. The acoustic recognition models listed below are third-party Vosk models, not models trained by TEUW.

## Spanish

- Model: `vosk-model-small-es-0.42`
- Source archive: https://alphacephei.com/vosk/models/vosk-model-small-es-0.42.zip
- Catalog size: approximately 39 MB
- License reported by Vosk's model catalog: Apache License 2.0
- Intended use: offline speech recognition on mobile devices.

## English (United States)

- Model: `vosk-model-small-en-us-0.15`
- Source archive: https://alphacephei.com/vosk/models/vosk-model-small-en-us-0.15.zip
- Catalog size: approximately 40 MB
- License reported by Vosk's model catalog: Apache License 2.0
- Intended use: offline speech recognition on mobile devices.

## Distribution and checksums

The workflow `.github/workflows/publish-language-models.yml` downloads these archives from the official Vosk model host, checks the ZIP archive, computes SHA-256 values, publishes the files as assets in a GitHub Release owned by Devicex18, and updates the pack/catalog metadata. TEUW must verify the SHA-256 value before installing an archive.

Vosk model catalog: https://alphacephei.com/vosk/models

The model archives retain their upstream license and attribution. TEUW's own JSON package data is maintained separately from the third-party acoustic-model files.
