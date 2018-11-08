# DeloitteDigital
Data Miner exercise general solution description (Python )
1.	Data was uploaded using standard functionality of Pandas library read_csv, which allows import data without unzipping it.
2.	Performed visual (DataFrame fuctions head(), describe()) and structural data analysis (DataFrame fuctions shape, info()) to understand that data are ready for processing: there are no empty and text fields. 
3.	Split data to validation sets (training data -> training and testing samples with known classifier values). Fitted training sample to mainly used models and performed evaluation of models’ predictions (quantified the quality of predictions with AUC ROC scoring metric):

Model name;	Maximum AUC ROC scoring metric values for testing sample of training data	Score difference, %;	Training execution time , hours;

Logistic regression;	0.63234171;	-27.8%;	0.15

Decision Tree;	0.60548538;	-30.8%;	0.5

Random Forest;	0.87542711;	0%;	3.3

k-nearest neighbors (kNN);	Execution exceeded reasonable amount of waiting time while training 	-	>3

Random Forest is the only one model from the tested that showed bigger estimated AUC ROC score in comparison with Logistic regression (+27,8% after tree parameters varience). All tested models’ scores are inside of AUC ROC score range for usable model (0.5<AUC ROC<=1).
4.	According to AUC ROC scoring metric values Random Forest model was selected to finally predict classifier values (see file “result.csv”).
