# RYOE-Multiple-Regression
The goal of this project is to analyze the predictability of NFL rushing data by using a multiple linear regression model.

The first step was to import NFL play-by-play data and perform EDA for various independent variables. The boxplot below depicts the distribution of rushing yards by down (1st, 2nd, 3rd, and 4th).

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/97e279f8-f96c-4c32-98ff-216137a3e433)

Next, we grouped average rushing yards by yards to go until endzone. We plotted the line of regression to show that there is a positive correlation of yards to go until endzone vs yards per carry. This makes sense, as defenses are more likely to prepare for the run when teams are closer to the endzone.

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/ea2fcbbc-9abd-43dd-a13d-8d2a8ec61104)

We plotted another boxplot, this time showing rushing yards by run location on the field (left, middle, right). The data shows that there is a wider range of outcomes when the player runs right or left vs running up the middle. This is significant for the sake of our multiple linear regression model.

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/9ad3cc82-6497-4741-861a-74a97e694ea6)

Finally, we plotted one more regression plot, this time showing the distribution of average rushing yards by score differential (negative differential indicates that the rusher's team is losing, and positive differential indicates that the rusher's team is winning). Although the regression line is essentially flat, outside research for other year's shows this to be an anomoly. For the sake of this project, we chose to keep score differential as an independent variable.

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/f85b3561-3942-4c9c-a07a-31caf8e7a5ab)

Next, we fit a multiple linear regression model, using the statsmodels package.

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/a5a013fe-7fad-45f7-9adc-c0518c62b4b1)

We took the residuals of the model, and saved them to a new variable called "RYOE"

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/b134f649-661d-448a-ace7-fd9bd00818ac)

The summary of the model is as follows:

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/52dc6371-9b9f-4dca-9812-ddc25fac0ab7)
![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/67423a3d-a95c-4602-bb0e-883b55959107)

The R-squared score of 0.016 is still not strong, but it is much stronger than that of a linear regression model approach.

Next, we analyzed RYOE by looking at league leaders over the last 7 seasons in RYOE per carry.

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/61ad51a0-c4f4-4d9b-82f3-cf65c7f45a78)

Then, we tested the correlation of year-over-year yards per carry, and we compared that to the correlation of year-over-year RYOE per carry. Here are the results:

![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/94f61c5a-3ad5-4dd1-a09c-c261279bdad8)
![image](https://github.com/jordankristek/RYOE-Multiple-Regression/assets/150874257/8aea9fd4-31c8-4bb7-88ad-ec42c071f0c7)

We conclude that there is a stronger year-over-year correlation of RYOE per carry than there is for regular yards per carry.
