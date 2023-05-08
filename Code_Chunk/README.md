## Tidy Data - Reshape with **Pivot Wider()**

### About Code

This code chunk reshapes and tidys data for ease of interpretation. It uses the `Titanic` dataset built-into R which provides information about the survival of passengers on the Titanic voyage. Using the [`pivot_wider()`](https://tidyr.tidyverse.org/reference/pivot_wider.html) function, it increases the number of columns while decreasing the number of rows. It renders a data frame that has unique observations. 

### Sample Code

```r
df %>% 
    distinct() %>%
    pivot_wider(
              names_from = x,    
              values_from = y) %>%  
   select() %>%   # rename & filter cols
   unnest(cols = everything()) %>% # removes duplicate rows if needed
   print()
```

