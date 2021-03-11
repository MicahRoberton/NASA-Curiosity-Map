# NASA-Curiosity-Map

Micah Roberton \
GEOG 482 \
Final Essay \

NASA’s “Where is Curiosity” interactive map is based on Mars near the Gale Crater which their Rover named ‘Curiosity’ journeyed through since landing on Mars in 2012. Along this robot’s journey it photographed and recorded its path so that the Curiosity NASA team could then build this map. The team made this map with the intention of providing a software experience of the Rover’s daily path. This map is another step towards mapping a new frontier, with Earth’s land having been mapped out (except for the ocean bed), Mars is the new platform to discover, hence such names as Curiosity. The map has many functions. It allows the user to look at the Rover’s entire distance traveled, examine specific geography landmarks, check every day’s (sol) ending point, examine 17 camera feeds attached to the Rover providing a Google Street experience on another planet. This means the Rover is recording data such as is its own coordinates and photo feeds. This data was then recorded at the end of each sol along the 3000+ day voyage. The Rover is also outfitted with many scientific measurement instruments which allows for “Geoscience data from orbit or previous missions [which] can be overlayed for cross instrument/mission analysis” (Calef et al., 2016). This data is recovered from software used by the mission team.

The nature of this being a cutting-edge scientific map means there are many map elements with the intention of providing the most amount of data and information possible. First at the top of the map is a tab bar allowing for the user to switch between the Rover’s location and selected points quickly. Next there is a Layers tab on the left side bar of the map that allows for layers to be peeled away between Current Position, Waypoints, Surface View, Rover Path, Labels, base map, Gale Crater Map. Below this tab is another tab for sites on the map (landmarks). At the bottom of this menu bar the user can copy a link to the map, download a screenshot, expand to full screen, or get help using the user interface of the map. There is a zoom feature on the right of the map and the longitude and latitude convey the cursor’s coordinate location on the map near the bottom right. Finally, there is a scale bar that changes measurement based on zoom level accordingly. 

These functions and elements come together to create a map that is intended for the general public accessing the NASA website and seeking info on the rover program. This is one of the ways NASA releases information with the intention of making the data they’ve collected more engaging to the public. This design for general use allows for a wide range of end users from entire classrooms using it as a learning tool to the millions tuning into internet news & social media platforms that circulated this map’s link. This map is made extremely accessible by being imbedded on the NASA website allowing for anyone with an internet connection to view and use the site which closes the digital divide between space age information and general world population users.

The map’s webpage states it was made by NASA engineers however gives no further info on the authors. I inspected the webpage and found a Github link in the HTML to the repository for the opensource software used to make the map. This repository is managed by Tariq Soliman who helped co-author the MMGIS (Multi-Mission Geographic Information System) alongside Fred John Calef, Hallie Gengl, and Mark W. Powell. They worked for the Mars Science Laboratory to make this Curiosity map and others like it for other rover programs.

This map software is “now entirely Node-JS based, removing any dependencies for a stand-alone webserver” (Calef et al., 2016). This means most server access will just be via single-sign on (SSO). Because the large amounts of data that come with orbital data, vector tiles have been added as the default format instead of the non-dynamic format of GeoJSON which is not as fast as tiles since tiles help “for the visualization of relatively static data” (Zhao, 2021). These vector files are in the Mapbox vector format. However, for the new Perseverance map on the Mars 2020 mission, cloud databases will be switched in such as Amazon’s EC2, an S3 bucket, and Elastic Block Storage (EBS, a cloud-based network drive). 

The map software’s main functionality is that it “provides workflows and a web-based interface to combine mission base maps with science products in their proper geospatial context including instrument results” ( Calef et al., 2016). The function that allows the main usability of the map is the vector functionality that allows the user to point and click on the map to bring up displays and images.

The user interface of the web map has been reiterated from the software’s original launch. Original screenshots of the old software reveal a worse color scheme, more graphic interface glitches, and far less fidelity. Now the imbedded map UI is more appealing partly because it uses modern icons for tabs in the menu and on the map. I think the exclusion of a compass element was smart since it would be entirely useless for helping the user generate context for the part of the map their viewing since the map is on a different planet that users aren’t used to applying the cardinal direction system to like they are with maps here on Earth. The UI also reminded me a lot of the submarine cable map that I examined in week 4 for GEOG458 because of the line paths with points at the beginning and end of cables which was sort of like the rover’s path with points at the end of each sol. 

The user experience is aided a lot by the use of the vector layers as mentioned before since scrolling around the Mars geography causes little loading bugs which keeps the display at a constant high level of detail. The user experience is also improved quite a lot by the dashboard that opens if the user clicks on “Surface” view tab. This dashboard allows the user to interact with the many cameras and see the rover as a 3d model in a 3d Mars enviroment. This environment is displayed with 3d topography to give a new level of depth to the surrounding area. The use of two smart dashboards as the GUI of the map makes traversing the many types of data available far more guided and simpler. The user experience was hampered by some site deterioration. Site deterioration occurs when a site is not kept updated and so links become deadlinks over time and functionality is leaked from the site. An example of this can be seen when the user clicks on certain sites on the rover’s marked path where the dashboard that views surface information doesn’t pop up and instead a 404 webpage is returned to. The site also lacks responsive design across different hardware displays but shows off responsive design when it comes to the embedded window the map is contained in reformatting correctly when the window is resized on desktop browser windows. The embedded window also performs well on a mobile screen, however it is unable to open in widescreen on mobile hence poor responsive design. 

The base map is made from a true color satellite imagery base map of Mars’ surface. This is overlaid a grayscale Gale Crater map. The grayscale map is larger than the color map, where the grayscale map spans the entire Gale Crater which spans 100 kilometers the true color map only spans a little under 10 kilometers. This color map contains the entire rover’s path by Bagnold Dunes over its mission duration so there is little reason to go outside of it other than to view the nearby Mount Sharp.  

I think a big accomplishment of this map’s software was that this Curiosity map helped inspire NASA to reuse the mapping software as their proprietary GIS for all rover mapping. This has allowed for UI and functionality improvements over the lifetime of this map making it an iterative and thus agile product. I think if there were multiple different map softwars with different UI/UX for each rover mission over the years it would make it harder and less compelling to interact with the maps and compare their information. Being able to compare the maps is important in familiarizing users with foreign geographies as humans map out planetary geography. I think the greatest shortcoming of the map is the webpage it is embedded in which doesn’t match the UI design of the map and more importantly retains little info on the map. In order to get any text information beyond the two types of base maps being used I had to look into the web inspector. Here I found a GitHub where I was able to find further documentation on the map online after looking up the Github owner’s name. I think this is because NASA is a government site which may have limited the amount of information allowed to be divulged on the front page to all users, lack of documentation may also be a competitive move in which NASA is trying to cover up their software’s documentation breadcrumb trail. Such government sites are notorious for far worse UI/UX so by normal industry standards this page may seem lacking for such a high-level technology field, but by government digital design standards it is quite cutting edge indeed.



Calef, F. J., Gengl, H., Soliman, T. K., Powell, M. W., & Abercrombie, S. P. (2016). MULTI-MISSION geographic information SYSTEM (MMGIS) for a Mars rover. doi:10.1130/abs/2016am-287379

Where is Curiosity? Location map. (2021, January 13). Retrieved March 11, 2021, from https://mars.nasa.gov/msl/mission/where-is-the-rover/

Zhao, J. (n.d.). Jakobzhao/geog458. Retrieved March 11, 2021, from https://github.com/jakobzhao/geog458/tree/master/weeks/week03
