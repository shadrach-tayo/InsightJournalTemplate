Insight Journal Publication Template
====================================

[![Build MyST Document](https://github.com/InsightSoftwareConsortium/InsightJournalTemplate/actions/workflows/build-myst.yml/badge.svg)](https://github.com/InsightSoftwareConsortium/InsightJournalTemplate/actions/workflows/build-myst.yml)

This repository contains a modern template for open science publications for the
[Insight Journal]:

    https://insight-journal.org

## Features

- 🚀 **Modern authoring** with [MyST Markdown]
- 📦 **Dependency management** with [Pixi]
- 🔄 **Reproducible builds** and environments
- 📄 **Multiple export formats** (PDF, HTML, DOCX, [MECA])
- 🧪 **Integrated source code** testing and validation support
- 📚 **Rich scientific features** (equations, citations, cross-references)

## Quick Start

See the complete documentation in [`docs/README.md`](docs/README.md).

### With Pixi (Recommended)

1. Install [Pixi]
2. Clone and build:

```bash
git clone https://github.com/InsightSoftwareConsortium/InsightJournalTemplate.git
cd InsightJournalTemplate
pixi install
pixi run build-complete
```

License
-------

All source code in this repository is distributed under the Apache 2.0
License. Please see the [LICENSE](./LICENSE) file for details.

All documents and works of art in this repository are distributed under the
[Creative Commons by Attribution License 4.0].

[Insight Journal]: https://insight-journal.org
[MyST Markdown]: https://mystmd.org
[Pixi]: https://pixi.sh/latest/
[MECA]: https://www.niso.org/standards-committees/meca
[Creative Commons by Attribution License 4.0]: https://creativecommons.org/licenses/by/4.0/