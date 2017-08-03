## Obtain a Google Maps API key

+ To be able to display a map, you will need to obtain a Google Maps API key

[[[generic-api-google-maps-key]]]

+ Make sure you paste in the code to use the API key into your page, just before the `</body>` tag, and that you substitute in your actual API key for the words `YOUR_API_KEY`.

```html
<script async defer
   src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap">
 </script>
 ```
