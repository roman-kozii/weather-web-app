
## Weather Web app

PHP web app to import weather forecast data from BMKG, and add it to the MYSQL database, so that if you need to retrieve weather data you can query directly without having to query again to the BMKG server

What do I do with this data?

My application can search for the nearest region from the table **t_region**, so that the weather displayed is according to the nearest region, on Android I created a SQLITE version and I query the nearest region from there, then take the weather data to the server.

This script can be run in a browser or in the command line, but it's best to run it in the command line and use [crontab](https://crontab.guru/#0_3_*_*_*) so that it is executed at the specified time

And remember, that you have to tell us if the data is from BMKG.

## Installation

Copy **config.example.php** to **config.php**
replace the contents with your database configuration
import **bmkg.sql** into your database
in the **bmkg.php** file at the bottom, **delete** the **git** section
unless you want to host the data on Github too

# Use it directly?

prepare endpoint url
```https://ibnux.github.io/BMKG-importer/```

from the app, download the region.json file
```https://ibnux.github.io/BMKG-importer/cuaca/region.json```

From the json, calculate the user's location with the nearest area, or the user chooses himself.

then download the weather in the selected area based on the code
```https://ibnux.github.io/BMKG-importer/cuaca/idWilayah.json```

example:
```https://ibnux.github.io/BMKG-importer/cuaca/501233.json```

adjust the weather code with the icon in the icon folder
```https://ibnux.github.io/BMKG-importer/icon/5.png```


# Example
check folder **examples**
- [HTML](example/html/)
- [PHP](example/php/index.php)


#### Source
- [BMKG](http://data.bmkg.go.id/prakiraan-cuaca/)
- [ICON](http://www.iconarchive.com/tag/weather)
- [Medoo](http://www.iconarchive.com/tag/weather)



Please use it for your needs
