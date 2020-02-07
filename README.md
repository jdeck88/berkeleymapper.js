# berkeleymapper.js

A 100% javascript implementation for berkeleymapper.  
The goal is to create a simple method for calling berkeleymapper like the following (NOTE
that we borrow heavily from Leaflet):
```
<head>
  <link rel="stylesheet" href="ROOT_URL/berkeleymapper.css">
  <script src="ROOT_URL/berkeleymapper.js"></script>
</head>
<body>
   <div id="mapid" style="width: 600px; height: 400px;"></div>
</body>
<script>
  var mymap = B.map('mapid').init('REMOTE_TABFILE','REMOTE_CONFIGFILE');  
</script>
```

Libraries to incorporate:
 * Leaflet
 * D3 (for charting)
 * Geo-processing functions: 
     * https://turfjs.org/
     * https://github.com/geoscript/geoscript-js
