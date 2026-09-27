# Multivariate Analysis of EuroBasket 2025 Player Statistics

Two homework assignments for a Multivariate Analysis course (autumn 2025). Both use player statistics from the four teams in the **FIBA EuroBasket 2025 Final Four**.

## Homework 1: Dimensionality reduction (`HW1_MVA.Rmd`)

- Exploratory analysis and correlations between the game statistics
- **PCA** with `Position` and `EFF` as supplementary variables; choice of components and interpretation of variable and individual plots
- **Metric MDS** with Euclidean distance (scaled numeric variables) and with Gower distance (including `Position`), plus a comparison of both
- **MCA** after turning each statistic into "over average" / "below average"

## Homework 2: Clustering and discriminant analysis (`HW2.Rmd`)

- **Hierarchical clustering** with complete, Ward, single, average and centroid linkage
- **K-means**: number of clusters chosen with the elbow (TWSS), pseudo F and silhouette indices; cluster profiling
- **Hierarchical clustering on PCA and MCA results** (HCPC)
- Comparison of clustering methods and final recommendation
- **Discriminant analysis**: normality and Box's M assumption checks, classification table, correct classification rate and Press's Q statistic

## Repository structure

| File | Purpose |
|---|---|
| `HW1_MVA.Rmd` | Homework 1: PCA, MDS and MCA |
| `HW2.Rmd` | Homework 2: clustering and discriminant analysis |
| `HW2_MVA_FALL2025.pdf` | Homework 2 statement (includes the variable definitions) |
| `data_Eurobasket_2025.xlsx` | Player statistics dataset |
| `HW2-MVA.Rproj` | RStudio project |

## Variables

`Position`, `MIN`, `FG`, `2PT FG`, `3PT FG`, `FT`, `OREB`, `DREB`, `REB`, `AST`, `PF`, `TO`, `STL`, `BLK`, `EFF`, `PTS`. See the PDF for full definitions.

## How to run

1. Open `HW2-MVA.Rproj` in RStudio.
2. Install the packages:

   ```r
   install.packages(c("readxl", "FactoMineR", "cluster", "corrplot", "ggplot2",
                      "ggrepel", "kmed", "dplyr", "factoextra", "biotools", "MASS"))
   ```

3. Knit `HW1_MVA.Rmd` or `HW2.Rmd`. Both read the Excel file from the project root.

## Authors

Elisa Müller and Runxiao Qiu
