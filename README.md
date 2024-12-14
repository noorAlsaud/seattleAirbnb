# Airbnb Seattle Analysis

## Project Overview
This project analyzes Airbnb listings in Seattle to answer specific questions about availability, pricing, and bookings. Using data from the Airbnb Seattle dataset, we provide insights that can help Airbnb hosts, travelers, and businesses make informed decisions.

---

## Questions of Interest

1. **Which seasons of the year have the highest room availability, and which season is the busiest?**

2. **What factors influence the price of listings in Seattle?**
   - This question explores how features like accommodates, bedrooms, bathrooms, host response time, and superhost status affect listing prices.

3. **What factors influence a guest's decision to book a listing?**
   - This question analyzes how factors like price, accommodates, bedrooms, bathrooms, superhost status, and having a profile picture impact booking rates.

---

## Libraries Used
- **pandas**
- **numpy**
- **matplotlib**
- **seaborn**

---

## Files in the Repository
- **`airbnb_seattle.ipynb`**: The Jupyter Notebook containing the code for data cleaning, analysis, and visualization.
- **`listings.csv`**: The cleaned dataset of Airbnb listings in Seattle.
- **`calendar.csv`**: The cleaned dataset showing daily availability and prices for listings.
- **`reviews.csv`**: The cleaned dataset of customer reviews for listings.
- **`README.md`**: This file explains the project purpose, questions, and results.

---

## Summary of Results
1. **Seasonal Trends**: Availability is highest in fall, while the busiest season is winter.
![seasons_airbnb](https://github.com/user-attachments/assets/c1465315-766f-4f90-b607-22c8f9004424)

2. **Pricing Factors**: The most significant factors influencing prices include accommodates, bedrooms, and response time.
![pricingFactor](https://github.com/user-attachments/assets/54a42481-ad37-4c6e-95c9-badaf1476a48)

3. **Booking Influences**: Price, accommodates, and the number of bedrooms strongly affect a guest's decision to book. Surprisingly, listings without a host profile picture have a higher booking rate.
![ListingsFactor](https://github.com/user-attachments/assets/9c46ed95-02a6-467a-8be2-9d14673cd552)

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

## Acknowledgments
- **Dataset**: Provided by [Kaggle](https://www.kaggle.com/datasets/airbnb/seattle).
- **Framework**: This project follows the CRISP-DM framework to ensure a structured analysis.

---

## Contact
For any questions or feedback, feel free to reach out via GitHub.

