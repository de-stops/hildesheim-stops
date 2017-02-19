# rvhi-stops

This is a simple script to download all [RVHI](http://www.rvhi-hildesheim.de) stops as [GTFS-compatible CSV](https://developers.google.com/transit/gtfs/reference/stops-file).

The script uses the following endpoint:

```
https://efa155.efa.de/efaws2/default/XML_COORD_REQUEST?mId=efa_www&language=en&itdLPxx_mapName=MRCV&coordOutputFormat=WGS84%5BGGZHTXX%5D&boundingBox=1&boundingBoxLU={minx}%3A{miny}%3AWGS84%5BDD.DDDDD%5D&boundingBoxRL={maxx}%3A{maxy}%3AWGS84%5BDD.DDDDD%5D&inclFilter=1&purpose=5&max=-1&coordListFormat=STRING&itdLPxx_mdvMapName=mdvMap_efaFullPanelMap&coordListOutputFormat=STRING&scale=13&outputFormat=JSON&type_1=STOP&inclDrawClasses_1=
```

It starts from bounding box `(6.2, 51.2, 11.6, 54.2)` and works down to smaller quadrants.

The script produces CSV output in the following format:

```
"stop_id","stop_name","stop_lon","stop_lat","stop_code"
"25721146","Hildesheim, Mittelfeld",9.9538184383,52.122492253299995,"de:3254:21146"
```

# Usage

```
npm install
node index.js
```

# Disclaimer

Usage of this script may or may not be legal, use on your own risk.  
This repository provides only source code, no data.

# License

Source code is licensed under [BSD 2-clause license](LICENSE). No license and no guarantees implied on the produced data, produce and use on your own risk.