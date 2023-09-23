# Irish Residential Property Price Register (RPPR) Analysis

The goal of this project was to gain insight into the Irish property market. At the time this project was being conducted, Ireland was in the midst of a housing crisis with homelessness at an all time high. This project looks at identifying any trends in residential property sales over the last 12 years. 

Below is the developmental process which took place.

## Data Used

The data comes from the [Residential Property Price Register (RPPR)](https://www.propertypriceregister.ie/website/npsra/pprweb.nsf/page/ppr-home-en). The Residential Property Price Register is produced by the Property Services Regulatory Authority (PSRA). At the time of project commencemnt, the data included Date of Sale, Price and Address of all residential properties purchased in Ireland since the 1st January 2010, until 5th May 2023, as declared to the Revenue Commissioners for stamp duty purposes. In this analysis, we focus on using the data collected by RPPR to build a data analytics solution for residential property price prediction.

## Data Cleaning

Multiple data cleaning procedures were undertaken to prepare the data for analysis, such as:
- Removing special characters and whitespace from feature names and Price data
- Removing duplicate rows.
- Converting feature values in Irish to their English translation.
- Dropping the Eircode feature as it had a large amount of null values.
- Removing outliers.

The full cleaning process can be found in the [Cleaning and Analysis Notebook](Residential_Property_Price_Register(RPPR)_Cleaning_&_Analysis.ipynb).

## Analysis & New Features

Once cleaned, the data was analysed in the notebook using matplotlib. In addition, a Tableau dashboard can be found [here](https://public.tableau.com/views/RPPR_20102023/IrishResidentialPropertySales010110-030523?:language=en-US&:display_count=n&:origin=viz_share_link). Some key findings are as follows:
- Over 80% of properties sold since 2010 have been second-hand. Dublin has the highest amount of properties sold, implying that there is a high demand for Dublin properties, yet it doesn't have one of the highest percentages of new houses sold. The two counties with the highest rates of new properties are Kildare and Meath, which neighbour Dublin, suggesting that if people can't get housing in Dublin, they will try to live nearby.
- The age of a property does not have an effect on whether a seller will get full market price for it. There does not appear to be a relationship to the price of a property and its age.
- The prices of new properties do not have VAT included in the price.
- Property prices appear to increase with the size of the property.
- There appears to be a relationship between the price of a property and its proximity to Dublin, with surrounding counties have the next highest average prices per county after Dublin.

Four new features were derived from the cleaned dataset to gather further insight into prices. These are Dublin Postal Code, Month of Sale, Year of Sale and Geolocation. Analysis of these new features resulted in some more findings:
- Dublin 15 appears to be a newly desirable area to live as it has the highest number of properties sold and the fourth highest rate of new properties sold in Dublin.
- Dublin 18 and County Dublin have the largest proportions of new houses sold compared to second hand houses. These areas are further out from the city centre than most other postal code areas which may indicate it is easier to build new properties further outside the city center.
- Dublin 4 appears to have the largest range of prices for Dublin properties, showing a high variability in price. High outliers seem to suggest a high demand with buyers more than willing to pay a high price. 
- Dublin 6 properties have the highest average Price, followed by Dublin 4, Dublin 14 and Dublin 6W. Interestingly, these are all areas south of the River Liffey. The highest prices in the northside are located in Dublin 3, which has the 7th highest average price per area code.
- It appears the amount of properties sold per month trends upwards throughout the year with total properties sold peaking in December.
- The average property price in Ireland has been increasing since 2012.
-  Most of the properties above or equal to the 75th percentile in price appear to be South Dublin. Most properties within this price range appear to be closer to the coast, regardless of whether the area is North or South of the River Liffey.