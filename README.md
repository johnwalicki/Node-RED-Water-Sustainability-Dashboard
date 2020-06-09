# Node-RED-Water-Sustainability-Dashboard
Display USGS Watershed maps on a Node-RED Dashboard with Water Quality Reports

Query the watershed area maps of the [Ridgewood, NJ](https://waterdata.usgs.gov/monitoring-location/01390500/#parameterCode=00060)
and [Atlanta, GA watershed](https://www.atlantawatershed.org/) using the
[USGS Hydro Network-Linked Data Index](https://waterdata.usgs.gov/blog/nldi-intro/)
and plot the water basins and rivers on a [Node-RED](https://nodered.org) Dashboard.  

The USGS [NLDI API](https://labs.waterdata.usgs.gov/api/nldi/swagger-ui.html) returns a [geojson](https://en.wikipedia.org/wiki/GeoJSON) set of latitude / longitude coordinates that can be plotted using the node-red-contrib-web-worldmap node.  You can [search for a river](https://waterdata.usgs.gov/nwis/inventory?state_cd=nj&format=station_list) near you.  To generate your own map visit - http://geojson.io - which allows you to quickly generate a geojson file.

The dashboard includes several colored map legend switches to show / hide the watershed details.

Water sustainability requires protecting the groundwater and sub-surface aquifer from dangerous / toxic pollutants.
[Aquagenuity](https://aquagenuity.com/) helps everyday people monitor water quality in their community.
The Aquagenuity GetWaterScore API provides water quality reports for many USA ZipCodes.
The chemical toxins found in the water are displayed in a Node-RED table.
If the toxins exceed the EPA limits, the table highlights the chemical in red and, when selected,
will popup an informational dialog about the health risks of that toxin.
USGS also publishes [Water Quality Data](https://www.waterqualitydata.us/portal/)

Sadly, the industrial revolution in the 1800s and early 1900s polluted many New Jersey waterways and communities that still linger today.
These toxins are evident in Aquagenuity water score reports for Ridgewood, NJ.
There is continued community dissatisfaction with the
[Ridgewood Water utility](http://water.ridgewoodnj.net/) efforts to provide safe and clean water to residents.

These example flows and Node-RED Dashboard might be useful as part of a [Call for Code](https://developer.ibm.com/callforcode/) Water Sustainability solution.

### Prerequistes

- [Install Node-RED](https://nodered.org/docs/getting-started/) on your system or in the cloud
- [Add the following nodes](https://nodered.org/docs/user-guide/runtime/adding-nodes) to your Node-RED palette
  - [node-red-dashboard](https://flows.nodered.org/node/node-red-dashboard)
  - [node-red-contrib-web-worldmap](https://flows.nodered.org/node/node-red-contrib-web-worldmap)
  - [node-red-node-ui-table](https://flows.nodered.org/node/node-red-node-ui-table)

## Node-RED flow in this repository:

- Import the [Ridgewood NJ waterbasin flow](flows/rwdnjwatershed.json)
- Import the [Atlanta GA waterbasin flow](flows/atlantawatershed.json)

---
### A flow that displays the Ridgewood NJ watershed on a map

![Watershed Dashboard](screenshots/Node-RED-Ridgewood-Watershed-dashboard.png?raw=true "Ridgewood Watershed Dashboard")

![Watershed Dashboard Alert](screenshots/Node-RED-Ridgewood-Watershed-dashboard-WaterReportAlert.png?raw=true "Ridgewood Watershed Dashboard Alert")

![Watershed flow](screenshots/Node-RED-Ridgewood-Watershed-flow.png?raw=true "Ridgewood flow")

---
### A flow that displays the Atlanta GA watershed on a map

![Watershed Dashboard](screenshots/Node-RED-Atlanta-Watershed-dashboard.png?raw=true "Atlanta Watershed Dashboard")

![Watershed flow](screenshots/Node-RED-Atlanta-Watershed-flow.png?raw=true "Atlanta flow")

---

### Authors

- [John Walicki](https://github.com/johnwalicki)
___

Enjoy!  Give us [feedback](https://github.com/johnwalicki/Node-RED-Water-Sustainability-Dashboard/issues) if you have suggestions on how to improve this tutorial.

## License

This tutorial is licensed under the Apache Software License, Version 2.  Separate third party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1 (DCO)](https://developercertificate.org/) and the [Apache Software License, Version 2](http://www.apache.org/licenses/LICENSE-2.0.txt).
