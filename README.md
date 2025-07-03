# A Data-Driven Approach to Flight Delay Analysis and Prediction

This project focuses on analyzing flight delay data to understand delay patterns, identify major causes, and predict whether a specific airport–airline–month combination is likely to be delay-prone. The dataset consists of aggregated flight performance statistics, including total flights, delay counts, and delay durations categorized by causes such as carrier issues, weather, NAS (National Airspace System), and late aircraft.

The first part of the project involves exploratory data analysis (EDA), where missing values are handled and new features such as delay ratio and average delay per flight are created. Various visualizations including line plots, bar charts, pie charts, and heatmaps are used to uncover seasonal trends, identify the most delay-prone airports and airlines, and understand the distribution of delay causes. The EDA also highlights patterns in delay duration and frequency, helping build a foundational understanding of the data.

The second part involves building a classification model to predict whether a given group (airport + carrier + month) is delay-prone, defined as having more than 15% of flights delayed. A Random Forest Classifier is trained using features like flight counts, delay causes, and encoded airline/airport information. Class imbalance is handled using SMOTE, and the model is evaluated using metrics like accuracy, F1-score, and ROC AUC. SHAP (SHapley Additive exPlanations) is used to explain feature impact on predictions and improve model transparency.

A custom metric called the Operational Adjustability Index (OAI) is also introduced. OAI assigns greater weight to controllable delays like those caused by the carrier or late aircraft, and lower weight to external causes like weather. This index helps airlines and airport operators focus on areas where operational improvements can realistically reduce delays.

The project is implemented using Python, with libraries such as Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn, SHAP, and imbalanced-learn.
