## Place a marker

+ Add a marker to your map. Put the marker code after the ending `}` of the `initMap()` function.

[[[generic-api-google-maps-marker]]]

At the moment our marker just appears at a fixed location. To make it easier to construct the map, let's add some code to only create a marker when we click on a position on the map.

+ Put your marker code inside a function called `place_marker()`

[[[generic-javascript-create-a-function]]]

+ Now we will add some code to "listen" for clicks on the map. When a click is detected, we will call the function we just created to place a marker. Locate the `initMap()` function and add the following code inside the function - this means after the other code in the function but before the closing `}`.

```javascript
zombie_map.addListener('click', function(e) {
  latlng = e.latLng;
  place_marker();
});
```
