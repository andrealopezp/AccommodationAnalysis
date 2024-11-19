# 🏡 🛌 Project Background
Airbnb operates as an online intermediary by connecting property owners who want to rent their places with those looking for accommodation. These accommodations can be very diverse, from rooms to entire apartments, and can be booked for short-term rentals. Guests can check out these properties, compare prices, read reviews and book them. All with just one click through the website or the application.

The company has substantial data on its accommodations details, location information, pricing, host profiles, availability, and guest reviews that have been underutilized. This project analyzes Airbnb's accommodations in Seville from January to June 2024 and synthesizes this data in order to uncover critical insights that will improve Airbnb's financial success. I am collaborating with the Head of Product and the Marketing team to leverage this data and develop actionable insights that will optimize pricing strategies, enhance guest experience, and ultimately drive revenue growth in the Seville market.

**Key Business Metrics**:
* **Total Listings**: Number of active listings in a specified area.
* **Occupancy Rate**: Percentage of days that properties are rented versus days that are available.
* **Average Daily Rate (ADR)**: Average price per night among all available listings.
* **Revenue Estimation**: Projected earnings for hosts determined by occupancy rate and daily price.
* **Market Share**: Proportion of total listings revenues captured by Airbnb compared to hotels.

**Insights and Recommendations** are provided on the following key areas:
* **Neighborhoods Performance:** Evaluation of historical listings volume across neighborhoods, assessing customer behaviour and revenue improvements.
* **Rental Preferences:** An analysis of room type trends in all neighborhoods, focusing on listings volume and consumer choices.
* **Price Distribution by Segment:** An evaluation of average daily rates and occupancy rates in Seville with emphasis in pricing strategies and market dynamics.
* **Occupancy and Demand Variation:** A review of occupancy rates and listing volume that shows patterns in both availability and demand.
* **Regulation:** An analysis of listing counts by license types.
* **Reviews and Reputation:** Examination of monthly reviews concentrating in the volume of listings, accentuating consumer preferences and satisfaction.

The Python queries used to inspect and clean the data for this analysis can be found [here.](https://github.com/andrealopezp/AccommodationAnalysis/blob/main/EDA_accommodation.ipynb)

An interactive Tableau dashboard used to report and explore sales trends can be found [here.](https://public.tableau.com/app/profile/andrealopezp/viz/SevilleVacationRentalsInteractiveAirbnbMarketDashboard/Dashboard)



# ⛩️ Data Structure & Initial Checks

The company main database structure as seen below consists of one table called "listings.csv", with a total row count of 7,885 records.\
The dataset contains information about advertisements for accommodations.

![Data Structure](/Images/DataStructure.png)



# 💼 Executive Summary

### Overview of Findings
The analysis included three crucial takeaways: first, entire accommodations attract the most guests. Particularly in high-demand neighborhoods. Second, neighborhoods adjacent to popular areas like *Casco Antiguo* help achieve occupancy rates. Which suggests that property owners in near premium areas are capturing the overflow demand. Additionally, low-demand neighborhoods struggle appealing visitors, therefore there is a disconnection between prices and market enchantment. The following sections will explore additional contributing factors and highlight key opportunity areas for improvement.

Below is the overview page from the Tableau dashboard and more examples are included throughout the report. It can be found [here.](https://public.tableau.com/app/profile/andrealopezp/viz/SevilleVacationRentalsInteractiveAirbnbMarketDashboard/Dashboard)

![Dashboard](/Images/Dashboard.png)



# 🚀 Insights and Recommendations
An analysis has been carried out on the accommodations available in Seville between January and June 2024 and useful observations have been extracted for making strategic decisions by the owners of said properties. Below we list the ideas:

- **1. Neighborhoods with the Best Performance:**
    - The neighborhood called *Casco Antiguo* has the largest number of properties in the city. Specifically, the *Alfalfa* sub-neighborhood has the most. Therefore, it can be considered the most popular area among visitors.
    - We suggest increasing the focus on this area that has expansion potential in surrounding neighborhoods to maximize on the high demand. Additionally, marketing efforts could highlight the historic charm of the downtown.
    - This would mean that properties here could increase prices due to their location, leading to higher returns.
- **2. Rental Preferences:**
    - In Seville, visitors largely opt for entire homes (which represent approximately 81% of the listings).
    - Taking these facts into account, property owners who are interested in investing should prioritize the offer of complete apartments over other types of spaces. In addition, property descriptions highlight those that have privacy and comfort to satisfy tourists' preferences.
    - We also recommend to evaluate the potential for optimizing pricing strategies for private rooms to increase their attractiveness and enhance occupancy rates. For instance, offering discounts for longer stays.
    - Occupancy and customer satisfaction could increase if marketing and investment strategies are in line with demand patterns.
- **3. Price Distribution by Segment:**
    - During this period, the average price per night is around 75.02€, with a distribution skewed to the right (since most listings have a price between 60€-80€). However, neighborhoods like *Tabladilla* and *El Cano* have higher prices (from 80€ to 119€). In contrast, other neighborhoods such as *Las Letanías* or *Avda. de la Paz* have a price of less than 30€.
    - To optimize prices, it is recommended to apply dynamic pricing strategies. In prime locations, property owners could adjust prices upwards during peak seasons, while in lower-demand areas they could offer discounts or improve the quality of accommodation to attract more visitors.
    - Price optimization increases both occupancy and revenue.
- **4. Occupancy and Demand Variation:**
    - There are neighborhoods like *San Pedro C* and *Polígono Sur* that have high occupancy rates, approaching or exceeding 70%. However, there are other areas like *La Oliva* and *Bami* that show occupancy rates below 25%.
    - In high demand neighborhoods, we recommend increasing prices or conducting a deeper analysis to identify specific amenities or features that appeal to guests in these neighborhoods and, based on the results, adding value through better services. On the other hand, in areas of low demand we recommend improving marketing efforts or focusing on long-term rentals.
    - This would maximize profitability by balancing occupancy and price.
- **5. Regulation:**
    - There are up to 345 listings with "exempt" licenses. That is, a considerable portion of listings may not require traditional licenses.
    - Property owners must stay up to date on regulatory changes and ensure compliance.
    - Ensuring compliance helps avoid legal issues and improves reputation among guests.
- **6. Reviews and Reputation:**
    - There are an average of 80 reviews per property, although some properties receive up to 1,157 reviews.
    - We recommend promoting the collection of guest opinions to generate credibility with potential visitors. Especially for newer properties. Additionally, offering discounts could help.
    - Clear and positive reviews improve the platform's ranking. This leads to greater visibility as well as better occupancy rates.



# 💭 Assumptions and Caveats
Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

* **Missing Values:**
    * **Reviews:** For those entries where there were missing values (last review date and the total number of reviews per month), we assumed that guests did not send any reviews. Therefore, we added a future date (in 2025) and zero respectively. This made it easy to manage information during analysis.

    * **Pricing:** Missing values ​​in the price column could be because these listings were temporarily unavailable (for example, due to renovations or facility upgrades). Either the file contains errors or the data collection is incomplete. It would be necessary to consult and/or verify with the corresponding department to better understand the situation.

    * **Licenses:** Missing values ​​in the license types column could be a result of these hosts not providing the necessary documentation in a timely manner and, therefore, the data collection is incomplete. It would be necessary to consult and/or verify with the corresponding department to better understand the situation.
  
* **Data Representativeness**: The analysis presumes that the properties listed in the Airbnb Seville file between January to June 2024 represent the market during this specific period and are similar to the data from previous and subsequent months. However, we take into account that there may be fluctuation in both supply and demand due to numerous influences such as seasonal trends, local events, economic and legal conditions. All of this could impact the aforementioned findings.

* **Market Dynamics:** It is assumed that preferences for entire homes over other types of spaces represent travelers' priority consumption based on their needs and comforts. Nonetheless, it is recommended to constantly monitor this aspect as customers could change their behavior towards shorter or longer stays, or greater demand for other types of properties like hotels.

* **External Factors:** It is vital to note that influences such as local regulations, economic changes or competitive actions could directly impact prices and, therefore, occupancy rates. Hence, obtaining reviews month after month is key so that the credibility of the property is maintained over time.



# 🛠️ Tech Stack
- **Programming Language**: Python
- **Data Analysis**: Pandas, NumPy, Scikit-Learn
- **Data Visualization**: Matplotlib, Seaborn, Tableau
- **Tools**: Jupyter Notebooks



# 🗂️ Data Source
In this analysis regarding the hosting service of AirBnB in Seville (Spain), data related to the advertisements were obtained from the
[Inside Airbnb - Sevilla.](https://insideairbnb.com/sevilla/)
