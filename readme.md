Ubuntu Beamer Template
======================

A simple template to be used for Ubuntu related slides.

![Ubuntu Beamer Template Screenshot](http://i.imgur.com/CoTi5.png)

### How to use

Make sure you clone this in your `texmf` folder.

Example:

```bash
$ git clone git@github.com:stas/beamer-ubuntu.git ~/texmf/tex/latex/beamer/themes/theme/Ubuntu
```

Now you should be able to use the theme:

```tex
\usetheme{Ubuntu}
```

### Requirements

On Ubuntu/Debian, installing the packages below, should be enough:

* latex-beamer
* texlive-xetex

### Compiling files

Please use `xelatex` to compile the `.tex` files so we can use Ubuntu system
font and other utf8 awesomeness.

Example `Makefile`

```make
PDFLATEX:=xelatex -shell-escape
TARGET:=slides

default: main

main:
  @$(PDFLATEX) $(TARGET)

.PHONY: clean

clean:
  @rm -f $(TARGET)*.aux \
    $(TARGET)*.log \
    $(TARGET)*.nav \
    $(TARGET)*.out \
    $(TARGET)*.snm \
    $(TARGET)*.toc \
    $(TARGET)*.vrb \
    $(TARGET)*.pdf \
    $(TARGET)*.dvi \
    $(TARGET)*.ps  \
    $(TARGET)*.bbl \
    $(TARGET)*.blg \
    $(TARGET)*.thm \
    $(TARGET)*.brf \
    $(TARGET)*.pyg \
    missfont.log  \
    x.log
    @rm -f *~
```

### Cedits

* [Ian Yang](https://github.com/doitian) for his work on Intridea template.
