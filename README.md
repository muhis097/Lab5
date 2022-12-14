<!-- badges: start -->
[![R-CMD-check](https://github.com/muhis097/Lab5/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/muhis097/Lab5/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->


## Section 1: Introduction of API
As requested in assignment the main objective in this task is to retrieve data from selected api and after some preparation, make some output through the methods we learned in R.
Kolada API contains interesting factors known as key indicators related to different municipalities across Sweden. Here first we get some economic indicators mentioned in "factors.xlsx" for 12 municipalities [mentioned here](https://en.wikipedia.org/wiki/List_of_municipalities_of_Sweden_by_wealth) including Linkoping.
1-First function outputs a list including factor values, municipality code(ID), period. Apart from readxl and httr, no external libraries are loaded here:

```{r ,echo=FALSE}
KoladaAPI()
```

2-As it can be seen, the list is now ready to be used for the defined ShinyApp. To load shiny we use function bellow:

```{r ,echo=FALSE}
plotfunction_ind()
```

This function calls shiny to make an interactive plot to show the end-user plots made by two variables of Municipality ID code and corresponding factor. Do note that it's planned to add more plot types and all 290 Swedish municipalities for future releases of this application.
