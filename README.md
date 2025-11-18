# Load required libraries
library(readr)

# Step 1: Import dataset
covid <- read_csv("C:\\Users\\gawas\\Downloads\\country_wise_latest.csv") 

# ----------- VISUALIZATIONS ----------- #

# 1. Pie Chart (Top 6 countries by Confirmed cases)
top_countries <- covid[order(-covid$Confirmed),][1:6,]
sectors <- top_countries$CountryRegion
values <- as.numeric(top_countries$Confirmed)
total <- sum(values)
percent_labels <- round(values / total * 100, 1)
labels <- paste0(sectors, "\n", values, " (", percent_labels, "%)")
mycolors <- c("tomato", "skyblue", "gold", "seagreen", "orchid", "grey70")
pie(
  values,
  labels = labels,
  col = mycolors,
  main = "Top 6 Countries by Confirmed Cases"
)

# 2. Stacked Bar Chart (Confirmed, Deaths, Recovered, Active in top 6 countries)
values_matrix <- as.matrix(top_countries[, c("Confirmed", "Deaths", "Recovered", "Active")])
rownames(values_matrix) <- top_countries$CountryRegion

barplot(t(values_matrix),
        beside = FALSE,
        col = c("tomato", "darkred", "skyblue", "green"),
        las = 2,
        main = "Pandemic Impact by Country (Top 6)")

legend("topleft",legend = colnames(values_matrix),fill = c("tomato", "darkred", "skyblue", "green"))


# 4. Scatter Plot (Confirmed vs Deaths, all countries)
plot(covid$Confirmed, covid$Deaths,
     col = "orange",
     pch = 19,
     main = "Confirmed vs Deaths (All Countries)",
     xlab = "Confirmed Cases",
     ylab = "Deaths")

# 5. Line Chart (Confirmed cases, top 6)
plot(1:6, top_countries$Confirmed, type = "o",
     col = "red",
     xaxt = "n",
     main = "Confirmed Cases in Top 6 Countries",
     xlab = "Country",
     ylab = "Region")
axis(1, at = 1:6, labels = top_countries$CountryRegion)
