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

### Flight Upload View: Image Uploads

After choosing a site, the user should be able to upload images, videos, and a gcp file. The workflow is to be speced out by the designer, but preferably has some way to represent the progress of asset uploads and the gcp workflow. 

### Flight Creation View: Share Settings

 When Phil goes to upload images of his flight, he should be able to choose what features of the flight. He should have been able to inherit the share settings of the site, and be able to choose further people to share certain features with. He can also choose the level of access each person has. Be it read, write, execture or some combination of the three. For convinence, all permissions are shown \(including those inherited from the site\) and can be overwritten. 

### Flight Creation View: Finish

Once the user is done setting the flight information, he can submit the flight for processing in this view.

### Timeline Visualization View

![](/assets/Timeline Visualization View.png)

Selecting any given site should show a view similar to what we have for dataprojects. The Orthophoto is shown with a colored outline for the current flight. What is new is the timeline visualization. The time line has a brush which selects the a section of available times. In this case the user has zoomed in to the range Dec 1 to Dec 3. From there the user can also click additional flights. Although only the currently selected flight will be shown in 3D \(for now?\) the orthophotos of the other flights is available in the 2D view. Each flight has a colored outline to show their extents. Measurements \(like the bench\) and Annotations \(like shotplan\) also have a colored outline. Selecting two annotations of the same type results in an overlay that shows the difference between them both. 

