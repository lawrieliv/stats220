# I hope this meme made you smile and if not .... I popped a smile under it
![my meme](https://user-images.githubusercontent.com/101287893/157534674-879d0f60-a670-4a9c-aa95-b8f2986eafeb.jpg)


![](https://cdn1.vectorstock.com/i/1000x1000/99/80/laughing-smiley-emoticon-cartoon-happy-face-vector-22209980.jpg)

# If this still failed to make you smile, i have linked a website with information that may help you
![(


Pharrell Williams - Happy (Video) - YouTubehttps://www.youtube.com › watch


)


---
title: "meme.R"
author: "Liv Lawrie 860370011"
date: "10/03/2022"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
install.packages("magick")
```

### R Markdown

```{r cars}
library(magick)

## creating word boxes
# grief box
grief <- image_blank(width = 200, 
            height = 200, 
            color = "#e6f7ff") %>%
  image_annotate(text = "5 stages of",
                 color = "#ff9966",
                 size = 40,
                 font = "Impact",
                 gravity = "center")
# denial box
denial <- image_blank(width = 200, 
                       height = 200, 
                       color = "#e6f7ff") %>%
  image_annotate(text = "Denial",
                 color = "#ff9966",
                 size = 40,
                 font = "Impact",
                 gravity = "center")
# anger box
anger <- image_blank(width = 200, 
                       height = 200, 
                       color = "#e6f7ff") %>%
  image_annotate(text = "Anger",
                 color = "#ff9966",
                 size = 40,
                 font = "Impact",
                 gravity = "center")
# bargaining box
bargain <- image_blank(width = 200, 
                       height = 200, 
                       color = "#e6f7ff") %>%
  image_annotate(text = "Bargain",
                 color = "#ff9966",
                 size = 40,
                 font = "Impact",
                 gravity = "center")
depression <- image_blank(width = 200, 
                       height = 200, 
                       color = "#e6f7ff") %>%
  image_annotate(text = "Depression",
                 color = "#ff9966",
                 size = 40,
                 font = "Impact",
                 gravity = "center")
# Acceptance box
acceptance <- image_blank(width = 200, 
                       height = 200, 
                       color = "#e6f7ff") %>%
  image_annotate(text = "Acceptance",
                 color = "#ff9966",
                 size = 40,
                 font = "Impact",
                 gravity = "center")

## picture boxes
grief2 <- image_blank(width = 200, 
            height = 200, 
            color = "#e6f7ff") %>%
  image_annotate(text = "R error grief",
                 color = "#ff9966",
                 size = 40,
                 font = "Impact",
                 gravity = "center")

denial_human <- image_read("https://image.shutterstock.com/image-vector/young-man-showing-crossed-hands-600w-2054500886.jpg") %>%
  image_scale(200)
denial_human

anger_human <- image_read("https://image.shutterstock.com/image-vector/anger-rage-screaming-concept-young-600w-1887490843.jpg") %>%
  image_scale(200)
anger_human

bargaining_human <- image_read("https://image.shutterstock.com/image-vector/people-begging-praying-hands-together-600w-1618420927.jpg") %>%
  image_scale(200)
bargaining_human

depression_human <- image_read("https://image.shutterstock.com/image-vector/sad-young-girl-flat-vector-600w-1609331719.jpg") %>%
  image_scale(200)
depression_human

acceptance_human <- image_read("https://image.shutterstock.com/image-vector/guy-sitting-lotus-position-600w-1410510524.jpg") %>%
  image_scale(200)
acceptance_human


## combining rows
# first row
firstrow_vector <- c(grief, grief2)
first_row <- image_append(firstrow_vector)
first_row

# second row
secondrow_vector <- c(denial, denial_human)
second_row <- image_append(secondrow_vector)
second_row

# third row
thirdrow_vector <- c(anger, anger_human)
third_row <- image_append(thirdrow_vector)
third_row

# fourth row
fourthrow_vector <- c(bargain, bargaining_human)
fourth_row <- image_append(fourthrow_vector)
fourth_row

# fifth row
fifthrow_vector <- c(depression, depression_human)
fifth_row <- image_append(fifthrow_vector)
fifth_row

# six row
sixthrow_vector <- c(acceptance, acceptance_human)
sixth_row <- image_append(sixthrow_vector)
sixth_row

## combining whole thing
meme <- c(first_row, second_row, third_row, fourth_row, fifth_row, sixth_row) %>%
  image_append(stack = TRUE) %>%
  image_scale(500)
image_write(meme, "my.meme.png")
```
