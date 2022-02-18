HW 1, CS 625, Fall 2021
================
Maryam Salehi, Sep 9, 2021

## Git, GitHub

1.  *What is your GitHub username?* msale007

2.  *What is the URL of your remote GitHub repo (created through
    Mr. Kennedy’s exercises)?*

<https://github.com/msale007/Myrepo-.git>

## R

The command below will load the tidyverse package. If you have installed
R, RStudio, and the tidyverse package, it should display a list of
loaded packages and their versions

``` r
library(tidyverse)
```

    ## -- Attaching packages --------------------------------------- tidyverse 1.3.1 --

    ## v ggplot2 3.3.5     v purrr   0.3.4
    ## v tibble  3.1.4     v dplyr   1.0.7
    ## v tidyr   1.1.3     v stringr 1.4.0
    ## v readr   2.0.1     v forcats 0.5.1

    ## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

## R Markdown

1.  *Create a bulleted list with at least 3 items*

-   First item
-   Second item
-   Third item

2.  *Write a single paragraph that demonstrates the use of italics,
    bold, bold italics, code, and includes a link. The paragraph does
    not have to make sense.*

This is **first** line. Here is the **second** line. This *text* is
really important. ***In this sentence I have used bold and italic
together.*** In the next section type `LINES OF MY CODE`. Here is the
link to see the [full text](https://fulltext.com)

3.  *Create a level 3 heading*

### Heading level 3

## R

#### Data Visualization Exercises

1.  (Q2) *How many rows are in mpg? How many columns?*

234 rows and 11 columns

1.  (Q4) *Make a scatterplot of hwy vs cyl.*

```{r}
ggplot(data = mpg) +    geom_point(mapping = aes(x = hwy, y = cyl))
```
![unnamed-chunk-2-1](https://user-images.githubusercontent.com/70677493/132733269-11f2e3a1-8699-448f-b7af-4528c5b97d7e.png)


#### Workflow: basics Exercises

1.  (Q2) *Tweak each of the following R commands so that they run
    correctly (`library(tidyverse)` is correct):*

``` r
library(tidyverse)
ggplot(dota = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))
fliter(mpg, cyl = 8)
filter(diamond, carat > 3)
```

`ggplot(data = mpg) +   geom_point(mapping = aes(x = displ, y = hwy))`
typo mistake: dota changed to data

`filter(mpg, cyl == 8)` ‘=’ replaced with ‘==’ Filter typo mistake

`filter(diamonds, carat > 3)` “diamond” replaced with diamonds

## Google Colab

1.  *What are the URLs of your Google Colab notebooks (both Python and
    R)?*

[Google Colab
URL](https://colab.research.google.com/drive/1KLX6zVpzqbDN66Ota8Z-KKF6S5siaYyS?usp=sharing)
[Practice exercises in Section
4.4.](https://colab.research.google.com/drive/1N2WSA3CBQyQ3OCTN7R84PRzedPSAl8im)

## Tableau

*Insert your the image of your final bar chart here*
![Sales-in-the-Central](https://user-images.githubusercontent.com/70677493/132733577-01e31dd9-9976-4c1f-b27a-2d0264ba4caf.jpg)


1.  *What conclusions can you draw from the chart?*

Over the time in the central region, the profit in technology goes
higher, especially for phones while the profit for office supplies got
negative.

## Observable and Vega-Lite

### A Taste of Observable

1.  *In the “New York City weather forecast” section, try replacing
    `Forecast: detailedForecast` with `Forecast: shortForecast`. Then
    press the blue play button or use Shift-Return to run your change.
    What happens?*

In the forecast section, there is short forecast instead of detail
forecast.

1.  *Under the scatterplot of temperature vs. name, try replacing
    `markCircle()` with `markSquare()`. Then press the blue play button
    or use Shift-Return to run your change. What happens? How about
    `markPoint()`?*

In the plot there would be squares instead of circles when we use
`markSquare()` and there would be points(empty circles) instead of
circles when I use `markPoint()`.

1.  *Under “Pick a location, see the weather forecast”, pick a location
    on the map. Where was the point you picked near?*

Kapowsin, WA.

1.  *The last visualization on this page is a “fancy” weather chart
    embedded from another notebook. Click on the 3 dots next to that
    chart and choose ‘Download PNG’. Insert the PNG into your report.*

![HW1-Observable](https://user-images.githubusercontent.com/70677493/132733479-f5c7dd25-d0b4-4ecf-bf13-97433c53cd19.png)


### Charting with Vega-Lite

`markCircle()`

1.  *Pass an option of `{ size: 200 }` to `markCircle()`.* The size of
    circles increased (200 times larger)
2.  *Try `markSquare` instead of `markCircle`.* Circles are replaced by
    squares
3.  *Try `markPoint({ shape: 'diamond' })`.* Empty diamonds plotted
    instead of filled circles

`vl.x().fieldQ("Horsepower")`, ..

1.  *Change `Horsepower` to `Acceleration`* There is a new plot when x
    is Acceleration and y is Miles\_per\_Gallon.  

2.  *Swap what fields are displayed on the x- and y-axis* If swap the
    axis the plot shape rotated 90 degree and mirrored.
    `vl.tooltip().fieldN("Name")`

3.  *Change `Name` to `Origin`.* Nothing changed.

Another example, `count()`

1.  *Remove the `vl.y().fieldN("Origin")` line.* There would be just one
    bar chart.
2.  *Replace `count()` with `average("Miles_per_Gallon")`.* The values
    for each bar changed.

## References

*Every report must list the references that you consulted while
completing the assignment. If you consulted a webpage, you must include
the URL.*

-   [Git tutorial](https://www.atlassian.com/git/tutorials/git-bash)
-   [Git
    Workshop](https://git.cs.odu.edu/tkennedy/git-workshop/-/wikis/Git-Workshop)
-   [Git](https://happygitwithr.com/hello-git.html)
-   [Ssh Key](https://happygitwithr.com/ssh-keys.html)
-   [Shell](https://happygitwithr.com/shell.html#shell)
-   [Git](https://r-pkgs.org/git.html#git-init)
-   [Git For Windows](https://www.youtube.com/watch?v=F_fPEMnr1OQ)
-   [R For Data Science](https://r4ds.had.co.nz/data-visualisation.html)
-   [Markdown Basic](https://www.markdownguide.org/basic-syntax)
-   [Markdown Cheatsheet](https://rmarkdown.rstudio.com/lesson-1.html)
-   [Markdown
    Image](https://www.earthdatascience.org/courses/earth-analytics/document-your-science/add-images-to-rmarkdown-report/)
-   [R For Data
    Science](https://r4ds.had.co.nz/data-visualisation.html#first-steps)
-   [R Basics](https://r4ds.had.co.nz/workflow-basics.html#practice)
-   [Google
    Colab](https://colab.research.google.com/drive/1yN0mKVc_Ssl8rQ74ShPnaMCnNhFc2__h)
-   [Tableau For Students](https://www.tableau.com/academic/students)
-   [Tableau
    tutorial](https://www.tableau.com/learn/tutorials/on-demand/getting-started)
-   [Observable](https://observablehq.com/@observablehq/a-taste-of-observable)
-   [Vega Lite](https://observablehq.com/@observablehq/vega-lite)
