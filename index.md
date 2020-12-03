## CLIM 680 Data Analysis

This page is dedicated to the different types of analyses preformed throughout the fall 2020 semester related to my project. The following analyses include: seasonal means, composites, correlation coefficient and linear regression.

## Project Description & Motivation

In my current research, I use hourly soil moisture values to understand how soil moisture content influences the initiation of organized convection. For this particular class, I used hourly soil moisture for homeworks 1 and 2. Using hourly data was a challenge for me, so for my project, I decided to use monthly soil moisture values instead. I wanted to assess the relationship (if any) that exists between soil moisture content and ENSO events. My thinking in choosing this pair was due to the known impacts of ENSO on precipitation globally. Precipitation directly impacts the regional soil moisture (due to rainfall or a lack thereof). While it is unlikely that soil moisture itself has an impact on ENSO, there could be an impact on soil moisture state from El nino and La nina events (i.e. increased precip/anomalously wetter soils, and vice versa). 

### Data Sources
-ECMWF ERA-40 Mean Monthly Soil Moisture (SWVL1)
- The entire ERA40 archive spans 45 years: September 1957 - August 2002
- 1.4° x 1.4° resolution

-Nino3.4 Index (calculated using the NOAA OISST data)
-Monthly mean values (1982 - 2019)

-Years used in analysis: 1982-2002 (20 years)

## Data Analysis

[Link to Seasonal Means of Soil Moisture](https://github.com/rgaal/clim680/blob/master/seasonal_means1.ipynb)

Firstly I wanted to plot the seasonal means of soil moisture to understand in general how it behaves year-round in different regions. Around the equator year-round there are higher soil moisture values due to the Inter-tropical Convergence Zone (ITZC) or the tropical rain belt. During boreal winter (northern hemisphere winter), there is increased soil moisture values in higher latitudes and extends further south, while boreal summer introduces lower soil moisture values in both northern and southern hemispheres. 

[Link to Composites](https://github.com/rgaal/clim680/blob/master/composites1.ipynb)

Next I wanted to look at composites. The composites of soil moisture anomalies during El Nino, La Nina, and Neutral events are all fairly identical, indicating that the mean soil moisture value made based on those certain conditions are not easily interpretable. By taking the difference of composites from El Nino-Neutral events, it is easier to see the subtle differences that only amount to a few percent in soil moisture. At the 95 % level, there are no areas of statistical significance indicating that it would be very difficult (and not smart) to base an estimate of soil moisture off of which phase of El Nino we are in. 

[Link to Correlation Coefficient](https://github.com/rgaal/clim680/blob/master/corr_coeff1.ipynb)

So far, there isnt any real relationship between the Nino 3.4 index and the soil moisture content. My next thought was to consider correlation to quantify how soil moisture at each point on the globe varies _lineraly_ with the Nino3.4 index. Red areas indicate that the soil moisture increases when Nino 3.4 goes up, and soil moisture decreases when Nino 3.4 goes down. Blue area indicate the oppposite: soil moisture increases when Nino 3.4 decreases and soil moisture decreases when Nino 3.4 increases. The values near zero indicate no relationship. 

At the 95% level, there is statistical significance over North America, the Middle East, and the southern portion of South America, suggesting soil moisture increases (associated with more rainfall) when there are higher values of Nino 3.4. There is also statistical significance over Australia, the northern portion of South America, and Southern Africa suggesting soil moisture decreases when there are higher values of Nino 3.4 (and an increase in soil moisture when there are lower values of Nino 3.4). The correlation coefficient values however are not extremely high, which indicates that these relationships might not be as robust compared to preforming a correlation test with precip and Nino 3.4.

[Link to Linear Regression](https://github.com/rgaal/clim680/blob/master/linear_regression1.ipynb)

Linear regression shoud give us a similar result to what we see in the correlation coefficient, however the magnitude of the regression coefficient will give us a better idea as to how good of a predictor Nino 3.4 can be for soil moisture state and vice versa. There are statistically significant areas (at the 95 % level) similar to our results from the correlation coefficient. However, the magnitude of the regression coefficient does not pass 1 (or -1) in any of these areas indiciating a weak linear relationship, or rather that they are not good predictors of one another. 

### Disclaimers & Other Notables

During my analysis, I struggled with adding the cyclic point to my data; I kept recieving an error that my longitudes were not evenly spaced. I also attempted to calculate the EOFs associated with soil moisture content, but with the lack of relationship presented in the previous analyses I thought it would be more similar to the saying 'garbage in = garbage out'. 

