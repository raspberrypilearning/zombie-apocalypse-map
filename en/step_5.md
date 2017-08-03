## Display the map

+ In the text editor, find the `<head>` tag in your code. On a blank line after this tag, add the following code:

```html
<style>
#zombie_map {
    width: 600px;
    height: 400px;
    background-color: grey;
}
</style>
```

This is some CSS code which will tell the map to be 600px wide and 400px high. You can change these values to make the map larger or smaller if you like. You will see the colour grey if your map doesn't load properly.

+ Locate the `<body>` tag in your code. On a blank line after this tag, add the following code to create a `<div>` (an invisible box) where your map will eventually appear

```html
My zombie map
<div id="zombie_map"></div>
```

+ Immediately underneath the `<div>` code you just added, add the following code to create the map:

```html
<script>
    var zombie_map;
    function initMap() {

            zombie_map = new google.maps.Map(document.getElementById('zombie_map'), {
            zoom: 10,
            center: {lat: 52.206727, lng: 0.124450}
        });
    }
</script>
```

+ Save your code and refresh your internet browser. You should see a Google map displayed with the centre of the map on Cambridge, UK (the location of Raspberry Pi HQ!)
