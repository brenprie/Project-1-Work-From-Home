# **Census Data Analysis (2013)**

This project analyzes demographic and employment data from the United States Census in 2013. The focus is on understanding trends in educational attainment, socioeconomic factors, and their correlations with key historical events such as the 2015 industry-specific downturn and the 2020–2021 pandemic.

## **Data Source**
The dataset used in this project is publicly available on Kaggle:

- **Dataset**: [Demographics and Employment in the United States](https://www.kaggle.com/datasets/econdata/demographics-and-employment-in-the-united-states)
- **Provider**: EconData on Kaggle
- **Description**: The dataset contains various demographic and employment metrics collected through the U.S. Census.

---

## **Project Overview**

### **Objective**
The goal of this analysis is to:
1. Explore trends in educational attainment (high school, bachelor's, master's, and doctorate degrees) over time.
2. Compare and correlate the data with historical socioeconomic events.
3. Use census data to derive meaningful insights into the evolving educational and employment landscape.

### **Key Features**
- **Educational Trends Analysis**:
  - Examines how educational attainment levels have shifted over the years, focusing on key degrees (high school, bachelor’s, master’s, doctorate).
  - Correlates trends with historical periods, including the 2015 industry-specific downturn and the 2020–2021 pandemic.

- **Socioeconomic Factor Analysis**:
  - Investigates correlations between demographic attributes and employment data.
  - Explores the impact of these factors on the U.S. workforce and education system.

---

## **Tools and Technologies**
- **Programming Languages**:
  - Python (analysis, visualization)
  - Jupyter Notebook (development environment)
  
- **Libraries Used**:
  - Pandas: Data manipulation and analysis
  - Matplotlib/Seaborn: Visualization
  - NumPy: Numerical computation

- **External Tools**:
  - Kaggle API: Accessing the dataset
  - Xcode: For testing and running analysis scripts outside Jupyter Notebook

---

## **How to Run the Project**

### **Prerequisites**
1. **Python Environment**:
   - Ensure Python 3.x is installed on your system.
   - Install required Python libraries:
     ```bash
     pip install pandas numpy matplotlib seaborn
     ```
2. **Dataset**:
   - Download the dataset from [Kaggle](https://www.kaggle.com/datasets/econdata/demographics-and-employment-in-the-united-states) and place it in the `data` directory of this project.

### **Execution Steps**
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd census-data-analysis
   ```
3. Open the `analysis.ipynb` file in Jupyter Notebook or run the scripts using Xcode (see below).
   ```bash
   jupyter notebook analysis.ipynb
   ```
4. If running via Xcode:
   - Open Xcode and create a Command Line Tool project.
   - Add the analysis script to the project.
   - Configure the Run Script phase if using Python scripts.

---

## **Results**
- **Educational Attainment Trends**:
  - Clear visualization of degree-level trends across the dataset.
  - Insights into how socioeconomic events have influenced education.
  
- **Correlations and Socioeconomic Landscape**:
  - Comparative analysis reveals key factors impacting employment and education.

---

## **Future Work**
- Expand the analysis to include additional census years.
- Integrate machine learning models to predict future trends.
- Include geographic segmentation for state-level insights.

---

## **Acknowledgments**
- **Dataset Source**: [Kaggle - Demographics and Employment in the United States](https://www.kaggle.com/datasets/econdata/demographics-and-employment-in-the-united-states)
- **Tools Used**: Python, Jupyter Notebook, Xcode
