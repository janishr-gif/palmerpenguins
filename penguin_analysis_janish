#install.packages("palmerpenguins")

#1  Calculate Summary Statistics by column-wise means for numeric variables

library(palmerpenguins)
library(tidyverse)

head(penguins)

numeric_means <- apply(penguins[, sapply(penguins, is.numeric)], 2, mean, na.rm = TRUE)

# Print the result
print(numeric_means)

#2  Count penguins by species
species_counts <- tapply(penguins$species, penguins$species, length)
print(species_counts)

#3  Analyze bill length by species

split_by_species <- split(penguins, penguins$species)
bill_length_means <- lapply(split_by_species, function(x) {
  mean(x$bill_length_mm, na.rm = TRUE)
})

# Print the result
print(bill_length_means)

#4  Create a summary table using sapply
numeric_cols <- penguins[sapply(penguins, is.numeric)]
summary_table <- sapply(numeric_cols, function(x) {
  c(mean = mean(x, na.rm = TRUE), 
    sd = sd(x, na.rm = TRUE))
})
print(summary_table)
