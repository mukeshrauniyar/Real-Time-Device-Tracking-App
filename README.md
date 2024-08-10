# Steps ongoing:

1. Check if the browser supports geolocation.

2. Set options for high accuracy, a 5-second timeout, and no cashing.

3. Use watchPosition to track the users location continuously.

4. Emit the latitude and longitude via a scocket with 'send=location'. Log any errors to the console.

5. Initialize a map centered at coordinates(0, 0) with a zoom level of 15 using Leaflet. Add openStreetmap tiles to the map.

6. Create an empty object markers.

7. When receving location data vie the socket. extract id, latitude, and longitude, and center the map on the new coordinates.

8. If a marker for the id exists, update its position, otherwise, create a new marker at the given coordinate and add it to the map. When a user disconnects, remove theri markers from the map and delete it from markers.