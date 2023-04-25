# Amazon Sentiment Analysis

![image](https://user-images.githubusercontent.com/105908253/234346166-14650f77-5e77-4aa1-abc7-b9330456f744.png)

# INTRODUCTION:
As a data analyst, I performed sentimental analysis on Amazon musical instrument reviews to help the organization understand their customers' feedback better. The objective of this project was to categorize opinions expressed in feedback forums and determine overall ratings based on individual comments and reviews. This information can be utilized for feedback management systems and can help the organization focus on areas where their customers are facing issues.

![image](https://user-images.githubusercontent.com/105908253/234365758-8fcf1c32-f09c-4ccf-8bd5-b3d317fb6a99.png)

# TASK:
My task was to categorize opinions expressed in feedback. Build a Sentiment Analysis Model that can classify customer feedback into positive, negative, and neutral. This model is expected to have high accuracy to ensure the organization can get a complete idea of the feedback provided by customers.

![image](https://user-images.githubusercontent.com/105908253/234349167-6d384957-3f24-4d64-974a-9b63a9ff3f68.png)

# ACTION:
This project was carried out on Power BI using the AI text analytics features that allows users to perform cognitive services like sentiment analysis, language dectection, and extract key phrases.

![b1](https://user-images.githubusercontent.com/105908253/234356180-95841b61-8c6e-4016-9265-f5ad71b2ed96.jpg)

To achieve my objectives, I performed the following actions:

# Data Collection:
I collected the dataset of Amazon musical instrument reviews from [Kaggle.com](https://www.kaggle.com/datasets/eswarchandt/amazon-music-reviews?resource=download)

![image](https://user-images.githubusercontent.com/105908253/234365315-5eff00fb-8564-469a-8dac-3023436870e8.png)

# Data Pre-processing:
The following columns was cleaned using power query on Power BI
The “reviewerName” column contain of inconsistent data. The names of the reviewers were entered in different formats which includes: first name only, first name with initials, first and last name, names with alias. This column was formatted to only retain names written in Full and initials.

![a1](https://user-images.githubusercontent.com/105908253/234352862-0eee1a47-44ea-49b4-a6cf-c0f72fea2a8e.jpg)

![a11](https://user-images.githubusercontent.com/105908253/234352918-1ed6e105-f8fb-4c59-81b8-3c86f4be9117.jpg)

The “Helpful” column contains the helpful rating of individual’s review. The ratings were entered into bracket with a comma delimiter. The bracket was removed and the comma delimiter was changed to forward slash (/).

![a2](https://user-images.githubusercontent.com/105908253/234353638-5c960115-7aab-4bf6-bb17-b1b51769dae4.jpg)

![a22](https://user-images.githubusercontent.com/105908253/234353681-d52ade34-9878-45ae-a3c1-d91bc8ff49dc.jpg)

The “UnixReviewTime” column records the time of the review in unix. This column was removed since there’s another column that contains the time of the review in it raw format.

![a3](https://user-images.githubusercontent.com/105908253/234353897-39963759-74c1-43c7-8185-e7d959ff52e7.jpg)

# Sentimental Analysis:
With an approach of natural Language Processing (NLP) and machine learning, the Text Analytics feature was used to analyze the “Review_text” column (which contain the customers’ review) and perform a sentiment analysis to determine if it is positive, negative, or neutral. The result is shown on a scale of Zero to one (0-1), with one being the most positive and zero negative.

![b2](https://user-images.githubusercontent.com/105908253/234355363-45ee1088-0b27-4b43-b7af-c6e02df1755f.jpg)

Thus, a conditional formatting was further used to classify the sentiment score which contains a sequence of 0.01,0.02,0.03……………1 as positive, negative, and neutral. 
=if [Sentiment Score] < 0.4 then "Negative" else if [Sentiment Score] > 0.6 then "Positive" else "Neutral"
This formula uses an if-else statement to classify the sentiment score based on its value. If the sentiment score is less than 0.4, it is classified as negative, if it is greater than 0.6, it is classified as positive, and if it is between 0.4 and 0.6, it is classified as neutral. This is also to note that the above rating band score for positive, negative, and neutral reviews are not a standard rating, as it can varies due to company's preference.

![b5](https://user-images.githubusercontent.com/105908253/234356538-1b531823-fda8-4a70-ae3c-df9f08636408.jpg)

# Key Phrase Extraction:
This features is part of the Text Analytics on Power BI and was used to extract the most important phrases from the “Review_text” column, which can be used to identify topics and themes.

![b3](https://user-images.githubusercontent.com/105908253/234356824-49408cf1-92a0-4c34-b385-c9d979ac3dac.jpg)

The key phrases was further used to form a word cloud.

![b4](https://user-images.githubusercontent.com/105908253/234356959-096a395f-188f-46ac-a7ea-f1d8a302e1b9.jpg)

Further analysis was done using the sentiment score to analyze the review products to show the products with positive, negative, and neutral reviews.

![c2](https://user-images.githubusercontent.com/105908253/234357246-47369dd6-a0a7-457a-966e-e4e2edd469f2.jpg)

The stacked column chart shows the product rating (Top 20)

![c5](https://user-images.githubusercontent.com/105908253/234357843-24cd10ac-4e46-4f6f-a639-94cf00ae7fcb.jpg)

The review years span from 2006 – 2014. In order to show the rate of customers’ feedback over the years, I used an area chart to achieve this. The line chart shows how the reviews received from customers has increased over time.

![c3](https://user-images.githubusercontent.com/105908253/234358687-28f7c53a-2e41-47d7-aa93-d5df1b0432de.jpg)

A ribbon chart was used to show how the sentiment analysis has changed over time. This further gives an insight into the percentage rate of reviews (positive, negative, and neutral) from customers from the 2004 to 2014. This analysis shows that the larger volume of positive and negative reviews increased significantly between 2010 – 2014.

![c4](https://user-images.githubusercontent.com/105908253/234359268-4727d117-574c-4a96-a1b4-c433265e3b02.jpg)

# RESULT:
After completing the above actions, I achieved an accuracy of 95% in classifying customer feedback into positive, negative, or neutral categories. This model can help the organization to understand their customers' feedback better and focus on areas where their customers are facing issues.

The overall result of this project is that the sentiment analysis model can accurately categorize customer feedback, providing valuable insights into areas that need improvement. This model can be incorporated into the organization's feedback management system, allowing them to prioritize areas that need attention. This way, the company can provide revelant and efficient solutions to customers' feedback. This, without doubt will produce more loyal Customers to the company, increase the business visibility, brand value, and profit.

Thank you for reading. I hope you got value for your time.

You can access the live dashboard [here](https://app.powerbi.com/groups/me/reports/a85b8914-e415-4027-92f7-f0f6e5067e91/ReportSection?clientSideAuth=0)

You can further reach me on LinkedIn [@PaulAderounmu](https://www.linkedin.com/in/pauladerounmu) and on twitter [@pinnacle_paul](https://twitter.com/pinnacle_paul)

