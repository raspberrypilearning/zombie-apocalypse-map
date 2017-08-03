## Create a web page to display the map

+ You will display your zombie map on a web page. Create and save a web page called `index.html`. You will need to use a text editor on your computer to do this rather than using an online HTML editor.

[[[generic-html-create-and-save]]]

+ Make sure you have the `index.html` file open in both your text editor and your internet browser. When you make changes to the code in the text editor, save the file and then refresh the internet browser to see your changes.

+ In the text editor, find the `<head>` tag in your code. On the line after this tag, add the following code:

```html
<style>
#map {
    width: 100%;
    height: 400px;
    background-color: grey;
}
</style>
```

This is some CSS code which will tell the map to take up the whole width of your screen, and be 400px high. You can change these values to make the map larger or smaller if you like.

+ Locate the `<body>` tag in your code. On the line after this tag, add the following code to create a <div> (an invisible box) where your map will eventually appear

```html
My Google map
<div id="map"></div>
```

+ Immediately underneath the `<div>` code you just added, add the following code to create the map:

```html
<script>

    function initMap() {

        var Cambridge = {lat: 52.206727, lng: 0.124450};

        var map = new google.maps.Map(document.getElementById('map'), {
            zoom: 10,
            center: Cambridge
        });
    }
</script>
```

+ Save your code and refresh your internet browser. You should see a Google map displayed with the centre of the map on Cambridge, UK.
