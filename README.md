# Airbnb Seattle Analysis

## Project Overview
This project analyzes Airbnb listings in Seattle to uncover insights that can guide business strategies and enhance customer experiences. Using the CRISP-DM process, we structured the project into well-defined stages to answer three main questions:
1. **Which seasons have the highest room availability, and which season is the busiest?**
2. **What factors influence the price of listings in Seattle?**
3. **What factors influence a guest's decision to book a listing?**

The analysis combines descriptive and inferential statistics with visualization techniques to deliver actionable insights.

---

## CRISP-DM Process

### 1. Business Understanding
The goal of this project is to explore patterns in Seattle's Airbnb listings to help hosts optimize pricing, availability, and booking rates. Specifically, we aim to:
- Identify seasonal trends in room availability.
- Understand the factors that drive pricing decisions for listings.
- Determine what influences guest booking decisions.

### 2. Data Understanding
We used the [Airbnb Seattle Dataset](https://www.kaggle.com/datasets/airbnb/seattle) from Kaggle, which contains the following datasets:
- **Listings:** Detailed information about Airbnb properties in Seattle.
- **Calendar:** Availability and pricing information for each property.
- **Reviews:** Customer reviews for properties.

#### Key Steps:
1. **Exploration:**
   - Analyzed the structure and key columns of each dataset (`.info()`, `.describe()`).
   - Plotted distributions and checked for outliers in important columns like `price` and `availability`.

2. **Insights:**
   - Identified missing values in key columns such as `price`, `reviews_per_month`, and `host_is_superhost`.
   - Noted duplicate rows, which were removed to maintain data integrity.

3. **Data Cleaning:**
   - Missing `price` values in the calendar dataset were filled using the `price` column from the listings dataset.
   - Columns irrelevant to the analysis were dropped for simplicity.

---

### 3. Data Preparation
The datasets were cleaned and preprocessed to ensure accuracy and consistency:
- **Handling Missing Values:**
  - Missing `price` values were imputed with median values from the listings dataset.
  - Columns such as `host_is_superhost` and `host_has_profile_pic` were filled using logical assumptions or default values (e.g., `True`/`False`).
  - Columns with over 95% missing data, like `square_feet`, were dropped.
- **Removing Duplicates:**
  - Ensured that all rows were unique for accurate analysis.
- **Transformations:**
  - Converted `t`/`f` values into `True`/`False` for better usability.
  - Simplified continuous variables (e.g., grouped `bathrooms` into categories).

#### Advantages and Disadvantages of Methods:
- **Imputation:**
  - **Advantage:** Prevents loss of data due to missing values.
  - **Disadvantage:** Can introduce bias if imputed values don’t reflect the true distribution.
- **Dropping Columns:**
  - **Advantage:** Simplifies the dataset and reduces noise.
  - **Disadvantage:** May remove minor but potentially relevant information.

---

### 4. Modeling (Optional)
This project did not involve machine learning models, as the questions could be answered using descriptive and inferential statistics. The insights were derived by:
- Correlation analysis to identify factors influencing `price` and `booking rate`.
- Aggregation and grouping to uncover seasonal and categorical trends.

---

### 5. Evaluation
The following insights were derived:

#### **Seasonal Availability**
- **Winter** is the busiest season, with the highest booking rates across properties.
- **Fall** has the most room availability, indicating lower demand compared to other seasons.

![seasons](https://github.com/user-attachments/assets/d9088664-8638-4b4c-9980-665cbd0ecf28)

#### **Pricing Factors**
- **Bedrooms, Bathrooms, and Accommodates**:
  - Larger properties with more bedrooms, bathrooms, and higher accommodates tend to have higher prices.
    
 ![price_accommodates](https://github.com/user-attachments/assets/3dcb55e4-5945-42ba-8983-c6aa5a4c5d00)

- **Superhost Status**:
  - Listings hosted by superhosts command higher prices on average.
- **Profile Picture**:
  - Hosts with profile pictures tend to list properties at higher prices.

#### **Guest Booking Preferences**
- Guests prefer:
  - Listings with lower prices.
  - Hosts who are superhosts.
  - Listings with profile pictures.
    
![listings_by_price](https://github.com/user-attachments/assets/0703a543-9d76-416b-a1c1-aa99a7deb10b)

---

### 6. Deployment
The deliverables for this project include:
1. **Jupyter Notebook:** A complete analysis with visualizations, code, and comments following the CRISP-DM structure.
2. **Blog Post:** A non-technical summary of the findings for a general audience.
3. **GitHub Repository:** Hosts the notebook, README file, and dataset details.

---

## Results Summary
- **Seasonality:** Winter is the busiest season, with the highest booking rates, while Fall has the most available rooms.

- **Price Influencers:** Larger properties (more bedrooms and bathrooms) and superhosts command higher prices.
- **Guest Preferences:** Profile pictures, lower prices, and superhost status strongly influence booking decisions.

---

## How to Run the Code
1. **Clone the repository** to your local machine:
   ```bash
   git clone https://github.com/noorAlsaud/seattleAirbnb.git
   ```
2. **Install required Python libraries** using `pip`:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. **Open the Jupyter Notebook**:
   - Run `airbnb_seattle.ipynb` step by step.

---

## Tools Used
- **Programming Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
- **Data Source:** [Kaggle Airbnb Seattle Dataset](https://www.kaggle.com/datasets/airbnb/seattle)

---

## Acknowledgments
- **Airbnb Seattle Dataset** provided by [Kaggle](https://www.kaggle.com/).
- Guidance and support from the Udacity Data Science Nanodegree program.

