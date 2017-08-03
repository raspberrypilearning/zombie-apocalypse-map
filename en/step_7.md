## Mark where you click

At the moment our marker appears when you click the map, but it always appears in the same place. Remember the code we added in the last step to listen out for clicks on the map?

```javascript
zombie_map.addListener('click', function(e) {
  place_marker();
});
```

Did you notice the `function(e)` part? The `e` stands for **event**, and clicking on the map is an event. The event records the longitude and latitude of the location that was clicked, and we can access them like this:

```javascript
var location = e.latLng;
```

+ Add this line of code to find the location inside your **listener** code, so that the code now looks like this:

```javascript
zombie_map.addListener('click', function(e) {
  var location = e.latLng;
  place_marker();
});
```

We need to pass the location data across to the `place_marker` function so that it can be used to position the marker. An item of data passed into a function is called an **argument**.

+ Add `location` as an **argument** to the `place_marker()` function. Arguments go inside the brackets. Your code should now look like this:

```javascript
place_marker(location);
```

+ Now locate where you **define** the `place_marker()` function. This is the line of code which begins `function place_marker()`. Add `location` inside the brackets here, so that it now looks like this:

```javascript
function place_marker(location){
    var marker = new google.maps.Marker({
      position: {lat: 52.206727, lng: 0.124450 },
      map: zombie_map
    });
}
```

+ Finally, instead of putting the marker at the specific latitude and longitude, we want to put it at the `location` that was clicked upon. Change one more thing inside your `place_marker()` function to put the marker at the clicked location rather than always on Cambridge, UK.

--- hints ---
--- hint ---
Which line of code contains the fixed position of the marker that is always placed on Cambridge, UK?
--- /hint ---

--- hint ---
Which variable contains the data of the location that was clicked on?
--- /hint ---

--- hint ---
Replace the fixed latitude and longitude code with the variable containing the location that was clicked on.
--- /hint ---

--- /hints ---

+ Save and refresh the page. Test your map - does a marker now appear anywhere you click on the map?

![Cambridge with lots of markers](images/cambridge-lots-of-markers.png)
