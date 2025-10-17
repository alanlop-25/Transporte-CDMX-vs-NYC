# Transport system CDMX vs NYC
This project is for practical purposes, it seeks to make a comparison between the effectiveness of the CDMX's Metro system compared to the NYC's Subway system.

## 🎯Objective
To compare the performance of the Mexico City Metro system with the New York City Subway, using available data and estimates, to analyze peak-hour efficiency, usage levels, and wait times.

## ❓Analysis questions
- Which of the two systems supports the highest passenger density per hour at the busiest stations?
- How much does the estimated wait time during peak hours differ from off-peak hours in each city?
- What percentage of daily flow occurs during peak hours, in each system?

## ⚙️Methodology
1. Public data collection (CDMX: daily traffic, frequency estimates; NYC: turnstile data, estimated frequencies).
2. Data cleaning and preprocessing.
3. Defining assumptions for estimates (e.g., peak-hour frequency, train capacity).
4. Calculating comparative metrics (passengers per hour, waiting time, density, etc.).
5. Visualization and comparative analysis.

## 🧮Assumptions
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

$Peak\space hour\space travel\space =\space 4.6M * 0.4 = 1.84M users $

8. Average wait estimate
    - During peak hours: if frequency = 2 minutes, average wait time could be ~1 minute (assuming random arrival).
    - Off-peak: frequency 7 minutes, average wait time could be ~3.5 minutes.

## 📁Structure (in progress)
- `data/`: CSV files  
- `notebooks/`: Jupyter notebook files)  
- `README.md` (Project's description)  
- `output/`: gráficos exportados
  
## 🔍Sources
1. https://metrocdmx.com.mx/
2. https://www.metro.cdmx.gob.mx/parque-vehicular
