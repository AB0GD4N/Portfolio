German Car Market Analysis

Executive Summary:
German car market is one of the most significant markets in the EU. However, offering clients car alternatives has been a problem, since
clients are looking for variety of features when buying a car. The aim of the project was to reduce the number of variables used for car
comparison, which has been achieved, as the original 6 variables has been reduced to 5 principal compoments, while keeping over 95% of variance
explanation. Moreover, with the new data, car clusters have been created, with car salesman can use to gradually offer more and more distinct 
car alternatives.

Data used:

Data was extracted from https://www.kaggle.com/datasets/yaminh/german-car-insights

Variables which were used: car age, car mileage, fuel consumptionn, fuel type, gearbox type, engine power. Original dataset also include
additional info about cars in form of short describtion and car color.

Data had to been cleaned, as there was a lot of missing values, and some values were put in the wrong columns. After data prep, which also
included transforming data types and normalization of variables, the number of observations decreased from original 100000 to 88000.

Methods used:

Principal Component Analysis - decreased 6 original variables into 5 principal components, while keeping over 95% of variance explanation.

Hierarchical Clustering - clustering has been performed using Ward method. Demo dendrogram has been created from first 20 observations. 
Example car recomendation algorithm: Let's assume our client was first interested in the Alfa Romeo 147, however the car was not available 
or there were some defects, which made the client reject the Alfa Romeo 147. Therefore, the next car that should be showcased to the client 
is Hyundai STARIA. If this car is also rejected, next cars that should be showcased are Hyundai i10 and Citroen Spacetourer. However, 
those cars vary more from the original Alfa Romeo. If this cluster is also rejected, we can move on to Honda CR-V and Ford Fiesta 
cluster, further more expanding the differences between original car and the offered cars.

Key Business Insights:

Dendrogram created on the car list showcases the car most similar to the one sought out by the client. Car salesmen can offer cars from the 
closest cluster, and further move to cars with greater differences from the original one, if the client's needs are still not met.

Final Thoughts:

Original dataset contained 100000 observations of cars listed on the german car market. After removing observations with missing data, 
or removing cars with rare state: such as ethanol fueled cars, we were left with close to 90000 observations. Later after transforming 
the data to numeric format, Principal Component Analysis has been performed, which led to a decrease in number of variables from original 
6 to 5, as the last variable did not contribute more than 0.05 additional variance explanation. Then after creating a new dataframe with 
car models and selected principal components, hierachical clustering with Ward method has been performed. This resulted in creation on a 
demo dendrogram.

What more could be done:

As mentioned earlier in the data cleaning part, each variable had an additional info about the car version, interior etc. 
This column was skipped. However, with use of Natural Language Processing, we could transform this variable into numeric one, 
which could showcase the level of premium equipment in the car on 0 to 1 scale.



