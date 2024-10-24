## Lab 7 Overview

This lab will use the Canadian cheese dataset to explore features of Shiny. 

Learn more about Shiny interactive documents at [https://shiny.posit.co](https://shiny.posit.co) and <https://quarto.org/docs/interactive/shiny/>.

### Question 1 (5 points)

Update the default Shiny app to use the cheese dataset to create a histogram using the moisture percentage of the cheeses. Replace the histogram with a ggplot version and input number of bins directly in `geom_histogram()`. Note that you'll need to import data & load libraries within the server code.

---

```
sliderInput("bins", "Number of bins:", 
            min = 1, max = 50, value = 30)
plotOutput("distPlot")
```

```
#| context: server
output$distPlot <- renderPlot({
  library(tidyverse)
  cheese <- read_csv('https://raw.githubusercontent.com/stat408/Data/refs/heads/main/cheese_data.csv') |>
    filter(!is.na(MoisturePercent))
  
   x <- faithful[, 2]  # Old Faithful Geyser data
   bins <- seq(min(x), max(x), length.out = input$bins + 1)
   hist(x, breaks = bins, col = 'darkgray', border = 'white',
        xlab = 'Waiting time to next eruption (in mins)',
        main = 'Histogram of waiting times')
})
```


---

### Question 2 (5 points)

Explore the control widgets available in shiny [https://shiny.posit.co/r/getstarted/shiny-basics/lesson3/](https://shiny.posit.co/r/getstarted/shiny-basics/lesson3/) and add another widget to your output from the first question.

---

### Question 3 (5 points)

Explore the reactive output options in Shiny [https://shiny.posit.co/r/getstarted/shiny-basics/lesson4/](https://shiny.posit.co/r/getstarted/shiny-basics/lesson4/) and add another output option.


---

### Question 4 (5 points)

Create a new reactive figure that allows the user to create side-by-side violin plots of `MoisturePercent` by a selected variable. Hint: use `varSelectInput` and see the reference on the main shiny page <https://shiny.posit.co>.

---

