---
title: Foundations of Mapping
cover title: Mapping
description: 'Mapping is a powerful way to analyze, visualize, and explore spatial data. A Geographic Information System (GIS) is a mapping technology that allows users to analyze spatial data and produce cartographic visualizations. This workshop will teach you the foundational concepts of GIS that are applicable across platforms. No prior experience necessary.' 

learning objectives:
 - Become familiar with the uses of cartography and spatial analysis
 - Identify fundamental mapping components
 - Distinguish between different forms of spatial data
 - Recognize some of the core ethical considerations of mapmaking.
 - Practice formulating spatial research questions
 
estimated time:
- 45 mins

instructors: 
    - 'Parisa Setayesh'

authors:
    - 'Anna Schlenz'

prerequisites:
  - data-ethics:
      description: "(Recommended) In order to have a better understanding of the data formats we handle in this workshop, if you don't already have a foundational understanding of data formats and types, you can start by walking through our Data Ethics workshop."
      recommended: true
  
installations:
  - none
  
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

scholarly resources:
  - "Harley, J. B. (1989). [Deconstructing the map](https://quod.lib.umich.edu/p/passages/4761530.0003.008/--deconstructing-the-map?rgn=main;view=fulltext). _Cartographica: The international journal for geographic information and geovisualization_, 26(2), 1-20. This is a classic text by Brian Harley – one of the first Foucauldian analyses of mapping."
  - "Pavlovskaya, M., & Martin, K. S. (2007). [Feminism and geographic information systems: From a missing object to a mapping subject](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1749-8198.2007.00028.x). _Geography Compass_, 1(3), 583-606. This article makes the case for feminist GIS." 
  - "Pavlovskaya, M. (2002) [Mapping urban change and changing GIS: Other views of economic restructuring](https://www.researchgate.net/publication/240107165_Mapping_Urban_Change_and_Changing_GIS_Other_views_of_economic_restructuring). _Gender, place and culture: A journal of feminist geography_ 9, 281-289. This study demonstrates how GIS can be part of a critical and feminist analysis of economic development." 
  - "Kwan, M. P. (2008). [From oral histories to visual narratives: Re-presenting the post-September 11 experiences of the Muslim women in the USA](http://meipokwan.org/Paper/SCG_2008.pdf). _Social & Cultural Geography_, 9(6), 653-669. This study by a feminist GIS scholar uses 3D body maps to challenge the 2D limitations of most maps. She also combines interviews and survey data to create the visualizations." 
  - "[Counter Mapping: Zuni Maps](https://emergencemagazine.org/feature/counter-mapping/). The indigenous Zuni people describe their mapping project and the ways it challenges Western modes of mapping." 
---

# The Power of 'Where'
### What can maps do?

A map is method of making sense of data. Maps can organize it, analyze it, visualize it, share it. More specifically, maps are best for examining the relationships between different things in a particular space--this is called **spatial analysis**. Maps use the 'where' of data to combine heterogenous datasets and reveal spatial relationships.

## Maps and spatial analysis
Here are some things maps and spatial analysis can be used for:
### Understand where

*Where is Cleveland, Ohio? Where are shoreline access points in my neighborhood? Where does my mom live?*

### Identify size, shape, and distribution

*What is the size of Lake Ontario? What is the geographic scale of my sample collection? What is the shape of Turkiye?*

### Determine how places are related

*Where is the closest fire station to a burning building?*

### Quantify patterns

*Where are building fires happening most often?*

### Find optimal locations or routes

*What streets should this firetruck take to get to the burning building as fast as possible?*
### Make predictions

*Where will the phenomena happen next?*

## Putting maps to work
In this example, considering the 'where' of public health data and of transportation data helps us learn about their underlying patterns and correlations. When Dataset A and Dataset B are cartographically combined we can more easily see a spatial relationship. 

![Combining Datasets of Trucking Routes and Lung Cancer in Texas](images/mapping/CombiningDataSets.png)

## Modern mapping - GIS 

A Geographic Information System (GIS) is a powerful tool for modern cartography and spatial analysis. At its most basic level, GIS transforms tabular data into cartographic visualizations. GIS takes an input table of names and addresses and outputs a visualization of those addresses in space. 

What makes GIS especially useful is that it can transform and integrate many large datasets as different layers within a single visualization. In the example below, individual datasets are transformed into layers and integrated into a complex visualization that represents the real world. 
![Visualization of GIS Integration of Layers](https://github.com/goforanna/mappingfoundations/blob/946f33d93dbfce5f6c03ee5211ad0a01a0894665/images/GISIntegration.jpg)

### Knowledge Check

Which of the following is GIS a useful tool for? (check all that apply)

<Quiz>
- Tracking the spread of an epidemic*
- Designing a logo for an Etsy business
- Studying income disparity*
- Creating a map of a fictional place 
- Identifying popular public beaches*
</Quiz>

# Components of a Map
In order to make a map, we need spatial data. **Spatial data** (also called **geospatial data**) refers to information about the **location, shape, and size** of objects or phenomena on the Earth's surface, and the relationships between them. In the real world and on globes, this data is often represented with geographic coordinates (latitude and longitude). But on flat surfaces, this data is represented with cartesian, or projected, coordinates (x,y coordinates). 
![Coordinate Systems](https://github.com/goforanna/mappingfoundations/blob/946f33d93dbfce5f6c03ee5211ad0a01a0894665/images/CoordinateSystems.png)

### Knowledge Check
What spatial data is needed to make a map like this one?
![Map of Walking Distance to Subway](https://github.com/goforanna/mappingfoundations/blob/946f33d93dbfce5f6c03ee5211ad0a01a0894665/images/subwaywalkingdistance.png)

<Quiz>
- Locations of NYC Roads*
- Shape and location of New York City*
- Shape of NYC Water Features
- Locations of NYC Subway Stations*
</Quiz>

## Types of Spatial Data: Vector and Raster 
There are two major file types of spatial data: **vector datasets** and **raster datasets**. Vector data is the most common type of GIS data. Vector data represents spatial data as collections of points, each with a given coordinate. Those points are then grouped into **features**. Before we talk more about vector data, we'll briefly touch on raster data. Raster data represents spatial data as a matrix of cells (or pixels) that each contain an attribute value (like elevation or temperature). Satellite imagery, jpeg scans of historical maps, or digital elevation models are all examples of raster data. Unlike vector data, the resolution is fixed in raster data, and the size of each pixel determines the level of detail in the map. Smaller pixels mean higher resolution, and larger pixels mean lower resolution. 

![Vector Data Versus Raster Data](https://github.com/goforanna/mappingfoundations/blob/946f33d93dbfce5f6c03ee5211ad0a01a0894665/images/rastervector.jpeg)

## Vector Data: Features and Attributes
Vector datasets represent spatial data as features. **Features** are the fundamental building blocks of map creation and are **displayed as points, lines, or polygons**. In the NYC Distance-to-Subway map from earlier, subway stations, streets, and the city boundary are the features of the map. 
- Subway stations are represented as point features, with no length or area.
- Streets are represented as line features, with length but no area.
- The city boundary is represented as a polygon, with both length and area. 

Features can also hold relevant non-spatial data, called **attribute data**. While spatial data represents the location, shape, and size of geographic features, **attribute data** provides more detailed, non-spatial information about those features, like subway station names (for points), street names (for lines), or populations (for polygons). Attribute data can be visually represented by changing the size, shape, or color of the feature (AKA the **symbology**), or by alphanumeric annotations. 

![Feature Types](https://github.com/goforanna/mappingfoundations/blob/946f33d93dbfce5f6c03ee5211ad0a01a0894665/images/featuretypes.gif)

## Vector Data: Layers and Feature Classes
GIS compiles and integrates data by layering different datasets on top of each other. These layers are called **feature classes**. Each feature class contains homogenous data, meaning that there is only one *kind* of feature in each feature class, whether its points, lines, or polygons, and the categories of attribute data are applicable to each feature within the feature class. For example, in the following image there are three feature classes. The street feature class contains line features, while the buildings and vegetation feature classes each contain polygon features. Each building is a polygon feature within the buildings feature class, and each feature contains attribute data like building type, address, number of floors, or hours of operation. 

![Visualization of GIS Integration of Layers](https://github.com/goforanna/mappingfoundations/blob/946f33d93dbfce5f6c03ee5211ad0a01a0894665/images/GISIntegration.jpg)
![Visualization of Feature Class]<img width="702" height="330" alt="featureclass" src="https://github.com/user-attachments/assets/3bc58563-4719-4ee8-98c4-9e5b0ae68d18" />


### Knowledge Check
The following are all types of vector data except:

<Quiz>
- Points
- Pixels*
- Lines
- Polygons
- Cells*
</Quiz>

# 'The Map is Not the Territory': Distortions, Decisions, and Ethics
Representing the real, 3D world in a contained, 2D display involves making choices and decisions that will necessarily be distortions of reality. At the most foundational level, every map begins with a lie--that the earth is flat. Any time you flatten a sphere you end up with distortion. This distortion worsens when the sphere isn’t a perfect sphere but is a kind of lumpy sphere--a geoid--like earth is. So when you flatten the earth into a **projection** you end up with some kind of distortion, no matter what. 

Distortion happens in four ways. **Shape** is distorted, **size** is distorted, the **direction** between point a to point b is distorted, and the **distance** between those points is distorted. To rectify this, cartographers have developed a myriad of different ways to project the earth onto a flat surface. These are called map projections. As a rule of thumb, each projection can preserve no more than two of the four distortions and usually is only applicable to different certain areas of the world at certain scales. 
![Projections and Distortion](https://github.com/user-attachments/assets/eff16094-86c0-4b17-b734-e47d2738607b)

For example, the Mercator Projection--the most famous and recognizable map projection--was originally developed for marine navigation across the Atlantic in the 16th century. The Mercator Projection preserves direction and distance near the equator at the cost of shape and size. See how at the world scale the Mercator Projection bloats the sizes and shapes of lands the further they are from the equator. Inappropriate and uninformed use of the Mercator Projection is how billions of people grew up thinking Greenland was the size of Africa.

 ![Mercator Distortion](https://github.com/user-attachments/assets/af5efac6-c648-401f-9423-29a4b0a64896)

 
Beyond visual misrepresentation, inappropriate projections can mess with the accuracy of your spatial analysis. If your analysis involves measuring large distances in the United States, for example, using the Mercator projection will produce a different calculation than a projection that preserves area and distance like the Albers Equal Area Conic.  
![Distance Distortion](https://github.com/goforanna/mappingfoundations/blob/946f33d93dbfce5f6c03ee5211ad0a01a0894665/images/distancedistortion.png)

### Knowledge Check
If you are making a map that shows how long it takes to walk to the nearest subway station in New York City, you should choose a map projection that preserves:

<Quiz>
- Size
- Distance*
- Direction
- Shape
</Quiz>

## Decisions and Ethics
So much of map-making is dependent on the positionality of the mapmaker and all of the subjective decisions that they must make when deciding what will be mapped, how the data will be manipulated, and how it will be visualized. Here are some questions to ask yourself as you begin to formulate your project:

- **What data should I use?** If you choose to use data that's already collected (e.g. Census data), are you using it because it's the easiest to access or because it's the most appropriate data to answer your research question? What are the limitations of using data that hasn't been collected or managed by you?
- **How should I classify the data?** What categories will you create? For example, if you are working with racial demographics, will you report on the categories such as Latinx, non-Latinx White, non-Latinx Black, Latinx White, Latinx Black, etc, or will you provide broader categories such as people of color and White? What are the implications of choosing more general or more particular categories?
- **At what resolution or scale should the data be aggregated?** If you are studying a phenomena at the neighborhood level, how do you define the boundaries of a neighborhood? Is it based on the school district, the Census Designated Place (CDP), the voting district, or maybe a boundary that doesn't have a formal delineation, such as a sense of community among people?
- **What projection should I use?** What kinds of distortion is it important for you to minimize? What are the consequences of sizes, shapes, distances, and directional aspects of your data being inaccurate?
- **How should my map be oriented?** Is it important that North be at the top of the map? What should be at the center of my map? 
- **What are the implications of aggregating the data at a certain scale?** For example, let's say you are studying the differences between urban and suburban areas. If you aggregate your data at the level of counties, what could be missing from that representation of the data? Is something happening at the level of the neighborhood or town that could prove useful to answer your research question? This is not to say that the smallest scales are always the best to work with, but rather to suggest that when we aggregate data, we need to be aware of what distinctions we are hiding in the process.
- **What colors and symbols should I use?** Should you represent a population in red or blue? Red normally signals something that is alarming, while blue is a more neutral color. These subjective cartographic design decisions greatly impact viewer's understanding of the map.

For more guiding questions on ethical decision making, please see ["Ethical Decision-Making"](https://serc.carleton.edu/geoethics/Decision-Making), a robust resource put together by the "Community of Earth Educators."

## Formulating a Spatial Research Question

Beginning with a well-framed spatial question about the problem or phenomena you're interested in is key to making a compelling map or producing informative results. Focus on the spatial relationships between research variables or the spatial characteristics of a single variable. 

The key is to start with a simple, answerable question. It's often the case that a seemingly simple and boring question can lead to bigger and more interesting questions. However, if you start with the big, complex question, it can be difficult to parse into concrete spatial relationships. So start small and then build on your question, if needed. 

Some spatial questions might take the form of:
- *How many are in an area?*
- *Which sites meet my criteria?*
- *What are the characteristics of an area?*
- *How is it distributed?*
- *What is near what?*
- *What is on top of what?*
- *How is it related?*
It's likely that your question will involve a combination of these formats, and its even more likely that exploration and experimentation during the map-making process will answer questions you hadn't thought to ask.

### Examples
- How do different land-use types (residential, commercial, industrial) influence traffic congestion in Los Angeles?
- What is the spatial distribution of public health facilities in the Bronx, and how does this relate to health outcomes?
- What are the patterns of unemployment rates across different neighborhoods, and what factors contribute to these patterns?
- How are the locations of ancient trade routes related to the development of cities in early civilizations?

# Break-Out Activity
1. Based on the examples and on the question formats, briefly try to formulate an aspect of your research interests into a spatial research question, thinking about all that is hidden within the relationships between places.
2. Share with your break-out group. What kinds of data do you need? What kind of spatial data might you already have?
