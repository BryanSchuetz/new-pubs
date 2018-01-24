---
title: About
date: 2015-11-06 18:37:00 -05:00
permalink: "/about/"
layout: page
---

The field of Information and Communications Technology for International Development (ICT4D) continues to vex development practitioners who want to deliver concrete results, at scale, in measurable ways. At DAI, we’ve been working in ICT4D for more than a decade. We’ve experienced the exhilarating moments when a project works better than expected, and the disappointment when it fails. We believe there is enormous potential in Digital for Development, and we know there is plenty of room for learning and improvement. We launched this blog as part of our own learning process, in the hope that our peers in the Digital for Development community will come along for the ride.

The scope of this blog is broad. We’ll bring you field insights from places as diverse as Afghanistan and El Salvador, Haiti, and Indonesia. We’ll review new tools and reflect on global ICT4D events. We’ll ruminate on digitizing physical addresses, offer a lesson on data mining, and recount what we learned hanging out with smartphone-savvy twentysomethings in Kabul. And whatever we do, we’ll try to do it in a way that will bring you back for more.

<iframe src="http://ictmap.s3-website-us-east-1.amazonaws.com/"></iframe>

<head>

    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css" integrity="sha512-Rksm5RenBEKSKFjgI3a41vrjkw4EVPlJ3+OiI65vTjIdo9brlAacEuKOiQ5OFh7cOI1bkDwLqdLw3Zg0cRJAAQ==" crossorigin=""/>
    <script src="https://unpkg.com/leaflet@1.3.1/dist/leaflet.js" integrity="sha512-/Nsx9X4HebavoBvEBuyp3I7od5tA0UzAxs+j83KgC8PU0kgB4XiK4Lfe4y4cgBtaRJQEIFCW+oC506aPT2L1zw==" crossorigin=""></script>
    <script src="data.js"></script>
</head>
<body>
<div id='map' style='width: 100%; height: 100%'></div>


<script>

	

	var mbAttr = 'Map data &copy; <a href="http://openstreetmap.org">OpenStreetMap</a> contributors, ' +
			'<a href="http://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, ' +
			'Imagery © <a href="http://mapbox.com">Mapbox</a>',
		mbUrl = 'https://api.tiles.mapbox.com/v4/{id}/{z}/{x}/{y}.png?access_token=pk.eyJ1IjoibWFwYm94IiwiYSI6ImNpejY4NXVycTA2emYycXBndHRqcmZ3N3gifQ.rJcFIG214AriISLbB6B5aw';

	var streets  = L.tileLayer(mbUrl, {id: 'mapbox.streets',   attribution: mbAttr}),
		grayscale   = L.tileLayer(mbUrl, {id: 'mapbox.light', attribution: mbAttr});
		

	var map = L.map('map', {
		center: [0, -0],
		zoom: 2,
		layers: [cities, streets]
	});

	var baseLayers = {
		"Streets": streets,
		"Grayscale": grayscale,
	
	};

	var overlays = {
		"Cities": cities
	};


var cities = L.layerGroup();

	L.marker([15.78, -90.25]).bindPopup('Guatemala.').addTo(cities),
	L.marker([18.97, -72.28]).bindPopup('El Salvador.').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Haiti.').addTo(cities),
	L.marker([18.73, -70.162]).bindPopup('The Dominican Republic').addTo(cities),
	L.marker([14.49, -14.45]).bindPopup('Senegal').addTo(cities),
	L.marker([6.428, -9.423]).bindPopup('Liberia').addTo(cities),
	L.marker([7.94, -1.023]).bindPopup('Ghana').addTo(cities),
	L.marker([-1.940, 29.87]).bindPopup('Rwanda').addTo(cities),
	L.marker([0.023, 37.90]).bindPopup('Kenya').addTo(cities),
	L.marker([5.15, 46.19]).bindPopup('Somalia').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Sudan').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Iraq').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Jordan').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Afghanistan').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('India').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Cambodia.').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Indonesia').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Morocco').addTo(cities),
	L.marker([39.77, -105.23]).bindPopup('Palestine').addTo(cities);
	
</script>
</body>


