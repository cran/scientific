# Two rmarkdown templates for scientific and technical reports
_merely a rebuild of the sciRmdTheme R package_

```r
install.packages("scientific") # install
library(scientific) # load library
```

## Use template 1

```
---
title: "Sample title"
codelang: "R" 
author: "Obinna Obianom"
date: "`r Sys.Date()`"
output:
  scientific::html: 
    template: template1
    toc: TRUE 
---

```
![](https://scientific.obi.obianom.com/screenshot/template1.jpg)


## Use template 2

```
---
title: "Sample title"
codelang: "R" 
author: "Obinna Obianom"
date: "`r Sys.Date()`"
output:
  scientific::html: 
    template: template2
    toc: TRUE 
---

```
![](https://scientific.obi.obianom.com/screenshot/template2.jpg)

### Project website: https://scientific.obi.obianom.com

### Sample HTML output: https://rstudio-pubs-static.s3.amazonaws.com/1268472_5dfbe81f2ec448518c5fd7f5082a83a7.html

## Example .Rmd
```
---
title: "Scientific Report Example"
highlighter: "dracula" # code theme
codelang: "r" #default is R, you may add js php python and so on
themecolor: brown #specify a theme color
author: "Obinna Obianom"
date: "`r Sys.Date()`"
output:
  scientific::html: 
    toc: TRUE
    self_contained: TRUE
    template: template1 # or template2
summaryslide: TRUE # whether to show summary slide on top
lightsummaryslide: FALSE # whether to make summary slide light
summarypoints:
    - Fusce id velit ut tortor pretium viverra. Lectus urna duis convallis convallis tellus id interdum. 
    - Erat imperdiet sed euismod nisi porta lorem. Sed viverra tellus in hac habitasse platea dictumst. 
    - Turpis egestas integer eget aliquet nibh praesent tristique. Ultricies integer quis auctor elit. 
    - Dictum varius duis at consectetur lorem donec massa. Convallis aenean et tortor at risus viverra. 
    - Egestas tellus rutrum tellus pellentesque eu tincidunt tortor aliquam nulla. Aliquet bibendum enim facilisis gravida neque. 
    - Porta lorem mollis aliquam ut porttitor leo a diam. Sit amet mattis vulputate enim nulla aliquet porttitor lacus. 
    - Vestibulum rhoncus est pellentesque elit ullamcorper dignissim. Risus feugiat in ante metus dictum. 
---


# Introduction

Sample text implemented in LaTeX and HTML/CSS

```{r, message=FALSE}
library(ggplot2)
mtcars2 <- mtcars
mtcars2$am <- factor(
  mtcars$am, labels = c('automatic', 'manual')
)
ggplot(mtcars2, aes(hp, mpg, color = am)) +
  geom_point() + geom_smooth() +
  theme(legend.position = 'bottom')
```

# Output

![](https://scientific.obi.obianom.com/screenshot/scientificscreenshot2.png)



## Highlighter options for `highlighter` argument

```{r}
Enlighter (enlighter, standard) - Enlighter`s default Theme
Classic (classic) - SyntaxHighlighter inspired
Bootstrap (bootstrap4) - Bootstrap 4 inpired themes, high contrast
Beyond (beyond) - BeyondTechnology Theme
Godzilla (godzilla) - A MDN inspired Theme
Eclipse (eclipse) - Eclipse inspired
MooTwo (mootwo) - Inspired by the MooTools Website
Droide (droide) - Modern, minimalistic
Minimal (minimal) - Bright, High contrast
Atomic (atomic) - Dark, Colorful
Dracula (dracula) - Dark, using official draculatheme colorscheme
Rowhammer (rowhammer) - Light, Transparent, divided rows
```

## Languages for `codelang` argument
```
ABAP (abap)
Apache HTTPD (apache)
Assembly (assembly, asm)
AVR Assembly (avrassembly, avrasm)
Windows Batch/Bat (bat,batch,cmd)
C/C++ (c,cpp, c++)
C# (csharp)
CSS (css)
Cython (cython)
CordPro (cordpro)
diff (diff)
Dockerfile (docker, dockerfile)
Generic (generic, standard) - default highlighting scheme
Groovy (groovy)
Go (go, golang)
HTML (html)
Ini (ini, conf)
Java (java)
Javascript (js, javascript, jquery, mootools, ext.js)
JSON (json)
JSX (jsx)
Kotlin (kotlin)
LATEX (latex)
LESS (less)
lighttpd (lighttpd)
LUA (lua)
MariaDB (mariadb)
Markdown (gfm, md, markdown)
Matlab/Octave (octave, matlab)
MSSQL (mssql)
NGINX (nginx)
NSIS (nsis)
Oracle Database (oracledb)
PHP (php)
Powerhsell (powershell)
Prolog (prolog)
Python (py, python)
PureBasic (purebasic, pb)
QML (qml)
R (r)
RAW (raw) - raw code without highlighting with EnlighterJS container styles!
RouterOS/SwitchOS (routeros)
Ruby (ruby)
Rust (rust)
Scala (scala)
SCSS (scss, sass)
Shellscript (shell, bash)
Generic SQL (sql)
Squirrel (squirrel)
Swift (swift)
Typescript (typescript)
VHDL (vhdl)
VisualBasic (visualbasic, vb)
Verilog (verilog)
XML (xml, html)
YAML (yaml)
```
