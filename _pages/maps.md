---
title: "Maps"
layout: splash
permalink: /maps/
date: 2019-07-18T00:41:00-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/splash_bg_robotteam_2013-1.jpg
  caption: "One of the first competition robots I helped program and build in 2013"
---

A map of where I've been in the world. Definitely not an exhaustive list.

* ![Blue Icon](/assets/images/marker-icon-blue.png) - Cities I've lived in (points aren't specific homes)
* ![Green Icon](/assets/images/marker-icon-green.png) - Cities I've traveled to (and not just passed through, 2018-Present)
* ![Orange Icon](/assets/images/marker-icon-orange.png) - Airports I've been in, 2018-Present)

<div id="mapid"></div>

<script src="https://unpkg.com/leaflet@1.5.1/dist/leaflet.js"
   integrity="sha512-GffPMF3RvMeYyc1LWMHtK8EbPv0iNZ8/oTtHPx9/cc2ILxQ+u905qIwdpULaqDkyBKgOaB57QTMg7ztg8Jm2Og=="
   crossorigin=""></script>
<script>
  // Set up map
  var myMap = L.map('mapid').setView([30, -50], 3);
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
  }).addTo(myMap);
  
  // Set up marker colors
  var blueIcon = new L.Icon({
    iconUrl: '/assets/images/marker-icon-blue.png',
    shadowUrl: '/assets/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
  });
  var redIcon = new L.Icon({
    iconUrl: '/assets/images/marker-icon-red.png',
    shadowUrl: '/assets/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
  });
  var greenIcon = new L.Icon({
    iconUrl: '/assets/images/marker-icon-green.png',
    shadowUrl: '/assets/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
  });
  var orangeIcon = new L.Icon({
    iconUrl: '/assets/images/marker-icon-orange.png',
    shadowUrl: '/assets/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
  });
  var yellowIcon = new L.Icon({
    iconUrl: '/assets/images/marker-icon-yellow.png',
    shadowUrl: '/assets/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
  });
  var violetIcon = new L.Icon({
    iconUrl: '/assets/images/marker-icon-violet.png',
    shadowUrl: '/assets/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
  });
  var greyIcon = new L.Icon({
    iconUrl: '/assets/images/marker-icon-grey.png',
    shadowUrl: '/assets/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
  });
  var blackIcon = new L.Icon({
    iconUrl: '/assets/images/marker-icon-black.png',
    shadowUrl: '/assets/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
  });
  
  
  // Add markers
  // Loop this with data file

  // Homes
  L.marker([39.099728, -94.578568], {icon: blueIcon} ).addTo(myMap).bindPopup("<b>Kansas City, MO</b><br />Lived: Birth-2002, 2006-2018<br />Blue area is approximate range of areas I've lived");
  var circle = L.circle([39.174320, -94.577271], {
      icon: blueIcon,
      color: 'blue',
      fillColor: '#00f',
      fillOpacity: 0.2,
      radius: 25000
  }).addTo(myMap).bindPopup("<b>Kansas City, MO</b><br />Lived: Birth-2002, 2006-2018<br />Blue area is approximate range of areas I've lived");
  L.marker([37.215520, -93.292360], {icon: blueIcon} ).addTo(myMap).bindPopup("<b>Springfield, MO</b><br>Lived: 2002-2006");
  L.marker([40.442169, -79.994957], {icon: blueIcon} ).addTo(myMap).bindPopup("<b>Pittsburgh, PA</b><br>Lived: 2018-Present");

  // Visited
  //L.marker([, ], {icon: greenIcon}).addTo(myMap).bindPopup("<b></b>");
  L.marker([37.386051, -122.083855], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Mountain View, CA</b>");
  L.marker([39.768188, -94.848160], {icon: greenIcon}).addTo(myMap).bindPopup("<b>St. Joseph, MO</b>");
  L.marker([30.267153, -97.743057], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Austin, TX</b>");
  L.marker([41.081444, -81.519005], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Akron, OH</b>");
  L.marker([36.162663, -86.781601], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Nashville, TN</b>");
  L.marker([42.886448, -78.878372], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Buffalo, NY</b>");
  L.marker([38.627003, -90.199402], {icon: greenIcon}).addTo(myMap).bindPopup("<b>St. Louis, MO</b>");
  L.marker([44.977753, -93.265015], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Minneapolis, MN</b>");
  L.marker([41.454929, -82.710960], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Sandusky, OH</b>");
  L.marker([51.507351, -0.127758], {icon: greenIcon}).addTo(myMap).bindPopup("<b>London, United Kingdom</b>");
  L.marker([39.961178, -82.998795], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Columbus, OH</b>");
  L.marker([42.480202, -83.240997], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Southfield, MI</b>");
  L.marker([41.499321, -81.694359], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Cleveland, OH</b>");
  L.marker([40.678177, -73.944160], {icon: greenIcon}).addTo(myMap).bindPopup("<b>New York, NY</b>");
  L.marker([42.314938, -83.036362], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Windsor, ON</b>");
  L.marker([42.331429, -83.045753], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Detroit, MI</b>");
  L.marker([59.913868, 10.752245], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Oslo, Norway</b>");
  L.marker([59.666640, 10.635610], {icon: greenIcon}).addTo(myMap).bindPopup("<b>Drøbak, Norway</b>");

  // Airports
  L.marker([39.8533333333, -104.6755555556], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Denver International Airport</b><br />DEN");
  L.marker([37.3627777778, -121.9291666667 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Norman Y. Mineta San Jose International Airport</b><br />SJC");
  L.marker([39.29749999, -94.71388888 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Kansas City International Airport</b><br />MCI");
  L.marker([38.7472222222, -90.3613888889 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Lambert-St. Louis International Airport</b><br />STL");
  L.marker([40.4913888889, -80.2327777778 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Pittsburgh International Airport</b><br />PIT");
  L.marker([39.1791666667, -76.6688888889 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Baltimore/Washington International Thurgood Marshall Airport</b><br />BWI");
  L.marker([32.84722, -96.85167 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Dallas Love Field</b><br />DAL");
  L.marker([29.6455555556, -95.2788888889 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>William P. Hobby Airport (Houston)</b><br />HOU");
  L.marker([30.1944444444, -97.67 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Austin-Bergstrom International Airport</b><br />AUS");
  L.marker([36.12666666, -86.68194444 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Nashville International Airport</b><br />BNA");
  L.marker([41.7861111111, -87.7525 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Chicago Midway International Airport</b><br />MDW");
  L.marker([44.8816666667, -93.2208333333 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Minneapolis-Saint Paul International Airport</b><br />MSP");
  L.marker([39.8686111111, -75.2483333333 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Philadelphia International Airport</b><br />PHL");
  L.marker([51.47138888, -0.45277777 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>London Heathrow Airport</b><br />LHR");
  L.marker([41.97805555, -87.90611111 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Chicago O'Hare International Airport</b><br />ORD");
  L.marker([55.6136111111, 12.645 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Copenhagen Airport, Kastrup</b><br />CPH");
  L.marker([60.1952777778, 11.0994444444 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Oslo Airport Gardermoen</b><br />OSL");
  L.marker([40.6897222222, -74.175 ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>Newark Liberty International Airport</b><br />EWR");
  //L.marker([, ], {icon: orangeIcon}).addTo(myMap).bindPopup("<b></b><br />");
  
  
</script>