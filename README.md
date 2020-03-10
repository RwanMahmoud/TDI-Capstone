# TDI-Capstone

This project aims to analyze location data of the available commercial listings in the city of Toronto in order to build a regression model that estimates the value of a certain place. This analysis can be used to determine the best location to start a new retail business.


### Data Ingestion:
1-	Scrapping spacelist.ca to find the available retail listings in Toronto.

2-	Using City of Toronto APl to add neighborhoods features (demographics, urban mobility, safety, etc.)

##### Subway stations (the radius of the circle marker reflects the avg. daily riders)
<img width="407" alt="image" src="https://user-images.githubusercontent.com/52165152/68085572-4d38a300-fe10-11e9-82fb-1fac5cb887a2.png">

##### example of the average crime rates in different neighborhoods 
<img width="399" alt="image" src="https://user-images.githubusercontent.com/52165152/68085590-807b3200-fe10-11e9-9d78-87508d2b6cb8.png">


3-	Using Foursquare API to collect information about the surrouding venues of each listing such as the average rating and number of check-ins

##### example of one listing (red) and the coffee shops (blue) within 500 meters from that listing
<img width="399" alt="image" src="https://user-images.githubusercontent.com/52165152/68085604-a30d4b00-fe10-11e9-87f9-5d5cdc377c97.png">






### Regression Model
The model consists of 26 features. After scaling the features we use Gradient Boosting regressor to train model. The model resulted in R-squared value of 0.35. From the  26 features and by looking to the features importance it appeared that:

•	Number of cafes within 500m

•	The distance to the nearest subway station

•	The space of the listing

Were the top 3 informative features. By studying these features we can have more insights to which kind of features are needed to build a better model.

Different models were also tested: Rdige regressor, Random Forest, Decision Tree and MLP.


