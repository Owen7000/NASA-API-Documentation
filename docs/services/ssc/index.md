# Satellite Situation Center

The [Satellite Situation Center](https://sscweb.gsfc.nasa.gov/) is a system to cast geocentric spacecraft location information into a framework of (empirical) geophysical regions and mappings of spacecraft locations along lines of the Earth's magnetic field. While SSCWeb provides access to this data through an HTML-based user interface, these Web services provides a [(Web) application programmming interface](https://en.wikipedia.org/wiki/API)(API) to SSC. If you are not a software developer and simply want to use the existing web (HTML) interface to SSC, then return to the [main SSCWeb page](https://sscweb.gsfc.nasa.gov/). If you are developing software that requires the type of information available at SSC, the the SSC Web services will provide a convenient API to the information.

## Web Services
The table below is a summary of the services which are available. Only the last part of each URL is shown in the table. The beinning part of all URL's for this service is `https://sscweb.gsfc.nasa.gov/WS/sscr/2`


| Category | Operation               | Implementation                                                                           | Details |
|----------|-------------------------|----------------                                                                          |---------|
| Metadata | Get WADL                | GET /application.wadl                                                                    |[Details](getWADL.md)|
| Metadata | Get Observatories       | GET /observatories                                                                       |[Details](getObservatories.md)|
| Metadata | Get Client Example      | GET /observatories/{observatory}/clientLibraryExample/{library}?mediaType={mediaType}    |[Details](getClientExample.md)|
| Metadata | Get SPASE Observatories | GET /spaseObservatories                                                                  |[Details](getSPASEObservatories.md)|
| Metadata | Get Ground Stations     | GET /groundStations                                                                      |[Details](getGroundStations.md)|
| Data     | Get Locations           | POST /locations<br>GET /locations/{observatories}/{timeRange}/{coordinateSystems}/       |[Details](getLocations.md)|
| Data     | Get Graphs              | POST /graphs                                                                             |[Details](getGraphs.md)|
| Data     | Get Conjunctions        | POST /conjunctions                                                                       |[Details](getConjunctions.md)|