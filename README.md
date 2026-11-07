# Text Mining with R and Quarto

A COMP 343 coursework exercise that downloads Albert Einstein's *Relativity: The Special and General Theory* from Project Gutenberg and converts it into a tidy, word-level dataset.

## Project files

- [Quarto source](p16.qmd): imports the text, keeps line numbers, and tokenizes words with `tidytext`.
- [Rendered HTML](p16.html): a self-contained copy of the rendered exercise. Download the file and open it in a browser to view it as a webpage.
- [RStudio project](p16-fa26-cirker.Rproj): opens the project in RStudio.

## Reproduce the exercise

Install R and Quarto. RStudio is optional. In R, install the packages used by the source:

```r
install.packages(c("tidyverse", "tidytext", "gutenbergr"))
```

From the repository folder, render the HTML output:

```bash
quarto render p16.qmd --to html
```

Rendering requires an internet connection to download the text from the Project Gutenberg mirror. The source also defines a Typst output format; the command above selects HTML only.

## Data and scope

The source text is [Project Gutenberg ebook 30155](https://www.gutenberg.org/ebooks/30155). The exercise removes the Gutenberg header and footer, splits the text into words, and counts the resulting rows. It is an introductory tokenization exercise rather than a complete text-analysis study.

The repository name is retained to preserve its course identity and existing links. This project does not currently have a GitHub Pages site.
