## Obtain a Google Maps API key

+ To be able to display a map, you will need to obtain a Google Maps API key

[[[generic-api-google-maps-key]]]

+ Make sure you have pasted in the code to use the API key into your page. The code goes immediately before the `</body>` tag, and you need to replace the words `YOUR_API_KEY` with the API key you just generated.

```html
<script async defer
   src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap">
 </script>
 ```
