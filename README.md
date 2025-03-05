# F21DL - Data Mining & Machine Learning Portfolio (Group10)
### ALWAYS MAKE SURE THAT YOU ARE COMMITING TO THE RIGHT BRANCH BY LOOKING AT THE BOTTOM LEFT CORNER OF VS CODE. 

## **README**
**Project Title:** Coffee, Chocolate, and Fruits

**Group Members:**
* Avoor Minha Fathima
* Arjun Girish
* Eman Iftikhar
* Mahak Bachani
* Mohammed Faiz Iqbal

**Project Milestones:**
* **Week 4:** Project Pitch Presentation
* **Week 8:** Dataset Exploration and Preprocessing Completed
* **Week 10:** Clustering Model Implementation and Evaluation
* **Week 11:** Predictive Modeling and Neural Network Implementation
* **Week 12:** Final Report and Presentation Preparation

**Dataset Sources:**

* **Dataset 1:** [Coffee Dataset]
    * **Source:** [https://www.kaggle.com/datasets/fatihb/coffee-quality-data-cqi]
    * **License:** [Database Contents License (DbCL) v1.0]
    * **Examples:**
        | variety          | processing_method | aroma | flavor | aftertaste | acidity | body | balance | uniformity | clean_cup | sweetness | cupper_points | total_cup_points | moisture | category_one_defects | quakers | category_two_defects | unit_of_measurement | altitude_low_meters | altitude_high_meters | altitude_mean_meters |
        |------------------|-------------------|-------|--------|------------|---------|------|---------|------------|-----------|-----------|---------------|------------------|----------|----------------------|---------|----------------------|---------------------|---------------------|----------------------|----------------------|
        | Bourbon          | Washed            | 8.5   | 8.75   | 8.5        | 8.75    | 8.25 | 8.5     | 10         | 10        | 10        | 8.75          | 87.5              | 11.8     | 0                    | 0       | 0                    | meters              | 1300                | 1600                 | 1450                 |
        | Typica           | Natural           | 8.25  | 8.5    | 8.25       | 8.5     | 8    | 8.25    | 10         | 10        | 10        | 8.5           | 86                | 11.5     | 0                    | 0       | 0                    | meters              | 1100                | 1400                 | 1250                 |


* **Dataset 2:** [Chocolate Quality]
    * **Source:** [https://www.kaggle.com/datasets/soroushghaderi/chocolate-bar-2020]
    * **License:** [Open Data Commons Attribution License (ODC-By) v1.0]
    * **Examples:**

      | Unnamed: 0 | ref  | company | company_location | review_date | country_of_bean_origin | specific_bean_origin_or_bar_name | cocoa_percent | rating | counts_of_ingredients | cocoa_butter     | vanilla        | lecithin       | salt           | sugar       | sweetener_without_sugar        | first_taste | second_taste | third_taste | fourth_taste |
      |------------|------|---------|------------------|-------------|------------------------|----------------------------------|---------------|--------|-----------------------|------------------|----------------|----------------|----------------|-------------|---------------------------------|-------------|--------------|-------------|--------------|
      | 0          | 2454 | 5150    | U.S.A            | 2019        | Madagascar             | Bejofo Estate, batch 1            | 76.0          | 3.75   | 3                     | have_cocoa_butter | have_not_vanila | have_not_lecithin | have_not_salt  | have_sugar  | have_not_sweetener_without_sugar | cocoa       | blackberry   | full body   | NaN          |
      | 1          | 2458 | 5150    | U.S.A            | 2019        | Dominican Republic     | Zorzal, batch 1                   | 76.0          | 3.50   | 3                     | have_cocoa_butter | have_not_vanila | have_not_lecithin | have_not_salt  | have_sugar  | have_not_sweetener_without_sugar | cocoa       | vegetal      | savory      | NaN          |




* **Dataset 3:** [Fruit Quality]
    * **Source:** [https://www.kaggle.com/datasets/muhammad0subhan/fruit-and-vegetable-disease-healthy-vs-rotten]
    * **License:** [CC0 1.0 Universal]
    * **Examples:** [Image Dataset - Please Check Repository]

**Data Preparation Pipeline:**
**Steps:**
1. Data Cleaning: Handle missing values, standardize column names, and remove irrelevant columns.
2. Data Transformation: Standardize numerical columns, label encode categorical columns.
3. Feature Engineering: Add derived columns like `coffee_grade` for classification.

**Coffee Dataset: Requirements and Results:**

* **R2: Data Analysis and Exploration:**
    * **Description:** Comprehensive EDA including histograms, boxplots, scatterplots, and heatmaps to visualize data distribution and feature correlations. Feature selection identified key attributes like `flavor`, `acidity`, and `cupper_points`.

* **R3: Clustering:**
    * **Description:** Implemented Hierarchical, K-Means, GMM, and DBSCAN clustering algorithms. Evaluated clusters using silhouette scores and visualizations. Identified natural groupings like `Below Specialty Quality`, `Very Good`, and `Excellent`.

* **R4: Baseline Training and Evaluation Experiments:**
    * **Description:** Models such as Decision Trees, Random Forest, XGBoost, and KNN were evaluated. Metrics include accuracy, precision, recall, and F1-Score.
    * **Table of Results:**
        | Model              | Accuracy | Weighted Precision | Weighted Recall | Weighted F1-Score |
        |--------------------|----------|--------------------|-----------------|--------------------|
        | Decision Tree      | 0.92     | 0.92               | 0.92            | 0.92               |
        | XGBoost            | 0.95     | 0.95               | 0.95            | 0.95               |
        | K-Nearest Neighbor | 0.82     | 0.79               | 0.82            | 0.78               |
        | Random Forest      | 0.95     | 0.95               | 0.95            | 0.95               |

* **R5: Neural Networks:**
    * **Description:** Implemented MLP and CNN models for classification. MLP achieved the highest accuracy of 0.97. CNN provided slightly better recall in the "Excellent" category.
    * **Table of Results:**
        | Model                                | Accuracy | Weighted Precision | Weighted Recall | Weighted F1-Score |
        |-------------------------------------|----------|--------------------|-----------------|--------------------|
        | Multi-Layer Perceptron (MLP)         | 0.97     | 0.95               | 0.96            | 0.95               |
        | Convolutional Neural Network (CNN)   | 0.96     | 0.94               | 0.96            | 0.95               |


**Chocolate Dataset: Requirements and Results:**

* **R2: Data Analysis and Exploration:**
    * **Description:** Comprehensive EDA including histograms, boxplots, scatterplots, and heatmaps to visualize data distribution and feature correlations. 

* **R3: Clustering:**
    * **Description:** Implemented Hierarchical, K-Means, GMM, and DBSCAN clustering algorithms. Evaluated clusters using silhouette scores, inertia, AIC/BIC and visualizations. Identified natural groupings within the dataset.

* **R4: Baseline Training and Evaluation Experiments:**
    * **Description:** Models such as Decision Trees, Random Forest, LightGBM, and KNN were evaluated. Metrics include accuracy, precision, recall, and F1-Score.
    * **Table of Results:**
    * **Best Case:**
        | Model              | Accuracy | Weighted Precision | Weighted Recall | Weighted F1-Score |
        |--------------------|----------|--------------------|-----------------|--------------------|
        | Decision Tree      | 0.49     | 0.48               | 0.49            | 0.48               |
        | LightGBM           | 0.57     | 0.57               | 0.57            | 0.57               |
        | K-Nearest Neighbor | 0.51     | 0.50               | 0.51            | 0.50               |
        | Random Forest      | 0.56     | 0.55               | 0.56            | 0.55               |


**Repository Structure:**
* **data:** Contains raw and preprocessed datasets
* **documentation:** Contains weekly updates for the portfolio
* **notebooks:** Notebooks for EDA, Pre-processing, Clustering, and Modeling
* **README.md:** Memo

## Using GIT
#### 1- CREATING A NEW BRANCH
```git branch``` - to check in which branch you are (you should be in the MAIN branch before making a new branch)

```git status``` - to check the status aka the updates - it should be no updates before making the new branch - recheck after git pull

```git pull``` - to get latest stuff from the main branch

g```it checkout -B feature/name``` - to create a feature branch for yourself 

#### 2-NOW, WRITE YOUR CODE

#### 3 - PUSH TO YOUR BRANCH
```git branch``` - MUST SHOW THAT YOU ARE IN THE BRANCH YOU MADE AND ARE EDITING

Go to SOURCE CONTROL IN VSCode and stage changes(ONLY CLICK THE PLUS to stage your files, nothing else)

```git commit -m "This is just to test git. Added a comment. "``` - to commit, add good comments 

```git push -u origin feature/name``` - To push your changes 

```git checkout main``` - to go to the main branch

#### 4 - CREATE PULL REQUEST
Go to GitHub, click on the CREATE PULL REQUEST on top of the repository

Write the description well

Click on the "Create Pull Request" button

#### 5 - CHECK THE LIST OF PULL REQUESTS AND MERGE (FOR CODE REVIEWER)

Make the file look like how you would want it to look like in the end
