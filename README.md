Insight Journal MyST Template
===============================

[![Build MyST Document](https://github.com/InsightSoftwareConsortium/InsightJournalTemplate/actions/workflows/build-myst.yml/badge.svg)](https://github.com/InsightSoftwareConsortium/InsightJournalTemplate/actions/workflows/build-myst.yml)

This repository contains a modern template for submitting Technical Reports to the
Insight Journal using MyST Markdown:

    https://insight-journal.org

## Overview

This template has been transformed from LaTeX to **MyST Markdown**, providing:

- 🚀 **Modern authoring** with MyST Markdown
- 📦 **Dependency management** with Pixi
- 🔄 **Reproducible builds** and environments
- 📄 **Multiple export formats** (PDF, HTML, DOCX, MECA)
- 🧪 **Integrated source code** testing and validation
- 📚 **Rich scientific features** (equations, citations, cross-references)

## Quick Start

See the complete documentation in [`doc/README.md`](doc/README.md).

### With Pixi (Recommended)

1. Install [Pixi](https://pixi.sh/latest/)
2. Clone and build:
   ```bash
   git clone https://github.com/InsightSoftwareConsortium/InsightJournalTemplate.git
   cd InsightJournalTemplate
   pixi install
   pixi run build-complete
   ```

### Legacy LaTeX Template

The original LaTeX template is still available in the `Document/` directory.

**Overleaf Link**: https://www.overleaf.com/latex/templates/insight-journal/grjrhxkzzsvf


License
-------

All source code in this repository is distributed under the Apache 2.0
License. Please see the LICENSE file for details.

All documents and works of art in this repository are distributed under the
Creative Commons by Attribution License 3.0.
