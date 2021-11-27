# MechaCar_Statistical_Analysis
## Overview of the project
The purpose of this analysis is to offer insights on the MechaCar's production to help the manufacturing team. In order to conduct this analysis, we use two datsets containing information related to the miles per gallon and the suspension coils of the MechaCar. 
### Results
## Linear Regression to Predict MPG
![image](https://github.com/YutaiLee/MechaCar_Statistical_Analysis/blob/main/images/mpg_line_regres_summary.png)
* The vehicle length and the vehicle ground clearance may statistically provide a non-random amount of variance for the model. In other words, on the MechaCar prototype, vehicle length and vehicle ground clearance have a significant impact on miles per gallon. Conversely, the p-values of vehicle weight, spoiler angle, and all-wheel drive (AWD) represent the amount of random deviation from the data set.
* The p-Value is 5.35e-11. The p-Value for this model is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further indcates that the slope of this linear model is not zero.
* The main indicator of whether the linear model predicts the mpg of the MechaCar is the r-squared value. In this case, it is at 0.7149 mean that out of 100 instances, this model would approximately predict the mpg of the MechaCar correctly 71 times. This means that the model would be considered effective.
## Summary Statistics on Suspension Coils
### Total Summary Table
![image](https://github.com/YutaiLee/MechaCar_Statistical_Analysis/blob/main/images/Total_Summary.png)
### Lot Summary Table
![image](https://github.com/YutaiLee/MechaCar_Statistical_Analysis/blob/main/images/lot_summary.png)
First the Suspicion Coil csv was converted into a dataframe and then created two subset tables with it: Total Summary and Lot Summary. The Total Summary table is looking at PSI statistics across all lots while the Lot Summary shows statistcs of each lot. As seen, Lot 1 and 2, are very similar while Lot 3 has a smaller mean with a bigger variance and standar deviation.
## T-Tests on Suspension Coils
The P-values from single T-Test on PSI values (compared to the standard of 1500 PSI) for suspicion coils were:

All PSI= 0.06028 Lot 1 PSI= 1 Lot 2 PSI= 0.6072 Lot 3 PSI= 0.04168 Assuming that the significant value should be below p = 0.05 (which is standard), then only Lot 3 is significantly different. All other lots perform the same (or are not significantly different) to the standard 1500 PSI. This, combined with the lower mean of Lot 3 and high variance, could indicate that Lot 3 is under-performing.
![image](https://github.com/YutaiLee/MechaCar_Statistical_Analysis/blob/main/images/T-test.png)
![image](https://github.com/YutaiLee/MechaCar_Statistical_Analysis/blob/main/images/T-test_Lot1.png)
![image](https://github.com/YutaiLee/MechaCar_Statistical_Analysis/blob/main/images/T-test_Lot2.png)
![image](https://github.com/YutaiLee/MechaCar_Statistical_Analysis/blob/main/images/T-test_Lot3.png)

## Study Design: MechaCar vs Competition
1. The metric I want to test is the fuel efficiency of cities and highways.
2. The null hypothesis is that all cars of the same class have the same fuel efficiency. The alternative hypothesis is that all cars of the same class have the different fuel efficiency.
3. I will use the analysis of variance test to complete the analysis of these two fuel efficiency.
4. I need fuel efficiency data from 100 individual cars to create a sample size of data for each car in the class type. For example, if there was 10 cars in the class type, I have a top of 1000 data points collected for each fuel efficiency type.
