---
title: 'Fundamentals of QGIS'
cover title: 'Fundamentals of QGIS'
description: "This workshop builds on the foundational concepts of cartography to teach you fundamentals of map creation in QGIS. You will analyze and visualize data from New York City's 311 hotline. Using a fundamental mapping workflow, you will find the answer to the question, 'In which NYC neighborhoods are the most noise complaints filed?' No mapping experience is necessary."

learning objectives:
    - Become familiar with the user interface of QGIS
    - Explore and set projected coordinate systems
    - Learn to add, organize, and inspect spatial data
    - Create and export a map layout

estimated time:
    - 2.5 hours

prerequisites:
    -  mapping-foundations:
        description: (Required) This workshop will teach you the foundational concepts and terms of GIS that are applicable across platforms.
        required: true
    - data-ethics:
        description: (Recommended) In order to have a better understanding of the data formats we handle in this workshop, if you don't already have a foundational understanding of data formats and types, you can start by walking through our Data Ethics workshop.
        recommended: true
  
installations:
    - qgisguide: 
        description: "(Required) To complete this workshop you will need to install QGIS. Step by step installation instructions are available [here](https://github.com/goforanna/fundamentalsofQGIS/blob/2b0494dbbe684a6d5d678f392c90ff46a5046991/QGISInstallInstructions.md)."
        required: true

instructors: 
    - 'Anna Schlenz'

authors:
    - 'Anna Schlenz'

additional readings:
    - "[Finding the Right Tools for Mapping](https://digitalfellows.commons.gc.cuny.edu/2019/06/03/finding-the-right-tools-for-mapping/)"
    - "[Finding Data for Mapping: Tips and Tricks](https://digitalfellows.commons.gc.cuny.edu/2018/11/24/finding-data-for-mapping-tips-and-tricks/)"
    - "[Create A Rich Multimedia Narrative with ESRI Story Maps](https://digitalfellows.commons.gc.cuny.edu/2019/02/12/create-a-rich-multimedia-narrative-with-esri-story-maps/)"
  
projects:
    - "[Visualizing NEH Open Data](https://digitalfellows.commons.gc.cuny.edu/2017/04/04/visualizing-neh-open-data/)"
    - "[Mapping Occupation](https://gcdi.commons.gc.cuny.edu/mapping-occupation-the-union-army-and-the-meaning-of-reconstruction/)"
    - "[NYC’s Worst Evictors](https://www.worstevictorsnyc.org/map/)"
    - "[Torn Apart/Separados](http://xpmethod.columbia.edu/torn-apart/volume/2/index)"
    - "[Native Land](https://native-land.ca/)"
    - "[COVID Mapping Projects](https://digitalfellows.commons.gc.cuny.edu/2020/11/02/mapping-the-effects-of-covid-19/)"

ethical considerations:
    - Starting from figuring out how to represent a 3D reality on a 2D plane, there are countless subjective decisions that every mapmaker must make, whether they are conscious of it or not. Mapmakers need to decide what data to represent and what to leave out. They also need to decide how to aggregate, categorize, project, combine, and visualize the data. All of these decisions will influence the story that the map tells. Additionally, as a critical tool of Western colonialism and imperialism, maps wield great authority. As mapmakers, it's essential to be conscious of this history not to reproduce harmful power dynamics through mapmaking. Once something is visualized in the form of a map, it is often understood as a Truthful representation of reality. Therefore, mapmakers have an important responsibility to be as honest and transparent as possible. Since the 1980's, there have been two emerging disciplines in academia—critical cartography and feminist GIS—that have brought to light many of the harmful applications of mapping. Rather than reject mapping, they have made significant contributions to the field of GIS and mapping, such as counter mapping, sketch mapping, participatory mapping, qualitative GIS and 3D body-mapping. See the Scholarly Resources provided to introduce you to some of the fundamental insights from critical cartography and feminist GIS that you can integrate into your mapping journey. The list also includes modern-day counter mapping projects.

scholarly resources:
    - "Harley, J. B. (1989). [Deconstructing the map](https://quod.lib.umich.edu/p/passages/4761530.0003.008/--deconstructing-the-map?rgn=main;view=fulltext). _Cartographica: The international journal for geographic information and geovisualization_, 26(2), 1-20. This is a classic text by Brian Harley – one of the first Foucauldian analyses of mapping."
    - "Pavlovskaya, M., & Martin, K. S. (2007). [Feminism and geographic information systems: From a missing object to a mapping subject](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1749-8198.2007.00028.x). _Geography Compass_, 1(3), 583-606. This article makes the case for feminist GIS." 
    - "Pavlovskaya, M. (2002) [Mapping urban change and changing GIS: Other views of economic restructuring](https://www.researchgate.net/publication/240107165_Mapping_Urban_Change_and_Changing_GIS_Other_views_of_economic_restructuring). _Gender, place and culture: A journal of feminist geography_ 9, 281-289. This study demonstrates how GIS can be part of a critical and feminist analysis of economic development." 
    - "Kwan, M. P. (2008). [From oral histories to visual narratives: Re-presenting the post-September 11 experiences of the Muslim women in the USA](http://meipokwan.org/Paper/SCG_2008.pdf). _Social & Cultural Geography_, 9(6), 653-669. This study by a feminist GIS scholar uses 3D body maps to challenge the 2D limitations of most maps. She also combines interviews and survey data to create the visualizations." 
    - "[Counter Mapping: Zuni Maps](https://emergencemagazine.org/feature/counter-mapping/). The indigenous Zuni people describe their mapping project and the ways it challenges Western modes of mapping." 
---
# Downloading Datasets
In order to follow along with this workhop, you will need to download the related data files. This workshop uses just two datasets: 

1. A shapefile of NYC Neighborhood Tabulation Areas (NTAs)
2. A CSV of 311 Noise Complaints filed between January and March of 2024 in NYC.

We will talk more about what this data is a little later. Let's just focus on downloading them for now. 

##
You will download 1 folder and 1 compressed CSV file linked below. Please read all of these instructions before downloading. The files are called *geo_export* and *311_Service_Requests*. Compressed (or zipped) files make it easier and faster to share big and complicated data, but once you download the files, you’ll need to decompress/un-zip/extract the folders in order to make use of the data inside. <br>
	
The folder contains numerous files, all of different types. It is very important that you do not attempt to rename or move any of these individual files, they’re named for QGIS to be able to read, not for humans to be able to read. QGIS knows how to package these files together into map-able data, so it’s important that these files keep their names and stay together. <br>

Moreover, when working with any data management software, but especially with mapping softwares, it’s very important that your files are organized on your computer in a way that both you AND your computer can understand and easily access. Please do not save this data folder in a subfolder of your photos folder that has pictures of your last vacation! And please do not leave it in your Downloads folder! Lots of errors that come up when people are learning QGIS originate in where they saved their data. Follow these steps:

**Workflow for best practices of data storage**

1. Create a new folder (on your desktop or wherever you can easily access it) to hold all of your present and future mapping projects, maybe titled ‘QGIS_Projects.’ 
2. In that folder, create a subfolder titled ‘First_Project’. This will be your project folder in which both your QGIS project file and your project data folder will be stored.
3. In the First_Project folder, create a subfolder titled "Data."  
4. Within the Data folder is where you’ll save the unzipped geo_export and 311_Service_Requests files. <br>

<Download files='311_Service_Requests_from_2010_to_Present_20250121.csv.zip, geoexport_2020(1).zip'> 

After you download, right-click the downloaded files one at a time (but do not click into the folder) and select Open, Extract, Unzip, or Decompress (this terminology depends on your OS).

You may be asked where to extract the files to. If so, navigate to the easily accessible Data folder that you just created.

If you are not asked about where to place the folder and it just decompresses in the downloads folder, move the decompressed files into the easily accessible Data folder that you just created. Now that the files are where they're supposed to be, open the Data folder to make sure that you have 6 files.

Congratulations! You’ve downloaded the software and organized the project files! That process of data download/organization is a constant one when working with GIS. And as you collect more and more data for mapping, you’ll often re-use data in multiple projects, so it’s good that you’re forming data organization habits that will help you in the long run. 

# About QGIS

QGIS (Quantum GIS) is a free and open-source Geographic Information System (GIS) that enables users to view, edit, analyze, and interpret spatial data.

**Why Use QGIS?**
- Free & Open-Source: No cost to use or distribute, and the source code is available for modification.
- Cross-Platform: Works on Windows, macOS, and Linux.
- Community Support: Active user and developer community offering tutorials, documentation, and forums.

**What is QGIS Not Good For?**
- High-End, Real-Time Analysis
- Large-Scale, Big Data Analysis
- Advanced 3D Visualization and Analysis

Now it's time to dive in and get a taste of what QGIS can do!

# Getting Oriented in QGIS
We're going to get ourselves oriented in QGIS. We'll go over the layout of the user interface, point out the main buttons and tools available, and practice navigating the map canvas.

## Navigating the User Interface
Open QGIS and you'll see the user interface. We'll briefly go through each area of the interface before creating a new project. The **Browser** and **Layers** panels are docked on the left side, and at the top are **Menu Bar** and the **Toolbars**. At the bottom is the **Status Bar** and the **Locator Bar**. The rest of the space is the **map canvas**, which at initialization is populated by thumbnails of recent projects, the news feed, and project templates. 

![Annotated screenshot of user interface](/images/mapping/qgis-ui.png)

### Browser Panel
The Browser panel contains a file tree that allows you to access your computer's files and folders, and this is how you'll add data into map projects. Below the drives are Database connections. Spend a minute expanding the file tree by clicking the arrows to the left of each folder. Navigate to the project folder that holds our data, right-click and select 'Add as Favorite.' This copies the folder to the Favorites folder at the top for quick and easy access. Collapse the file tree by clicking the arrows again. 

### Customizing the UI
You can reorganize the various panels and bars in the UI to your liking by clicking on the name of the panel and dragging. Left click on 'Browser', and drag the panel toward the right side of the screen by moving your mouse while the left-click is still engaged. Notice how the Browser panel is now free floating as a standalone panel. Continue to drag the Browser panel to the right side of the screen, and a highlighted blank space will appear. You can dock the Browser panel on the right by dropping the panel into the highlighted space. 

![Screenshot of QGIS UI with Browser panel undocked](/images/mapping/browser-panel.png)

You can also convert a docked panel into a standalone panel by clicking the icon with overlapping squares in the top right corner of the panel. You can remove unnecessary panels by clicking the X icon in the top right corner. Remove the layers panel by clicking the X icon. 

You can add panels or toolbar into the UI by clicking **View** in the Menu Bar and hovering over Panels or Toolbars, then clicking the items you want to be added into the UI. Add the Layers panel with View | Panels | Layers. Dock the Layers panel on the left side of the screen. 
## Creating a project
Now its time to create our first project. You can create a project by double clicking on the 'New Empty Project' template in the templates window, or you can go to Project | New in the menu bar. 

To save the this project, navigate to File | Save As in the menu bar, name the file 'Fundamentals_311Data' and save the file in a QGIS dedicated folder. 
### Adding a Basemap
Now we have an empty map canvas that we can fill with spatial data. To orient ourselves in the map canvas, we're going to add a **Basemap**. A basemap is a background layer that provides contextual geographic information for your data. Basemaps are typically static layers that show general geographic features such as streets, terrain, satellite imagery, or topographic maps, but they do not contain specific data that you want to analyze. 

We're going to use the default basemap from OpenStreetMaps. To do this, expand **XYZ Tiles** in the Browser Panel and double click or drag OpenStreetMap into the Map canvas. Notice that OpenStreetMap is now a layer in the Layers Panel. We'll talk more about this in a bit. But first we'll learn how to navigate the map with **zooming** and **panning**. 

## Navigating the Canvas

### Zooming
You'll often zoom in and out to different scales by using the Mouse Scroll Wheel:
- **Zoom In**: Scroll **up** on your mouse wheel to zoom in.
- **Zoom Out**: Scroll **down** on your mouse wheel to zoom out.
Practice zooming in and out while positioning your cursor in different areas on the map. Notice that as you zoom in, the map readjusts to keep that area in view.  

You can also use the Zoom Tools in the Toolbar. Clicking the **Zoom In** tool (magnifying glass with a "+") in the toolbar. Click around the map in different areas. Notice that as you zoom in, the map readjusts toward the area that you click on. Now, click and drag a rectangle around the area you want to zoom into. This will zoom into that selected region. Now click the Zoom Out tool (magnifying class with a "-"). Click around the map to zoom out. 

To quickly view the entire map extent, click the **Zoom to Full Extent** button (magnifying glass with three arrows). This zooms out to show all data layers in the project. You can also manually set the scale of your map by entering a scale ratio in the Scale Box in the Status Bar. 

### Panning
You can move the map view, which is called panning, in a few ways: 
1. Click the **Pan** tool (hand icon) in the toolbar and then click and drag the map to move around.
2. Hold down the **spacebar** and drag the cursor around the map. Notice that holding down the spacebar turns the cursor into a little fist. 
3. If you have a mouse, you can click and hold the **scroll wheel** and drag the cursor around the map. 
4. Use the **arrow keys** on your keyboard to move the map in small increments.
5. You can also type specific **coordinates** in the **Coordinate Box** in the Status Bar. This allows you to quickly navigate to a precise location based on known coordinates.

### Knowledge Check
1. Zoom to the full map extent.
2. Zoom in to the Continental United States.
3. Pan down to the bottom tip of South America.
4. Zoom in to the Falkland Islands.
5. Zoom to the full map extent.
6. Type the coordinates **-8230535, 4967483** into the **Coordinate Box** and type **1:250000** into the **Scale Box**.
7. Press Enter. Where are we? 


<Secret>
New York City!
</Secret>

### Bookmarks
Since we'll be working at the scale of New York City, we should create a **Spatial Bookmark** of this extent so that we don't have to zoom and pan to it over and over. To do this, click on the Spatial Bookmark button in the toolbar (blue bookmark with yellow star icon). In the Bookmark Editor dialog box, name the bookmark "New York City" and click Save. Now in the Browser panel, expand Spatial Bookmarks and Project Bookmarks to see that the New York City bookmark has saved. Whenever we want to return to this extent, we can click this bookmark. 

# Adding and Organizing Data
Now its time to add our own data into the map. 

We have two sets of spatial data for this project: 

**A shapefile of the New York City Neighborhood Tabulation Areas (NTAs): "geo_export_941b0fdf..."**
- This file was downloaded from [NYC Open Data](https://data.cityofnewyork.us/City-Government/2020-Neighborhood-Tabulation-Areas-NTAs-/9nt8-h7nd/about_data). NTA boundaries are used for statistical purposes only and may not reflect all local understandings or definitions of NYC neighborhoods. While they use familiar names, they aren't official neighborhood boundaries.


**A CSV of 311 Noise Complaint Data with x,y coordinates: "311_Service_Requests_from_2010_to_Present"**
- Even though the file name says all service requests 2010 to Present, the data only contains noise complaints from the first three months of 2024.
- The main dataset for this workshop is from [NYC Open Data](https://data.cityofnewyork.us/Social-Services/311-Noise-Complaints/p5f6-bkga/about_data) collected from NYC’s 311 call center. Some of the most popular complaints filed through 311 are about parking, noise, garbage, etc. We’ll be working with just the noise complaints in this workshop.

  The 311 dataset is a great resource for anyone studying New York City. However, it is important to remember that 311 data tracks complaints, not necessarily the real conditions themselves. Because the data relies entirely on people choosing to speak up, it carries a natural bias toward the habits of those who complain. While 311 is a powerful tool for understanding city life, we must look at it critically, recognizing that this dataset shows us what people are bothered by noise by rather than a real picture of the noisiness of the city.
   
## Adding Data: Shapefiles

We'll start by adding the two shapefiles and will deal with the CSV in a bit.

In the Browser panel, expand the Data subfolder in the First_Project folder. Add the "geo_export_941b0fdf" file into the map by double clicking. 

QGIS randomly assigns a fill color to the neighborhood features, and we can change the color later. 
Notice how the Neighborhoods layer was added to the Layers panel on top of the basemap. 
Rename the Neighborhoods layer by right-clicking the file name in the Layers panel > selecting 'Rename Layer' > typing in 'NYC Neighborhoods' > and hitting enter. 

## Data Layers

Since we added the NYC Neighborhoods layer most recently, QGIS automatically places the data as the topmost layer in the map canvas above the base map, and this layering correlates with the ordering in the Layers panel. This ordering is called the **drawing order**.  

Click the checkmark to the left of NYC Neighborhoods. This checkmark toggles the layer visibility. It does not remove the data from the map project, it just tells QGIS to not render the data in the canvas so that you can see the layers underneath in the map canvas. 

Now turn the visibility of NYC Neighborhoods back on. You can change the drawing order of the data layers by clicking and dragging the layers up or down in the Layers panel. Play with the drawing order of the two layers, and notice how the map canvas changes to reflect the drawing order. 

When you're done experimenting, place the OpenStreetMap layer at the bottom of the drawing order. 

To fully remove data from the project, right-click the layer you want to remove and select 'Remove Layer.' Right-click the NYC Neighborhoods layer. Before we select remove, let's pause and go over some of the other options accessible with a right-click in the Layers panel: 

- **Zoom to Layer** zooms and pans the map canvas to bring the selected layer into view.
- **Copy Layer** adds a temporary copy of the layer to your clipboard so you can paste it into other projects.
- **Duplicate Layer** creates a copy of the layer within the same project and adds it below the original layer in the drawing order. 
- **Open Attribute Table** opens the attribute table of the layer to let you review or edit it. We'll talk more about attribute tables later.
- **Set Layer Scale Visibility** allows to you set a particular scale at which QGIS will render the layer in the map canvas. This can be useful for layers that have extremely local data which might obscure other map features at a small scale. 
- **Properties** opens the Layer Properties window, which is where you can review the metadata and access even more tools for data analysis and visualization.

Now we can remove the NYC Neighborhoods layer. Click Remove Layer. 

### Knowledge Check
Add the NYC Neighborhoods layer back into the map from the **Browser**. 

<Secret>
Navigate the Browser panel to the Data folder of First_Project. Drag and drop "geo_export" into the map canvas.
</Secret>


## Setting A Coordinate Reference System

Remember from the previous workshop that all maps are projections, and they should be projected differently depending on a map's purposes and goals. The basemap that we added, OpenStreetMaps, is meant to be useful at a world scale and local scales, so it uses a **Coordinate Reference System** (CRS) that is applicable to world scales, but not particularly accurate for our New York-based project. As a reminder, a CRS defines how the two-dimensional or three-dimensional coordinates of a location on Earth are mapped onto a flat surface, these are often called projections. 

We're going to change the CRS to one that's useful for this project. 

In the bottom right corner of the interface, you'll see an icon of a globe intersected by a plane with text to the right that most likely says something like "EPSG: 3857." Hover over this button to see information about the current CRS applied to the map project. The EPSG code is a numeric identifier that uniquely represents a specific CRS or projection. The code helps standardize the use of projections across different GIS software and systems. To the right of the EPSG code is the name of the CRS. If the EPSG is 3857, the CRS is the Web Mercator projection. 

Click the **CRS button** to open the **CRS Tab** in the Project Properties window, where you can explore and change the CRS for this project. 

![Screenshot of Coordinate Reference System Window](/images/mapping/crs-window.png)

At the top of this window is a Filter Bar where you can search for a particular CRS. This filters the catalog of CRSs below. Under the Filter Bar is a catalog of recently used CRSs, which has the current CRS highlighted. Next down is the catalog, which is organized first by CRS types: Compound, Geocentric, Geographic, or Projected. We need a Projected CRS. Expand the Projected folder. Here you'll see subfolders of many different types of projections. And these subfolders expand to show the different projections of that type. Browsing these projections can be quite overwhelming, especially if you aren't familiar with all the different projection types. That's ok! At the bottom of the window is projection information and projection preview, which offer useful information on how the selected projection works and what its useful for. 

Spend a few moments exploring the catalog, expanding the subfolders and clicking various projections to see how the properties and previews change for each projection. (Don't click apply or OK). 


Now its time to find the projection we need, which is **NAD 1983 (2011) StatePlane New York Long Isl FIPS 3104 Ft US**. Instead of browsing through the whole catalog to find this projection, use the Filter Bar to pare down the projections that display in the catalog. Begin to type 'NAD83' into the Filter Bar, and notice that the catalog filters accordingly, but there are still so many projections to choose from! Continue to type the rest of the projection name into the Filter Bar, and soon you should be left with just a few projections. 

Select **NAD_1983_2011_StatePlane_New_York_Long_Isl_FIPS_3104_Ft_US**. 

Notice that in the projection preview, the area in the red box is the projection's area of accuracy, and the purple box represents the current view in our map canvas. Click Apply. 

A Dialog Window will open asking you to decide how to transform the data from the current projection (Mercator) to the selected projection (NAD83). Explaining this transformation is a bit beyond what you need to know for most projects, so usually you'll select the first operation, which is bolded to indicate the recommended option. Select the first operation, click OK to close the Dialog Window. Then click OK in the CRS Properties Window to close the window. It may look like not much has changed, but the layers have adjusted at a minute scale to conform to the NAD projection.   

## Adding Data: CSVs

So far we have one polygon shapefile (NYC Neighborhoods) and a basemap (OpenStreetMap) added a layers into the map. It's time to add our Noise Complaints data, which is held in the CSV file. Drag the '311_Service_Requests' file from the Data folder in the Browser into the map canvas. 

Nothing about the map changed! That's because CSVs are not formatted as spatial data, they're just tabular data. Notice that even though nothing changed in the map canvas, the Noise Complaints file was added into the drawing order as a **Table**, marked with a table icon.  
## Inspecting the Attribute Table

We'll inspect the tables of our two data formats to see their differences. Open the NYC Neighborhoods attribute table by right-clicking the layer in the Layers Panel and selecting **Open Attribute Table**. The layer's attribute table will open in a new window. This is almost as simple as an attribute table will ever look. There are 11 fields, indicated by the eleven columns with field names at the top of the table. Scroll to the bottom of the table and not that there are 262 rows, indicating that there are 262 features in this layer. Each row contains data for one feature--one neighborhood. So, there are 262 rows holding the data for the 262 polygon features, which are the 262 neighborhoods in New York City. The last two fields, shape_area and shape_leng hold the data that tells QGIS what the placement and shape of each feature is. These should almost never be edited. 

If you need to edit other data--let's say there was a typo in one of the neighborhood names, you can toggle editing mode by clicking the **pencil icon** in the top left corner of the attribute table window. Click the pencil icon and hover over the buttons to the right of the pencil to briefly learn about the tools for editing the Attribute Table. Be sure to not click any of these tools. Turn off editing mode by clicking the pencil icon again.  Close the Attribute Table. 

Open the 311_Service_Requests Table. Just like the Neighborhoods attribute table, this table has fields in the columns, and has entries for every noise complaint in each row. Scroll to the right to explore the different fields, taking note of Agency, Descriptor, X Coordinate, and Y Coordinate. Close the table.


## Converting a CSV to Point Feature Layer
We are going to use the data in the X Coordinate and Y Coordinate fields to convert this CSV into a point feature layer. 

To do this, we will use just one of the many, many, many tools available for data management in QGIS. It's likely that your future projects will require that you do some learning on your own to figure out which tool is right for the job at hand. But for this workshop, we will use just a few tools. 

Click **Layer** in the menu bar, then hover over **Add Layer**. To the right, select **Add Delimited Text Layer**.  This tool allows you to convert delimited text files into feature layers, which is exactly what we need. 

In the Data Source Manager Window that opens, click the ellipses in the top right corner to navigate to the 311_Service_Requests CSV in your file explorer. 

In the Layer name field, type: 2024 Noise Complaints Jan - Mar.
Under Geometry Definition, select Point coordinates. Click the drop down arrow in the X field box. Here is where we tell QGIS what field in the CSV to use as X Coordinates. Scroll to and select "X Coordinate (StatePlane)." Do the same thing for the Y field, selecting "Y Coordinate (StatePlane)" instead. 
Make sure that:
- the selected file format is CSV
- 'First record has field names' is checked
- the Geometry CRS is NAD 1983 State Plane NY Long Isl FIPS 3104 US Ft. 

Click Add and Close the window. 

![Screenshot of Delimited Text Layer Export Window](/images/mapping/delimited-text.png)

Open the Attribute Table of the newly created Noise Complaints Layer to see that the fields and attributes were accurately converted and that there are no unexpected NULL values. Close the Attribute Table.

Remove the 311_Service_Requests CSV table from the Layers panel. 

## Exporting Feature Layers

Before we go further and play with how this data is visualized, we should export this point feature layer for future use. An important thing to note that while we continue to change and visualize this data in the map project, the original files housed in the browser haven't changed. So, while we have the Noise Complaint layer in the map project, it doesn't exist in our browser. If we delete it or want to use it in a different project, we would have to create this layer over again. Instead, we can export the layer as a standalone file housed on your computer and accessible through the browser. 

To export the Noise Complaint feature layer, right-click 2024 Noise Complaints and hover over **Export**, then select **Save Features As**. 

Select **ESRI Shapefile** from the Format Dropdown box. 
For File Name, use the ellipses to navigate to the data folder for this project, and name the file 2024NoiseComplaints. 
Select **point** for the **Geometry Type**. 
Uncheck 'add saved file to map' and click Save. 

Now expand the Data folder in the Browser to see that the point feature layer has been saved into the folder. 

Later on in this workshop, we are going to combine the NYC Neighborhoods layer with the Noise Complaints layer. In order to do that, we need to make sure both layers are using the same Coordinate Reference System. Let's check the Coordinate Reference System of the NYC Neighborhoods layer by right-clicking the layer in the Layers panel, then hovering over "Layer CRS." At the top of the new drop-down menu is the Reference System that the file was created in, which is **WGS 84**. This is different from the Noise Complaints layer. The x,y coordinates used to plot the points in the Noise Complaint layer were collected in **NAD 1983 State Plane NY Long Isl FIPS 3104 US Ft**. 

To ensure that these layers can be combined, we're going to the NYC Neighborhoods layer as a new layer with a **NAD 1983 State Plane NY Long Isl FIPS 3104 US Ft** as its Coordinate Reference System.

### Knowledge Check
Follow the same steps for exporting the NYC Neighborhoods layer as you did for exporting the Noise Complaints layer, with a few adjustments. 
- Name the file "NYC_Neighborhoods_NAD"
- Select **polygon** for the "geometry type
- Select NAD 1983 State Plane NY Long Isl FIPS 3104 US Ft for the CRS.
<Secret>
To export the NYC Neighborhoods feature layer, right-click NYC Neighborhoods and hover over **Export**, then select **Save Features As**. 

Select **ESRI Shapefile** from the Format Dropdown box. 
For File Name, use the ellipses to navigate to the data folder for this project, and name the file NYC_Neighborhoods_NAD. 
Select **polygon** for the **Geometry Type**. Then change the CRS to NAD 1983 State Plane NY Long Isl FIPS 3104 US Ft.
Uncheck 'add saved file to map' and click Save. 
</Secret>

Notice that the re-projected NYC Neighborhoods NAD layer has been added to the map at the top of the drawing order. Move this layer below the Noise Complaints layer. 

Remove the original NYC Neighborhoods layer so that there are only three layers in the Layers panel: 
1. 2024 Noise Complaints
2. NYC Neighborhoods NAD
3. OpenStreetMap

# Analyzing Data
Now we have a map of each noise complaint filed in New York City from January to March of 2024. But because there are so many point features, this map can hardly tell us anything about where the most noise complaints are filed. In order to figure that out, we need to aggregate our point data to the New York City NTA polygons. 

## Joins and Spatial Joins
Now that we have an appropriate spatial layer, we need to count up how many complaints fall within each neighborhood. To do this we’re going to do something called a **Spatial Join**. **Joins** are the bread and butter of GIS. There are two kinds of join processes in GIS. The first is just a regular ‘**join**,’ and it joins fields from one layer to another based on shared attributes. 
For example, say we have a two different files. One has data on the Names and Addresses of your family members. The other file has data on the Names, Birthdays, and Allergies of your family members. Because both files have data on Names, you can use the join function to append the Birthdays and Allergies attribute data to the layer with the Address data. 

A **spatial join** is just a bit different, but the difference is important. A spatial join is based on spatial relationships rather than attribute values, and it joins the two layers by comparing their geolocation. 

We’re going to do a spatial join today, because we want to compare the locations of the noise complaints with the locations of the neighborhoods. 

### Building a Spatial Index

Since our Complaints point dataset is so large, we first need to create a **spatial index**. A spatial index is A spatial index is a specialized data structure that allows a QGIS to efficiently categorize features based on their location on a grid. Having a spatial index for our Complaints layer will allow our spatial join to run much more quickly. Without an index, the spatial join could take hours to complete. 

To build a spatial index of our Complaints layer, right click the Complaints layer, and select Properties. Click the Source tab of the Layer Properties Window. Then, under the Geometry heading, select the "Build Spatial Index" button. Close the Layer Properties window. 

### Counting Complaints by Location

There are multiple tools to use to do a spatial join in QGIS, the most common one being "Join by Location." But since we also want to _count_ the points, we're going to use a tool called "Count Points in Polygon." This tool is located in the Processing Toolbox. This toolbox is not currently visible right now, so we’re going to have to pull it up.
Go to View > Panels > Processing Toolbox. Dock the Processing Toolbox underneath the Browser in the right corner. 

In the processing toolbox is a catalog of the various geoprocessing tools QGIS has to offer. There are a lot. Spend a few seconds opening and closing the carrots to see all the kinds of tools and get a sense of how they’re organized. 

When you're ready, search for "Count Points in Polygon," which will appear under the Vector Analysis tab. 

In the Count Points in Polygon window, select the neighborhoods layer from the Polygons drop-down menu. Then, select the Complaints layer from the Points drop-down menu. Under "Count field name" type, "NumPoints". Click Run. Even with a spatial index, this may take several minutes. Go stretch your legs!

Once the geoprocessing tool has finished running, a new polygon layer named Count will be added to the top of the drawing order. This layer is an amended copy of the Neighborhoods layer. Rename the layer "Neighborhood Complaints." Open the attribute table of this layer and scroll to the right end of the table to confirm that the NumComplaints field has been created and is populated with the number of noise complaints that fall within each neighborhood.

Close the Attribute Table. 

# Visualizing Data
Congratulations, you've made it to the fun part of mapping! Playing with data visualization in GIS is where personality, creativity, and design really get a chance to shine. It is how data transforms into a compelling narrative. We will do this by adjusting the **symbology** of the Neighborhood Complaints layer. Symbology is the use of graphic elements (color, size, shape, transparency) to represent geographic features on a map. While a raw dataset might contain coordinates and numbers, symbology is what turns that data into a visual story. It determines how a point, line, or polygon appears to on the map based on its attributes.

Currently, the Neighborhood Complaints layer is symbolized as a single color. In this section you will change the symbology so that the polygons--the neighborhoods--vary in color according to the number of complaints filed within each group.  

Make sure that the Neighborhood Complaints layer is at the top of the drawing order.

## Applying Graduated Symbology to a Polygon Layer

In order to adjust the symbology of the Neighborhood Complaints layer, right-click the layer in the Layers Panel and select Properties. This opens the Layer Properties window. Select the "Symbology" tab from the left hand side. 
This brings up the Symbology window. There are many options to choose from when styling a layer, and this window can be disorienting. 

![QGIS canvas showing Neighborhoods with Graduated Symbology](/images/mapping/graduated-symbology.png)

At the very top is a drop-down menu that lists the primary symbology styles. Currently, "Single Symbol" is selected. Expand the drop-down menu and select "Graduated." Notice that this changes the stylization options that are available below. 

**Graduated symbology** is used to show quantitative differences between features by placing them into classes (or "bins") and assigning a specific visual style to each class. Instead of every single feature having a unique size or color, the data is grouped into ranges (e.g., low, medium, and high number of noise complaints).

First, we need to determine the attribute field that the polygons will be graduated by. Click the empty drop-down box to the right of "Value," and you'll see just the fieldnames for just the numeric attribute data in the Neighborhood Complaints layer. 

Select "NumComplaints."

### Classification Mode 

Next, we must select the mode of classification and the number of classes. This sets the size and number of the bins QGIS will sort each feature into. Class Mode is the statistical rule used to group data into different categories. 

The mode you choose determines exactly where the "breaks" occur--deciding which number of complaints is considered minimal, medium, or a lot. 


| Mode  | How it Works | Best Used For |
| ------------- | ------------- | -------------
| Natural Breaks (Jenks) | The computer looks for ""gaps"" and ""clumps"" in your data to find the most natural groupings.| Data that is unevenly distributed or has clusters (the GIS ""default"") |
| Equal Interval | Divides the range of data into equal sized chunks (e.g., 0–25, 25–50, 50–75). | Familiar ranges like temperature, percentages, or grades. |
| Quantile | Places an equal number of features into each class (e.g., 20% of features in each of 5 classes). | Relative rankings; showing the "top 10%" or "bottom 20%." |
| Standard Deviation | Shows how much a value varies from the average (Mean). | Highlighting outliers or seeing what is "normal" vs. "extreme." |
| Manual / Pretty Breaks | You (the human) type in the specific numbers you want for the breaks. | When you have legal or specific industry cutoffs (e.g., Poverty Line).

Most cartographers recommend 5 to 7 classes. Using 15 classes makes it impossible for the human eye to distinguish between the subtle shades of color.
Increase the number of classs to 6 on the right side of the Symbology window. 

Adjust the Symbology window so that both the window and the map canvas are visible. Then, select Natural Breaks and click **classify**. 6 classes populate in the middle of the Symbology window. Click Apply. Notice that the map canvas as re-rendered to display the polygons in colors that correspond to the number of complaints filed in each neighborhood.

Now let's customize the stylization of the graduated symbology.

## Stylizing the Symbology

Click the drop-down arrow on the right hand side of the Color Ramp. Hover over "All Color Ramps" and select **Oranges**. 

Next we will change the weight of the border lines between each polygon. Single-click the white color swatch in the first class. Then, hold the shift key down and double-click the dark orange swatch in the last class class. This opens up the **symbol selector.** 

Because we selected all of the swatches by holding down the shift key, any adjustments made in the **symbol selector** will apply to all of the classes. 

Click "Simple Fill" in the Style Tree at the top of the window. This opens new options for adjusting the Symbol Layer type. Simple Fill is currently selected. Click the drop-down menu for Symbol layer type and explore how the options change when selecting different Symbol layer types. When finished, re-select Simple Fill. 

Adjust the Stroke color by clicking the drop-down arrow to the right of the color swatch. Select the orange hue from the standard colors row, the last swatch on the right. 

Now adjust the Stroke width to 0.100000 millimeters. Click Ok to close the Symbol Selector. 

Click Apply to apply the style changes to the map canvas. Close the Symbology window. 
## Creating Labels

The final step in visualizing the data is to label the neighborhoods with the highest number of noise complaints. These are the 3 darkest polygons in the northwest corner of Manhattan. 

Make sure that Neighborhood Complaints is highlighted in the Layers panel. In the Layers tab of the menu bar, click Labeling. This opens the Label Styling tab of the Layer Properties window. 

Click the drop-down menu that reads "No Labels" to expand the labelling options:

- Single Labels: This is the most straightforward method. Select one column from your attribute table, and QGIS labels each feature in that layer with its attribute data.
- Rule-based labeling: Rule-based labeling applies labels only to features that meet certain user set requirements.
- Blocking isn't a labeling method, but rather a setting that tells QGIS: "Do not let any other labels overlap the features in this layer."

Select **Rule-based Labeling**. 

This brings us to the rule directory that will list the rules applied to the labels. It's empty now. We're going to create one rule to label features with. 

Click the green plus icon at the bottom of the Layer Styling window. 

In the **Description box**, type "Features with most complaints."

Next, click the purple sigma icon (Σ) to open the Expression Builder. Here's where we will define the rule. Since we want to label only the three features with the most noise complaints, we're going to build a rule that selects features with NumComplaints of 2199 or more. 

In the blank expression box, type the following:

 "NUMPOINTS" >= 2199

Click OK to close the Expression Builder. 

Next, under the Labels heading, change the Value to **ntaname**. Select the **buffer tab**, represented by abc surrounded in blue. Check "Draw text buffer". 

Click Apply. 

Now only North Harlem, the Central Upper West Side, and Lincoln Square are labelled. 

![Screenshot of QGIS Canvas with 3 Neighborhoods labeled](/images/mapping/labels.png)

Before we move on to creating a Print Layout, remove all other layers from the **Layers Panel** so that only the Neighborhood Complaints layer is in the drawing order.  

# Creating a Map Layout

You've made it to the final step of the map-making workflow for QGIS, which is transforming this map canvas into a final, sharable format. This is called a map **Layout**. 

Once your map looks exactly how you want it in the map canvas (layers turned on, colors set), go to the menu and select Project > New Print Layout.

Give your layout a name (e.g., "NYC Noise Complaints, Jan-March 2024").

A new window will open. This is your page layout workspace.

## Getting Oriented

Let's briefly talk about the new panels and toolbars available in the layout workspace. 

**The Left Sidebar: "The Toolbox"**

This is where you find the tools to add graphic items to your layout. Here are a few commonly used tools, starting from the top:

- Pan Layout: The white glove. Just like in the map canvas, this tool lets you pan within the print layout by clicking and dragging your cursor around the print layout.

- Zoom: The magnifying glass. Just like scrolling up and down on the mouse, this tool allows you to zoom in and out from the print layout.
   
- Select/Move Item: The white arrow. Use this to move or resize items in the layout (the map, the legend, etc.).

- Move Item Content: (Crucial!) The blue arrows inside a box. This lets you pan and zoom _inside the map frame_ without moving the frame itself.

- Add Map: The unrolling piece of paper with the green plus icon. This tool draws the **map frame** that will display your GIS data.

- Add Legend, Scale Bar, North Arrow: The "Big Three" map elements. Use these tools to add the map elements into your print layout by clicking and dragging to place and size them. 

**Panels**

Usually docked on the right-hand side, the Layout panels help with fine-tuning. It usually has two or three tabs, and you can pull them up by selecting View > Panels from the menu bar:

- Items Panel: Shows a list of everything on your page (Map 1, Legend, Label 1). It works like the layers panel in the main QGIS mapping window; you can select, lock, or hide layers here.

- Item Properties: This is the most important tab. When you click on an item (like your Legend), this panel changes to show settings for only that item (fonts, colors, columns, etc.).

- Layout Panel: General settings for the whole page, like export resolution (DPI) and world file settings.

**The Top Toolbars**: The Actions Toolbar, the Layout Toolbar, the Atlas Toolbar, and the Navigation Toolbar. 

These buttons handle the "big picture" tasks:

Layout Bar: The top left side of the toolbar contains tools for saving and exporting the print layout to Image, SVG, or PDF.

Atlas Bar: The top right side of the toolbar. Buttons that look like a world globe with a blue "play" button. They are usually greyed out. Use these if you are generating dozens of maps at once.

Navigation Bar: The bottom left of the toolbar. Standard magnifying glasses to navigate your paper workspace.

Actions Bar: The bottom middle of the toolbar, this row of icons helps with positioning map elements. You'll find tool like "Align Left," "Distribute Vertically," or "Bring to Front."

**The Print Canvas**  (The Middle)

This is the page on which you'll create the print layout by adding and arranging map elements to the page. Also in the middle are the **rulers**--located at the top and left. You can click and drag from these rulers to pull out **Guides** (red lines) to help you align your map elements perfectly with your print layout. Finally there is the **Status Bar** at the bottom. This displays the X/Y coordinates of your mouse on the page and the current zoom level of the paper.

If you're not sure what an icon does, you can hover over it with your cursor to display the name of the tool. 


Before we get started adding map elements to the print layout, here's what the final result will look like.

![Example of Final Map Layout](/images/mapping/final-layout.png)

The title will be at the top, the legend will be at the left, the map frame will be in the bottom right corner, and the scale bar and north arrow will be small and in the bottom right corner as well. Keep this positioning in mind and use this image as a reference while you follow along. 

## Setting the Page Properties

To set the size of the paper layout, click **View** in the menu bar, hover over **Panels**, and click **Item Properties** if it's not already checked on. Then click once on the white page layout to bring up its properties options in the **Item Properties** window. 

Select Letter in the Size drop-down menu and Portrait for the Orientation. 

Now that we've set the page properties, it's time to add the map into the layout. 

## Adding Map Elements

### Adding and Adjusting a Map Frame

From the left-hand Toolbox toolbar, click the Add Map icon (it looks like an unrolling blank page with a plus sign). Click and drag a box on your print canvas where you want the map to appear. The map will automatically render in the map frame at the extent set in the mapping canvas. 

Let's display just Manhattan to center the three neighorhoods with the most noise complaints. 
To move the map extent: Use the Move Item Content tool to pan or zoom inside the map box without moving the box itself. Once you've got the map extent and the map frame positioned how you want them, lock the map frame layer by checking the box under the padlock icon in the **Items** panel. This will prevent any accidental adjustments or misclicks on the map frame. 

### Adding a Legend

To add a legend, click **Add Legend** from the Toolbox, then drag a box. This automatically generates a legend with all items from the **Layers panel** of the mapping window.  

In QGIS, the legend doesn't behave like a simple image you can stretch. If you drag the corners, you often just change the "window" size rather than the text size. To truly adjust it, you have to use the Item Properties panel.

With the legend selected in the print layout, open the Item Properties tab to see adjustment options for the legend. To remove layers you don't want shown, uncheck "Auto update" under Legend Items and use the plus/minus buttons at the bottom of the window. Let's rename the Neighborhood Complaints layer. With the Neighborhood Complaints layer selected under Legend Items, click the pencil icon in the row of buttons at the bottom of the window. In the text box that pops up, type "Number of Complaints Filed". Then click the blue back arrow.

Scroll down in th Item Properties window to view the other Legend properties options, like adjusting the text formatting and positioning. 

## Adding a Scale Bar and North Arrow.

To add a **scale bar**, Click Add Scale Bar in the lefthand Toolbox. Then, click and drag a box in the print layout where you want to scale bar to be placed. With the new scale bar selected, you can change its properties in the Item Properties panel. Change the scale bar units to **Miles**, then scroll down and expand the **Appearance** heading. Click the down arrow to the right of the primary fill color swatch and select **Red**, the third color from the right in the row of Standard colors. 

To add a north arrow, click Add North Arrow from the Toolbox. Then click and drag a box in the page layout to create a north arrow. Just like the scale bar, you can change its appearance in the Item Properties window. To change the icon, click the "arrows" folder and select a new arrow icon from the SVG images box that populates on the right. 

## Adding a Title and Data Source

The title is the first thing a reader looks at. It should be prominent and clear, usually at the top.

Click the Add Label icon on the left toolbar and drag a box across the top of your map to create a text box for the title. In the **Item Properties** panel on the right, look for the Main Properties text box. Delete the default "Lorem Ipsum" and type your title, "Neighborhoods with the Most Noise Complaints Filed in New York City, January to March,  2024". 

Now let's style the font. Scroll down to the Appearance section. Click the Font button to change the typeface, set the style to Bold, and increase the size (usually 24–36 pt for titles). Click the blue back bottom to go to the main options of Item Properties, and change the Horizontal Alignment to "Right."

### Knowledge Check

Using the same process, add the data source just underneath the title with the text, "_Dataset from NYC Open Data,  "311 Noise Complaints." Updated January 2025._" Make the font size 15 points. 

## Exporting Your Map

It's time to export it as an image file to share with your friends. 

In the **Layout** **toolbar**, select the Export as Image tool, which is the icon with the page with a mountain image and a rightfacing arrow. Set the file name to "NYC Noise Complaints 2024" and the save location to your First_Project folder. Click Save. 

Keep the image export options as they are, but check "Open File After Exporting" on. Click Save. 

Congratulations! You've created your very first map. This workflow of Adding and Organizing data from the Browser, Analyzing it with geoprocessing tools, Visualizing it with the symbology window, and building a Print Layout is the most standard workflow when working in any mapping platform. Now you'll be able to practice this workflow with data of your own. 
