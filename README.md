### **1 - Introduction**



### **2 - Table of Contents**

- [1 - Introduction](#1---introduction)
- [2 - Table of Contents](#2---table-of-contents)
- [3 - Usage](#3---usage)
- [4 - Project Structure](#4---project-structure)
- [5 - Data](#5---data)
- [6 - Analysis](#6---analysis)
- [7 - Results](#7---results)
- [8 - Visualizations](#8---visualizations)
- [9 - Conclusions](#9---conclusions)
- [10 - Acknowledgement](#10---acknowledgement)
- [11 - Contact](#11---contact)


### **3 - Usage**

 .ipynb:
Google Colab: Upload directly via the "File" menu or open from Google Drive<br>
Jupyter Notebook: Install Jupyter, start it via terminal, and open the .ipynb file through the interface

. python:<br>
	- pandas<br>
	- numpy<br>
	- matplotlib<br>
	- seaborn<br>
	- sqlalchemy<br>
	- math<br>
	- sklearn<br>


### **4 - Project Structure**
```
Diabetes_Features_Selection/
│
├── data/: # Reference to dataset and used aggregated dataset at various granularity level
|   └── diabetes_BRFSS2015 - diabetes_binary_5050split_health_indicators_BRFSS2015.csv
│
├── notebooks/: # Jupyter notebooks with the analysis/segmentation code
│   └── Diabetes_risk_factors_analysis.ipynb
│
├── results/: # Output files, results, project report, .ppt presentation
│   ├── presentation_material
│   │   ├── BRFSS logo.png
│   │   └──CDC logo.png
│
│   ├── Diabetes risk factors analysis slides.pdf
│   ├── Diabetes risk factors analysis.pdf
│   ├── corr_heatmap.png
│   ├── feature_selection_chi2.png
│   ├── feature_selection_random_forest.png
│   ├── possible_false_negative.png
│   ├── possible_false_negative_ratio.png
│   ├── univariate.png
│   └── univariate_split.png
│
└── README.md
```
### **5 - Data**
The dataset `diabetes_BRFSS2015 - diabetes_binary_5050split_health_indicators_BRFSS2015.csv`
- Diabetes_binary<br>
- HighBP<br>
- HighChol<br>
- CholCheck<br>
- BMI<br>
- Smoker<br>
- Stroke<br>
- HeartDiseaseorAttack<br>
- PhysActivity<br>
- Fruits<br>
- Veggies<br>
- HvyAlcoholConsump<br>
- AnyHealthcare<br>
- NoDocbcCost<br>
- GenHlth<br>
- MentHlth<br>
- PhysHlth<br>
- DiffWalk<br>
- Sex<br>
- Age<br>
- Education<br>
- Income<br>


### **6 - Analysis**

The analysis was conducted in the following steps:<br>
1. **Exploratory Data Analysis (EDA)**: Identified key patterns and trends in the data.<br>
2. **Feature Engineering**: Created new features to facilitate definition of thresholds and metrics<br>
3. **RFM**: Conducted a Recency, Frequency, Monetary segmenting<br>
4. **Segmentation by branching**: Conducted a segmentation with a branching method<br>
5. **Perks**: Attributed perks to each generated groups<br>
3. **Extra: Clustering**: Applied K-Means clustering to segment customers into distinct groups.<br>


### **7 - Results**


### **8 - Visualizations**

Plots viz located in:
`results/`


### **9 - Conclusions**



### **10 - Acknowledgement**



### **11 - Contact**

Bertrand Flanet<br>
E-mail: bertrand.flanet@gmail.com<br>
linkedIn: https://www.linkedin.com/in/bertrand-flanet-67b1b2299/
