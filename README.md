Colored Skycons
===============

Colored Skycons is a set of ten animated weather glyphs, procedurally generated by
JavaScript using the HTML5 canvas tag based on [Skycons](https://github.com/darkskyapp/skycons).
They're easy to use, and pretty lightweight, so they shouldn't rain on your parade:

You can see in action [here](http://kriyeng.github.io/colored-skycons/)

    <canvas id="icon1" width="128" height="128"></canvas>
    <canvas id="icon2" width="128" height="128"></canvas>

    <script>

      // You can specify the stroke width and the colors for each element
        var skycons = new Skycons({
                               "stroke" : 0.08,
                               "color" : "Gray",
                               "cloudColor" : "DarkGray",
                               "sunColor" : "Gold",
                               "moonColor" : "DodgerBlue",
                               "rainColor" : "RoyalBlue",
                               "snowColor" : "LightGray",
                               "windColor" : "LightSteelBlue",
                               "fogColor" : "LightGray"
                                });
      // on Android, a nasty hack is needed: {"resizeClear": true}
      // you can specify a default color: {"color": "gray" }
      // If no options defined, the default values will be applied:
      //    var skycons = new Skycons();

      // you can add a canvas by it's ID...
      skycons.add("icon1", Skycons.PARTLY_CLOUDY_DAY);

      // ...or by the canvas DOM element itself.
      skycons.add(document.getElementById("icon2"), Skycons.RAIN);

      // if you're using the Forecast API, you can also supply
      // strings: "partly-cloudy-day" or "rain".

      // start animation!
      skycons.play();

      // you can also halt animation with skycons.pause()

      // want to change the icon? no problem:
      skycons.set("icon1", Skycons.PARTLY_CLOUDY_NIGHT);

      // want to remove one altogether? no problem:
      skycons.remove("icon2");
    </script>

Colored Skycons were adapted by Kriyeng based on [Skycons](https://github.com/darkskyapp/skycons):
Skycons were designed for [Forecast](http://forecast.io/) by those wacky folks
at The Dark Sky Company, and were heavily inspired by Adam Whitcroft's
excellent [Climacons](http://adamwhitcroft.com/climacons/). The source code has
been released into the public domain, so please do with it as you see fit! ♡
