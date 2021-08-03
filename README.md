UPenn Project One – “It’s the Hot Knock Life”
* Colleen Daily, Hao Dong, Stefan Johnson, and Ana Stefanski

Hypothesis: With climate change, we predict that there is a greater strain on quality of life. 

We are defining climate change as extremes in both heat index, wind speed, and precipitation. The quality-of-life measures are defined by crime rates, property values, and traffic fatalities.  We chose four of the most populous cities in the United States: New York, Los Angeles, Chicago, and Philadelphia. While we understand that climate change is a global issue, measuring our hypothesis with U.S. cities allows us to measure climate change on quality of life without having to resolve socioeconomic factors that would interfere with measuring the data set.

Data Retrieval and Cleaning: The data retrieval process for quality-of-life measures began by finding the Open Data Websites for the four major cities. This provided us with the data for our crime rates. Next, the traffic fatality data was found at the website for the National Highway Traffic Safety Administration. Lastly, property values were obtained by accessing the Federal Housing Finance Agency website.  Our weather data by city was found at Meteostat.net, which provided historical weather data in temperature, wind speed, and precipitation.

After assessing all the data sets it was determined that we would have to find the data for years that appeared in all the data sets. While we initially tried to retrieve data for a ten-year span, we were limited by the extent to which data was kept over 10 years ago. We were able to find data across all data sets that matched the years of 2012 and 2019. Because of this, we then pivoted to assessing our data over a seven-year span.

As you can imagine, the largest data set was for crime rates, with more than 7 million lines of data. To efficiently clean the data, the csv files were imported into Jupyter lab, and the data was “cleaned” by calling on the dates for the crimes reported.  Traffic Fatalities, Property Values, and Weather data sets were less cumbersome, thus allowing us to clean the csv files prior to import.

Questions for Hypothesis: 
1. Is there a correlation between climate change and traffic fatalities? 
2. Is there a correlation between climate change and crime? 
3. Is there a correlation between climate change and property prices? 
4. Is there a correlation between climate change and quality of life? 
5. Does 2012 have an increase or decrease in quality of life? 
6. Does 2019 have an increase or decrease in quality of life?

T tests were conducted on all metrics compared year over year, and the returned p values did not indicate a significant change in weather averages.  While the averages in the two years were not significantly different, it is clear that there are peaks in temperature that effect quality of life metrics.

The strongest argument can be made that climate change directly impacts traffic fatalities. When measuring the data for traffic fatalities, those months with the most fatalities are the same months with extreme heat and precipitation across all four of our cities. While one would think that cold temperatures along with precipitation in the form of snow would cause more fatalities, the months with rain and the hottest temperatures caused the most deaths. 

Is there a relationship between weather and crime? Any police officer you know would say yes. Our data proves that in the four cities measured, crime increases as the maximum temperature increases, that being the months between April and September. Without delving into the types of crimes committed, we will never know why, but one can assume it is because more people are out, taking vacations, socializing, etc. leaving them exposed to become victims of crime.

Can climate change effect property prices? Our data shows there is no correlation between the weather and property prices. Property prices do not show a significant increase or decrease based on the weather. While property prices increased from 2012 to 2019, the contributing factors to this would be based on the economy and income, not on the weather. 

With combining the metrics of crime, traffic fatalities and property prices, we can use these metrics to show the quality of life.  Measuring quality of life to climate change shows us that indeed, changes in weather does impact our daily lives, thus changing the quality of life overall. Increase in crime and traffic fatalities are small measures as to what one would determine the quality of our lives, but there is no direct correlation to these factors and the weather. To measure quality of life in 2012 versus 2019, we can deduce that in all four cities the quality of life in 2019 is better than that of 2012. With less crime, traffic fatalities, and a steady property market, 2019 seems to be less affected by climate change than in 2012.  The limitation of this data set cannot conclusively prove our hypothesis, our hypothesis can only be determined by analyzing decades of data. 
Does this mean that climate change isn’t real? Absolutely not.  Climate change is defined by the human-induced emissions of greenhouse gases and the resulting large-scale shifts in weather patterns. Our measures of the weather data produce evidence of the shifts in weather patterns, thus proving that climate change is real, and has the potential to affect the quality of life for all of us. 


Data Sources:
NYC Crime: Need to combine felony, misdemeanor and violation 2000-2020 
https://www1.nyc.gov/site/nypd/stats/crime-statistics/historical.page 
LA Crime Index 2000-2019:
https://data.lacity.org/Public-Safety/Crime-Data-from-2010-to-2019/63jg-8b9z 
Chicago Crime 2000-present:
https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2 
Philadelphia Crime Rates:
https://www.opendataphilly.org/dataset/crime-incidents 
Traffic Fatalities:
https://www.nhtsa.gov/crash-data-systems/fatality-analysis-reporting-system
Property Values:
https://www.fhfa.gov/DataTools/Downloads/Pages/House-Price-Index-Datasets.aspx#mpo 
Weather Data:
https://meteostat.net/en


R-values:

--Correlation Coefficient for 2012—
x_values = 
y_values = 
correlation_matrix = np.corrcoef(x_values, y_values)
correlation_xy = correlation_matrix[0,1]
r_squared = correlation_xy**2

2012 Max Temp vs Traffic
Chicago , r^2 = 0.20148554509136435
LA, r^2 = 0.114452496849059
NY,  r^2 = 0.03
Philly, r^2 = 0.22941359932697558

2012 Max Temp vs Crime
Chicago, r^2 = 0.8735903131126331
LA, r^2 = 0.04946906130933052
NY, r^2 = 0.8314233307168056
Philly, r^2 = 0.8029501430609822

2012 Max Precipitation vs Traffic
Chicago, r^2 = 0.4150585718047978
LA, r^2 = 0.18218335595906493
NY, r^2 = 1.4195055906698547e-06
Philly, r^2 = 0.09187022917104579


2012 Max Precipitation vs Crime
Chicago, r^2 = 0.26698386032667504
LA, r^2 = 0.19057223869246342
NY, r^2 = 0.0004191589340197248
Philly, r^2 = 0.007793726609579096


2012 Max Wind Speed vs Traffic
Chicago, r^2 = 0.11344919162775263
LA, r^2 = 0.20921869909064042
NY, r^2 = 0.10272216882536239
Philly, r^2 = 0.10416381289611724


2012 Max Wind Speed vs Crime
Chicago, r^2 = 0.18903601169341003
LA, r^2 = 0.2480903145058827
NY, r^2 = 0.22084684024222356
Philly, r^2 = 0.36746443468614165


--Correlation Coefficient 2019 --
2019 Max Temp vs Traffic
Chicago , r^2 = 0.34621455901279696

LA, r^2 = 0.0006906527549468788

NY,  r^2 = 0.030268182103342242

Philly, r^2 = 0.03334403654601978


2019 Max Temp vs Crime
Chicago, r^2 = 0.8254694719673792
LA, r^2 = 0.04243998526844447

NY, r^2 = 0.6805663063820073

Philly, r^2 = 0.8062517010725668


2019 Max Precipitation vs Traffic
Chicago, r^2 = 0.0052456978631169136

LA, r^2 = 0.004346715788505352

NY, r^2 = 0.2732723885129301

Philly, r^2 = 0.038054863017089144


2019 Max Precipitation vs Crime
Chicago, r^2 = 0.15612646144519668

LA, r^2 = 0.34219071211401864

NY, r^2 = 0.42081749784046973

Philly, r^2 = 0.08846571198542162



2019 Max Wind Speed vs Traffic
Chicago, r^2 = 
LA, r^2 = 
NY, r^2 = 
Philly, r^2 = 


2019 Max Wind Speed vs Crime
Chicago, r^2 = 
LA, r^2 = 
NY, r^2 = 
Philly, r^2 = 






