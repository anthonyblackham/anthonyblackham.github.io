---
layout: post
title: Abandoned Railways
date: 2026-10-03 5:30:00 -0800
description: Replaying old timetables with GTFS and indexing Oregon's ICC valuation maps # (optional)
img: abandoned-railways-cover.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [railroad, trains, gtfs, maplibre, historic, oregon, icc, nara]
---

Back in 2019 when I mapped the [Willamette Valley Southern](https://anthonyblackham.com/wvsr/) I noted at the end that it would be a cool idea to build a scalable platform that integrated the modern GTFS transit data model so you could create a map that shows old abandoned trains running realtime as if they existed today.

I shelved the idea primarily due to the amount of time and effort it would take to research and code the model. 7 years later the coding roadblock has essentially been removed with AI tools like Claude. While Claude can also help with tools integrating research, the actual research portion is still best done with a human touch, which became readily apparent once I actually started looking for historic railroad data.


### The Oregon ICC Valuation Index

in 1913 the Interstate Commerce Commission (ICC) required railway engineers generate detailed maps and reports to provide a valuation of every asset the railroads owned. If you want any historic map information on old railroads the ICC valuation maps are the defacto standard (most were completed from 1915-1920), but I quickly found that the amount of data they have and the amount of data that is readily [available online](https://www.archives.gov/findingaid/stat/discovery/134) are two different things. As of this reading on 10/3/2026 it estimates only 5.38% are available online: 3,579,710 textual scans online out of 66,525,550 estimated total textual pages in this Record Group.

The interurban railroads did not receive an ICC valuation so Oregon Electric Railway and any of the tracks owned by Portland Railway Light and Power Company were excluded (though later acquisitions from Southern Pacific had some valuations for subsets of the original lines, eg Willamette Falls Electric Railway, Portland Traction Co etc.)

There are a few local resources that have some valuation sheets and railroad plats, either recorded in county records or through the [Association of Oregon Counties Railroad Research](https://rrsearch.aociris.org/) but these resources have gaps and are largely incomplete. I am not aware of any comprehensive Oregon valuation records outside of the National Archives.

Which leads me to step one of this project to create a basic map based ICC index so people can easily locate where in the NARA archives they need to look to pull the respective valuation maps. 

The indexes were compiled from the railroad specific index maps from 1916 that NARA has available online and correlated with a master spreadsheet of the finding aids that included bundle and railroad line information. I was hoping that the final land reports would be available so I could also get a tally of how many pages each valuation section had but they aren't available online.



[Link for mobile users](https://anthonyblackham.com/oregon-icc-valuation-index/)

<div class="embed-container">
  <iframe
      src="https://anthonyblackham.com/oregon-icc-valuation-index/"
      width="700"
      height="480"
      frameborder="0"
      allowfullscreen="">
  </iframe>
</div>


### Abandoned Railways

[Abandoned Railways](https://anthonyblackham.com/abandoned-railways/) takes the timetables of defunct railways and replays them against today's clock. Open it up and you see where the trains would be right now if they were still running. You can also scrub through the day or speed it up to watch a whole day's service go by.

[Link for mobile users](https://anthonyblackham.com/abandoned-railways/)

<div class="embed-container">
  <iframe
      src="https://anthonyblackham.com/abandoned-railways/"
      width="700"
      height="480"
      frameborder="0"
      allowfullscreen="">
  </iframe>
</div>


There are six lines in it so far:

- **Willamette Valley Southern Railway** (1915–1933), Oregon City to Mt. Angel. It uses the 1915 timetable from Richard Thompson's book *Willamette Valley Railways* and the PEPCO right-of-way plats I traced for the original map.
- **Willamette Falls Railway** (1925 timetable), Tualatin River to West Linn to Magones. It ran 62 trips a day from 6:00 am until midnight, and I traced the track from the Southern Pacific right-of-way and track maps for the line.
- **Oregon City Line** (1911 and 1916 timetables), Portland to Milwaukie, Oregon City and Canemah Park. This was Portland Railway, Light & Power's busiest interurban, with trains every half hour or so.
  - **Golf Junction to Oregon City:** I rebuilt the track from the curve data on the Portland Traction Co. valuation plats, then pinned it to control points on georeferenced plats. It sits within a few feet of the old right-of-way parcels.
  - **Oregon City to Canemah:** this end comes from a 1920s state highway right-of-way plat, plus a 1910 county survey for the final stretch along Water Street.
  - **Downtown to Golf Junction:** this comes from the City of Portland's street and Springwater on the Willamette trail data.
- **Springwater Line** (1916 timetable), Portland through Lents, Gresham, Boring and Estacada to Cazadero, the "Trout Route" up the Clackamas.
  - **Portland to Boring:** this follows the Springwater Corridor trail, which runs on the old roadbed.
  - **Boring to Estacada:** this comes from Portland Traction Co. valuation sheets and a 1911 Estacada survey, centred on the old right-of-way parcels.
  - **Faraday to Cazadero:** this comes from the 1923 Oak Grove hydro project maps.
- **Mount Hood Line** (1916 timetable), Portland to Gresham and Bull Run. It shares the Springwater Line's track to Linnemann Junction. East of there, the track and stations are from Cameron Booth's 1920 map of the Portland and Willamette Valley interurbans.
- **Troutdale Line** (1916 timetable), from Montavilla and Linnemann Junction through Ruby Junction to Fairview and Troutdale. Its track and stations are also from Cameron Booth's map.

The PRL&P lines' stations, flag stops and mileposts come from the company's January 1917 list of stations and table of distances. The 1916 times come from "The Trout Route" public timetable in the Sheldon Perry collection, and the 1911 Oregon City schedule from the *Morning Enterprise*. Most stations between the printed timepoints are estimated by distance.

### Future

I'm hoping to expand the Abandoned Railways GTFS Viewer with more railroad data as I come across old valuation plats, timetables, and time to do process it. Perhaps one day there will be a readily available public archive of all the old railway valuation plats for Oregon.
