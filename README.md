##   FAKE WEBSITE DETECTION
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/logos.jpeg)

## Inspiration 🤔
Fraudulent websites pose as legitimate sources of information, goods, 
product and services are propagating and resulted in loss of billions of dollars targeting indivisuals , organization and even governments.Websites 
are great tool to access information, services and product, however like any other 
online service, they can be utilized by fraudsters to prey on victims and propagate 
fraud.

Phishing attacks have been a persistent threat, with over 300,000 phishing attacks occurring every quarter as of Q2 2023. The first quarter of 2023 saw more than 40,000 unique email subject lines used in phishing attempts each month, indicating a high level of tailoring and sophistication by attackers.[[2]](https://www.comparitech.com/blog/vpn-privacy/phishing-statistics-facts/)

![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics1.jpeg)
<img src="https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics2.png" alt="Description" width="1000" height="400">

## Problem Statement 

In the contemporary digital landscape, the proliferation of
 cyber security threats has become a matter of grave concern for
 both individuals and institutions. Of the various forms of cyber
 attacks, phishing stands out as one of the most ubiquitous,
 wherein attackers employ deceptive tactics to procure sensitive
 user information like username, password and credit card
 information by posing as legitimate entities.[[1]](https://www.researchgate.net/publication/345977903_A_Novel_Ensemble_Machine_Learning_Method_to_Detect_Phishing_Attack)

 Currently, there’s a noticeable scarcity of resources
specifically dedicated to fake website detection, leaving users vulnerable to on-
line scams and threats.

In order to effectively and precisely identify phishing sites, it is imperative that a better system be created that combines feature engineering, advanced machine learning techniques, and behavioral analysis. The suggested methodology seeks to solve these issues in order to increase online user security, safeguard sensitive data, and promote a safer online environment.

## Introduction 
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics3.gif)

The basic goal of this is to develop an effective fraudulent website detection model that should be able to address these 
challenges and deliver accurate results within a reasonable time frame. The contribution 
proposes a fraudulent website detection model based on sentiment analysis of textual 
contents (URLS and HTML) of a given website and supervised machine learning techniques.

Further in the upcoming sections we are going to explain in more detail every modeule giving a breif overlook of all the steps done in the code and what problems were being faced during the execution of our model.

## Roadmap

- Dataset regarding malicious URLS is collected from open-source platform eg. Kaggle 

- Performing Data Analysis and applying EDA Techniques
- Dividing the dataset into Train-Test split 
- Applying Supervised Machine Learning and  Deep Learning Models like Logistic Regression, SVM,Random Forest, 
- Evaluating the models using the Performance Metrics and unveiling the magic of data through colorful Visualization plots.
- Concluding the results by comparing the Applied Models.

## Approach
### 1) Installed Libraries:
    Tensoflow
    Numpy
    Pandas
    SciKit-Learn
    plotly
    Seaborn
    Tld
    URL Parser


### 2) Data Exploration:
Our Dataset contains 651191 rows that includes 2 columns one holds the URL's and the other includes it's Labels . Labels column includes 4 categories :

    Benign :: URLs refer to safe-to-browse websites

    Defacement :: URLs which created by hackers with the intent to replace the original hosted website with its own content

    Phishing :: URLs aim to steal sensitive information such as login credentials and financial data

    Malware :: URLs inject harmful software into a victim’s system upon accessing the URL

### Visualizing Target Class turning it into insight!
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics4.png)

### 3) Feature Engeneering:
Candidly, our initial foray into content-based URL detection led us down an enlightening path. However, we encountered a couple of stumbling blocks along the way. Firstly, the reluctance of numerous websites to permit content extraction or web scraping posed a formidable challenge. Secondly, we faced a critical deficit in the necessary infrastructure to safeguard against potential viruses from the sites we were attempting to scrape. This posed a significant concern, as our system risked exposure to malware, phishing, and defacement—a trifecta of perilous categories. Safeguarding against these digital dangers became paramount in our pursuit of effective URL detection.

So we moved our exploration for feature Extraction on the basis of URL Domain and Address Bar :
Having IP Address : It checks if the an IP address is placed in the place of the domain name in the URL. as it is common technique used by cyberattackers to conceal their identities

    Abnormal URLS 

    Google Index 

    Count dot 

    Count www 

    Count @ 

    Count directories 

    Count Embed Domain 

    Doubtful Words 

    Short URLs 

    Count https

    Count http 

    Count % 

    Count ? 

    Count - 

    Count = 

    URL Length 

    Hostname Length 

    First Directory Length 

    Length of Top Level Domains 

    Entropy of the URL 

Extracting total of 21 Features based on the URL dataset. 
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics5.png)
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics6.png)
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics7.png)

### 4) Building and Training the Model:
Before commencing the training of our ML models,we partition the dataset into an 80-20 split, 80% for Training and 20% for Testing. As we scrutinize the dataset, its nature as a supervised machine-learning endeavor becomes evident.

Our objective is to classify URLs, delineating them as either phishing (3), benign (0), defaced (1), or infiltrated by malware (2).

MODELS APPLIED INCLUDE :

- Logistic Regression
- Random Forest 
- MLP 
- XGBoost 
- CNN
- Decision Trees
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics8.png)
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics9.png)
  
### 5) Model Prediction :
Evaluating the Models Accuracy and Visualizing the predictions.

## Evaluation and Model Performance
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics10.png)

After splitting the Dataset into 80 by 20 ratio and fitting the models we get all the  Accuracies as :
![](https://github.com/InzishKhan/Fake-Website-Detection/blob/main/pics11.png)


## Results 
From the obtained results of the above models,  Random Forest has highest model performance of 92% accuracy . The rest of the Models applied except the CNN have good performance but the Random Forest outperforms from the rest.


