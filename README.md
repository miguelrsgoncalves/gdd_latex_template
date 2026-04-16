![GDD LaTeX Template Logo](images/gdd_latex_template_logo.png "GDD LaTeX Template Logo")

GDD LaTeX Template is the open source template for your Game Design Document! This template was built so that it stays out of your way while providing you with all the tools, formatting and project structure needed out of the box.

## Project Structure

This project is organized into modular components, where all files are stored inside each respective folder. Knowing where each file you need to edit is crucial.

```
.
├── main.tex                         # The main tex file
├── preamble/
│   └── preamble.tex                 # The formatting and commands
├── front_matter/
│   ├── metadata.tex                 # The document data: Title, company/author, subtitle, etc...
│   ├── cover.tex                    # The cover of the document
│   ├── abstract.tex                 # The abstract
│   └── _table_of_contents_list.tex  # List of Lists to show as Table of Contents
├── content/                         # All of your content will be stored here in this folder
│   ├── file_1.tex                   
│   ├── file_2.tex
│   ├── file_3.tex
│   ├── etc...
│   ├── _definitions.tex             # Create definitions to be used globaly
│   └── _list.tex                    # When a new file is created it needs to be added in this list
├── images/                          # Where to store images
├── bibliography/
│   └── bibliography.bib             # Bibliography
├── templates/
│   ├── template1.tex                # Templates are stored in this folder
│   ├── template2.tex
│   └── etc...
└── placeholders/
    ├── placeholder1.tex             # Placeholders are stored here. They are used for the default tempalte build
    ├── placeholder2.tex
    └── etc...

```

## Using this template

### 1. Main File

The main file is the main.tex, this is the document that gets compiled and exported as a PDF. The PDF gets its name from this file, so if you want the PDF to be exported with a different name change the main.tex's name.

### 2. Define your Metadata

To set document metadata edit the front_matter/metadata.tex file.

```latex

\gdef\gddtitle{GDD LaTeX Template}
\gdef\gddsubtitle{The best one there is!}
\gdef\gddfranchise{Franchise Name}
\gdef\gddauthor{Company/Author Name}
\gdef\gddversion{1.2.0}
\gdef\gdddate{\today}

\gdef\gddcoverimage{gdd_latex_template_logo}
\gdef\gddlogo{gdd_latex_template_logo}

```

Metadata entries can be used in the content using their respective commands, for example:

```latex

This document serves as the comprehensive Game Design Document (GDD) for \textbf{\gddtitle}.

```

This makes it usefull

**Note:** Leaving the date as \today will set the date to the compiliation date automatically.

**Note:** Leaving optional entries empty will not render them.

## Adding Content

To add new content, go to content/ and create a new .tex file, then, in _list.tex, use the command:

**To add chapters:**
```latex
\addchapter{file_name}{Chapter Title}
```

**To add content:**

The second argument can receive "b" and/or "a" to insert \newpage before and/or after respectively.

```latex
\addcontent{file_name}{}
\addcontent{file_name}{b}
\addcontent{file_name}{a}
\addcontent{file_name}{ba}
```

## Custom Commands

The template makes use of a number of custom commands to make writting easier.

```latex
% Add bold and italic text with one command
\textbfit{text}
```

## Compilation Requirements

The template requires Biber as the bibliography compiler to sucessfully compile, although you can easily change it by digging the formatting.tex file.

**Note:** This template was only used and tested in TexStudio, with TexLive, but it should work in other editors and compilers.
