# World Data League 2023



## 🎯 Challenge
Determining The Main Mobility Flows in the City of Lisbon Based on Mobile Device Data

Challenge Provider: LxDataLab Lisbon

## Team Name
K-MENA Team


## 👥 Authors
* Sara Sabzikari
* Mine Yasemin 


## Introduction
From 1980s-2017, the population of the city of Lisbon decreased from 800.000 to 500.000 to its metropolitan area - this has lead to increased car use in daily commuting between the city and the metropolitan area, overloading of the road network, coupled with decrease in public transport.

The Lisbon City Council's objectives for the 2023-2027 period include boosting soft mobility modes, making it easier and more affordable use of public transportation, and promoting the development of an integrated, connected, accessible, multimodal ecosystem.

Our team helped with the strategic planning towards a city with "Smooth Traffic Flow". To this end, we developed a deep-learning-based forecasting model to support the mobility policies for the city of Lisbon by predicting futures trends on mobility flow at particular areas in the city and clustering these areas by impact levels. We have produced a model and product plan that can help users themselves identify inefficient routes and when to consider alternative routes/modes of transport. People in Lisbon need alternatives, and they need ones that are reliable and easily accessible.

The output of this project led to us being ranked 5th place amonst 29 other teams.

 

## 🔢 Data 

The two main datasets used (along with shapefiles of Lisbon) were the mobile traffic datasets locating and quantifying mobile terminals as a proxy for traffic within Lisbons road network and the main entry and exit points. We were provided with some links to public transport coordinates and use, but these didn't seem to match the timeframe of the main datasets. If these datasets had matching timeframes, we could create models that would account for traffic levels and the relationships different traffic levels have with public transport usage.

We also used traffic dataset to label each timeframe of the mobile phones dataset for classification model. We noted some lists of point of interest (POI) in Lisbon, such as architecture, restaturants, etc. These data can be found online in Google maps. 


## 🧮 Methods and Techniques 

We chose to utilize long short-term memory (LSTM) for modeling our time series data, which is ordered in a sequence. By using an LSTM-based model, we can effectively handle the nonstationarity of the time series data. Before constructing the model, we first determine the relationship between variables to determine if one time series can be used to forecast another. In our dataset, the two main features are the number of mobile phones entering and exiting the city on the main axes. We discovered that the number of entrances serves as a predictive factor for the future number of exits. Additionally, we incorporate the weekday as an extra feature by transforming it into a categorical variable. To enhance the model's performance, we can consider including additional information such as working hours, holidays, rainfall, events, and more.


## 💡 Main Insights 
#### Observations of mobility:
- Looking at entry and exit data, the busiest days across most roads were Monday-Wednesday and Friday-Saturday, the latter being the busiest (party time?)
- The top 3 busiest roads across the week were 1) IC19, 2) IC2, 3)IC16. The least busiest was A1.  
- The busiest time period during the day for both entry and exit into Lisbon was within 7am and 8am.
- There are clearly tourist hotspots that can be distinguished from total mobile devices - roaming traffic contributed a large amount to total number of mobile devices recorded within many grids.
- Mobile devices in roaming makes a peak at the grids in Parque das Nações in the first days of November. We found out that Web Summit 2022 took place at this area.
- Traffic issues correlate with the total mobile devices.


## 🛠️ Product
### Definition
Application with interactive map for daily use to help people in Lisbon plan more efficient routes.


### Users
Commuters and travelling individuals can open the app at any given point and use it to plan their routes in the near future - it will be reliable and tailored specifically to the population and road networks. It could incorporate public transport data, suggesting alternative routes that are likely to evade traffic. 


### Activities
* Predicts the most likely locations for traffic accidents
* Suggests the fastest route from dispatch centres
* It is up-to-date with model, providing reliable insights to the users.


## 🌍 Social Impact
Our model estimates the mobility flow (number of entrances and exits) in the near future. These predictions are visualised on an interactive map and suggest users different, more sustainable and efficient modes of transport, for example, car sharing or shifting their short distance car trips by greener transport options such as walking or cycling. It can also help mobility providers with making decisions such as how many buses should operate on a route at different times of day.