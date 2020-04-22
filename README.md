# COVID-19 Hospital Bed Shortage

The Corona Virus Pandemic is a global force impacting all facets of government, society, and health. Although it is tough to determine when a realistic end point for this situation would be, it is clear that changes need to be made for us to be able to accomodate with the variable circumstances. A big problem here is resource allocation and supply chain issues. Hospitals specifically are being over worked. One factor to consider is hospital beds. 

## Business Question: What counties across the US are most at risk for not being able to serve their citizens from a health perspective?

Some places have been harder hit than others. As not all the problems can be solved all together, it is crucial that we are efficient and methodical in our approach. We want to know where the problem hotspots are, specifically with lack of beds and resources to serve the local community. In this manner, resource allocation can be effecitvely prioritized.

## Data Question: What data and metrics can show if hospitals are capable of serving local communities?

I will use data from the following sources to assess our business question:

[Johns Hopkins University Center for Systems Science and Engineering](https://github.com/CSSEGISandData/COVID-19) (COVID-19 case, death, recovered data)
[Homeland Infrastructure Foundation-Level](https://hifld-geoplatform.opendata.arcgis.com/datasets/hospitals) (US Hospital Data)

## Data Answer

To be able to answer the question, I obtained county-level USA data regarding confirmed, cumulative COVID Cases, active cases, and number of hospital beds available at hospitals across the US. From here various data cleaning, merging, and visualization steps were followed, as indicated in the Jupyter Notebook attached above. The final calculated metric at the county level was a "shortage of hospital beds" which was determined by the difference between available hospital beds and the number of active cases. As can be seen, this is not a problem for much of the US. The few areas which are significantly impacted include the North East, particularly New York and Boston, as well as several counties in Arizona. 

![alt text](https://github.com/PaarthSharma98/COVID-19_Hospital_Bed_Shortage/blob/master/Figures/Hospital_Bed_Shortage.png)

## Business Answer
At a surface level, one can ascertain that New York City and much of the counties in Arizona are locations where the number of active cases outweighs the bed availability. With regards to the othe public data, this certainly makes sense as New York has some of the highest number of cases in the country. However, this is certainly faulty for Arizona which only has about 4000 confirmed cases to date. Part of this could be improper cleaning in the data source (perhaps a -999 value could be associated as a symbol instead of NaN). 
