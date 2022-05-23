# MechaCar_Statistical_Analysis

## Overview
An analysis using R of a vehicle prototype'd production data to determine areas for improvement. Several areas were the focus of testing, and I have highlighted them below:

## Linear Regression to Predict MPG
![Linear_Regression_Mechacar](https://github.com/Tbrecke01/MechaCar_Statistical_Analysis/blob/main/images/linear_regression_mechacar.png)

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? A confidence level of 95% is being used.
- MPG, Vehicle Length, and ground clearence all had a statistically significant, non-random amount of variance
- Vehicle Weight and Spoiler angle all had a not statistically significant levels of variation

2. Is the slope of the linear model considered to be zero? Why or why not?
- Given the above coefficients, and the linear regression formula for mpg = -0.01 + 6.267 (vehicle length) + 0.001 (vehicle weight) + 0.069 (spoiler angle) + 3.546 (ground clearance) - 3.411 (AWD) results in a non-zero slope of ~6.5.

3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
- The R squared value is 71%, which suggests that this model is a good predictor of mpg values 71% of the time. There are likely other variables not included in the dataset that contribute to the mpg variance.

## Summary Statistics on Suspension Coils
![Total_Summary](https://github.com/Tbrecke01/MechaCar_Statistical_Analysis/blob/main/images/total_summary.png)
![Lot_Summary](https://github.com/Tbrecke01/MechaCar_Statistical_Analysis/blob/main/images/Lot_summary.png)

1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
- Variance for the total lots is 62, which is within expectations being below 100psi. However, when reviewing lot data individually we can see that lot 3 has a vastly oversized variance of 170, far exceeding the design variance of 100psi, which is massively inflating the total lot variance. By contrast, lot 2 and 3 only have a variance of 0.98 and 7.5 respectively.

## T-Tests on Suspension Coils
![All_Lots_Ttest](https://github.com/Tbrecke01/MechaCar_Statistical_Analysis/blob/main/images/All_lots_ttest.png)

- the p value for all lots was 0.0602 > 0.05 meaning the total lots are not statistically significant and fall within normal distribution.
<insert lot 1 ttest>
- The p value for Lot 1 is 1 > 0.05, meaning Lot 1 was not statistically significant.
<insert lot 2 ttest>
- The p value for Lot 2 is 0.607 > 0.05 which means Lot 2 was not statistically significant.
<insert lot 3 ttest>
- The p value for Lot 3 was 0.042 < 0.05 which means that it is statistically significant and falls outside of normal distribution. However the mean falls within the 95% confidence interval.
- Distribution for Lots 1 and 2 fall within expected levels and there is not enough data available to reject the null hypothesis as the two means are statistically similar.

## Study Design: MechaCar vs Competition
- When comparing MechaCar to its competitors, there are several other variables that are important and should be taken into account. Some of these include: cost, safety rating, and highway vs city fuel efficiency. Using 'safety rating' as an test example, we can use a null hypothesis of "MechaCar's safety rating is 4 stars or greater". We would test this using multiple linear regression statistical analysis to show how the amalgamation of variables effects MechCar's safety rating vs their competition. A random sample of n > 30 for MechaCar and their competitors of all variables related to the safety score (such as crash score, air bag rating, car frame tensile strength, etc.) would need to be gathered, compared, and used to calculate separate safety scores and their significance. 
