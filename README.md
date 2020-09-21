# Lab7


For this document, turn in your R Markdown document that embeds Shiny. Note this will not generate a static html output file.


### 1.  Read Covid19 Data (4 points)

First read in the data and convert from wide to long.
```
library(tidyverse)
library(shiny)
library(DT)
covid_cases <- read_csv("https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv") 
```


### 2. Create an Interactive Table (4 points)

Allow users to select the date to display in the table. Note the `DT::renderDataTable` might be useful (this is the `renderDataTable` function in the `DT` package).





## 3. Interactive Figure (6 points)

Read in a US level covid dataset and convert this to a long dataframe.
```
US_data <- read_csv("https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_US.csv") 
```

Create an interactive figure of your choice. You can consider filtering by state / province to show curves, include colors and/or faceting based on selected variables, or something else of your choosing.
