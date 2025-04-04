<<<<<<< HEAD
# leaflet-challenge
=======
Leaflet Challenge

This project focuses on creating an interactive map to visualize earthquake data provided by the USGS (United States Geological Survey). Using Leaflet.js, we developed a tool to plot earthquake data dynamically, providing insightful visuals to better understand seismic activity worldwide.

We started by setting up the foundation with a basemap tile layer from OpenStreetMap to serve as the map's background. Additionally, an optional street tile layer was created to offer users a secondary map style. To display the data, we initialized the map object, centered at [0,0] with a zoom level of 2, ensuring a global view. The layers, including earthquakes and optional tectonic plate data, were managed using separate layer groups for clarity and interactivity.

The earthquake data, retrieved dynamically from the USGS GeoJSON API, was plotted using L.circleMarker .The size of each marker was determined by the earthquake's magnitude, using a scaling function to ensure visual prominence for stronger earthquakes. Depth information was encoded using a color scale, with deeper earthquakes represented in darker tones and shallower ones in lighter hues. The markers were further enhanced with interactive popups that display details such as the earthquake's magnitude, depth, and location.

A legend was added to the map, positioned in the bottom-right corner, to provide context for the color coding of earthquake depths. However, during development, we encountered an issue where the colors were not showing up in the legend. After investigating, we discovered that the missing colors were due to the absence of proper CSS styling for the <i>  elements used to represent colored squares. To resolve this issue, we added the following CSS to our stylesheet:

.info.legend i {
  width: 18px;
  height: 18px;
  float: left;
  margin-right: 8px;
  opacity: 0.8;
}

This styling ensured that the colored squares in the legend were displayed properly. After refreshing the browser, the colors appeared as intended, matching the depth intervals defined in the JavaScript code.
For testing and development, we used the VS Code Live Server extension to serve the project locally. This allowed us to quickly test changes in real time and ensure that everything was functioning as expected without browser-related caching issu

This project successfully combines dynamic data visualization with user-friendly interactivity, offering an intuitive way to explore global earthquake activity. By leveraging Leaflet.js, D3.js, and GeoJSON data, the tool not only educates users about seismic events but also demonstrates the power of interactive mapping in scientific and public communication.

Referances
https://leafletjs.com/reference.html
https://d3js.org/getting-started
https://www.w3schools.com/js/default.asp

>>>>>>> master
