# Web Scraper for Air Pollution Data in India (Central Pollution Control Board)

This project includes a Python 3 implementation to scrape Air Pollution Data for Indian Cities from the Central Pollution Control Board website. The Implementation uses
the Selenium Library to scrape data (for any number of Pollution measures) for all cities across any time period. 


### Requirements

ChromeDriver -- Download Chrome Driver Extension from https://sites.google.com/a/chromium.org/chromedriver/downloads
Python (>= 3.x), Selenium, bs4, pandas

### Usage

```
python scraper.py --dir C:\MyDirectory --driver C:\chromedriver.exe --output Data --p PM2.5 CO --sdate 01-01-2018 --edate 05-04-2018 --duration 1 Hour 
```

### Installing

To install the packages use the following code:

```
pip install -r setup.py
```


### Explanation

There are multiple parameters to be passed onto the command line.


```
--dir 	   : This refers to the Working directory in which the current file resides
--driver   : The full path of the Chrome Driver
--output   : The Folder inside the Working Directory where all the csv files would be saved
--p 	   : The list of parameters can pass multiple values
--sdate    : Date from which the data is required
--edate    : Date upto which the data is required
--duration : CPCB website provides data at different intervals. Specify the Interval at which the data is required
```

In the Usage code above I have my scraper.py file in 'MyDirectory' and the Chrome driver in C:\ drive, the Scraped files would get saved in 'MyDirectory/Data'.
I have passed the parameter arguments as PM2.5 and CO. The code will scrape hourly data for all cities between the dates 01-01-2018 and 05-04-2018.

Date Format -- "dd-mm-yyyy"

Duration Takes the Following values --

1. "15 Minute"
2. "30 Minute"
3. "1 Hour"
4. "4 Hours"
5. "8 Hours"
6. "24 Hours"
7. "Annual Average"

Any of the above entries can be passed in the --duration argument

The possible parameter values are:

1. NO
2. NO2
3. NOx
4. SO2
5. CO
6. Ozone
7. PM10
8. PM2.5
9. NH3
10. Rack Temp
11. AT
12. RH
13. WS
14. VWS
15. WD
16. SR
17. BP
18. RF
19. Benzene
20. Toluene
21. Eth-Benzene
22. MP-Xylene
23. Xylene


## Authors

* **Rachit Kamdar**


## Acknowledgments

* https://github.com/bhanu13/cpcb_air_quality
