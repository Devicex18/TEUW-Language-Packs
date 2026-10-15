# TEUW Language Packs

Public repository for downloadable TEUW language packages.

## Initial packages

- **Español (México)** — `packs/es-MX/pack.json`
- **English (United States)** — `packs/en-US/pack.json`

The JSON packs contain original TEUW command phrases, wake-phrase templates, assistant responses and UI labels. They are designed to be downloaded independently of the APK and checked against the SHA-256 digest in `catalog.json`.

## Offline recognition models

TEUW will distribute the compact offline recognition archives through GitHub Release assets rather than putting them in the APK or committing large binaries to the source tree. The first model publication is automated by the workflow [Publish language model assets](.github/workflows/publish-language-models.yml).

The compact acoustic models are third-party Vosk models licensed under Apache 2.0 as listed in the [Vosk model catalog](https://alphacephei.com/vosk/models). They are not trained by TEUW. See [MODEL-SOURCES.md](MODEL-SOURCES.md) for source and attribution.

## Integrity

The catalog contains a SHA-256 digest and byte length for each JSON language pack. The model-release workflow computes a separate SHA-256 digest for each model archive, updates the package, then updates the catalog. The Android app must verify both files before installing.

## Schema

- `schemaVersion`: JSON package schema version.
- `packId`: canonical BCP 47 language tag.
- `commands`: command phrases grouped by canonical action ID.
- `responses`: localized assistant response strings.
- `recognitionModel`: upstream model identity, release asset URL, digest, and attribution.
- `ui`: labels for the language-pack experience.

Original TEUW package data is maintained separately from third-party model artifacts.
