<template>
  <div id="container">
    <div id="mapContainer"></div>
  </div>
  
</template>
  
  <script>

  import "leaflet/dist/leaflet.css";
  import L from "leaflet";
  
  export default {
    name: 'BaseMap',

    methods: {
     setupLeafletMap: function () {
       const mapDiv = L.map("mapContainer").setView([59.43, 24.73], 11);
       
        L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
        }).addTo(mapDiv);
          },
   },
   mounted() {
     this.setupLeafletMap();
   },
  }
  </script>

<style>
  #mapContainer {
  width: 100%;
  height: 500px;
  }
</style>
  
  

  