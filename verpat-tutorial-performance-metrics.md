## Performance Metrics

https://github.com/gregorbj/VisionEval/wiki/VERPAT-Modules-and-Outputs#module-outputs-18

**TODO: Update these tables for current data**

**What is the source of these numbers?  VERPAT output files?**


### Direct travel impacts

Daily vehicle trips

|                        | Description                      | Vehicle trip decrease |
|------------------------|----------------------------------|----------------------:|
| Density                | Household/Population density     | -0.043                |
| Diversity              | Land use mix (entropy)           | -0.051                |
| Design                 | Intersection/streen density      | -0.031                |
| Regional Accessibility | Job accessibility by auto        | -0.036                |
| Distance to transit    | Distance to nearest transit stop | 0                     |

Daily transit trips

|                        | Description                      | Transit trip increase |
|------------------------|----------------------------------|----------------------:|
| Density                | Household/Population density     |                  0.07 |
| Diversity              | Land use mix (entropy)           |                  0.12 |
| Design                 | Intersection/streen density      |                  0.23 |
| Regional Accessibility | Job accessibility by auto        |                     0 |
| Distance to transit    | Distance to nearest transit stop |                  0.29 |

  + Daily vehicle miles traveled
    - Light VMT for each household and place type
    - Regional VMT for heavy trucks and buses
  + Peak travel speeds by facility class
    - VMT by speed bin and class (freeway, arterial, other)
    - Average speeds by class
  + Vehicle hours of travel, delay
    - Vehicle hours of travel at free flow
    - Vehicle hours of travel in congestion
	
### Energy impacts

Fuel consumption

  + calculated from VMT and fuel economy, split into fuel types
  + calculated for light vehicles, heavy trucks and buses
  
| Year | Auto <br> Proportion <br> Diesel | Auto <br> Proportion <br> CNG | Lt. truck <br> Proportion <br> Diesel  | Lt. truck <br> Proportion <br> CNG | Gas <br> Proportion <br> Ethanol    | Diesel <br> Proportion <br> Biodiesel   |
|------|------------|------------|------------|------------|------------|------------|
| 1990 | 0.007      | 0          | 0.04       | 0          | 0          | 0          |
| 1995 | 0.007      | 0          | 0.04       | 0          | 0          | 0          |
| 2000 | 0.007      | 0          | 0.04       | 0          | 0          | 0          |
| 2005 | 0.007      | 0          | 0.04       | 0          | 0.1        | 0.01       |
| 2010 | 0.007      | 0          | 0.04       | 0          | 0.1        | 0.05       |
| 2015 | 0.007      | 0          | 0.04       | 0          | 0.1        | 0.05       |
| 2020 | 0.007      | 0          | 0.04       | 0          | 0.1        | 0.05       |


### Environmental impacts

Greenhouse gas emissions

  + Light vehicles calculated by household
  + Regional heavy truck and transit emissions

| Fuel type                                               | Carbon intensity <br> (g per mega joule ) |
|---------------------------------------------------------|---------------------|
| Ultra-low sulfur diesel (USLD)                          | 77.19               |
| Biodiesel                                               | 76.81               |
| Reformulated gasoline (RFG)                             | 75.65               |
| CARBOB (gasoline formulated to be blended with ethanol) | 75.65               |
| Ethanol                                                 | 74.88               |
| Compressed natural gas (CNG)                            | 62.14               |

Criteria emissions

  + Emission rates from MOVES 2010a database
  + Volatile organic compounds (VOC)
  + Carbon monoxide (CO)
  + Oxides of nitrogen (NOx)
  + Sulfur dioxide (SO2)
  + Particulate matter (PM)

### Financial & economic impacts

Regional highway infrastructure costs

  + FHWA Highway Economic Requirements System (HERS)
  + Construction costs per lane mile in 2002 dollars
  
| Functional <br> Classification  | Small Urban | Small <br> Urbanized | Large <br> Urbanized      |
|----------------------------|--------------|--------------|--------------|
| Freeways                   | $3.1 - $11.1 | $3.4 - $12.1 | $5.7 - $60.0 |
| Principal Arterial         | $2.6 - $9.4  | $2.9 - $10.2 | $4.2 - $15.0 |
| Minor Arterial / Collector | $2.0 - $7.0  | $2.1 - $7.4  | $2.9 - $10.2 |

Regional transit infrastructure and operating costs

  + National Transit Database (NTD)
  + Net cost to supply an unlinked passenger trip by mode (2009)
  
| Mode          | Capital Cost | Operating <br> Cost      | Total Cost | Fare Revenue | Net Cost |
|---------------|--------------|-----------|------------|--------------|----------|
| Bus           | $0.71        | $3.40     | $4.11      | $0.91        | $3.20    |
| Heavy Rail    | $1.78        | $1.80     | $3.58      | $1.09        | $2.49    |
| Commuter Rail | $5.74        | $9.80     | $15.54     | $4.69        | $10.85   |
| Light Rail    | $7.82        | $3.00     | $10.82     | $0.78        | $10.04   |

Annual traveler cost - fuel

  + $0.585 per mile in 2010 for auto users
  + Includes variable costs (gas, oil, maintenance and tires) and fixed costs (insurance, license, registration, taxes, depreciation and finance charges)
 
Annual travler cost - travel time

  + Urban Mobility Report (TTI)
  + Average travel delay for each metropolitan region
  + Only includes auto users
  
### Location & community impacts

Relative increase in jobs accessibility by auto

  + Function of distribution of growth by place type
  + Weighted by population and employment growth
  
Livability

  + FTA criteria
  + Use of alternative modes
    - transit vehicle trips
	- bike ownership
  + Mixed use land use
    - mixed use place type
    - transit oriented development place type
  + Household transportation expenditures as a function of budget
  + Use of alternative modes by low income households
  
Equity impact

  + Regional accessibility by income group
  
### Community impacts

Public health impacts and costs

  + Road safety impacts (daily VMT * 347 = annual VMT)
    - Fatal = 1.14 per 100 million VMT
	- Injury = 51.35 per 100 million VMT
	- Property damage = 133.95 per 100 million VMT
  + Amount of walking (proxy for physical fitness)
  
    | D                      | Description                       | Walking increase |
    |------------------------|-----------------------------------|------------------|
    | Density                | Household / Population density    | 0.07             |
    | Diversity              | Land use mix (entropy)            | 0.15             |
    | Design                 | Intersection / street density     | 0.39             |
    | Regional accessibility | Job accessibility by auto         | 0                |
    | Distance to transit    | Distanct to nearest transity stop | 0.15             |

  + Emissions (PM, NOX, VOC)
  
### Visualizing performance metrics

**TODO:  UPdate this for VERPAT!**

<img align="center" width="500" border=1 src="VERPAT-Tutorial-images/performance_metric.png"> </img>

VERPAT's charting is very easy to use and follows a template so each chart can be easily interpreted

In this example, **scenarios 3 and 8** have the highest reduction in vehicle hours of delay (23-24%) due to additional lane miles.  **Scenario 4** includes ITS treatments, which also reduce congestion a significant amount.

[top](https://github.com/gregorbj/VisionEval/wiki/VERPAT-Tutorial#table-of-contents)
