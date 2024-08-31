### **1 - Introduction**

We were provided with a 2015 dataset from the Behavioral Risk Factor Surveillance System (BRFSS) that records various behaviors, conditions, and symptoms for U.S. individuals with or without diabetes. For this study, the dataset was cleaned and reduced to 70,692 responses, evenly split between those with diabetes and those with prediabetes or no diabetes. Our goal was to identify the most predictive risk factors for diabetes. Given the time constraints, we conducted a brief exploratory data analysis (EDA), categorized features using domain knowledge, performed a Chi-square test for initial selection, and refined our results with a Random Forest model.

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
	&emsp;- pandas<br>
	&emsp;- numpy<br>
	&emsp;- matplotlib<br>
	&emsp;- seaborn<br>
	&emsp;- sklearn.feature_selection --> SelectKBest, chi2<br>
	&emsp;- sklearn.preprocessing --> MinMaxScaler<br>
	&emsp;- sklearn.ensemble --> RandomForestClassifier<br>
	&emsp;- sklearn.feature_selection --> SelectFromModel<br>
	&emsp;- sklearn.model_selection --> train_test_split, GridSearchCV<br>
	&emsp;- sklearn.metrics --> accuracy_score, classification_report, confusion_matrix<br>


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
	&emsp;- Diabetes_binary<br>
	&emsp;- HighBP<br>
	&emsp;- HighChol<br>
	&emsp;- CholCheck<br>
	&emsp;- BMI<br>
	&emsp;- Smoker<br>
	&emsp;- Stroke<br>
	&emsp;- HeartDiseaseorAttack<br>
	&emsp;- PhysActivity<br>
	&emsp;- Fruits<br>
	&emsp;- Veggies<br>
	&emsp;- HvyAlcoholConsump<br>
	&emsp;- AnyHealthcare<br>
	&emsp;- NoDocbcCost<br>
	&emsp;- GenHlth<br>
	&emsp;- MentHlth<br>
	&emsp;- PhysHlth<br>
	&emsp;- DiffWalk<br>
	&emsp;- Sex<br>
	&emsp;- Age<br>
	&emsp;- Education<br>
	&emsp;- Income<br>


### **6 - Analysis**

The analysis was conducted in the following steps:<br>
1. **Exploratory Data Analysis (EDA)**: Univariate and Bivariate analysis (Pearson correlation), comparing negatively and positevely diagnosed group.<br>
2. **Chi2 test features selection**: Performing statistical test for features selection<br>
3. **Random Forest features selection**: Refining the results of our Chi2 with model-based features selection<br>
4. **Addendum**: Conducting a quick investigation on a group possibly at risk with the help of our Random Forest results<br>


### **7 - Results**

By combining domain knowledge with statistical and model-based feature selection, we identified four potential risk factors for diabetes.
However, these results should be interpreted cautiously.
First, no single feature stands out as a clearly distinguishable predictor, suggesting that diabetes risk is likely multifactorial. 
The relationships and interactions between features may be more significant than the individual features themselves. Future analyses should explore feature combinations that could be more predictive of diabetes.
Among the four remaining features, three fall into the "Physiological Conditions" category, highlighting the connection between individual health habits and diabetes diagnosis. However, each of these habits may be influenced or conditioned by other factors, raising questions about how socio-economic conditions affect physiological conditions and potentially lead to diabetes.
Additionally, even though correlations were found between certain features and diabetes status, they do not necessarily indicate direct causation.

Mitigating Results and Considering False Negatives
After identifying potential risk factors, we analyzed a sample of the population that tested negative but had not seen a doctor in the past year due to cost and lacked healthcare coverage. We sought to determine if this group might be at risk or falsely negative for diabetes. We found that this population exhibited higher risk factor metrics compared to the negative group with healthcare access, though cholesterol levels were similar. Notably, heavy alcohol consumption was higher in the at-risk group, suggesting that alcohol might be a risk factor. Once positively diagnosed, individuals may consume less alcohol due to health concerns.


### **8 - Visualizations**

Plots viz located in:
&emsp;`results/`


### **9 - Conclusions**

There are elements of our approach that could be refined. The sample population used in this study may not be optimal for such classification and selection, as it was limited to a single year (2015). The BRFSS study began in 1984, so there is more data available that could help us track individual behaviors and pathologies over time.
Observing the evolution of individuals’ health might yield more fruitful results by allowing us to compare behaviors before and after diabetes diagnosis while comparing features of individuals who remain healthy. 
Recognizing the multifactorial nature of diabetes, other factors such as environmental components (e.g., temperature affecting blood sugar and insulin levels), pollutants, or genetic contributions, which are already known to influence human physiology, should also be considered.


### **10 - Acknowledgement**

XXX

### **11 - Contact**

Bertrand Flanet<br>
E-mail: bertrand.flanet@gmail.com<br>
linkedIn: https://www.linkedin.com/in/bertrand-flanet-67b1b2299/
