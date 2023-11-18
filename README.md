# Customer_Journey_Analytics

### Table of Contents
1. [Overview](#overview)
2. [Project Goals](#goals)
4. [Project Structure](#structure)
3. [Results](#results)
5. [Insights](#insights)
6. [File Descriptions](#files)

## Overview<a name="overview"></a>

This project involves exploring real-world data from 365's online subscription-based learning platform to analyze user behavior. The term 'user journey' refers to each user's experience while navigating the product or platform, specifically the sequence of pages they visited before purchasing a subscription.
Analyzing this data is crucial for businesses as it helps identify key pages or sequences that contribute to user conversions. Additionally, it provides insights into user behavior, enabling businesses to optimize marketing campaigns and identify unnecessary pages.

## Project Goals<a name="goals"></a>

The primary goal of this project is to build robust tools and functions in Python for the analysis of various users' website journeys. The focus is on developing the right set of tools to generate meaningful metrics that offer valuable insights into user behavior.

## Project Structure<a name="structure"></a>

- Data Analysis: Explore and analyze user journey data to derive meaningful metrics.
- Data Preprocessing: Implement functions to clean and prepare the data for analysis.
- Metrics Generation: Develop functions to generate key metrics such as page count, page presence, page destination, page sequences, and journey length.
- Subscription Plan Analysis: Incorporate a parameter to analyze user behavior based on different subscription plans.

## Results<a name="results"></a>

The main findings of the project can be found in the file `User_journey_analysis.ipynb`

## Insights<a name="insights"></a>

First, we can look at the difference in page count and presence for the different plans. For this to be relevant and compared, we need to check the total amount of pages or journeys because there could be different amounts of monthly and annual users. What can be seen is the relatively high presence of the resource center for users that purchased a yearly plan.

This may suggest that people are comfortable subscribing to our platform for extended periods because of the high quality of resources we provide.

But correlation doesn’t always imply causation, which might be the case here. People already interested in long-term learning are the ones who check out the Resource Center. And, of course, those will be the ones to purchase an annual plan.

This hypothesis can be considered if we look at the page presence rather than the absolute count. In this metric, the Resource Center is present in about 12% of the journeys of monthly users and around 14% of the annual journeys. This is a slight increase, but ultimately, insignificant, given our sample sizes of ~300 and 900 journeys. The increase in total page counts is much more significant than the increase in the presence of this page, indicating that there aren’t more annual people who look at these resources, but the ones that do, stay for much longer.

Another difference between monthly and annual users can be found when we look at the destination pages after the homepage. For the monthly side, Pricing is ranked 5th highest with 102 clicks, while for annual users, it’s the second highest follow-up after the homepage, with 329 clicks.

This is a bit difficult to conclude, but the annual users were more ready to purchase even at the beginning of their journey. We would want to attract and spend marketing resources on these visitors because they’re more inclined to buy the product, not just the annual plan. After all, going to pricing immediately indicates they want to consider the best option.

Another interesting observation is that monthly users often check out the career tracks page. This page contains our course library grouped into several sequences called ‘career tracks.’ It structures the potential learning process by saying, “Hey, you want to become proficient in this field? Then, take these courses in this order.” This construct caters to those with short-term goals or wanting to learn this specialty. It’s difficult to say whether those types of people wouldn’t have subscribed if we didn’t provide career tracks or if they would have maybe chosen more long-term plans.

The preprocessing options depend on what you want to take away from the analysis, and many combinations can be tried. Regarding which sessions to group, the first few sessions can indicate the users’ assumptions and objectives before getting to know the platform. This can help you identify the general behavior of the user.

The last sessions are cluttered, with many log-ins and checkouts. But among the clutter, you can see if a page convinced the user to purchase. These previous sessions may include the tipping point. As for pages to be removed, the apparent candidates are ‘Log in,’ ‘Checkout,’ and ‘Sign up.’

 
## File Descriptions <a name="files"></a>

 - `User_journey_raw.csv` provides the raw data about the customer's journey before preprocessing
 - `User_journey.csv`` provides the customer's data after preprocessing
 - `User_journey_preprocessing.ipynb` contains the preprocessing fucntions needed to clean the dataset
 - `User_journey_analysis.ipynb` contains the data analysis process of customer's journey
 



