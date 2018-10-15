
Making Sense of Asteroids observed with the Gaia Space Telescope
================================================================

Daniela Huppenkothen

.. raw:: html

  <iframe width="560" height="315"
   src="https://www.youtube.com/embed/3OWXRbyjl1Q" frameborder="0"
   allow="autoplay; encrypted-media" allowfullscreen></iframe>

In April 2018, the European Space Agency released a massive dataset taken by
the Gaia Space Telescope. Among the haul in Data Release 2 (DR2) were time
series for over 14,000 known asteroids in our own solar system. Observing
asteroids is important for many reasons: they help us understand the formation
and evolution of the solar system and its planets, including Earth.
Characterizing the properties and paths of asteroids is also crucial in order
to be forewarned of a potential impact on the Earth. Asteroids are mainly
observed by the light from the sun they reflect (much like the moon). How much
light we receive at any given time from an asteroid depends on its position
and angle relative to sun and the telescope, its orientation and its form.
Understanding the time series of asteroids can give us important clues about
its orbit, its structure and its shape.

As astronomy moves into the era of big data, it is more important than ever to find new ways to visualize and interact with data. This was the purpose of the data visualization presented here, designed using the Python package [altair](https://altair-viz.github.io/index.html): to give researchers a quick glance at the Gaia data (augmented by other data sources), and aid them in selecting which of the observations might be the most promising for detailed analyses. The figure summarizes crucial information about the observations. In the top two panels it shows the position in the sky where the asteroid was observed and a histogram of the number of observations for each asteroid. In the second row we show the knowledge we have about the asteroids' orbits (parametrized in the quantities semi-major axis, eccentricity, and inclination), which can tell us important things about which asteroid family these asteroids belong to (are they near Earth? Are they caught around Jupiter? Are they somewhere beyond Neptune?). The last row presents the time series for any asteroid selected in the top left plot. The interactions are designed to maximize the amount of information to be gleaned. A hover panel in the top left and middle row allows the user to immediately see the name of any asteroid. An interval selection on the counts plot in the upper right allows the selection of asteroids with a certain range of observations. Similarly, a linked interval selection in the second row allows users to select different asteroid families. Clicking on any asteroid in the top left sky position plot will show the time series recorded by Gaia in the third row. The latter also allows moving around and zooming in and out in order to probe the different relevant time scales on which observations were taken.

The figure was designed to be located on the web and accessible for researchers without having to download and prepare large amounts of data themselves. It is visible to the world here: https://epyc.astro.washington.edu/~dhuppenk/gaiadr2_sso/
The web figure was designed in Altair (notebook attached), then exported into the lower-level Vega-Lite and embedded into a simple HTML file.

Note that the figure file upload in this form will not allow me to upload the HTML file with the interactive figure (the file type is restricted), so I am uploading a movie demo of the interactive capabilities. For the full interactive version, please see the link above.

I'd like to acknowledge Jake VanderPlas and Dominik Moritz for various Altair and Vega-Lite related suggestions.



**Code and data:** `1 <https://drive.google.com/open?id=14eH_ddIhWm5qa9h3Qrb16_tau69p18no>`__, `2 <all code available here: https://github.com/dirac-institute/GaiaDR2_SSO_DataViz>`__
