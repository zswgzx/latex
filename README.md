# LATEX UX

Have been using **LATEX** instead of *MS Word* for documentation. Just some useful tips for beginner or experience users.

---
## Installation on Ubuntu
`apt install texlive -y`

## **Online** latex editor

[Overleaf](https://www.overleaf.com) was where it all began and it is highly recommended for beginners.
Easy to find templates, compile tex files and generate pdf, and has other learning resources. 

## Compile .tex (and .cls if any in same folder) to pdf
`pdflatex [file].tex [> /dev/null]`

## Install tex package

For example, if error like 'letltxmacro.sty not found' occurs, try below:

1. Find the required package repo. [here](https://ctan.org/pkg/letltxmacro)
1. Install it in current path from terminal by
  `wget --no-check-certificate https://mirrors.ctan.org/macros/latex/contrib/letltxmacro.zip`

- cd to unziped folder and run
  `tex letltxmacro.dtx`

- then move the generated files to appropriate path, and refresh
  `tex_path='your_path'`
  `mv letltxmacro.sty ${tex_path}/tex/latex/letltxmacro`
  `mv letltxmacro{-showcases.tex,.pdf} ${tex_path}/doc/latex/letltxmacro`
  `mv letltxmacro.dtx ${tex_path}/source/latex/letltxmacro`

- other generated files can be deleted. then run below and all set
  `texhash` or `mktexlsr`

## Useful tips

- escape **&** if it needs to be printed literaly

- use package *hyperref* to link to url or style it nicely, e.g.
`\usepackage{hyperref}`
`\href{mailto:abc@xyz.com}{abc@xyz.com}`
`\href{http://abc.com}{abc.com}`
`\url{http://abc.com}`

- use package *xcolor* together with *hyperref* to add color to the url or link in it, e.g.
`\url{\textcolor{blue}{http://abc.com}}`