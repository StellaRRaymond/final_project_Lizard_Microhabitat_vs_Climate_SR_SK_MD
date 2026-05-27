Project Proposal

Project by: 
Sage K., Stella R., and Monique D. 

1.) Brief introduction/background

Microhabitats are small, localized areas within a larger habitat that often possesses unique environmental conditions.
The specialized conditions that animals experience often differ from broader climatic conditions but little is known about how much these two differ 
from each other from a data science point of view. When it comes to the Western Fence lizard (Sceloperus occidentalis), microhabitat temperature is especially
important for maintaining thermal homeostasis. As a part of a lizard physiology project to determine the relationship between daily activity patterns and microhabitat parameters,
fine scale temperature loggers (HOBOs) were placed at 11 different campuses in Southern California to record daily minimum and maximum temperatures.
By placing HOBOs in different microhabitats, researchers were able to record fine scale differences in temperatures and compare that to lizard observations. 
However, in most cases it is infeasible to collect microhabitat data on a broad spatial-scale. Each HOBO logger costs around $100 dollars, and maintaining them and processing the data is time consuming and can be expensive for labs with limited resources.
Alternatively, climate data exists that is available on several publicly available open source databases, such as PRISM and NOAA. While this data is easy to download and covers a broad spatial and temporal scale, 
it lacks fine scale measurements of temperature such as those experienced in microhabitats. For example, PRISM is a set of monthly, yearly, and single-event gridded data products of mean temperature and precipitation, max/min temperatures, and dewpoints, primarily for the United States, with years of record from 1895-01 to 2023-04 (PRISM Group, accessed May 2026). This data has been useful for providing ecologists with relevant and multi-scaled climate data for research pertaining to species and their responses to climate change (O’Donnell and Ignizio 2012), but when applied at smaller scales may miss the heterogeneous nature of climate, such as below the landscape scale (Strachan and Daly 2017). Using Sceloperus occidentalis as a case study, our goal is to compare the relative minimum and maximum daily temperatures from fine scale biologgers to broad scale climate data to assess the magnitude of  differences between reporting daily temperatures to better inform when it is more appropriate to use one over the other for asking ecological questions. 

2.) Main question (that we will be answering with our methodology): 

How does broad scale, publicly available climate data compare to fine scale microhabitat temperature data?

3.) Stretch Questions (the goal of asking the above question/further directions):

a.) Can publicly available climate datasets be used to accurately predict lizard activity (phenology and daily activity patterns)
b.) Are there differences in how broad scale temperature records scale with fine scale measurements when considering urban vs more wild habitats?

4.) Hypothesis/reasoning:

The use of fine scale, daily weather biologging may be a more accurate method for asking ecological questions pertaining to species that have specific daily temperature requirements such as Sceloperus compared to more commonly used methods for gathering climate data such as using publicly available climate data like Prism. 

Prediction 1: If broad scale climate data is statistically similar to hobo temperature data across sites at different elevations, then the use of climate data may be useful to answer ecological questions pertaining to the activity levels of ectotherms.

Prediction 2: If there is a statistically significant difference between climate data and hobo data, then ecologists should consider deploying localized biologging sensors as opposed to relying on climate data when studying species with physiology that depends on specific daily temperature requirements. 

5.) Data science/analytical approaches we plan to use

We plan to take hobo logger data and extract daily averages, min, and max temperature values and make a model to compare those values to the same values from a PRISM climate dataset. We will also build our model to compare temperature parameters between sites and across elevations. 

6.) Data science tools we plan to develop

As a part of building our model, we will make several functions for processing and downloading data:
Develop a function that changes fahrenheit to celsius 
Develop a function to calculate daily averages from PRISM climate data
Develop a function to import multiple files containing climate data
Develop a function to filter data points were hobo logger was experiencing direct sunlight
Develop a function for making maps for campuses where temperature biologgers were deployed

7.) Project updates

Week 8.)
Built code for importing data: 
    Calculated daily min, max, and averages for HOBO data
Built code for cleaning data: 
    cleaned both data sets (HOBO and PRISM). Renamed column headers so they matched. Turned columns into proper date format
Data join PRISM and HOBO data
Built code for processing data (temperature conversion, calculating averages)
    created function for converting Farenheit to celsius for the entire dataset
Began statistical analysis (ANOVA for between sites, T-test for between PRISM and HOBO logger groups)
LGM for including elevation and site as variables
Started making a figure for report/presentation

Week 9.)
Finalize statistical analysis 
Interpret statistical test
Build maps

Week 10.)
Wrap up loose ends
Clean up code
Finalize QMD 
Sort out github

8.) Literature cited
O’Donnell, M.S., and Ignizio, D.A., 2012, Bioclimatic predictors for supporting ecological applications in the conterminous United States: U.S. Geological Survey Data Series 691, 10 p.

PRISM Group, Oregon State University, https://prism.oregonstate.edu, accessed 13 May 2026.

Strachan, S., and C.Daly (2017), Testing the daily PRISM air temperature model on semiarid mountain slopes, J. Geophys. Res. Atmos., 122, 5697–5715, doi:10.1002/2016JD025920.
