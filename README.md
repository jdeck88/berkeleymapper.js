# berkeleymapper.js

A proposed 100% javascript implementation for berkeleymapper.   Berkeleymapper currently runs as an installed java application.  Anyone can call Berkeleymapper with a configuration file and tab delimited text file, and the application creates a session for the user in a new browser window.  The issue with this is that there is alot of overhead in running and maintaining the application. Also, requiring spawning the application in a new browser window puts limits on implementations.  With the advent of better javascript libs for handling mapping functions it is now feasible to create a javascript library that can be easily embedded in calling web sites.  This gives sites more power for integration and adoption of Berkeleymapper.

Following is an example of how we can call berkeleymapper.js  (NOTE that we borrow heavily from Leaflet):
```
<head>
  <link rel="stylesheet" href="ROOT_URL/berkeleymapper.css">
  <script src="ROOT_URL/berkeleymapper.js"></script>
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
