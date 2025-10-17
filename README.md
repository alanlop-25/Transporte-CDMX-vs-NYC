# Transport system CDMX vs NYC
This project is for practical purposes, it seeks to make a comparison between the effectiveness of the CDMX's Metro system compared to the NYC's Subway system in 2021, under similar conditions (both cities in the process of reactivation).

## 🎯 Objective
To compare the performance of the Mexico City Metro system with the New York City Subway, using available data and estimates, to analyze peak-hour efficiency, usage levels, and wait times.

## ❓ Analysis questions
- What percentage of daily flow occurs during peak hours, in each system?
- Which of the two systems supports the highest passenger density per hour at the busiest stations?
- How much does the estimated wait time during peak hours differ from off-peak hours in each city?

## ⚙️Methodology
1. Public data collection (CDMX: daily traffic, frequency estimates; NYC: turnstile data, estimated frequencies).
2. Data cleaning and preprocessing.
3. Defining assumptions for estimates (e.g., peak-hour frequency, train capacity).
4. Calculating comparative metrics (passengers per hour, waiting time, density, etc.).
5. Visualization and comparative analysis.

## 🧮 Assumptions
(CDMX)
1. During peak hour, trains run every ~2 minutes at busy stations.
2. During periods of lower demand, frequency intervals typically increase to ~5‑10 minutes.
3. A total of 394 trains (331 pneumatic + 63 rail).
4. Train capacity varies depending on the number of cars: 6-car train: ~1,020 people; 7-car train: ~1,475 people; 9-car train: ~1,530 people.
5. Approximate daily users: 4.6 million people each day. (INEGI data, in pre-pandemic context)
6. Theoretical maximum hourly capacity 
Let's assume that during rush hour, trains run every 2 minutes, and each train carries approximately 1,530 passengers. Therefore, at a busy station, the following could pass in 1 hour:

$\frac{60\space minutes} {2\space minutes \space per \space train} = 30\space trains\space per\space hour$

$30\space trains * 1,530\space people = 45,900\space people\space per\space hour.$ (at that station if all the trains are full)
That would be theoretical capacity if everything were ideal. In reality, not all trains will be full; there will be variations, etc.

7. Estimated peak vs. off-peak usage
If the daily total is ~4.6 million users, and we assume for example:
    - Morning peak hour: 7:00-9:30 (2.5 hours)
    - Late peak hour: 17:00-20:00 (3 hours)
    - We assume that during these periods, say, 35-40% of the total number of trips per day occur.
Then it could be estimated:

$Peak\space hour\space travel\space =\space 4.6M * 0.4 = 1.84\space M\space users $

8. Average wait estimate
    - During peak hours: if frequency = 2 minutes, average wait time could be ~1 minute (assuming random arrival).
    - Off-peak: frequency 7 minutes, average wait time could be ~3.5 minutes.

## 👓Conclusions
1. What percentage of daily flow occurs during peak hours, in each system?

   The CDMX system shows more concentrated usage during peak hours, while NYC has a more distributed usage pattern throughout the day.

   In the case of the Mexico City Metro, it was assumed that 60% of the total daily passenger traffic travels during peak hours, distributed symmetrically between the morning (30%) and afternoon (30%), while the remaining 40% travels during off-peak hours.

   This estimate is based on general traffic data and practical assumptions based on typical urban mobility patterns. In contrast, the NYC Subway shows a more dispersed layout, with higher usage during off-peak hours. This could be due to a combination of factors such as more flexible work schedules, constant tourist activity, and a city that operates virtually 24/7.
   
3. Which of the two systems supports the highest passenger density per hour at the busiest stations?

   Pantitlán, the busiest station in Mexico City, handles an estimated 27.96 million passengers during peak hours (morning and afternoon), more than double the busiest station in NYC, 34 St-Penn Station, which handles approximately 5.24 million passengers during the same periods. The next busiest stations in CDMX, such as Indios Verdes (~14.07 million) and Constitución de 1917 (~12.3 million), also show significantly higher numbers than the top stations in NYC, where the second busiest station, 86 St, has around 4.09 million.

   This reveals an extremely high concentration of passengers at specific nodes in the Mexico City system, reflecting a network with critical points of high demand. In contrast, the NYC system presents a more balanced distribution, with several important nodes but lower volumes per station.

   These differences may be related to the structure and extent of the networks, urban density, and passenger flow distribution strategies in each city. From an operational standpoint, Mexico City may face greater challenges managing congestion at key stations, while NYC distributes the load across more stations.


## 📁 Structure (in progress)
- `data/`: CSV files  
- `notebooks/`: Jupyter notebook files)  
- `README.md` (Project's description)  
- `output/`: exported graphs


## 🔍 Sources
1. https://metrocdmx.com.mx/
2. https://www.metro.cdmx.gob.mx/parque-vehicular
3. https://datos.cdmx.gob.mx/dataset/afluencia-diaria-del-metro-cdmx
4. https://catalog.data.gov/dataset/turnstile-usage-data-2021
5. 

#### ⚙️Work in progress
