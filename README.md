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
├── content/                         # All of your content will be stored here in this folder
│   ├── file_1.tex                   
│   ├── file_2.tex
│   ├── file_3.tex
│   ├── etc...
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

### 1. Define Your Metadata

To set document metadata edit the front_matter/metadata.tex file.

```latex

\gdef\gddtitle{GDD LaTeX Template}
\gdef\gddsubtitle{The best one there is!}
\gdef\gddfranchise{Franchise Name}
\gdef\gddauthor{Company/Author Name}
\gdef\gddversion{1.1.2}
\gdef\gdddate{\today}

\gdef\coverimage{example-image-a}
\gdef\coverlogo{example-image-b}

```

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

## Compilation Requirements

The template requires Biber as the bibliography compiler to sucessfully compile, although you can easily change it by digging the formatting.tex file.

**Note:** This template was only used and tested in TexStudio, with TexLive, but it should work in other editors and compilers.
