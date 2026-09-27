# Multivariate Analysis of the Diamonds Dataset

Final project for a Multivariate Analysis course (December 2025). It applies a full set of multivariate techniques to the classic **diamonds** dataset (53,940 diamonds, 10 variables; a random sample of 500 is analysed, `set.seed(12345)`) to study how price relates to the physical and quality attributes of each stone.

## What it covers

1. **Data preparation and EDA**
   - Outliers, distributions and Box-Cox / log transformations of `carat` and `price`
   - Normality checks of `depth`, `table`, `x`, `y`, `z`
   - Regrouping of rare categories in `cut`, `color` and `clarity`
   - Correlations and KMO index
2. **Principal Component Analysis (PCA)** on `logCarat`, `depth`, `table`, `x`, `y`, `z`, with `logPrice` as supplementary
3. **Multidimensional Scaling (MDS)** with Euclidean and Gower distances
4. **Correspondence Analysis (CA)** for each pair: cut × color, cut × clarity, color × clarity
5. **Multiple Correspondence Analysis (MCA)**: dimension selection, clouds of individuals, categories and variables
6. **Clustering and profiling**: hierarchical clustering (5 linkage methods), k-means and hierarchical clustering on principal components (HCPC)
7. **Discriminant analysis**

## Repository structure

| File | Purpose |
|---|---|
| `DiamondsAnalysis.Rmd` | Full analysis and report (knits to PDF) |
| `diamonds.csv` | Dataset: `carat`, `cut`, `color`, `clarity`, `depth`, `table`, `price`, `x`, `y`, `z` |
| `multivariate-analysis.Rproj`, `MA_project.Rproj` | RStudio projects (either one works) |
| `Index` | Leftover file listing the UCI *wine* dataset; not used by the analysis |

## How to run

1. Open `multivariate-analysis.Rproj` in RStudio.
2. Install the packages:

   ```r
   install.packages(c("FactoMineR", "MASS", "biotools", "cluster", "corrplot", "dplyr",
                      "factoextra", "ggplot2", "ggrepel", "klaR", "kmed", "psych"))
   ```

3. Knit `DiamondsAnalysis.Rmd`. PDF output uses `xelatex`, so a LaTeX distribution is needed (for example `tinytex::install_tinytex()`).

## Authors

Laia Jané, Elisa Müller, Runxiao Qiu and Berta Torrents
