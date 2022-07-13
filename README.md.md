# COVID-19  DASHBOARD TRACKER (JAN 2020 - JULY 2022)

## Introduction
Covid-19 is a viral communicable respiratory disease that has led to loss of lives of millions of poeple across the globe. With increasing medical interventions such as vaccines and medication, this analysis seeks to investigate if the disease is being contained. The number of reported confirmed cases and deaths will help to provided this insight.  
## Data Source
The dataset for this analysis was got from [JHU CSSE COVID-19 Data ](https://github.com/CSSEGISandData/COVID-19 "JHU CSSE COVID-19") repository. The data for [global confirmed cases](https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv) was imported into Microsoft Excel using the URL of the web page.
## Data Cleaning and Transformation
Data cleaning was done using Power Query editor in Microsoft Excel. The transformations were applied in the following order:
1. The number of columns was removed from the "source" tab to enable refreshing of the data in real time
1. All first rows were promoted to headers
1. The data format was changed from wide to long data by unpivoting the date columns.
1. The new columns were appropriately renamned and their types changed.
1. Next, the [global deaths](https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_global.csv) and [global recovery](https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_recovered_global.csv) datasets were similarly imported and same transformations applied to them.
1. Finally, the three tables were merged as one.

## Data Analysis
Before analysis was done, the date column was expanded into 'year', 'month' and 'day' columns using Excel text functions. The data was summarised using pivot tables. Instead of expressing them as 'sum of ...', they were expressed as 'max of ...' due to the cumulative nature of the dataset. The **sort** and **filter** functions were extensively used to sieve relavant data. 

## Data Visualization
The pivot tables were converted into charts and maps. The dashboard was designed in Microsoft Excel by dragging and dropping relevant charts.

## Limitations
The dataset showing number of recovered cases topped being updated from 5th August 2021. Thus the data was not included in the analysis.
