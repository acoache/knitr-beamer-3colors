## Sweave/TeX template for beamer presentations


This Sweave template for beamer presentations uses three colors, mainly a theme color (blue), an alert color (orange) and a third color (green) that are easily customizable. R code and outputs fit with the colors defined in the template.
    
If you want to add R codes and outputs in your slides, use the Sweave (.Rnw) file so their colors will fit with the theme of the beamer. Otherwise you can use either the Sweave or TeX (.tex) file.

For more information about **knitr** and options of R code chunks, see https://yihui.name/knitr/. 

## Define new colors


If you want to change the three colors to create another color theme in any file, set new RGB color codes in the following commands:

```tex
% Define colors
\definecolor{mgreen}{rgb}{0,0.6,0.35}
\definecolor{mblue}{rgb}{0,0.4,0.6}
\definecolor{mred}{rgb}{0.9,0.3,0}
\definecolor{mgrey}{rgb}{0.95,0.95,0.95}
\definecolor{mblack}{rgb}{0,0,0}
```

If you are using the Sweave file, modify RGB codes in the first chunk accordingly so that your R outputs fit with the color theme:

```r
mblue <- function(alpha = 1){rgb(0,0.4,0.6,alpha)}
mred <- function(alpha = 1){rgb(0.9,0.3,0,alpha)}
mgreen <- function(alpha = 1){rgb(0,0.6,0.35,alpha)}
```

### Authors


- Anthony Coache *(creator, author)*
- Renaud Alie *(author)*