

# View by View Specification

The Site architecture requires the modification of a few views. Most views will remain largely the same, and the look and feel is to be designed in the future by a graphic designer. This document is more concerned with the functionality and the interaction design, not the exact look and layout.

All screens are created in HTML. They will be converted to nested angular components by programmers. 

Each screen is known by a canonical name which will always appear, in this document, in italics, so you know we're referring to a screen by name, for example,_ Site List View._

### Site List View![](/assets/Site List View%281%29.png)

Entry point after login. The user should be able to see all sites he has access to. Not show is a background map that shows markers representing the location of every site. When a site is clicked, the map should zoom in on the location and show the extents of the site. Clicking on a flight should show meta data for that flight or go straight to the flights view. There should also be fairly prominent buttons for uploading a Flight/creating a Site

###### Technical Note:

Showing the extents of a site can be done after the initial flight. Using the exif information for every image in the flight we should be able to generate a polygon dictating the area the done flew over using a simple convex hull algorithm. This data can be saved as an annotation for the flight, and be pulled into the map. 

### Flight Upload View: Choose Site

![](/assets/Flight Creation View%282%29.png)

First view of flight upload. Say Bern the Berm inspector wants to upload several flights. The first flight is for a completely new site he inspected today, the other is for the Chico site. He creates a new site, and sets the location by uploading one of the images he has on hand. He confirms its the right general location though the minimap, but adjusts the center a bit by panning. He then continues the rest of the wizard. Afterwards he uploads a flight again; this time he chooses to map this flight to his Chico site.

##### Technical Note:

Location informaiton can be uploaded manually through Lat/Long, or by inspecting the exif data of one of the images. We will need to decide whether the user should be able to set the extent of the site as well or only the center point. 



