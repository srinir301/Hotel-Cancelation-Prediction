# Hotel-Cancelation-Prediction
### By: Srinivasan Ramakrishnan

![Hotel-Booking-1280x720](https://user-images.githubusercontent.com/122238220/224576688-a2c6e38c-1c4d-49c4-835b-a06bd464e0ab.jpg)

## Business Understanding
The issue of cancelations for hotel reservations is that it leads to financial losses because there will be open rooms that are not being utilized which can take away the opportunity of increased revenues. This is why Marriott needs a classification model to predict whether a customer will cancel their reservation or not.

![slide 1](https://user-images.githubusercontent.com/122238220/224576718-783f63fe-53de-4bac-833d-569778dd2b7d.jpg)

## Data Understanding
I got my data from Kaggle that is not based on a specific company and it has 36,275 rows with 19 columns including type of meal plan, market segment, if a car parking space is required, and number of adults.

![slide 2](https://user-images.githubusercontent.com/122238220/224576960-5ed7a16e-2e24-4d79-bdb5-145fa26263cb.jpg)

## Data Preparation
From the data there were no missing/null values, but the target variable (booking status) had unbalanced binary values which I fixed using SMOTE. SMOTE samples on extra values to the dataset to make the target variable values balanced. It seems like having a car parking spot paid for causes probability of the a customer cancelling their reservation less likely.

![slide 3](https://user-images.githubusercontent.com/122238220/224577242-bb555a27-b7ad-4217-840f-1f380bb04d30.jpg)

## Modeling
I started out with a basic logistic regression with no hyperparameter tuning which gave a me good precision, but I found a better precision score. I am using precision to choose my model because I want the best predictor of the reservation being not cancelled. If a reservation was predicted as not canceled, but it was actually canceled then that would not increase the profitability of Marriott. I then ran a more complex model, random forest classifier, which creates a group of uncorrelated decision trees to create a more accurate prediction compared to a single decision tree.

![slide 4](https://user-images.githubusercontent.com/122238220/224577259-3a9701e3-f221-47e0-a65a-2e2c7dc43b4e.jpg)

## Evaluation
For my final model I decided to go with the knieghbors classifier because it gives me the best precision score. Out of 4,367 values 3,997 values were correctly predicted as not canceled, but 370 values were actually canceled. This model is not the best for other scores, but it is the best model I got so far for precision which is the most important for the Marriott. The two most important values for the booking status is car parking space requirement and corporate employees.

![slide 5](https://user-images.githubusercontent.com/122238220/224577269-ff7cc02d-0478-4167-b82d-b97b9b17f37d.jpg)

## Recommendations
I recommend that Marriott offer discounts for their car parking spaces to increase the likelihood that the customer will not cancel their reservations. Next, Marriott does not have to worry about corporate employees cancelling as corporate employees usually book their hotel close to their check in date. Lastly, the longer the time between a customer booking their reservation and checking in there is a higher chance the customer will cancel their reservation.

![slide 6](https://user-images.githubusercontent.com/122238220/224577291-2fb22a83-e8f2-4a1c-bd89-82151d92ec76.jpg)

## Next Steps
I want to take out the features that are not the most important and make that into a model see how the precision score changes. Next, I want to look into the data further and look at other models to find better results.

![slide 7](https://user-images.githubusercontent.com/122238220/224577304-92d081b5-029d-4ca6-ba2a-dcae39cc4600.jpg)
