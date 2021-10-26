## Sweave/TeX template for beamer presentations


This Sweave/TeX template for beamer presentations uses three colors, mainly a theme color (blue), an alert color (orange) and a third color (green) that are easily customizable. R code and outputs fit with the colors defined in the template.
    
If you want to add R codes and outputs in your slides, use the Sweave (.Rnw) file so their colors will fit with the theme of the beamer. Otherwise you can use either the Sweave or TeX (.tex) file.

For more information about **knitr** and options of R code chunks, see https://yihui.name/knitr/ or the [R Markdown cheat sheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf). 

## Define new colors


There are already four color themes in this template: a light theme, dark theme, black and white theme, and Metropolis theme. If you want to change the colors to create another color theme in any file (i.e. .Rnw or .tex), there are two possibilities. You can either modify the RGB colors in the **beamerthemeknitr-beamer-3colors.sty** file for an existing theme by changing the following commands:

```tex
% Define colors
\definecolor{mgreen}{rgb}{0,0.6,0.35}
\definecolor{mblue}{rgb}{0,0.4,0.6}
\definecolor{mred}{rgb}{0.9,0.3,0}
\definecolor{mgrey}{rgb}{0.85,0.85,0.85}
\definecolor{mblack}{rgb}{0,0,0}
```

You can also create a brand new theme by adding a conditional statement and a new color customization section, i.e.

```tex
\newif\if@doNewNameTheme
\@doNewNameThemefalse
\DeclareOption{NewNameTheme}{\@doNewNameThemetrue}

...

\if@doNewNameTheme
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%                            NEW NAME THEME
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
...
```


If you are using the Sweave file, modify RGB codes in the first chunk accordingly so that your R outputs fit with the color theme:

```r
mblue <- function(alpha = 1){rgb(0,0.4,0.6,alpha)}
mred <- function(alpha = 1){rgb(0.9,0.3,0,alpha)}
mgreen <- function(alpha = 1){rgb(0,0.6,0.35,alpha)}
```

To customize even more this beamer template, you can modify commands in the "colors customization" or "configure visual aspects" sections. You can either create new environments with different colors, redefine colors of R code or change every color displayed in the template from the text to the background.


If you change several colors or add customization commands, feel free to contribute to this template to enhance its look and usefulness! This template is still under construction.


### Authors


- Anthony Coache *(creator, author)*
- Renaud Alie *(author)*
