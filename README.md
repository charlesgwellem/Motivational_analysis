# Unsupervised Clustering of Patient Motivation Data

## **Overview**

This project applies various unsupervised clustering techniques to group patients based on their motivation scores from a study. The study contains responses from **49 patients** to **12 different motivational factors**, each score representing the average response to several questions under a particular factor.

The main goal is to identify meaningful groups of patients (clusters) and understand the motivational factors that drive these groupings. The project involves the use of hierarchical clustering, k-means clustering, and other exploratory data analysis techniques to explore and validate the number of clusters.

## **Project Structure**

### **Milestones**

1. **Data Preprocessing:**
   - Check for missing values.
   - Standardize the data to ensure comparability of features, since they may not be on the same scale.
  
2. **Similarity Metric:**
   - Compute the distance between observations using **Euclidean distance** as the similarity metric.

3. **Clustering:**
   - Perform hierarchical clustering using various linkage methods: **complete**, **single**, and **average** linkage.
   - Use **k-means clustering** to determine the optimal number of clusters using **within-cluster sum of squares** and **silhouette analysis**.

4. **Analysis:**
   - Use **Principal Component Analysis (PCA)**, **Correlation Analysis**, and **Recursive Partitioning** to examine which factors drive patient groupings.
   - Visualize the clusters using **heatmaps** and other graphical methods.

### **Key Results**

- Hierarchical clustering identifies three main clusters of patients, with the most distinctive cluster containing patients **P1, P23, P44**, and another patient, **P26**, joining based on k-means clustering results.
- **PCA** and **correlation analysis** show that features such as **Macht_und_Einfluss**, **Eros_und_Schoenheit**, **Wettkampf**, and **Essen** strongly influence patient groupings.
- Recursive partitioning and variable importance analysis further confirm these findings.

## **Directory Structure**

- `solution_script.Rmd`: The R Markdown file that contains all code used in the analysis.
- `raw_data/`: Directory containing the dataset.
- `figures/`: Directory with figures such as dendrograms, PCA plots, clustering plots, and heatmaps.
- `results/`: Directory where results (e.g., PCA variance data) are stored.

## **Installation and Setup**

### **Requirements**

This analysis requires **R** and the following R packages:

- `openxlsx`
- `ggplot2`
- `purrr`
- `dplyr`
- `tidyr`
- `rafalib`
- `cluster`
- `corrplot`
- `rpart`
- `genefilter`
- `RColorBrewer`
- `gplots`
- `fpc`
- `vip`

You can install the required packages by running the following in R:

```r
install.packages(c("openxlsx", "ggplot2", "purrr", "dplyr", "tidyr", "rafalib", "cluster", "corrplot", "rpart", "genefilter", "RColorBrewer", "gplots", "fpc", "vip"))
```

### **Running the Analysis**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/charlesgwellem/Motivational_analysis.git
   cd Motivational_analysis
   ```

2. **Run the RMarkdown File**:
   Open the `solution_script.Rmd` file in RStudio and knit it to generate the analysis report in **HTML**, **PDF**, or **Word** format.

3. **Examine Results**:
   Generated figures will be saved in the `figures/` directory, and the PCA analysis results will be saved in the `results/` directory.

## **Detailed Methodology**

### **Data Preprocessing**
- Standardize the data to ensure that all features have a mean of 0 and a variance of 1, allowing for comparability.
- Check for missing values to ensure data completeness.

### **Clustering**
- **Hierarchical Clustering**: Performed using **complete**, **single**, and **average linkage** methods. The dendrogram visualizations illustrate the clustering hierarchy.
- **K-Means Clustering**: Used to determine the optimal number of clusters using **within-cluster sum of squares** and **silhouette analysis**.

### **Principal Component Analysis (PCA)**
- Identify the features that drive variation in patient responses.
- Use **loading scores** to determine which factors influence the clustering most significantly.

### **Correlation Analysis**
- Perform **Spearman correlation analysis** to identify relationships between motivational factors.
- Generate correlation plots to visualize these relationships.

### **Recursive Partitioning**
- Use recursive partitioning to identify the most important motivational factors that differentiate between clusters.

### **Visualization**
- Visualize clustering results with **heatmaps**, **PCA plots**, **dendrograms**, and other plots.

## **Outputs and Visualization**
- **Dendrograms**: Visualize hierarchical clustering results.
- **PCA Plot**: Visualize the separation of patients on the principal components.
- **Heatmap**: Visualize feature values across clusters.
- **Elbow Plot**: Determine the optimal number of clusters for k-means clustering.
- **Silhouette Analysis**: Validate the number of clusters.

## **Contact**
If you have any questions about this project or suggestions for improvement, please feel free to contact me at charlesgwellem@yahoo.fr.

## **License**
This project is licensed under the MIT License - see the LICENSE file for details.
