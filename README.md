<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.3/dist/leaflet.css" integrity="sha256-kLaT2GOSpHechhsozzB+flnD+zUyjE2LlfWPgU04xyI=" crossorigin=""/>
    <script src="https://unpkg.com/leaflet@1.9.3/dist/leaflet.js" integrity="sha256-WBkoXOwTeyKclOHuWtc+i2uENFpDZ9YPdf5Hf+D7ewM=" crossorigin=""></script>
</head>
<style>
#map {width: 1900px; height: 950px}
</style>
<body>
    <div id="map"></div>
</body>
<script>
    var map_center = [-37.72941, 144.94258];
    var mapOptions = {
      center: map_center,
      zoom: 5.5
    }
    var map = L.map('map', mapOptions);
    L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
        maxZoom: 18,
        attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
    }).addTo(map);
    
    // Places

    fuji = [35.36277, 138.73078];
    fuji_circle = L.circle(fuji, {radius: 600, color: 'red'}).addTo(map);
    fuji_popup = L.popup().setLatLng(fuji).setContent("Mount Fuji").addTo(map);
    
    beijing = [39.910330305629465, 116.4082943628998];
    beijing_circle = L.circle(beijing, {radius: 100000, color: 'red'}).addTo(map);
    beijing_popup = L.popup().setLatLng(beijing).setContent("Beijing China").addTo(map);

    south_korea = [37.35293114817678, 127.15627728781749];
    south_marker = L.marker(south_korea).addTo(map);
    south_popup = L.popup().setLatLng([37.45293114817678, 127.15627728781749]).setContent("South Korea").addTo(map);

    san_francisco = [37.83071746954997, -122.24741413431259];
    san_francisco_circle = L.circle(san_francisco, {radius: 150000, color: 'pink'}).addTo(map);
    san_popup = L.popup().setLatLng(san_francisco).setContent("San Francisco").addTo(map);

    denmark = [52.10374052344996, 5.150504311131545];
    denmark_circle = L.circle(denmark, {radius: 100000, color: 'red'}).addTo(map);
    denmark_popup = L.popup().setLatLng(denmark).setContent("Denmark").addTo(map);

    jakarta = [-6.238287967709805, 106.78795030804145];
    jakarta_circle = L.circle(jakarta, {radius: 150000, color: 'pink'}).addTo(map);
    jakarta_popup = L.popup().setLatLng(jakarta).setContent("Jakarta").addTo(map);

    canada = [53.48276239308968, -113.33276912232068];
    canada_marker = L.marker(canada).addTo(map);
    canada_popup = L.popup().setLatLng([54.28276239308968, -113.33276912232068]).setContent("Canada").addTo(map);

    cebu = [10.314419759263567, 123.90151783569056];
    cebu_marker = L.marker(cebu).addTo(map);
    cebu_popup = L.popup().setLatLng([10.414419759263567, 123.90151783569056]).setContent("Cebu").addTo(map);

    var england = [
        [52.9514884991322, -3.125157380248484],
        [52.65133400804033, -0.30311326293972],
        [51.11112498014041, -2.811596922769734],
        [51.38101120462614, -0.17246307232357355]
    ];
    var polygon = L.polygon(england, {color: 'red'}).addTo(map);
    england_popup = L.popup().setLatLng([52.9514884991322, -3.125157380248484]).setContent("England").addTo(map);

    var letterJ = [
        [-19.578962, 131.863901],
        [-29.578962, 131.863901],
        [-29.578962, 136.863901],
        [-29.578962, 126.863901],
        [-29.578962, 131.863901],
        [-19.578962, 131.863901],
        [-19.578962, 136.863901],
        [-19.578962, 126.863901],
    ];
    var polyline = L.polyline(letterJ, {color: 'red'}).addTo(map);
    aust_popup = L.popup().setLatLng([-18.578962, 131.863901]).setContent("Australia (Letter I)").addTo(map);

    </script>
</html>
