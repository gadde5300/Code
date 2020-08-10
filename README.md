# Code
Email Spam Detection
# Table of Contents
| TOPICS  | |
| ------------- | ------------- |
| INTRODUCTION  | 
| DIFFERENCE BETWEEN SPAM AND NORMAL E-MAILS | 
| PROBLEM STATEMENT  | 
| OBJECTIVE |
| LITERATURE REVIEW  |
| METHODOLOGY  |
|CONCLUSION  | 
# ABSTRACT
The upsurge in the volume of unwanted emails called spam has created an intense need for the
development of more dependable and robust antispam filters. Machine learning methods of recent
are being used to successfully detect and filter spam emails. We present a systematic review of
some of the popular machine learning based email spam filtering approaches. Our review covers
survey of the important concepts, attempts, efficiency, and the research trend in spam filtering.
The preliminary discussion in the study background examines the applications of machine learning
techniques to the email spam filtering process of the leading internet service providers (ISPs) like
Gmail, Yahoo and Outlook emails spam filters. Discussion on general email spam filtering
process, and the various efforts by different researchers in combating spam through the use
machine learning techniques was done. Our review compares the strengths and drawbacks of
existing machine learning approaches and the open research problems in spam filtering. I
recommended deep leaning and deep adversarial learning as the future techniques that can
effectively handle the menace of spam emails.
# INTRODUCTION
Emails are important because they creates a fast, reliable form of communication that is free and easily accessible. They allow people to foster long-lasting, long-distance communication .
Spam e-mails can be not only annoying but also dangerous to customers.Spam e-mails can be defined as   
 - Anonymity
 - Mass-Mailing
 - Unsolicited

Spam e-mail messages are randomly sent to multiple addresses by all sort of groups , but mainly by lazy advertisers and criminals who wish to lead you to phishing sites. 
# How Spam and Normal e-mails look like?
### Spam Email
![spam](https://user-images.githubusercontent.com/69344247/89771780-81b75900-db1e-11ea-821e-0417de87b936.png)
### Normal Email
![ham](https://user-images.githubusercontent.com/69344247/89772081-073b0900-db1f-11ea-920d-6aed6553a5ee.png)
# PROBLEM STATEMENT
I have chosen this project because nowadays there are lots of people trying to fool you just by sending you fake e-mails like you have won a 1000 dollars, this much amount is deposited in your account once you open this link and then they will try to hack your information.
 - Unwanted emails irritating internet consumers.
 - Critical e-mail messages are missed and/or delayed.
 - Identity Theft.
 - Spam can crash mail servers and fill up hard drive.
 - Billions of dollars lost worldwide.
# OBJECTIVE
The objective of identification of spam e-mails are :
 - To give knowledge to the user about the fake e-mails and relevant e-mails.
 - To classify that mail is spam or not.
# LITERATURE REVIEW
 - I referred  the paper S. Sharmin and Z. Zaman, "Spam Detection in Social Media Employing Machine Learning Tool for Text Mining," 2017 13th International Conference on Signal-Image Technology & Internet-Based Systems (SITIS), Jaipur, 2017, pp. 137-142.
 - Spam prevention is often neglected , although some simple measures can dramatically reduce the amount of spam that reaches your mail box.
 - Before they send you spam , spammers obviously first need to obtain your e-mail address , which they can do through different routes.
# METHODOLOGY
| METHODOLOGY  |DESCRIPTION |
| ------------- | ------------- |
| Collecting Dataset  | The test data is used to check the accuracy of the model built with the training data. The training data set contains  4137 emails . The test data contains 1035 emails .|
| Data Preprocessing | For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. STOP WORDS ,CREATING WORD DICTIONARY |
| Feature Selection | Once the dictionary is ready, I can extract word count vector (our feature here) of 3000 dimensions for each email of training set. Each word count vector contains the frequency of 3000 words in the training file. |
| Model Construction | Naive Bayes ,Random Forest , SVM |
# Bag Of Words
#### Ham
![ham wordcloud](https://user-images.githubusercontent.com/69344247/89773689-09eb2d80-db22-11ea-81b0-3deb4eae08c0.png)
#### Spam
![spam word cloud](https://user-images.githubusercontent.com/69344247/89773691-0bb4f100-db22-11ea-9d57-13b6ffcc45b0.png)

# STEP BY STEP PROCESS
## DATA PREPROCESSING
The emails in the learning data are in plain text format. I need to convert the plain text into features that can represent the emails. Using these features we can then use a learning algorithm on the emails. A number of pre-processing steps are first performed like normalization , binary data..  convert the plain text files to files with one word per line. In this project, I look at emails just as a collection of words. So, to make it easier I convert each file into a list of words.
### Why is Data Preprocessing important?
 - For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw dataset.
# STOP WORDS
There are some English words which appear very frequently in all documents and so have no worth in representing the documents. These are called STOP WORDS and there is no harm in deleting them. Example: the, a, for etc. There are also some domain specific (in this case email) stop words such as mon, tue, email, sender, from etc. So, delete these words from all the files.
# CREATING WORD DICTIONARY
 - 1.  It can be seen that the first line of the mail is subject and the 3rd line contains the body of the email. We will only perform text analytics on the content to detect the spam mails. As a first step, we need to create a dictionary of words and their frequency. For this task, training set of 4137 mails is utilized. 
 - 2.  Once the dictionary is created we can add just a few lines of code to the above function to remove non-words. I have also removed absurd single characters in the dictionary which are irrelevant here by inserting the code in the function def make_Dictionary(train_dir).
 - 3.  Dictionary can be seen by the command print dictionary. You may find some absurd word counts to be high, it’s just a dictionary and you always have the scope of improving it later. Here I have chosen 3000 most frequently used words in the dictionary.This is how a dictionary looks like with the frequency of the words.
 - [('order', 1414), ('address', 1293), ('report', 1216), (‘email’, 1051)]
# FEATURE EXTRACTION PROCESS
 - Once the dictionary is ready, we can extract word count vector (our feature here) of 3000 dimensions for each email of training set. Each word count vector contains the frequency of 3000 words in the training file. Of course you might have guessed by now that most of them will be zero. Let us take an example. Suppose we have 500 words in our dictionary.
 - Each word count vector contains the frequency of 500 dictionary words in the training file. Suppose text in training file was “Get the work done, work done” then it will be encoded as [0,0,0,0,0,…….0,0,2,0,0,0,……,0,0,1,0,0,…0,0,1,0,0,……2,0,0,0,0,0]. Here, all the word counts are placed at 296th, 359th, 415th, 495th index of 500 length word count vector and the rest are zero.
# NAIVE BAYES CLASSIFIER
A Naive Bayes classifier is a probabilistic machine learning model that’s used for classification task. The crux of the classifier is based on the Bayes theorem.Bayes Theorem:
For example, a fruit may be considered to be an apple if it is red, round, and about 3 inches in diameter. Even if these features depend on each other or upon the existence of the other features, all of these properties independently contribute to the probability that this fruit is an apple and that is why it is known as ‘Naive’.
#### P(A/B) = P(B/A)P(A)/P(B)
## Results and Roc Curve
![Naive Bayes ROC](https://user-images.githubusercontent.com/69344247/89773053-d065f280-db20-11ea-85c8-e06f94173ef2.png)
![Naive bayes](https://user-images.githubusercontent.com/69344247/89773056-d1971f80-db20-11ea-8f8c-01d95f771345.png)
# RANDOM FOREST
 - Random forest is a supervised learning algorithm which is used for both classification as well as regression. But however, it is mainly used for classification problems. As we know that a forest is made up of trees and more trees means more robust forest.
 - Put simply: random forest builds multiple decision trees and merges them together to get a more accurate and stable prediction.
 - It is an ensemble method which is better than a single decision tree because it reduces the over-fitting by averaging the result.
 ## Results and Roc Curve
![Random Forest ROC](https://user-images.githubusercontent.com/69344247/89773229-25096d80-db21-11ea-875d-bf7b40f05021.png)
![Random Forest](https://user-images.githubusercontent.com/69344247/89773234-26d33100-db21-11ea-9f9b-a49ccfa79bf4.png)
# SUPPORT VECTOR MACHINE
 - Support vector machines (SVMs) are powerful yet flexible supervised machine learning algorithms which are used both for classification and regression. But generally, they are used in classification problems.
 - An SVM model is basically a representation of different classes in a hyperplane in multidimensional space. The hyperplane will be generated in an iterative manner by SVM so that the error can be minimized. The goal of SVM is to divide the datasets into classes to find a maximum marginal hyperplane (MMH).
 - SVM kernel converts non-separable problems into separable problems by adding more dimensions to it. It makes SVM more powerful, flexible and accurate.(Linear,gaussian,polynomial,rbf).
 ## Results and Roc Curve
![SVM n](https://user-images.githubusercontent.com/69344247/89773410-787bbb80-db21-11ea-9a08-e4b804a4c131.png)
![SVM roc](https://user-images.githubusercontent.com/69344247/89773413-79ace880-db21-11ea-87a4-1cd257dfdfb8.png)

# CONCLUSION 
I was able to classify the e-mails are spam or non-spam .With high number of e-mails lots if people using the system it will difficult to handle all possible mails as our project deals with only limited amount of corpus.




