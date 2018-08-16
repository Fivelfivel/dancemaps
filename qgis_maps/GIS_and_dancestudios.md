What determines the location of dance studios in New York City?

As an artform that organizes both time and space, dance has particular needs not only for its performance, but also for its creation. Dance needs spaces in which to be created, spaces which can approximate the spaces in which it will be performed.

The following visualizations attempt to consider how these spaces impact dance creation. But it's not directly considering the studios themselves; it's not the space *of* the dance studios, but the *location* of the studios — an aspect of space "once-removed," we might say. A vital element for the creation of dance, how do the locations of dance studios get determined, and what can this tell us about dance itself?

## The Visualizations

What follows is a series of visualizations that help point to one factor that may have determined the location of dance studios in New York City.

First, a map with a number of dance spaces. Mostly studios, and some theaters:

![Studio Dots](https://github.com/Fivelfivel/dancemaps/blob/master/qgis_maps/studio-dots.jpg)

In the above image, all the dots represent spaces that are associated with dance. In most cases, these are explicitly dance studios. In some cases, they are other kinds of spaces — Churchs, community centers — that have otherwise been significant as resources for supporting dance practice. Some of the dots also represent theaters — spaces that are used primarily to present performances of dance.

One theory would be that dance studios would be more likely to appear closer to theaters — that places where dance gets made might more easily thrive near the places that dance gets performed. In order to test this theory, first we'll visually distinguish the theater spaces:

![Theater Triangles](https://github.com/Fivelfivel/dancemaps/blob/master/qgis_maps/theatre-triangles.png)

With the theaters visually distinguished, we see that they generally congregate in lower Manhattan. This is already well-known anecdotally, and doesn't need a map to prove it. However, we can use this map to quickly identify a few other relationships between theaters and studios:

![Closest Theater](https://github.com/Fivelfivel/dancemaps/blob/master/qgis_maps/closest-theater.jpg) 

The turquoise lines are identifying the theater that is closest to each studio. Several studios can share the same closest theater, but each studio has only one closest theater. This map shows us some interesting information, but it also shows that proximity to a theater is not the determining factor in studio location: many studios are quite far from their closest theater. We can try another version of this that calculates the distance from each studio to each theater, to get an idea of the overall distance between a theater and the studios in the city:

![Studio Distance Matrix](https://github.com/Fivelfivel/dancemaps/blob/master/qgis_maps/theatre-distance-matrix.jpg)

We can use this map to come up with a kind of cumulative distance from a theater to the various studios around the city — the distances of each line are encoded into the properties of the line. So while the distance isn't visible on the map itself (in this visualization), we have the distances to work with should we need them. This would give us a sense of which theater is overall "closest" to studios in general; however, a visual overview still shows that proximity to a theater does not seem to determine studio location. If it did, most studios would be closer to theaters, whereas in this dataset, they don't correlate, seemingly evenly distributed across Manhattan and Brooklyn.

There is another dataset we can bring in which could provide some clarity. So far, I have been looking at straight-line distance, or "as the crow flies." However, as people travel between dance studios and theaters, in New York, they are not generally moving in direct lines. More significant than even the right-angles of the city blocks is, of course, public transportation. Moving between one place and another in New York almost always makes use of the subway system. Lets see what happens when we place the subways onto our map of dance studios.

![Subways](https://github.com/Fivelfivel/dancemaps/blob/master/qgis_maps/studios-subways.png)

Already this is pointing to a correlation, but we can make it much more clear very simply. We'll take a 1/4 mile buffer around each of the subway lines, and see how many of our studios fall within this buffer. A 1/4 mile is roughly a 5-min walk; if a location is within a 1/4 mile of a subway line, it is fair to assume a station is within 5-10min walk, a very accepted walking distance for an average New Yorker.

![Subway Buffer](https://github.com/Fivelfivel/dancemaps/blob/master/qgis_maps/all-subway-buffer.png)

With the buffer in place, there is an immediate correlation between studio location and proximity to subway line. Of the 55 studios in this dataset, only 5 fall outside of this buffer. What seemed like an usual extension into Brooklyn when considering proximity to theaters, now appears not only obvious but intuitive: studios in the north of Brooklyn practically trace the L-train through Williamsburg, Bushwick, and into Ridgewood. So while these studios may have a large straight-line distance to theaters, their proximity to transportation can make them closer by another metric: travel time.

That the location of anything in New York — including avant-garde dance spaces — has a correlation to the subway system should not surprise. But this gives concrete information we can start to consider in the production of dance: how has transportation and commute times impacted dancers practices over the years? Have these factors changed, and if so, what have been the effects of these changes?