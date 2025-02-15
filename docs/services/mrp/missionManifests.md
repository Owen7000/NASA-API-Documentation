!!! failure "Dead Route"
    At time of writing - __15/02/2025__ - it appears that this API route has already died. No data is returned when calling the route for any Rovers supported by the API. The expected behaviour for this route is documented incase this is fixed moving forward.

A mission manifest is available for each Rover at the /manifests/<rover_name>. This manifest will list details of the Rover's mission to help narrow down photo queries to the API. The information in the manifest includes:

- name
- landing_date
- launch_date
- status
- max_sol
- max_date
- total_photos

It also includes a list of objects under the photos key which are grouped by sol, and each of which contains:

- sol
- total_photos
- cameras

An example entry from /manifests/Curiosity might look like:
```json
{
  sol: 0,
  earth_date: "2012-08-06"
  total_photos: 3702,
  cameras: [
    "CHEMCAM",
    "FHAZ",
    "MARDI",
    "RHAZ"
  ]
}
```