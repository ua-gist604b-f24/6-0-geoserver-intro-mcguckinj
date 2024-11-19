#### Q1: What is the URL of the WMS GetCapabilities request?
https://glorious-bassoon-4jw6jv6gxp59277qq-8080.app.github.dev/geoserver/ows?service=WMS&version=1.3.0&request=GetCapabilities

#### Q2: What is the URL of the WFS GetCapabilities request?
https://glorious-bassoon-4jw6jv6gxp59277qq-8080.app.github.dev/geoserver/ows?service=WFS&acceptversions=2.0.0&request=GetCapabilities

#### Q3: Submit a screenshot of your updated WFS Layer Preview
screenshot: archsites.png

#### Q4: What does drawing order refer to? Which layer goes on `top`, the first or the last layer in the list?
The drawing order refers to how the layers will be rendered. The 'top' layer will be the last layer in the list. So the bugsites will be on top of the other layers. 

#### Q5: Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer.
Screenshot: Q5_DEM_3rd.png

#### Q6: What is the WMS url for the single-tiled request?
https://glorious-bassoon-4jw6jv6gxp59277qq-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&SRS=EPSG%3A26713&WIDTH=1901&HEIGHT=1001&BBOX=594662.3989771116%2C4914761.672850657%2C603731.0437478076%2C4919535.547944639

#### Q7: What is the WMS url for one of the tiled requests? What is the image size?
https://glorious-bassoon-4jw6jv6gxp59277qq-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&tiled=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&tilesOrigin=589425.9342365642%2C4913959.224611808&WIDTH=256&HEIGHT=256&SRS=EPSG%3A26713&BBOX=593708.96010888%2C4920698.953330398%2C594930.5834835896%2C4921920.576705107

Image size: Width = 256 Height = 256

#### Q8: What is the URL of your coarse resolution sample of a WMTS url? What level does this tile refer to? Notice the differences. What are some of the fields that are unique to this url?
https://glorious-bassoon-4jw6jv6gxp59277qq-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A12&TileCol=1732&TileRow=1036

This tile refers to level 12. 
Fields unique to this URL are calls to a specific tile column and tile row. 

#### Q9: In the zoomed-out URL, what are the TileCol and TileRow?
Zoomed out TileCol = 433, TileRow = 259

#### Q10: In the zoomed-in URL, what are the TileCol and TileRow?
Zoomed in: TileCol = 27752, TileRow = 16595

#### Q11: Why are they so different for the same location in the map?
The zoom levels are different, so the horizontal and vertical positions of the tile are going to be different based on the zoom level and the level of detail in the grid. 

#### Q12: Is there a difference in the TileMatrix? %3A is an HTML encoding for a colon, `:`.What does the number after EPSG:4326 mean?
Yes, the number after the colon is the zoom level. For the zoomed-in, the level is 16. For the zoomed-out, the level is 10.