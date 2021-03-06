---
layout: post
title: The Giant Lighted Lucite Map of Gotham City
date: 2019-12-01 5:30:00 -0800
description: Mapping the Giant Lighted Lucit Map of Gotham in Real Life # Add post description (optional)
img: gotham-cover.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [batman, webmap, leaflet, qgis, qgis2web]
---

I recently watched all 3 seasons of the 1966 Batman TV series with Adam West and Burt Ward as the dynamic duo. A recurring element in many of the episodes was the Giant Lighted Lucite Map of Gotham City..

![Giant Lighted Lucite Map of Gotham]({{site.baseurl}}/assets/img/gotham-lucite-map.jpg)

If you look closely at the map you can see that it is actually a map of St. Louis, Missouri. I took a screenshot of the map and georefererenced it in QGIS. I sketched out the features on the map from every episode it was used. I then used the [qgis2web](https://github.com/tomchadwin/qgis2web) plugin to generate a web map. There are some changes in the city since the map was drawn in 1966 but overall it matches up pretty well.

You can see the map in action below:

<div class="embed-container">
  <iframe
      src="https://anthonyblackham.github.io/gotham"
      width="700"
      height="480"
      frameborder="0"
      allowfullscreen="">
  </iframe>
</div>

Here is an alternate map based on the 1998 version created by Eliot Brown for DC comics, GIS conversion by Danielle Pugh

<div class="embed-container">
  <iframe
      src="https://anthonyblackham.com/gotham-1998/#13/39.4493/-74.1878"
      width="700"
      height="480"
      frameborder="0"
      allowfullscreen="">
  </iframe>
</div>


Here is a rough summary of episodes and timestamps for when the map showed up in the series:

- S1 E07 11:45, 18:29 (Mr. Freeze)
- S1 E13 16:52 (mad hatter)
- S1 E18 03:00
- S1 E21 17:08 (small)
- S1 E26 06:48 (brief)
- S1 E28 11:48, 15:15 (King Tut)
- S2 E05 17:20
- S2 E27 17:00 (good)
- S2 E34 09:03 (batmobile signal)
- S2 E53 11:23, 17:35 (best view)
- S2 E54 2:38 brief, 9:58

Bonus Maps:

- S3 E25 19:12 alternate Gotham map
- S2 E37 00:30 rare art map
- [Gotham City Map](https://www.arcgis.com/apps/opsdashboard/index.html#/03bdb383c96a4a2ba41c30daccb4730f)

### Future Ideas

In the second season the map was repurposed as the Batmobile Tracking Map and utilised a series of lights flashing to simulate trackers. Leaflet has a variety of tools to animate features that could be used to recreate tracking catwoman to her hideout like in Season 2, Episode 34.

### Source Files

The data used to create the map can be found at my repository [here](https://github.com/anthonyblackham/gotham)
