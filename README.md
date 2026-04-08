# GDD LaTeX Template

GDD LaTeX Template is the open source template for your Game Design Document! This template was built so that it stays out of your way while providing you with all the tools, formatting and project structure needed out of the box.

## Project Structure

This project is organized into modular components, where all files are stored inside each respective folder. Knowing where each file you need to edit is crucial.

```text
.
├── main.tex                         # The main tex file
├── formatting/
│   └── formatting.tex               # The formatting
├── front_matter/
│   ├── metadata.tex                 # The document data: Title, company/author, subtitle, etc...
│   ├── cover.tex                    # The cover of the document
│   ├── abstract.tex                 # The abstract
│   └── _table_of_contents_list.tex  # List of Lists to show as Table of Contents
├── chapters/                        
│   ├── chapter1.tex                 # All your chaptors will be stored here in this folder
│   ├── chapter2.tex
│   ├── chapter3.tex
│   ├── etc...
│   └── _list.tex                    # When a new chapter is created it needs to be added in this list
├── images/                          # Where to store images
└── bibliography/
    └── bibliography.bib             # Bibliography
```

## Using this template

### 1. Define Your Metadata
Open `main.tex`, this is where you set the global variables that populate the cover and footers:

```latex
\newcommand{\gddtitle}{Project Name}
\newcommand{\gddsubtitle}{Tactical Espionage Action}
\newcommand{\gddauthor}{Studio Name}
\newcommand{\gddfranchise}{}
\newcommand{\gddversion}{1.0.4}
\newcommand{\gdddate}{\today}
```

**Note:** Leaving the date as \today will set the date to the compiliation date automatically.

**Note:** Leaving optional entries empty will make them dissapear.

## Adding Content

To add a new chapter, go to chapters/ and create a new .tex file, then, in _list.tex, use the custom command:

```latex
\addchapter{Gameplay Mechanics}{gameplay_mechanics}
```

This automatically handles correct generation of the chapter and addition to the document.

## Compilation Requirements

The template requires Biber as the bibliography compiler to sucessfully compile, although you can easily change it by digging the formatting.tex file.
