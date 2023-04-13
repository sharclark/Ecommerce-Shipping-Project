# Ecommerce-Shipping-Project

Shar Clark
Source: https://www.kaggle.com/datasets/prachi13/customer-analytics

## Predicting On Time Shipments

### Data
  - For this data set there were 12 columns and 10,999 rows 

**Exploratory Data Analysis**
   - During Exploratory Data Analysis, multiple bar graphs were used to show the distribution between groups. A heatmap was also used to show the correlation between columns. The heatmap showed that there was a medium correlation between Cost of the product and Customer Care calls. There was also a direct negative correlation between weight and on time shipments. 
   
     ![Screen Shot 2023-04-06 at 9 10 50 PM](https://user-images.githubusercontent.com/123594410/230539306-88fcabb8-e00c-4f2f-9b16-a9bfc9e2dedd.png)

 **Explanatory Data Analysis**
   - In order to get a better understanding of the relationship between the data columns, I created multiple bar graphs. I noticed that the average discount rate for shipments that were on time were around 17.5, which is significantly higher than the shipments that were not on time. 
   
   ![Screen Shot 2023-04-06 at 9 14 30 PM](https://user-images.githubusercontent.com/123594410/230539770-54b1beca-7d35-4a70-a100-60fd046a8c72.png)

  ### Machine Learning using the following models:
   - KNN Classifier
   - XGBoost Classifier
   - Random Forest Classifier
   
 ### Models Evaluated and Results
 
 - KNN Model Train F1 Scores
    - Pre Tune: .78
    - Post Tune: 1.0
      
- KNN Tree Model Test F1 Scores
    - Pre Tune: .64
    - Post Tune: .65
 
 - XGB Model Train F1 Scores
    - Pre Tune: .92
    - Post Tune: .68
      
- XGB Tree Model Test F1 Scores
    - Pre Tune: .66
    - Post Tune: .68
    
 - Random Forest Model Train F1 Scores
    - Pre Tune: 1.0
    - Post Tune: 1.0
    
  - Random Forest Model Test F1 Scores
    - Pre Tune: .67
    - Post Tune: .66
  
I would reccomend using the XGB Tuned Model, when compared to the KNN Model. The F1 Scores are higher. When looking at the confusion matrices between the two models the pre-tuned XGB Model showed great predictions, however those accurate predictions did not transfer over to the test set. 

### Recommendations
  - **Ecommerce Shipping Insights**
      - Based on the data that was gathered in this data set, there doesn't seem to be a concrete or highly correlated variable for whether or not a shipment will make it to the destination on time. There is a medium correlation between discount offerred and whether or not the shipment will arrive on time, however most of this data set had the mode of transportation as ship. Ship shipments are in transit for a very long time to begin with. I believe we can explain this correlation by the nature of having customers check in on their shipments over time. There was also an uptick in a correlation between customer care calls and if the shipments were on time, which can also be explained by customers checking in on their shipments. 
      - There was a direct negative correlation between weight and on time shipments. The higher the weight of the shipment, the more weight the shipment had, the more likely it was to be late. This is also explained with logic, as the heavier the shipment, the more likely the mode of transport is to be shipped by a boat. 
      - These models will accurately predict whether or not shipments will be on time around 70% of the time. I would not deploy this model. I would look for more data to find more relevant and higher correlations. 
  
