# Will the Customer Accept the Coupon?

## Problem Statement
This project is to determine if a driver is likely to accept coupons from restaurants. The data for the project is based on a survey that describes different driving scenarios including destination, weather, passenger, and whether the people will accept the coupon if they are the driver. You can find a link to my Jupyter notebook detailing my work here.

## Data Available

### User Attributes
- **Gender**: male, female
- **Age**: below 21, 21 to 25, 26 to 30, etc.
- **Marital Status**: single, married partner, unmarried partner, or widowed
- **Number of children**: 0, 1, or more than 1
- **Education**: high school, bachelors degree, associates degree, or graduate degree
- **Occupation**: architecture & engineering, business & financial, etc.
- **Annual income**: less than $12500, $12500 - $24999, $25000 - $37499, etc.
- **Number of times that he/she goes to a bar**: 0, less than 1, 1 to 3, 4 to 8, or greater than 8
- **Number of times that he/she buys takeaway food**: 0, less than 1, 1 to 3, 4 to 8, or greater than 8
- **Number of times that he/she goes to a coffee house**: 0, less than 1, 1 to 3, 4 to 8, or greater than 8
- **Number of times that he/she eats at a restaurant with average expense less than $20 per person**: 0, less than 1, 1 to 3, 4 to 8, or greater than 8
- **Number of times that he/she goes to a bar**: 0, less than 1, 1 to 3, 4 to 8, or greater than 8

### Contextual Attributes
- **Driving destination**: home, work, or no urgent destination
- **Location of user, coupon, and destination**: We provide a map to show the geographical location of the user, destination, and the venue, and we mark the distance between each two places with time of driving. The user can see whether the venue is in the same direction as the destination.
- **Weather**: sunny, rainy, or snowy
- **Temperature**: 30F, 55F, or 80F
- **Time**: 10AM, 2PM, or 6PM
- **Passenger**: alone, partner, kid(s), or friend(s)

### Coupon Attributes
- **Time before it expires**: 2 hours or one day

### Data Exploration and Preparation
Data exploration consisted of 
- Investigating dataset for missing
- Checking for duplicates
- Checking for constant value columns
- Checking for correct data types such has integer for Age

Data Preparation consisted of
- Dropping irrelevant columns such as car
- Filling missing data columns
- Replace the age column with values and change the column to a integer type

## Data Analysis and Findings
![Alt text](../images/CouponAcceptanceByType.png?raw=true "Title")

The graph presents the count of accepted and not accepted coupons across different coupon types. Here are the key insights:
- Coffee House coupons have the highest acceptance rate, with nearly equal counts of accepted and not accepted coupons.
- Restaurant (<$20) coupons show a significant disparity while a large number are accepted, a notable portion is not.
- Carry Out & Take Away coupons have a high acceptance rate compared to their rejection count.
- Bar coupons show a lower acceptance rate, with more not accepted coupons.
- Restaurant ($20-$50) coupons have relatively low acceptance and rejection rates compared to other categories.

Overall, coupons for coffee houses and lower-cost restaurants are more frequently used, whereas those for bars and higher-cost restaurants see lower acceptance rates.

![Alt text](../images/CouponUsageTimeOfDay.png?raw=true "Title")
![Alt text](../images/CouponUsageAge.png?raw=true "Title")

Above graphs show that 
- Most coupons were used at 6 PM, followed by 7 AM and 10 AM.
- The age group that used coupons the most was 21-year-olds, followed by 26-year-olds and 31-year-olds.
- By Time and Age Group:
-- 6 PM is the peak time across all age groups, with 21-year-olds using the most coupons (413 times).
-- 7 AM and 10 AM also show high usage, especially for 21 to 31-year-olds.
-- Older age groups (50+) use coupons most at 6 PM (240 uses), followed by 7 AM (214 uses).
-- Younger age groups (below 21) have lower overall usage but peak at 6 PM and 7 AM.


![Alt text](../images/CarryOutAgeWeatherMaritalStatusFacetGrid.png?raw=true "Title")
The above heatmap visualizes the frequency of "Carry Out" behavior segmented by age, weather conditions, and marital status. Here are some key observations:

- Higher Activity in Sunny Weather:
-- The highest frequencies are observed under sunny conditions, particularly for single individuals and married partners.
-- Young adults (ages 21-31) exhibit the most carry-out activity.

- Lower Activity in Rainy & Snowy Weather:
-- The frequency is significantly lower under rainy and snowy conditions, regardless of marital status.
-- However, younger age groups (21-26) still show some activity in these conditions.

- Age-Related Trends:
-- Younger individuals (21-31) are the most frequent users of carry-out services.
-- Older individuals (41 and above) show lower overall participation, with some notable engagement under sunny conditions.

- Marital Status Influence:
-- Singles and married partners seem to order carry-out more frequently than divorced or widowed individuals.
-- The most notable high-frequency category appears under "Sunny-Single (age 21-26)", suggesting that young singles are the most active users.

![Alt text](../images/BarGoersAgeDistribution.png?raw=true "Title")
- Bars are be more frequented by younger individuals who are single or in unmarried partnerships.
- The decision to accept a coupon doesn't seem to be strongly correlated with age for married or divorced bar-goers.
- The sample size for widowed bar-goers is too small to make any meaningful inferences about their age or coupon acceptance.

## Recommendation based on above Findings
-- Coupon ads and delivery could be targeted to Young adults perhaps in 4-5 window as 6.00 pm seems to be highest usage.
-- Given Coffee goers seem to use the coupons most, perhaps target that audience
-- Carry out coupons could be targeted towards Singles and married partners.

## Link to Jupyter file
https://github.com/lakshmivelandai/Will-The-Customer-Accept-The-Coupon-AIML-Module5.1/blob/main/Will-Customer-Accept-Coupon.ipynb
