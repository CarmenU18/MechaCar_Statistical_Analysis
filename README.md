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
