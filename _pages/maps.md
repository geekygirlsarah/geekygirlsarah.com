---
title: "Maps"
layout: splash
permalink: /maps/
date: 2019-07-18T02:48:00-04:00
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
* ![Red Icon](/assets/images/marker-icon-red.png) - Countries I have been to (2018-Present)

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
  // (they're backward from listed at top to put blue on top, green next, then orange)

  // Countries
  {% for item in site.data.travels.countries %}
    L.marker([{{ item.latitude }}, {{ item.longitude }}], {icon: redIcon}).addTo(myMap).bindPopup("<b>{{ item.name }}</b>");
  {% endfor %}  

  // Airports
  {% for item in site.data.travels.airports %}
    L.marker([{{ item.latitude }}, {{ item.longitude }}], {icon: orangeIcon}).addTo(myMap).bindPopup("<b>{{ item.name }}</b><br />{{ item.code }} ");
  {% endfor %}  

  // Visited
  {% for item in site.data.travels.visited %}
    L.marker([{{ item.latitude }}, {{ item.longitude }}], {icon: greenIcon}).addTo(myMap).bindPopup("<b>{{ item.name }}</b>");
  {% endfor %}  

  // Homes
  {% for item in site.data.travels.lived %}
  L.marker([{{ item.latitude }}, {{ item.longitude }}], {icon: blueIcon} ).addTo(myMap).bindPopup("<b>{{ item.name }}</b><br />Lived: years");
  {% if item.radius %}
  var circle = L.circle([{{ item.latitude }}, {{ item.longitude }}], {
      icon: blueIcon,
      color: 'blue',
      fillColor: '#00f',
      fillOpacity: 0.2,
      radius: {{ item.radius }}
  }).addTo(myMap).bindPopup("<b>{{ item.name }}</b><br />Lived: {{ item.years }}");
  {% endif %}
  {% endfor %}  

</script>