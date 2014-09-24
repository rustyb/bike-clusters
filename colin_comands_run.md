**Downloaded data from the following:**

- NYC Bike Share Monthly System O/D Trip Data -  [www.citibikenyc.com/system-data](http://www.citibikenyc.com/system-data)
- NYC Bike Stations - [www.citibikenyc.com/stations/json](http://www.citibikenyc.com/stations/json)

### Data Download URL:
Sub in **YYYYMM **with desired year. Ranges from 201307 -> 201408 as of 24.09.14

https://s3.amazonaws.com/tripdata/YYYYMM-citibike-tripdata.zip

###Commands Run

    awk -F "," -v OFS=',' '{print $1,$5,$6}' stations.txt`