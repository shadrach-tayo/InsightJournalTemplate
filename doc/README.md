# Insight Journal MyST Template

[![Build Document](https://github.com/InsightSoftwareConsortium/InsightJournalTemplate/actions/workflows/build-myst.yml/badge.svg)](https://github.com/InsightSoftwareConsortium/InsightJournalTemplate/actions/workflows/build-myst.yml)

This repository contains a modern template for submitting Technical Reports to the
Insight Journal using MyST Markdown:

    https://insight-journal.org

## Overview

This template demonstrates how to create reproducible, open science articles using:

- **MyST Markdown** for rich scientific document authoring
- **Pixi** for dependency management and build automation  
- **Source code** organization in `src/`
- **Data** organization in `data/`
- **Multi-format exports** (PDF, HTML, DOCX, MECA, etc.)

## Repository Structure

```
├── doc/                    # MyST Markdown documents
│   ├── index.md           # Main article
│   └── references.bib     # Bibliography
├── src/                   # Source code (C++/ITK examples)
│   ├── CMakeLists.txt     # CMake build configuration
│   ├── ImageCopy.cxx      # Example ITK filter
│   └── ImageCompare.cxx   # Example comparison tool
├── data/                  # Data files and images
│   └── img1.png          # Sample test image
├── myst.yml              # MyST configuration
├── pixi.toml             # Pixi dependency management
└── requirements.txt      # Python requirements
```

## Quick Start

### Prerequisites

1. Install [Pixi](https://pixi.sh/latest/):
   ```bash
   curl -fsSL https://pixi.sh/install.sh | bash
   ```

2. Clone this repository:
   ```bash
   git clone https://github.com/InsightSoftwareConsortium/InsightJournalTemplate.git
   cd InsightJournalTemplate
   ```

### Building the Document

1. Install dependencies:
   ```bash
   pixi install
   ```

2. Build HTML version:
   ```bash
   pixi run build-html
   ```

3. Build PDF version:
   ```bash
   pixi run build-pdf
   ```

4. Build all formats:
   ```bash
   pixi run build-complete
   ```

5. Start development server:
   ```bash
   pixi run serve
   ```

### Building Source Code

1. Build the C++ examples:
   ```bash
   pixi run build-src
   ```

2. Run tests:
   ```bash
   pixi run test-src
   ```

## MyST Markdown Features

This template demonstrates:

- ✅ **Rich frontmatter** with authors, affiliations, ORCID
- ✅ **Mathematical equations** with LaTeX syntax
- ✅ **Code syntax highlighting** for multiple languages
- ✅ **Cross-references** to figures and equations
- ✅ **Bibliography management** with BibTeX
- ✅ **Multiple export formats** (PDF, HTML, DOCX, MECA)
- ✅ **Jupyter notebook integration** (optional)
- ✅ **Reproducible builds** with Pixi

## Export Formats

The template is configured to export to:

- **HTML**: Interactive web version
- **PDF**: 
  - arXiv two-column format
  - Plain LaTeX book format
- **DOCX**: Microsoft Word format
- **MECA**: Manuscript Exchange Common Approach bundle
- **TeX**: LaTeX source files

## Customizing the Template

### Document Content

1. Edit `doc/index.md` with your article content
2. Update frontmatter (title, authors, abstract, etc.)
3. Add your bibliography entries to `doc/references.bib`
4. Add figures and data to `data/`

### Source Code

1. Replace the example C++ files in `src/` with your code
2. Update `src/CMakeLists.txt` for your build requirements
3. Add data files to `data/`

### Configuration

1. Update `myst.yml` with your project settings
2. Modify `pixi.toml` for additional dependencies
3. Update export settings in `myst.yml` as needed

## Development Workflow

1. **Write**: Author content in MyST Markdown (`doc/index.md`)
2. **Preview**: Use `pixi run serve` for live preview
3. **Build**: Generate outputs with `pixi run build-complete`
4. **Test**: Validate source code with `pixi run test-src`
5. **Deploy**: Publish to Insight Journal or other venues

## Advanced Features

### Jupyter Integration

Add Jupyter notebooks to your project:

```yaml
# In myst.yml
project:
  jupyter: true
  execute:
    execute_notebooks: auto
```

### Custom Templates

Specify custom LaTeX templates:

```yaml
# In myst.yml
project:
  exports:
    - format: pdf
      template: path/to/custom/template.tex
```

### Multi-language Support

Include code examples in multiple languages:

````markdown
```cpp
// C++ example
typedef itk::Image<unsigned char, 3> ImageType;
```

```python
# Python example
import itk
image = itk.imread('data/image.png')
```
````

## Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test with `pixi run build-complete`
5. Submit a pull request

## License

- **Source code**: Apache 2.0 License
- **Documentation**: Creative Commons Attribution License 3.0

## Resources

- [MyST Markdown Guide](https://mystmd.org/guide)
- [Insight Journal](https://insight-journal.org)
- [ITK Software Guide](https://itk.org/ItkSoftwareGuide.pdf)
- [Pixi Documentation](https://pixi.sh/latest/)

---

**Latest version available at the [Insight Journal](https://insight-journal.org)**

**Distributed under [Creative Commons Attribution License](http://creativecommons.org/licenses/by/3.0/us/)**
