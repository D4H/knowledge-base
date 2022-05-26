# Adding Custom Basemaps

#### WEB APP

It is possible to add any basemap you like as long as the map tiles can be accessed using the **zoom / x / y** format.\
\
A custom basemap has a **Name** and can have multiple imagery **Layers** associated with it. While most will only have one layer, you may overlay multiple layers such as hybrid layers with place names, roads, or land parcels overlaid on satelite imagery treated as a single basemap.

To add a custom basemap:

* Click on the **green ⇅** in the top right hand corner.
* Go to **Admin Area**
* Navigate to **Settings** > **Preferences** on the left side bar.
* Scroll down to **Map** > **Custom Basemaps**
* Press **+ Add Custom Basemap**
* Enter a **Name**
* Press **+ Add Layer** and enter the **Tile Service URL**, and an **Attribution** e.g. the source or copyright.&#x20;
* Press the main **Save** button at the bottom of the page.\


![](<../../../.gitbook/assets/adding custom basemaps.png>)

The zoom / x / y format makes map tiles available as we need them at the right {z} for zoom, {x} for longitude, and {y} for latitude. If the baselayer is private, it may have a secret token or key in it you need to generate.

{% hint style="info" %}
**Where can I get more basemaps?** Basemaps are available from hundreds of sources including your own ArcGIS Online service. For examples, we'd recommend taking a look at:

* [LINZ New Zealand](https://data.linz.govt.nz/data/category/topographic/maps/)
* [Thunderforest](https://www.thunderforest.com/maps/outdoors/)
* [OpenSeaMap](https://map.openseamap.org/)
{% endhint %}



