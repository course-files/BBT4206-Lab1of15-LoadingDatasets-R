Business Intelligence Project
================
Allan Omondi
2023-11-23

- [Setup Chunk](#setup-chunk)
- [Understanding the Dataset (Exploratory Data Analysis
  (EDA))](#understanding-the-dataset-exploratory-data-analysis-eda)
  - [Loading the Dataset](#loading-the-dataset)

## Setup Chunk

**Note:** the following KnitR options have been set as the global
defaults: <BR>
`knitr::opts_chunk$set(echo = TRUE, warning = FALSE, eval = TRUE, collapse = FALSE, tidy = TRUE)`.

More KnitR options are documented here
<https://bookdown.org/yihui/rmarkdown-cookbook/chunk-options.html> and
here <https://yihui.org/knitr/options/>.

# Understanding the Dataset (Exploratory Data Analysis (EDA))

## Loading the Dataset

The dataset that was used is available here:
<https://drive.google.com/drive/folders/1igmH49mZiY3VWKHt21AvFFe-3kFRWsub?usp=sharing>

``` r
library(readr)

su_advanceddb_bbit_2022_grades <- read_csv(
  "../data/SU_AdvancedDB_BBIT_2022_Grades.csv",
    col_types = cols(
        Proj_Sec0 = col_number(),
        Proj_Sec1 = col_number(), Proj_Sec2 = col_number(),
        Proj_Sec3 = col_number(), Proj_Sec4 = col_number(),
        Proj_Sec5 = col_number(), Proj_Sec6 = col_number(),
        Proj_Sec7 = col_number(), Proj_Sec8 = col_number(),
        Essay = col_number(), Quizzes = col_number(),
        Labs = col_number(), CAT = col_number(),
        Mid_Term_Evaluation = col_number(),
        End_Term_Evaluation = col_number(),
        Absenteeism_Percentage = col_number(),
        CourseWork_Total = col_number(),
        Exam = col_number(),
        Final = col_number(),
        Grade = col_factor(levels = c("A", "B", "C", "D", "E"))))

summary(su_advanceddb_bbit_2022_grades)
```

    ##    Proj_Sec0        Proj_Sec1        Proj_Sec2        Proj_Sec3    
    ##  Min.   :0.0000   Min.   :0.0000   Min.   :0.0000   Min.   :0.000  
    ##  1st Qu.:0.5000   1st Qu.:0.5000   1st Qu.:0.6000   1st Qu.:0.600  
    ##  Median :0.8000   Median :0.7000   Median :0.7000   Median :1.200  
    ##  Mean   :0.6829   Mean   :0.6486   Mean   :0.6793   Mean   :1.066  
    ##  3rd Qu.:0.9000   3rd Qu.:0.9000   3rd Qu.:0.8000   3rd Qu.:1.600  
    ##  Max.   :1.0000   Max.   :1.0000   Max.   :0.9200   Max.   :1.840  
    ##  NA's   :10       NA's   :10       NA's   :10       NA's   :10     
    ##    Proj_Sec4       Proj_Sec5       Proj_Sec6       Proj_Sec7     
    ##  Min.   :0.000   Min.   :0.000   Min.   :0.000   Min.   :0.0000  
    ##  1st Qu.:1.200   1st Qu.:0.475   1st Qu.:0.600   1st Qu.:0.0000  
    ##  Median :1.600   Median :1.600   Median :1.200   Median :0.0000  
    ##  Mean   :1.421   Mean   :1.243   Mean   :1.068   Mean   :0.4808  
    ##  3rd Qu.:1.800   3rd Qu.:1.800   3rd Qu.:1.600   3rd Qu.:1.4000  
    ##  Max.   :2.000   Max.   :2.000   Max.   :2.000   Max.   :2.0000  
    ##  NA's   :10      NA's   :10      NA's   :10      NA's   :16      
    ##    Proj_Sec8         Essay          Quizzes           Labs      
    ##  Min.   :0.600   Min.   :0.000   Min.   :0.000   Min.   :1.000  
    ##  1st Qu.:1.800   1st Qu.:2.900   1st Qu.:2.380   1st Qu.:5.000  
    ##  Median :1.900   Median :3.250   Median :3.130   Median :5.000  
    ##  Mean   :1.822   Mean   :3.086   Mean   :3.027   Mean   :4.766  
    ##  3rd Qu.:2.000   3rd Qu.:3.500   3rd Qu.:3.880   3rd Qu.:5.000  
    ##  Max.   :2.000   Max.   :4.500   Max.   :5.000   Max.   :5.000  
    ##  NA's   :65      NA's   :68      NA's   :1       NA's   :2      
    ##       CAT        Mid_Term_Evaluation End_Term_Evaluation Absenteeism_Percentage
    ##  Min.   :0.730   Min.   :1.364       Min.   :1.455       Min.   : 0.000        
    ##  1st Qu.:2.067   1st Qu.:4.000       1st Qu.:4.000       1st Qu.: 4.545        
    ##  Median :2.565   Median :4.364       Median :4.364       Median :13.636        
    ##  Mean   :2.719   Mean   :4.267       Mean   :4.259       Mean   :17.979        
    ##  3rd Qu.:3.438   3rd Qu.:4.727       3rd Qu.:4.818       3rd Qu.:27.273        
    ##  Max.   :4.560   Max.   :5.000       Max.   :5.000       Max.   :95.455        
    ##  NA's   :14      NA's   :14          NA's   :25                                
    ##  CourseWork_Total      Exam           Final        Grade   
    ##  Min.   : 0.00    Min.   : 0.00   Min.   :12.61   A   :20  
    ##  1st Qu.:19.60    1st Qu.:18.00   1st Qu.:41.66   B   :24  
    ##  Median :23.75    Median :27.00   Median :50.23   C   :29  
    ##  Mean   :23.07    Mean   :26.72   Mean   :50.93   D   :43  
    ##  3rd Qu.:27.37    3rd Qu.:37.00   3rd Qu.:61.61   E   :29  
    ##  Max.   :35.81    Max.   :54.00   Max.   :83.74   NA's:17  
    ##  NA's   :1        NA's   :17      NA's   :17

…to be continued
