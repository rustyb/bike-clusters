**Downloaded data from the following:**

- NYC Bike Share Monthly System O/D Trip Data -  [www.citibikenyc.com/system-data](http://www.citibikenyc.com/system-data)
- NYC Bike Stations - [www.citibikenyc.com/stations/json](http://www.citibikenyc.com/stations/json)

### Data Download URL:
Sub in **YYYYMM **with desired year. Ranges from 201307 -> 201408 as of 24.09.14

https://s3.amazonaws.com/tripdata/YYYYMM-citibike-tripdata.zip

###Commands Run
To convert the stations.json to stations.txt using the GDAL library:

	ogr2ogr CSV -f stations.csv stations.json

To extract the columns we want (id, lat, long) from the csv file we can run the following:

    awk -F "," -v OFS=',' '{print $1,$5,$6}' stations.txt`

Now Remove the header rows from the NYC `data/nyc/stations1.txt` and save to `data/nyc_station_latlons.txt`



