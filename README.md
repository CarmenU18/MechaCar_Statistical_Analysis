# MechaCar_Statistical_Analysis

## Overview

AutosRUs' new prototype, the MechaCar, is experiencing production issues that are blocking the manufacturing team's progress. AutosRUs' senior management has asked to review production data to obtain information that can help the manufacturing team.

## Linear Regression to Predict MPG

As a first step, a multiple linear regression was performed in order to identify the effect of the variables vehicle length, vehicle weight, spoiler angle, ground clearance, drive train (AWD) on vehicle performance (MPG):

![img](https://github.com/CarmenU18/MechaCar_Statistical_Analysis/blob/main/Resources/Linear_regression.PNG)

Subsequently, the p-value and r-squared were determined, with which we can conclude:

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

    The variables vehicle_length and ground_clearance present a statistically non-significant Pr(>|t|) value, as they are less than the expected ~0.05.
    The intercept was also statistically significant, indicating that there are likely other factors, not included in our dataset, that have a strong impact on the MPG.

- Is the slope of the linear model considered to be zero? Why or why not?

    The slope of the linear model cannot be considered zero, since the p-value of 5.35e-11.

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

    The R-squared value is 0.7149 which indicates that the model is 71% explained, although the non-statistically significant variables (Vehicle Length and the Ground Clearance) indicate that there are still factors that are not being considered within the model.

![img](https://github.com/CarmenU18/MechaCar_Statistical_Analysis/blob/main/Resources/Summary_lm.PNG)


## Summary Statistics on Suspension Coils

- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

    Overall for the data set the design specifications are met, this is proven by the variance value of 62.29356 < 100 PSI.

    ![img](https://github.com/CarmenU18/MechaCar_Statistical_Analysis/blob/main/Resources/total_summary.PNG)

    However, when the individual lots are reviewed, Lot 3 is found to be above the acceptable threshold (100 PSI) with a value of 170.28.Therefore, coils from Batch 3 are not acceptable at all. These coils should be rejected and not be used in the MechaCar as they do not meet the design specifications. 

    ![img](https://github.com/CarmenU18/MechaCar_Statistical_Analysis/blob/main/Resources/Lot_summary.PNG)

## T-Tests on Suspension Coils

We need to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.

![img](https://github.com/CarmenU18/MechaCar_Statistical_Analysis/blob/main/Resources/One%20Sample%20t-test.PNG)

The overall t-test has a mean of 1498.78 PSI a value less than the mean of 1500 PSI. 
The p-value is 0.06, slightly above the desired significance level of 0.05, but we still do not reject the null hypothesis.

![img](https://github.com/CarmenU18/MechaCar_Statistical_Analysis/blob/main/Resources/One%20Sample%20t-test_Lot1.PNG)

The T-test for Lot1 has a mean of 1500 (ideal mean) and a p-value of 1, the null hypothesis is accepted:
H0 : The mean of the sample is equal to the mean of the population (1500 PSI)

![img](https://github.com/CarmenU18/MechaCar_Statistical_Analysis/blob/main/Resources/One%20Sample%20t-test_Lot2.PNG)

A review of the results of the T-test for Lot2 shows that they are not statistically different from the population mean, and the p-value is not low enough (0.6072) for us to reject the null hypothesis.

![img](https://github.com/CarmenU18/MechaCar_Statistical_Analysis/blob/main/Resources/One%20Sample%20t-test_Lot3.PNG)

T-test for Lot3 shows that they are slightly different from the population mean, and the p-value is less (0.0417) than the expected value of 0.05 so the null hypothesis is rejected.

## Study Design: MechaCar vs Competition

There are many factors that consumers take into consideration when evaluating a car to purchase, for example: cost, city fuel efficiency, maintenance cost, interior comfort and additional add-ons.

If you want to compete in the market, all these factors must be considered in order to gain ground in such a complicated market as the sale of cars.

As a first step it is necessary to define the type of variables to work with. Depending on the type of data treated as metrics, different types of tests will have to be used to analyze different data sets.

For example, a one-sample t-test is ideal for analyzing cost, city fuel efficiency and maintenance cost:

- T-Cost Test : Cost of MechaCar vs cost of competition
    Ho : MechaCar's average cost = average cost of competition
    Ha : MechaCar's average cost is different from that of its competitors

In general, the hypothesis would be:
    Ho = MechaCar's cars have an average capacity to that of its competitors
    Ha = MechaCar's cars have a different capacity than its competitors.

In order to test our hypotheses it would be necessary to have both MechaCar and competitor performance data over a specified period of time.
