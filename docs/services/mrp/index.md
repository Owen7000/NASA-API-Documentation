# Mars Rover Photos
 This API is designed to collect image data gathered by NASA's Curiosity, Opportunity, and Spirit rovers on Mars and make it more easily available to other developers, educators, and citizen scientists. This API is maintained by [Chris Cerami](https://github.com/corincerami/mars-photo-api).

!!! warning "A word of warning"
    Please be aware. As noted in a [GitHub issue](https://github.com/corincerami/mars-photo-api/issues/189), Chris Cerami intends to leave the project on October 8th 2025.
    If nobody steps forward to take over by that date, the api will likely die.

Each rover has its own set of photos stored in the database, which can be queried separately. There are several possible queries that can be made against the API. Photos are organized by the sol (Martian rotation or day) on which they were taken, counting up from the rover's landing date. A photo taken on Curiosity's 1000th Martian sol exploring Mars, for example, will have a sol attribute of 1000. If instead you prefer to search by the Earth date on which a photo was taken, you can do that, too.

Along with querying by date, results can also be filtered by the camera with which it was taken and responses will be limited to 25 photos per call. Queries that should return more than 25 photos will be split onto several pages, which can be accessed by adding a 'page' param to the query. 

----
You can interact with this API at two different URLs.

| URL | Description |
| --- | ----------- |
| https://api.nasa.gov/mars-photos/ | This is the normal way to ineract with the API. You need your NASA API_KEY to use it. |  
| https://mars-photos.herokuapp.com | This URL provides support for cross-origin requests and has _no API_KEY requirement_. Use this if you are making a web application. |