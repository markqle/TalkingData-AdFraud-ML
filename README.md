# TalkingData-AdFraud-ML

This project were using the data from Kaggle:
Since the data is very large, you can fetch it directly from Kaggle, Github doesn't have enough capacity to upload that large data. Thus, only the train sample is uploaded.
For further investigation, here is the original dataset:
#### Kaggle Data Source: https://www.kaggle.com/competitions/talkingdata-adtracking-fraud-detection

1.	Introduction: Fraud risk is everywhere, but for companies that advertise online, click fraud can happen at an overwhelming volume, resulting in misleading click data and wasted money. Attribution fraud in mobile app marketing refers to artificially inflating the number of app installs or clicks attributed to a particular advertising source, typically to generate fraudulent payouts. This is a severe problem for advertisers, as it can lead to significant financial losses and a decrease in trust in the effectiveness of mobile advertising. In this project, we propose to develop a machine-learning model to detect attribution fraud in mobile app marketing.
2.	Project Objectives: The primary objective of this project is to develop a machine learning model that can accurately identify instances of attribution fraud in mobile app marketing. Specifically, the model should be able to distinguish between legitimate and fraudulent app installs/clicks and identify the specific sources of fraudulent activity.
3.	Data Collection: To train the machine learning model, we will use the data from the TalkingData dataset, one of the largest independent big data service platforms that cover over 70% of active mobile devices. This data will include information such as the timestamp of the install/click, the device ID, the IP address, the app ID, and the advertising source ID. We will also need to label each instance of install/click as either legitimate or fraudulent.
4.	Data Preprocessing: We will need to preprocess it to ensure it is suitable for machine learning. This will involve cleaning the data, removing duplicates, and encoding categorical variables. We will also need to perform feature engineering to extract relevant features from the data, such as the time of day, the device type, and the location.
5.	Model Development: We propose using a combination of supervised and unsupervised learning techniques for this project. We will first develop a supervised learning model, such as a random forest or a neural network, to classify instances of install/click as legitimate or fraudulent. We will then use unsupervised learning techniques, such as clustering or anomaly detection, to identify the sources of fraudulent activity.
6.	Model Evaluation: To evaluate the machine learning model's performance, we will use a variety of metrics such as precision, recall, and F1-score. We will also use techniques such as cross-validation and ROC curves to ensure the model is not overfitting the training data. Finally, we will thoroughly analyze the model's performance on real-world data to ensure that it is accurate and reliable.
Evaluation: 
-	For each click_id in the test set, predict probability for the target is_attributed variable
-	Evaluated on area under ROC curve between the predicted probability and the observed target
7.	Conclusion: This project aims to develop a machine-learning model to detect attribution fraud in mobile app marketing. By accurately identifying instances of fraudulent activity and the sources of that activity, this model will enable advertisers to take action to prevent fraud and protect their investments in mobile advertising and assist TalkingData with their current prevention approach to prevent click fraud for app developers to measure the journey of a user's click across their portfolio, and flag IP addresses who produce lots of clicks, but never end up installing apps. With this information, they can build an IP blocklist and device blacklist more accurately and timely.

Data fields
Each row of the training data contains a click record, with the following features. <br>
•	ip: ip address of click. <br>
•	app: app id for marketing. <br>
•	device: device type id of user mobile phone (e.g., iphone 6 plus, iphone 7, huawei mate 7, etc.) <br>
•	os: os version id of user mobile phone <br>
•	channel: channel id of mobile ad publisher <br>
•	click_time: timestamp of click (UTC) <br>
•	attributed_time: if user download the app for after clicking an ad, this is the time of the app download <br>
•	is_attributed: the target that is to be predicted, indicating the app was downloaded <br>
Note that ip, app, device, os, and channel are encoded. <br>
The test data is similar, with the following differences: <br>
•	click_id: reference for making predictions <br>
•	is_attributed: not included <br>
