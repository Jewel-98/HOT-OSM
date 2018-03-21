# Humanitarian OpenStreetMap

This is a reusable visualization of nursing homes(and retirement homes) for senior citizens(elder,older,pensioner) in India displayed using Mapbox GL.

## Prerequesites:

1.To download India.mbtiles,goto the following link and copy the link to india.mbtlies

 [https://osmlab.github.io/osm-qa-tiles/country.html](https://osmlab.github.io/osm-qa-tiles/country.html)

 Now run the following command on terminal

 `wget <link to india.mbtiles>`

 To unzip the india.mbtiles file:

 `gunzip india.mbtiles.gz`

2.Now run the following commands:

`sudo apt-get update

 sudo apt-get install git-core
 
 git --version
 
 git clone https://github.com/mapbox/osm-tag-stats.git

 cd osm-tag-stats

 <sudo> npm install

 <sudo> npm link`

3.Write a query to extract data from OSM using OSM tags in a JSON file.

    *Name the JSON file as **filter.json**
    
    *Save the [filter.json](https://github.com/Jewel-98/HOT-OSM/filter.json) file in the same folder as the india.mbtiles file
    
4.Now run the following command for data extraction:

 `osm-tag-stats --geojson=results.geojson --mbtiles="india.mbtiles" --filter='filter.json' --count`

 The result will be stored in results.geojson file.

 To view extracted data on map:
 Copy the contents of results.geojson on [https://geojson.io](https://geojson.io.)

5.To visualize map using Mapbox GL:
  Create an html file ([index.html](https://github.com/Jewel-98/HOT-OSM/index.html)) with data in results.geojson file.
  
 **View the visualized map on nursing homes for senior citizens [here](https://jewel-98.github.io/)**






