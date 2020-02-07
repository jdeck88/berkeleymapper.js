# berkeleymapper.js

With the advent of better javascript libs for handling mapping and geoprocessing, it is now feasible to create a pure javascript implementation of Berkeleymapper that can be easily embedded in calling web sites.  This change will give calling sites more options for integrating the features of berkeleymapper while eliminiting much of the overhead in maintaining a standalone website.  In addition, we propose to bundle additional graphing and charting functions to work with datasets, expanding the available features.  

Following is an example of how berkeleymapper.js will be called from a web-page:

```
<head>
  <link rel="stylesheet" href="URL_ROOT/berkeleymapper.css">
  <script src="URL_ROOT/berkeleymapper.js"></script>
</head>
<body>
   <div id="mapid" style="width: 600px; height: 400px;"></div>
</body>
<script>
  // The datafile can be something we already have in Javascript memory, or can 
  // be a pointer to a remote URL
  var mymap = B.map('mapid').init('DATAFILE','CONFIGFILE');  
</script>
```

Libraries to incorporate:
 * Leaflet
 * D3 (for charting)
 * Geo-processing functions: 
     * https://turfjs.org/
     * https://github.com/geoscript/geoscript-js
