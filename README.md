# Preventing Customer Churn, Identifying Hidden Segments and Improving Satisfaction of Pharmaceutical Drug Users


## Problem Statement

Pharmaceutical companies are facing the challenge of customer churn. Unhappy customers are switching to other companies and giving bad reviews that might negatively impact their brand value. Therefore, there is a need to efficiently identify unhappy customers and quickly conduct customer recovery. Companies will also need to make improvements to their drugs after gathering more information from unsatisfied customers. This is especially important in the internet era, where reviews could be written anywhere on the internet such as website, blogs and social media. In most instance, no explicit rating or score will be given, these reviews will come only in text form. Therefore, it is necessary to develop classification models to quickly and automatically classify reviews based on sentiments. Besides that, pharmaceutical companies will need to know their customer segments in order to provide tailored services to enhance customer experience and also to develop marketing strategies to boost sales. Lastly, companies will need to efficiently recommend medicines to customers based on their condition or switch drugs when customer is not satisfied with their existing drug. 

Therefore, our problem statement can be summed up to: preventing customer churn, identify hidden segments and improving satisfaction. 

Pharmaceutical companies, clinics and hospitals will benefit from this project. Companies could use the models created to quickly identify positive or negative reviews on websites or social media where no explicit score/rating was given. It will help them to reduce customer churn, improve their service offering and making their business more profitable. Patients will also benefit from better service and more effective medicines. 

Note: Dataset is from UCI Machine Learning Repository: Drug Review Dataset (Drugs.com) Data Set

## Executive Summary

### Data Dictionary 

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**drugName**|*object*|df|Name of drug.| 
|**condition**|*object*|df|Name of condition.|
|**review**|*object*|df|Patient review.|
|**rating**|*int*|df|10 star patient rating.| 
|**date**|*datetime*|df|Date of review entry.|
|**usefulCount**|*int*|df|number of users who found review useful.|
|**sentiment_rate**|*int*|df|Binary 0 represents negative review, 1 represents positive review.|
|**month**|*datetime*|df|Month of the post made.|
|**year**|*datetime*|df|year of the post made.|

### Data Cleaning

1. All duplicated data were removed 
2. Null cells were replaced with empty spaces 
3. All text were converted to lower case
4. All non letters were removed
5. All HTML special entities removed
6. All hyperlinks removed
7. All punctuations removed
8. Words with 2 or fewer letters removed
9. Whitespace were removed
10. All emoji removed
11. Remove characters beyond Basic Multilingual Plane (BMP) of Unicode
12. All words were lemmatized 

### Cluster 1: The Image Conscious 
The image conscious segment are customers who uses birth control, weight loss and anti-acne drugs. While using these drugs they are concerned about the side effects on their physical appearance. This segment mostly contains young to middle age female users, image conscious. The customers in this segment tends to be short to mid term drug users. Typical customer look as such:  

"Fantastic! No bloating or weight gain!! Yippee!!! Hot flashes are gone, helped the first week, would have a few here and their but they were mild and by the second month- they are totally gone and sleeping so much better- the feeling of anxiety is gone- life grand again! \r\r\nImmmmmm soooo happy!"

"I got Nexplanon in October of 2014. Since getting it, I have not had a period. No spotting or bleeding, periods just stopped. It&#039;s great! No random breakouts on my face and no weight gain from it. Definitely the best option if taking a pill is hard for someone. I never could remember to take my pill, this was the best option. The insertion was much better than I thought and it&#039;s been great ever since."

### Cluster 2: The Mental Well-Being

The mental well being segment are customer who uses anti-depression, anxiety, ADHD and other mental well being drugs. While using these drugs they are more concerned about their mood, engery level, positive thoughts and living life normally. This segment is a mixed of both male and female, could be parents purchasing drugs for their childern. Generally, the customers in this segement are long-term drug users. A typical customer look as such: 

"This is my miracle. I was put on it in Germany and had to go off it until I had insurance again. I suffer from depression and anxiety. Often I would find myself stuck in a daydream world because of all the things going on in my life, including my partner of years (15-25). I would have no energy and just feel so low. Finally I had insurance and was put on 1800mg a day. I feel so much better. I feel like I can handle life and set goals for myself. I don&#039;t feel anxiety. I don&#039;t sit here and think of the negative and focus on a positive life. I am more fun and interactive with my son. \r\n\r\nIt literately saved my life. I don&#039;t know why."

### Cluster 3: The Pain Killers
The paink killers segment are customers who uses pain-easing drugs. While using these drugs, they are more concerned about mobility and level of pain. This segement tends to be male customers. In terms of drug usage duration, customers in this segement come from two extreme. Customers could either be short term drug users who uses the drugs only when they feel the pain and stop using after the pain subsides or they are long term users who suffer from chronic pain for many years. A typical pain killer customer looks as such: 

"I am allergic to caffeine and spicy foods that give me all kind urinary infections. However, just one Cipro pill makes the pain just disappear! I have no known side effect from Cipro. Cipro is simple awesome!"

"I have severe psoriatic arthritis and I&#039;ve had it since I was 18. I&#039;ve been on remicade for almost 10 years and I have almost no pain. My joints get a little stiff close to my infusion but that&#039;s it. It is my miracle drug and I owe my life to it. I would be crippled without it."

### Conclusion and Recommendation

#### Product/Service
1) Companies should focus on developing drugs for birth control, weight loss, depression, anxiety and pain. Based on cluster analysis and topic modelling. Three clusters were identified, the first segement mostly suffer from condition such as birth control, obesity and acne. This segement is highly image conscious, they are concerned about whether the drug will make them gain weight. Therefore, companies should take note to reduce the effect of weight gain when developing drugs. The second cluster are those with mental illness, such as depression and anxiety. The third cluster are those dealing with pain. Besides that, based on exploratory data analysis, the most frequent conditions are birth control, depression, pain, anxiety, acne, bipolar disorder, insomnia, weight loss, obesity and ADHD. It is therefore recommended for companies to focus on drugs in these areas to maximise customer base and increase profit. 

2) Companies should quickly conduct customer recovery service when a negative sentiment was detected. Companies can use the random forest classification model developed to classify customers into positive or nagative. Prescence of words such worse, disappointed, would't recommend, ruined or worst are strong indicators of nagative customers. Companies can quickly contact these customers to understand more about their experience and use the recommender system developed to recommend alternative medicine to them. Based on the customer feedback, companies and conduct more R&D to improve on the drug. Such a way, customer churn could be avoided and valuable information were gathered for drug improvement. 
  
#### Promotion
1) Different marketing strategies should be developed for different segments. When targeting the image conscious segment, the message should be along the line to better apperance, not gaining weight or better skin. When targeting the mental well-being segment, the message should be better mood, mental positivity and good energy because this is what concerned this segment the most. When targeting the pain killer segement, the message should be along the line, disappearing pain. 

2) The marketing message should include words such as love, amazing, miracle or changed life. These words are generally associated with positive sentiment and what most drug users yearn for. 
