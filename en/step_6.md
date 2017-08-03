## Place a marker

+ Add a marker to your map.

[[[generic-api-google-maps-marker]]]

--- hints ---
--- hint ---
Put the marker code on a blank line before the ending `}` of the `initMap()` function.
--- /hint ---

--- hint ---
You will need to make sure that the marker has the correct map set. The map in the example is called `mymap` - what is the map we have created called?
--- /hint ---

--- /hints ---

![Cambridge with a marker on it](images/cambridge-marker.png)

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
