# TTCSubwayDelay

Motivated by the objective to enhance Toronto Transit Commission (TTC) riders’ experiences and improve travel efficiency, this project focused on predicting subway delays while optimizing passenger travel routes during TTC subway disruptions. The study aims to analyze factors influencing TTC subway delays using data from the Toronto Open Data Catalogue (2017-19, 2023-24) [1], historical weather records from Environment and Climate Change Canada [2], and transit data integrated with OpenStreetMap [3] and TTC schedules [4]. The study employed three analytical methods: binary classification to predict the occurrence of TTC delays, regression modeling to estimate delay duration, and optimization techniques to minimize travel time through different routing and transportation methods. 

An initial random guessing model for delay classification with 0.55 accuracy and a 0.34 F1 score. To improve performance, scaling, feature selection and engineering, model selection, and bagging methods were used. Models such as Logistic Regression, Decision Trees, and XGBoost were examined with parameter optimization via GridSearchCV. With a Bagging Classifier, the model’s accuracy improved to 0.66. The Random Forest classification model achieved the best F1 score of 0.49 and a 0.58 accuracy. For delay duration, a mean-based time prediction baseline model showed a mean absolute error (MAE) of 4.78 minutes. Given the average TTC subway arrival interval of 2.5 to 6 minutes [5], a Support Vector Regression (SVR) with a linear kernel improved the predicted delay time with a lowest MAE of 3.80 minutes. For the optimization task, analysis of walking routes between subway stations using the A* shortest path algorithm showed encouraging results [6]. Using Google Maps as a baseline, 29% of optimized routes had distances shorter than or equal to their Google Maps equivalents. For instance, travelling from Museum to St. George station would take an estimated 10.5 minutes, including 7.5 minutes of predicted delay. The optimized walking route is approximately 6 minutes, saving 4.5 minutes. 

While weather conditions do inform TTC subway delays to an extent, the impact is limited, possibly due to other factors causing randomness in delays. The optimization analysis highlights the impact of multi-modal transportation data on real-time decision-making to minimize passenger inconvenience. Further research should incorporate additional passenger-centric features such as proximity of emergency or paramedic services and explore more transportation options to further improve model performance.
