# Surfs Up

## Overview 
In this project , we are analysing the temperature trends in Oahu,Hawaii in opening the Surf shop with the help of investor W.Avy. The investor requested the temperature data for specific months of June and December to determine if the Surf and ice cream shop business is sustainable year around.
The Investor W.Avy, provided us the sqlite database containing temperatures recoded in Hawaii from 2010 to 2017 by various weather observation stations. In order to check , if the business is sustainable both in summer and winter months , the investor W.Avy decided to analyze the month of June and December in Oahu as the starting point for a potential Surf and ice-cream shop.

## Data Source :
 SQLAlchemy, SQLite,Python, Jupyter Notebook


## Results :
 
### Queries for June and December 

Below are the queries for extracting the June and December temperatures

* Query for extracting June Temperatures
    ```javascript
    june_results = session.query(Measurement.date,Measurement.tobs).\
        filter(extract('month',Measurement.date)==6).all()
    ```
     <img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/June_Temps.png" width=300/>

* Query for extracting December Temperatures

    ```javascript
    december_results = session.query(Measurement.date,Measurement.tobs).\
        filter(extract('month',Measurement.date)==12).all()
    ```
    <img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/December_temps.png" width=300/>
    
The Below is combined temperature list where we can compare side by side together.

    <img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/Combined_temps.png" width=430/>


### June Temperatures Statistics

June statistics show that there are 1700 data entrees with mean temperature in Oahu being 74.9 F . The lowest it can go is 64 F and high being 85 F. This show a 20 degree variation in data.
     
<img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/June_stats.png" width=250/>

However, the December data shows that there are 1517 data entrees with mean temperature in Oahu being 71.04 F. The lowest it reaches is 56 F and highest being 83 F. This shows a 27 degree varaiation in data

### December Temperatures statistics
<img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/Dec_stats.png" width=260/>

### June Vs December Statistical comparison
<img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/June_Dec_Stats.png" width=320/>



## Summary
 Based on the mean temperature statistics, we can see that , the temperatures are very ideal. The mean temperatures of June representing summer show 75 F and December temperatures representing winter drops to 71 F. Since both the temperatures are ideal , it looks a prefect place for the tourist to visit.

 ### <b>Histogram Plots to visualize the data</b>


*  <b>Histogram of June Temperatures </b>

  The Histogram chart shows that most of temperatures falls between  71 and 79 F. This shows that Summer are extremely good for Surf shop business

<img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/JuneTemps.png" width=550/>


* <b>Histogram of December Temperatures</b>

  The Histogram chart of December shows that the temperatures mostly fall between 66 F and 76 F. The high peak shows that many days in December have 72 F . Although there are temperatures drop in December compared to summer, it is not as bad since its only few degrees less than summer months.

<img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/DecemberTemps.png" width=550/>


* <b>Histogram of Combined Temperatures</b>

    The combined histogram gives a clear picture of the both the months together. We can see that June data is slight skewed to right than December and the weather mostly varies between 66 F and 77 F, indicating a favorable weather for the tourists visitng Oahu.
    
<img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/June_Dec_Temps.png" width=550/>


### <b>Box Plots to check for check for possible outliers </b>

The box plot of June shows few outliers on the upper and lower limit. However , in December there are quite a few in the lower limit.
Although the image shows more outliers in the lower limit, they are however very close to each other.

<img src="https://github.com/hsurisetti/Surfs_Up/blob/main/images/BoxPlot.png" width=650/>


 Although, we know that the plots represents the outliers based only on the data, there could be other factors involved which we are not counting like precipitation, wind etc. But, looking at the temperatures and their possible outliers would give a rough idea about how optimal the weather might be for the tourists to visit. 


## Conclusion

Based on the above analysis , we can state that , Oahu is the best place to setup the Surf shop with summers being extremely nice and winters being slightly cool but not cold enough to be unpleasent which makes it ideal to open the shop year around.

