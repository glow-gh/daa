---
layout: default
title: "4. QGIS"
rank: 16
---

# Spatial data
This and succeeding modules [3.5 QGIS](./3_5_qgis.md) and [3.6 QGIS](./3_6_qgis.md) will introduce you to the structure, capability, and usage of software applications for working with spatial data. Spatial data applications allows for the integration, analysis and visualisation of spatial data collections, for producing maps, and for understanding spatial relationships.

## Introduction
'Spatial data' defines any type of standardised information that incorporates a spatial dimension. A spatial dimension can be relational, defining spatial relationships between entities (i.e. something is inside, outside, or next to something else), or geographical, defining location and extent within a geometric system. While we will primarily be working with the latter type of spatial data in this and subsequent modules, it is important to remember that relational spatial data also has uses of relevance for cuneiform studies, for example in the study and analysis of historical geographies.

### Spatial data applications

The present module will introduce you to the concept and basic structure of [Geographical Information Systems (GIS)](https://en.wikipedia.org/wiki/Geographic_information_system) and their usage. A GIS is a data structure or computer application that can store, manipulate, and present a complex range of data according to both spatial and attribute parameters using a wide range of tools.

A related type of application are [web maps](https://en.wikipedia.org/wiki/Web_mapping), such as [Google Maps](http://maps.google.com) or [Bing Maps](https://www.bing.com/maps), or any other static or interactive geographical visualisation of data found online. While these utilise many of the same functions as GIS software, they are primarily designed for data visualisation and consumption, and less for data generation and manipulation.

The first conceptual definition of a GIS was made by British geographer [Roger Tomlinson](https://en.wikipedia.org/wiki/Roger_Tomlinson) in 1968. The [Canada Geographical Information System (CGIS)](https://en.wikipedia.org/wiki/Canada_Geographic_Information_System), the first ever operational GIS, was launched in the 1960ies by the Canadian government as a tool for land resource mapping and analysis. 

Structuring data according to spatial characteristics has a great many applications - some of which you have no doubt made use of yourself in everyday life. Aspects of GIS are used in [indoor positioning systems](https://en.wikipedia.org/wiki/Indoor_positioning_system) and wayfinding applications, such as [MazeMap](https://www.mazemap.com) used for the Uppsala University campus.

![MazeMap indoor wayfinding tool](./_images/image_3_5_mazemap.png "Path from ground floor entrance of Building 9 to room 9-3042")

If you haven't used indoor positioning systems, you most certainly have used [Google Maps](http://maps.google.com) or similar applications for mobile and desktop devices. These services rely on the same basic data elements as the indoor positioning systems, but are true geographic applications, in that they rely on geographical coordinates.

![Google Maps](./_images/image_3_4_googlemaps.png "Google Maps vector graphics view of Uppsala University Engelska Parken campus")

They also typically include the option to switch between two basic types of views; one using [vector graphics](https://en.wikipedia.org/wiki/Vector_graphics) (such as the map of Engelska Parken campus above), and one using [raster graphics](https://en.wikipedia.org/wiki/Raster_graphics) (such as the map of Engelska Parken campus below). We will get back to the essential differences between these two types of data in a moment.

![Google Maps](./_images/image_3_4_googlemaps_sat.png "Google Maps raster graphics view of Uppsala University Engelska Parken campus")

If you have used [Google Maps](http://maps.google.com), chances are that you have also encounted [virtual globe](https://en.wikipedia.org/wiki/Virtual_globe) applications such as [Google Earth](https://earth.google.com/web/). This is another type of spatial data application that employs 3D software models to visualise the surface of the Earth (or other planets), typically using satellite imagery.

These are some examples of common spatial data applications for visualising or working with geographical information. A GIS software package is the desktop application that allows you to create, manipulate, store and visualise this type of data yourself. Let us now take a look at the structure of a GIS.

### Spatial data types
A GIS stores spatial data in **one** of **four** different types; **point**, **line**, **polygon**, and **raster**

* A **point** is a single vector location, which has no extent
* A **line** is a geometric shape with no width between two or more vector points
* A **polygon** is a contiguous surface between three or more vector points

**Point**, **line**, and **polygon** are vector graphics. The fourth type is **raster**, or **raster graphics**.

* **Raster** data consists of an orthogonal (square) grid of rows and columns of cells in which each cell holds a single value (colour, altitude, or temperature, for example)

The different structure of **vector** and **raster** graphics means that they are stored in different file formats. Where **vector** grphics can be stored as text, **raster** graphics are typically stored as images. This has an impact on the way in which data can be imported into a GIS. A set of GPS points, for example, will be stored as a list of numbers, in **vector** format. A scan of a print map, on the other hand, will be stored as an image, in **raster** format.

### Attribute data types
Next to spatial data types, a GIS will also include attribute data types. These are tabular data that is linked to spatial data records, holding quantitative or qualitative information about vector data types such as **points**, **lines**, and **polygons**.

A GIS orders different spatial data types and files into different **layers** in a single data frame. Overlay of different spatial data sets enables us to select and analyse these data sets based on spatial and associated attribute conditions. If you have ever worked with Adobe Illustrator, Adobe Photoshop, or Adobe InDesign, you will be familiar with this way of ordering data within a single coordinate system. The main difference in functional terms is that a GIS uses a geographical coordinate reference system, making it useful for spatial data. But it is perfectly possible to draw a flower or a sunset in a GIS, should you want to.

![Layers](./_images/image_3_5_overlay.jpg "Illustration of overlay of different data types and sets in a GIS")

### Coordinate reference systems
A [coordinate reference system](https://en.wikipedia.org/wiki/Spatial_reference_system) or a CRS defines the spatial frame of a GIS. All types of spatial data are represented in GIS through **coordinates** (X, Y - and sometimes Z). Coordinates represent a specific location within a defined **coordinate reference system**. If you have coordinates for a given dataset, but do not know the coordinate reference system that they relate to, you will not be able to place the data correctly in space. A GIS can integrate and present data derived from many different **coordinate reference systems**.

Generally speaking, there are two different types of coordinate reference system in a GIS. One is a [geographic CRS](https://en.wikipedia.org/wiki/Geographic_coordinate_system), which models the Earth as a sphere and uses longitude and latitude coordinates (degrees-minutes-seconds, or DMS, or its numerical conversion, decimal degrees). Another is a [projected CRS](https://en.wikipedia.org/wiki/Projected_coordinate_system), which represents part of the Earth on a planar surface using a projection (conversion) of three-dimensional space to a two-dimensional surface.

### The interface of a GIS
Summing up the above elements, the user interface of a GIS will therefore typically contain the following principal elements:
* A toolbar, including some or all of the tools that can be deployed to create, manipulate, store, analyse, and visualise spatial and attribute data
* A layer index, listing all data files loaded to the current project
* A viewer, showing the spatial data frame of the GIS
* A project coordinate reference system

### Summary
To sum up this introduction, let us rehearse a couple of central points about GIS:

* Remember, GIS is both a computational tool and a form of data storage and data analysis framework
* GIS integrates structured data that has both spatial characteristics and attribute characteristics
* This means that GIS can be used to order, integrate, and analyse large amounts of data deriving from multiple spatial locations

#### Applications
* [Google Earth Pro](https://www.google.com/earth/about/versions/) - a virtual globe desktop application, using Google satellite imagery
* [QGIS](https://www.qgis.org/) - a free open source GIS

#### Resources
* [Gregory and Ell 2007]













* [Working with coordinates](#working-with-coordinates)
* Task 4 (link to subheader in ## Tasks below)
* [Using Google Earth Pro](#using-google-earth-pro)



## Tasks
(Step-by-step listing of tasks to be completed)

### Using Google Earth Pro
To introduce you to the world of spatial data, let us start with introducing you to an application that you probably know - even if you think you don't; [Google Earth Pro](https://www.google.com/earth).

Google Earth was launched in 

1. Open **Google Earth Pro**
2. Copy 59.8539, 17.6254 into the **Search** field and click **Search**
3. 

### Working with remote data
The native file format for Google Earth is **.kml** or its compressed version, the **.kmz**. KML stands for [Keyhole Markup Language](https://en.wikipedia.org/wiki/Keyhole_Markup_Language), which is an XML notation for storing geographical information. Any data to be viewed in Google Earth Pro must be **.kml** or **.kmz**-format. You can also add image files (for example .jpg or .tiff), but these are subject to different rules that will be discussed later (see [3.5 QGIS](./3_5_qgis.md)).

A couple of very useful spatial data files used in cuneiform studies are available as **.kmz**-files. And when data is available online in a public location, it is usually better to connect to it remotely rather than download a static copy of the dataset. Ideally, loading a dataset remotely from its original location should ensure that you always have the latest version.

To add a remote resource to Google Earth Pro, you will first need to know the exact download location of the **.kml** or **.kmz**-file that you are interested in. We know of two files that you should consider taking a look at:

* The [ANE Placemarks for Google Earth](https://zenodo.org/record/6384044), developed by Olof Pedersén and first released in 2007, contains basic information on c. 2,500 archaeological sites from all over the Middle East. This dataset has recently been made available on [Zenodo](https://zenodo.org), a research data hub run by CERN and the European Research Council. The download URL of the .kmz-file for this index is [https://zenodo.org/record/6384045/files/ANE.kmz?download=1](https://zenodo.org/record/6384045/files/ANE.kmz?download=1)

* The [Cuneiform Inscriptions Geographical Site Index (CIGS)](https://doi.org/10.5281/zenodo.4960710), which contains a comprehensive spatial index of more than 550 locations where cuneiform texts have been found, prepared by researchers of Uppsala University. The link to the **kml**-version of the most recent (v. 1.4, 1 November 2021) release of this resource is: [https://zenodo.org/record/5642899/files/CIGS_v1_4_20211101.kml?download=1](https://zenodo.org/record/5642899/files/CIGS_v1_4_20211101.kml?download=1)


###

### Task 4