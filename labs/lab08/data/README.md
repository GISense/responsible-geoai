Four files, all used by the notebook. Nothing here needs to be downloaded.

  Demand_County.csv         254 Texas counties and the number of births in each.
  Supply_County.csv         The 101 counties that have obstetric beds. The other
                            153 have none, so they are simply absent from this
                            file -- the notebook joins them back in as zero.
  ODCost_County_Matrix.csv  64,516 county pairs: drive minutes, drive miles and
                            straight-line miles between every pair.
  tx_counties.geojson       The 254 county polygons, in EPSG:4326.

Project to EPSG:3083 before you measure any distance or area. EPSG:4326 is
degrees, and a degree is not a fixed number of metres.

Where the data comes from: it is aggregated from a Texas maternal-health dataset
that tracks individual patients. Those individual records cannot be shared; these
county totals can. Travel times were computed for this lab using OSRM, an
open-source routing engine, on the OpenStreetMap road network.

Totals, if you want to check your loading worked:
337,674 births and 5,140 obstetric beds across 254 counties.
