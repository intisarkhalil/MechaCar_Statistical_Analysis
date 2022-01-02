# MechaCar_Statistical_Analysis

  - Statistical analysis using R.
  - AutosRUs’ newest prototype, the MechaCar performance.

## Overview
The data analytics team of the  AutosRUs is in charge of performing a retrospective analysis of historical data, analytical verification, and validation of current automotive specifications, and study design of future product testing. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress.
The purpose of this project it to perform analytical review to provide some insights to:
-	Identify which variables in the dataset predict the mpg of MechaCar prototypes.
-	Provide statistical summary on the PSI of suspension coils
-	Identify if manufacturing lots are statistically different from the mean population.
-	Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

## The results:
### Linear Regression to Predict MPG
1.	Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
The veraiables ``` ground_clearance``` and ````vehicle_length```` are show highly statistical signifficant effect on the mpg in the dataset; the p-value for ground_Clearance is (5.21e-08) and for the variable vehicle length is (2.60e-12)

![image](https://user-images.githubusercontent.com/62036983/147868503-2f75bbb3-0b38-4bba-b7b2-96bd43564a4c.png)

2. Is the slope of the linear model considered to be zero? Why or why not?
The slope of the model cannot considered to be zero, because the p-value is less than 0.05.

![image](https://user-images.githubusercontent.com/62036983/147868643-bc1e339f-8677-4854-bb08-aa40b56214e5.png)

3.	Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
The R-squared value is ```0.71```, which indicates that the model will  roughly predict the mpg values correctly.There may be other factors that will contribute to the mpg variability of the MechaCar prototypes.

![image](https://user-images.githubusercontent.com/62036983/147868651-41223c00-ce52-47ab-b699-77948b3c3cbc.png)

### Summary Statistics on Suspension Coils,
The Total Summary data above, indicates that the variance is under 100 psi and meets specifications, there is a problem with one of the individual lots. As shown in the Lot Summary, the variance for Lot 3 is well over the acceptable threshold, at 170.28.

![image](https://user-images.githubusercontent.com/62036983/147868755-832ff7a8-797d-4929-8252-5fa96f3ba612.png)

![image](https://user-images.githubusercontent.com/62036983/147868735-3770b942-5bfa-4eb3-8904-1a80e1be8160.png)

### T-Tests on Suspension Coils
The results of the T-test for the suspension coils across all manufacturing lots shows that they are not statistically different from the population mean, and the p-value is (0.06028) which indicates that we have not enouph evedence to reject the null hypothesis. 

![f](https://user-images.githubusercontent.com/62036983/147868798-a641cf4d-3fe3-4b28-aac1-032dc9f1316d.png)

## Lot1:
The results of the T-test for the suspension coils for Lot1 shows that they are not statistically different from the population mean, and the p-value is (1.00) which indicates that we have not enouph evedence to reject the null hypothesis.
## Lot2:
The results of the T-test for the suspension coils for Lot2 shows that they are not statistically different from the population mean, and the p-value is (0.6072) which indicates that we have not enouph evedence to reject the null hypothesis.
## Lot3:
The results of the T-test for the suspension coils for Lot3 shows that there are a statistical different from the population mean, and the p-value is (0.0416) which indicates that we have enouph evedence to reject the null hypothesis and accept the alternative hypothesis.

![image](https://user-images.githubusercontent.com/62036983/147868829-11efa3d4-f8bd-463a-8c75-23523cdf724d.png)

### Study Design: MechaCar vs Competition:
In odrder to establish a place for comarison we must provide information about customers' choices and preferences for the quality of the car. If, for example, the information indicates that customers prefer in the first place the vehicle length. In this case, we will construct a comparative study as follows:
  - First, we define the metrics and statistics required to complete the comparison. We will use the t-test in this case to compare the mean of vehicle length of MechaCar (mu1) with other type of car say X (mu2). 
  - Second, we define the null hypothesis and the alternative hypothesis as follows:
  
  ```
          Ho: mu1 equal mu2  
          Ha: mu1 not equal mu2
  ```
  - Third, we conduct the statistical study and apply the statistical tool to the data.
  - Fourth, we use two-tail test  of significant to show is there sufficient evidence to reject the null hypothesis?
 - Finally we formulate the conclusion based on the test results and recide whether MechaCare are better than other cars in the cometition market. 
It can also be use ANOVA, if we need to compare more than two means. 
