# Module_14
The goal is to enhance the existing trading signals with machine learning algorithms that can adapt to new data.
The idea is to compare the baseline model with the svc model and decision tree classifier model. 

## Implementation 
1. Read emerging_markets_ohlcv.csv with market data details such as open, close, high, low , volume 
2. Clearn the data , calculate actual returns 
3. Generate trading signals using short window = 4 and long window =100
4. calculate statergy returns 
5. Split the data to test & training data 
6. scale the data 
7. Use SVC classifier model, fit & predict & calculate statergic returns 
8. Use decision Tree classifier model, fit & predict & calculate statergic returns 
9. Compare the new models with baseline . 

## Summary
There were three approaches to enhance the existing trading signals
1. The baseline model without any ML algorithms was implemented with logic below 
- set the short window as 4 and long window as 100 and calculated the slow moving averages 
- Then when the Actual Returns are greater than or equal to 0, we generate signal to buy stock long
- When Actual Returns are lesser than  0, generate signal to sell/hold stock long and the 'Statergy Returns' are calculated
- This performed worse compared to SVC & DTC
2. SVC Model 
- After the data is cleaned, split to train & test data & scaled, we use the scaled data to fit & predict using SVC model
- Note, that SVC Strategy Returns was comparable to the actual results and this model performed better than baseline & DTC. 
3. Decision Tree Classifier 
- After the data is cleaned, split to train & test data & scaled, we use the scaled data to fit & predict using DTC classifier.
- Decision tree uses the tree representation to solve the problem in which each leaf node corresponds to a class label and attributes are represented on the internal node of the tree. We can represent any boolean function on discrete attributes using the decision tree
- This model performed worse as compared to SVC 

Note: Please look at the combine_df & plot that compares the statergy returns of the three approaches as compared to the 'actual results'







