# Awesome Bible Translation Tools
## A curated list of libraries and tools supporting Bible Translation

## Scripture Projects

### Documentation

- **[Scripture Burrito](https://github.com/Bible-Translation-Tools/scripture-burrito)**: Our fork of the Scripture Burrito specification, with documentation for how to follow WA conventions. Scripture Burrito is a metadata standard for describing Bibles, Scripture Resources, etc., and can be used as a data interchange format to transfer translation projects between applications.
- **[Resource Container](https://resource-container.readthedocs.io/en/latest/)**: The original metadata format for Scripture and Parascriptural resources in the WACS/DCS ecosystem. This is a legacy format; new projects and software should prefer Scripture Burrito.

### Libraries

- **[Kotlin Scripture Burrito](https://github.com/Bible-Translation-Tools/Audio-Bible-Software/tree/main/libs/scripture-burrito)**: A Kotlin library for working with Scripture Burrito. Part of the Audio Bible Software monorepo.
- **[kotlin-vtt](https://github.com/Bible-Translation-Tools/Audio-Bible-Software/tree/main/libs/vtt)**: a library for parsing and writing VTT timestamps
- **[kotlin-scripture-alignment](https://github.com/Bible-Translation-Tools/Audio-Bible-Software/tree/main/libs/scripture-alignment)**: a library for working with the Scripture Burrito alignment standard
- **[Kotlin Resource Container](https://github.com/Bible-Translation-Tools/Audio-Bible-Software/tree/main/libs/resource-container)**: A Kotlin library for working with Resource Containers. Part of the Audio Bible Software monorepo.
- **[Tstudio2rc](https://github.com/Bible-Translation-Tools/Audio-Bible-Software/tree/main/libs/tstudio2rc)**: A Kotlin library for converting tstudio (BTT-Writer) projects to Resource Containers. Part of the Audio Bible Software monorepo.

## Text

### Documentation

- **[Scripture Kitchen (USFM toolkit monorepo)](https://wycliffeassociates.github.io/scripture-kitchen/)**

### Libraries

- **USFM Parsers**:
  - **USFM Onion** Part of Scripture Kitchen. Rust + Wasm bindings, Lossless CST. Docs for the monorepo are [here](https://wycliffeassociates.github.io/scripture-kitchen/).
  - **[USFMToolsSharp](https://github.com/WycliffeAssociates/USFMToolsSharp)** - A USFM and rendering toolkit for C#
  - **[USFMToolsJava](https://github.com/WycliffeAssociates/USFMToolsJava)** - A java port of the parser from UsfmToolsSharp
- **USFM Linters**
  - **Sous Chef** (in the Scripture Kitchen monorepo): Rust + Wasm. [Docs](https://wycliffeassociates.github.io/scripture-kitchen/). Statistical in nature.
- **Misc**
  - **[Scripture Kitchen: Galley](https://github.com/WycliffeAssociates/scripture-kitchen/tree/master/galley)**: A crate (Rust + Wasm) that provides caching and handles USFM parse and proofread in one export.

### Infra

- **[Public Data API / Language API](https://github.com/WycliffeAssociates/languageapi)**: Azure function, dockerized, with a Postgres DB for dev and prod. The Postgres DB also lives in Azure. Explorers for the Hasura GraphQL API:
  - [Dev](https://api-explorer-dev.walink.org/)
  - [Prod](https://api-explorer.bibleineverylanguage.org/)
- **[WACS](https://github.com/WycliffeAssociates/WACS)**
  - As of October 28, 2026: Forgejo in dev, Gitea in prod.
  - A [proxy](https://github.com/WycliffeAssociates/wacs-browser-git-proxy) for browser-based (isomorphic git) clients. It is needed because of Cloudflare bot protection and some CORS rules.
  - **[Topic manager](https://github.com/WycliffeAssociates/wacs-topic-manager)**: A cron job on Jenkins that looks for book-per-file repos. Recommended for deprecation in favor of better APIs in Translation Hub.

### Apps

#### Sefer

- Sefer is the full app for revising and editing Bibles with full USFM support. It is built with Tauri, so it supports iOS, Android, and desktop, plus web (via a separate build).
- **[Sefer's USFM editor](https://github.com/Bible-Translation-Tools/Sefer/tree/master/packages)**: The JS editor for Sefer, as its own TS package. Its only dependencies are CodeMirror and Scripture Kitchen (for the parser). A [playground](https://github.com/Bible-Translation-Tools/Sefer/tree/master/packages/editor/bench) in this repo shows how it handles the WYSIWYG aspects of editing.

#### BTT Writer

#### Read on Web / Live Reader

- Old. Reads pregenerated USFM HTML from SRP. Recommended to replace with on-demand rendering from Scripture Kitchen.

#### BIEL

- Headless WordPress with Astro. Static site, except the `/languages/resources` page. Fed by the Public Data API.
- Also reads [Translation Services support files](https://github.com/WycliffeAssociates/TS-biel-files).

## Audio

### Documentation

### Libraries


### Apps

- **[Audio Bible Software](https://github.com/Bible-Translation-Tools/Audio-Bible-Software)**: A monorepo for our oral translation software, including the latest version of Orature and BTT-Recorder, written in Kotlin Multiplatform/Compose Multiplatform. (Android + Desktop). 
- **[Orature](https://github.com/Bible-Translation-Tools/Orature)**: [Deprecated] The original repository for the JVM/JavaFX version of Orature.
- **[BTT-Recorder](https://github.com/Bible-Translation-Tools/BTT-Recorder)**: [Deprecated] The repository for BTT-Recorder, a BTT rebranding of translationRecorder.
- **[translationRecorder](https://github.com/WycliffeAssociates/translationRecorder)**: [Deprecated] The original repository for translationRecorder.

