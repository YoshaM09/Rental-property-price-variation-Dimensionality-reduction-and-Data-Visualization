# Rental Property Price Variation
<img width="458" alt="Screenshot 2023-05-30 at 9 00 22 AM" src="https://github.com/YoshaM09/Dimensionality-reduction-and-Data-Visualization/assets/105993890/5b350809-d6f1-4c3e-9baf-b8d641d8f2f1">

### Purpose:

Examine NYC rental property pricing information to gain a better understanding of the availability and variability in price range of rental properties. 

### Problem Statement:

Residents looking for a place to live are drawn to New York City (NYC), which has a thriving rental market. Based on a variety of factors like location, facilities, and closeness to other attractions, these rental costs might vary greatly. In the NYC area, costs vary due to the wide range of rental options, including hotels and apartments. Securing a decent deal in this cutthroat market is essential because rental rates frequently fluctuate because of monetary trends and real estate development. Data that is highly dimensional can provide several difficulties, including a rise in analyzing complexity, overfitting, and difficulties with visualization. 

### How the problem was efficiently solved:

MATLAB served as the primary tool utilized throughout the analysis on the dataset for rental property pricing, processing the data set and visualizing it using a variety of dimensionality reduction approaches. Some features differ by an order of magnitude in terms of feature scaling, but not all of them do. To pre-serve the geometry and lessen the effects of distortion on all the data, transformations were used. Normalization was used to make sure that the data for comparison was uniform. Data skewness was improved by applying log transforms. 

### Approach:

#### 1. Data analysis and visualizations:
Before dimensionality reduction can be used, the data must first be displayed, and its characteristics must be recognized. Because there were so many features, data was initially plotted by room type and then systematically plotted based on price range.  
#### 2. Principal component analysis: 
To project the new variables onto a 2D coordinate system, where the axes stand in for the directions of the data with the highest levels of variability, PCA was applied to the data which first computes new variables by applying linear transformation to the original observed data. 
#### 3. Linear discriminant analysis: 
LDA was applied to the data followed by PCA to create new variables from the original observed data by applying a linear transformation, and then to project the new variables onto a 2D coordinate system to maximize group separation. Here, the axes represent the directions in which the data have the highest levels of variation. 
#### 4. Multidimensional scaling: 
Multidimensional scaling (MDS) is a technique for reducing high-dimensional data to only two dimensions while maintaining the relative distances between observations.Initial pairwise similarities between the data were created using the cosine metric. However, after closely studying the data, city block measure was chosen since it offers a more intriguing perspective on the rental data. 

### Results:

* The visualization demonstrates that the distributionof room types is biased towards the "Entire home/apt" and"Private room" categories, which are the most prevalent room types in the dataset. 
* Despite the uniform distribution of private room and entire home/apt, the Manhattan region of the plot is made up of shared rooms, which makes sense given how crowded it is there, according to a graph created by plotting the longitude and latitude of each rental. Most rental properties share the same lower relative price range, according to the pricing plot. However, some Manhattan properties are more expensive than average. 
* It can be seen that "Entire home/apt" and "Private room" were the most frequently available and occupied accommodations, while "Shared room" and "Hotel room" were occupied less frequently. One of the causes of this visual might be that these two occur less often in the dataset. Comparing properties by price range, the lower price range properties were more frequently available and occupied. 
* The category Room type experiences a lot of overlap in 2D PCA plot based on room types. It could be a result of the similar pricing range, days of occupancy, or geographic location. The PCA plot based on price range shows that there are fewer outliers with the higher price range and that most rental properties fall in the lower price range regardless of the room types. 
* LDA's performance is not noticeably superior to PCA's. Three of the groups can clearly be distinguished from one another, while the two lower price ranges continue to overlap. 
* Regardless of the room type or price range in which the data points were located, it is seen from the plots for the cosine metric that there is a great deal of overlap between all the data points. In other words, attempting to approximate and project angles from a high-dimensional space into these metric spaces is not a good fit for the data. This suggests that the data's structure may be simpler, in which case an alternative metric should be employed. 
* The cityblock metric based MDS estimates are significant because they seem to agree with the PCA projections. Classes are difficult to distinguish from one another, although groups of classes with similar numerical properties can be identified. This shows that separation across classes is poor but good among groups that have the same numerical properties when general distances from the original space are maintained. When both in-class and out-of-class differences are considered, there don't appear to be any significant disparities between the generic groupings of data, indicating that we have achieved good class separation.  

### Tools & Tech: MATLAB
### Dataset Link: 
https://www.kaggle.com/datasets/ivanchvez/ny-rental-properties-pricing
