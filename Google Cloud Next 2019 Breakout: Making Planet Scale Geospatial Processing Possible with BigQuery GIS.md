# Google Cloud Next 2019 Breakout: Making Planet Scale Geospatial Processing Possible with BigQuery GIS
#gcp #cloud

* Descartes Labs - Founding team from Los Alamos National Laboratory 2014 Santa Fe, NM
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_102628.jpg)
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_102837.jpg)
* BigQuery GIS available
	* features
		* see picture

![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_102340.jpg)


* train model that can identify boat type by it’s pattern
* find the “dark fleet”
	* mostly likely ships that don’t send out AIS pings are a part of the dark fleet
	* use Sentinel-1 to process coastlines
		* ~1 PB data
		* use Google Earth Engine
			* data catalog + computation platform
		* do smart interpolation to match detected ships and AIS datasets in BigQuery
			* do JOIN on AIS data (WKT) and identify which vessels match up with detections from radar
			* see picture
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_103357.jpg)
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_104938.jpg)
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_105207.jpg)
* BigQuery GIS
	* S2 Geometry Library
		* low-level library doing geometry on earth’s surface
		* open source
		* https://s2geometry.io
		* https://github.com/google/s2geometry
		* see picture
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_110118.jpg)
	* compute the coverage of every shard of data
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_110118%202.jpg)
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_110239.jpg)
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_110316.jpg)
	* prune out partitions
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_110527.jpg)
![](Google%20Cloud%20Next%202019%20Breakout:%20Making%20Planet%20Scale%20Geospatial%20Processing%20Possible%20with%20BigQuery%20GIS/20190411_110738.jpg)