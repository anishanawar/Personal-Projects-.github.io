# Warehouse SKU Data Analysis

This repository focuses on analyzing and visualizing warehouse SKU inventory data. It explores data through clustering, dimensionality reduction, and feature extraction, with the aim of identifying patterns in inventory pick trends throughout the day. The techniques used include KMeans clustering for grouping similar SKUs and Principal Component Analysis (PCA) for reducing the data's dimensionality, which helps in visualizing large-scale data in a simplified 2D space.

### Description

The dataset in this project contains various details of warehouse SKUs, including their category, weight, volume, total inventory picks, and hourly data for each time slot between 7 AM and 8 PM. The objective is to uncover patterns related to how frequently different SKUs are picked at various times of the day, and to group similar SKUs together using clustering techniques.

Key steps involved include:
- **Data Preprocessing**: Cleaning and organizing the data to be used for analysis.
- **Clustering**: Using KMeans clustering to assign SKUs into distinct groups based on their hourly pick patterns.
- **Dimensionality Reduction**: Applying PCA to reduce the dataset's complexity and visualize it in two dimensions while retaining most of the original variance.

### Project Highlights

- **Data Loading and Inspection**: The project begins with loading the dataset and displaying the first few rows to ensure the data is correct and ready for processing.
- **Clustering Using KMeans**: The KMeans algorithm is used to divide the data into five distinct clusters, based on SKU's inventory pick patterns throughout the day. This helps to identify groups of SKUs with similar demand and can inform inventory management strategies.
- **PCA for Visualization**: Principal Component Analysis (PCA) is performed on the data to reduce its dimensionality. By transforming the data into two principal components, the project allows for a clear 2D visualization of the clustering results. This step aids in understanding how different SKU clusters relate to each other visually.
- **Data Export**: Once clustering and PCA analysis are completed, the enriched dataset (including cluster labels) is saved, making it available for future use or sharing.

### Project Workflow

1. **Data Loading & Inspection**: The data is first loaded and examined to understand its structure, ensuring no errors or missing values that might affect analysis.
   
2. **Clustering Analysis**:
   - The hourly pick data is extracted and used as features for clustering. This data is scaled for standardization, ensuring that each feature has a similar weight in the clustering process.
   - KMeans clustering is applied to group the SKUs into five clusters based on their hourly inventory picks.

3. **Dimensionality Reduction with PCA**:
   - PCA is applied to reduce the high-dimensional data into two components, which simplifies the analysis and makes it easier to visualize.
   - The results of the PCA are plotted on a 2D graph, with different colors representing the distinct SKU clusters identified by KMeans.

4. **Save Processed Data**:
   - The final enriched dataset, now containing cluster labels, is saved to a new CSV file for further analysis, reporting, or sharing with stakeholders.

### Outcomes and Insights

By analyzing SKU data through clustering and dimensionality reduction, this project helps identify specific groups of SKUs that share similar picking trends. These insights are valuable for warehouse managers, allowing them to:
- **Optimize inventory management** by understanding which SKUs are picked more frequently at certain times of the day.
- **Make data-driven decisions** about stock replenishment and shelf placement based on picking patterns.
- **Enhance operational efficiency** by grouping items with similar pick patterns and streamlining workflow processes.

### Installation

To run this project locally, you’ll need to install the following Python libraries:

- **pandas**: For data manipulation.
- **numpy**: For numerical operations.
- **scikit-learn**: For machine learning models, including KMeans and PCA.
- **matplotlib**: For visualizing the results.

### Usage

1. **Clone the repository** and install dependencies:
   - Clone the repository to your local machine and install the necessary libraries using `pip`.
   
2. **Load and Inspect Data**: Load the data from a CSV file and inspect the first few rows to verify its structure.
   
3. **Perform Clustering**: Apply KMeans to group SKUs based on hourly inventory pick data.

4. **Run PCA for Visualization**: Reduce the dataset's dimensionality to two components using PCA and visualize the results in a 2D plot.

5. **Export the Processed Data**: After clustering and dimensionality reduction, save the updated dataset with cluster labels for further analysis.

### Conclusion

This project serves as a practical example of how to apply machine learning and data science techniques to warehouse inventory data. By clustering SKUs based on their pick patterns and using PCA to visualize the data, it provides actionable insights that can help optimize inventory management and operational processes in a warehouse setting.
