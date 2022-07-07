---
layout: default
title: "6. QGIS"
rank: 18
---
# QGIS
(Module title should match title given in programme title)

## Introduction
In the last session (see [3.5 QGIS](./3_5_qgis.md)), we looked at how to add or georeference, and compare raster data, namely maps and satellite images. While raster data is the primary gateway for converting analogue spatial data, for example maps or aerial photography, into a digital format, raster data has a somewhat limited range of uses when working with historical data. When you have reliably georeferenced raster data, you can begin to build and edit vector data in the form of points, lines, and polygons by drawing on top of raster data. 

Whereas raster data cells can only hold information on **one variable** (for example colour or elevation), vector data can hold an almost infinite range of information on multiple variables (for example text strings, numerical data, area, dating, etc.). Attribute data can be easily integrated into and analysed with vector spatial data, which makes vector data much more central for analysis and map making purposes than raster data, at least in historical research. In this session, we will introduce you to the basics of creating vector data and generating maps.

* [Creating vector data](#creating-vector-data)
* [Editing vector data](#editing-vector-data)
* [Linking attribute data](#linking-attribute-data)
* [Making maps](#making-maps)

#### Applications
* [QGIS](https://www.qgis.org/) - a free open source GIS

#### Resources

## Tasks

### Creating vector data
Vector data share a lot of features with tabular spreadsheets in Excel or Access. All entities in a vector spatial data file will have one or several spatial coordinates (which is what you see visualised in the **Viewer** panel) and an associated row of attribute data fields (which is what you see in the **Attribute Data Table**). More fields in a vector file attribute data table can be added directly from a tabular file format, like **.xls** (Excel).

A vector data file needs to be created before it can be edited. That means that you have to set up the file format and decide on what the data in that format should look like and what information it should be able to contain, _before_ you can create the actual data points within this file. There are many different formats for vector data packages. For now, we will stick with the most widely used and most autonomous format, namely a **shapefile** (**.shp**). A shapefile is good because it packs all the necessary information into a single file and can be used across multiple platforms. It does, however, detach the data from large spatial data package formats (such as a **Geopackage**, or **.gpkg**) or newer and more versatile open text formats (such as **.geojson**), which may be more useful when working with larger datasets. We will make three shapefiles for each of the three vector types. The procedure is largely the same.

1. To create a shapefile, click **New Shapefile Layer** in the Toolbar
2. Under **File Name**, click the [...] box to the right and make sure that the file will be stored in
the right location
3. Check that **File encoding** is set to **UTF-8**
4. Choose the desired **Geometry type**, either **Point**, **Line**, or **Polygon**
5. Choose the desired CRS (in this case, it should be **WGS 84 / UTM 38N**)

A shapefile comes with a pre-defined table for **attribute data**. This means that you will have to define attribute data categories before you can start adding data to the file. A vector data file will always contain a generic **id** field, typically called **FID** (for **Feature ID**), which assigns a unique number to any vector feature that you create. Here, we will add two customised attribute data fields to a point vector data shapefile, called **Name** and **Type**.

An attribute data field will need a specific **field type**, which determines how QGIS will understand the data contained in the field. There are **four basic field types** available for vector data in QGIS: **Text data** (which is also called **string**), **Whole number** (which can also be called **short integer**), **Decimal number** (which can also be called **Long integer**), and **Date**. The length of a field determines the maximum number of characters that can be inserted into a field. Text data fields should generally be long (+10), while number fields can be relatively short (5-10). This all depends on what kind of data you want to put into the field, however.

6. Create a **Text** data type field with the name **Name**
7. Create a **Whole number** type field with the name **Type**
8. Click OK

### Editing vector data
You should now see the shapefile in the **Layers** panel. In order to add vector data to a shapefile or edit data already in the shapefile, you will first need to toggle the shapefile for editing. The default edit setting of any layer in a GIS will be locked, which prevents accidentally deleting or changing spatial data. When editing a shapefile, you most likely want to edit attribute data as well. You can visualise the attribute data table of a shapefile by opening the attribute table in a panel below the Viewer window.
1. Right-click the shapefile in the **Layers** panel and choose **Open Attribute Table**
2. Right-click the shapefile in the **Layers** panel and choose **Toogle Editing**
3. When editing is on, you will see that a number of buttons in the **Digitizing** toolbar are activated
4. Click the button **Add point feature**
5. Add a point feature in the centre of the Ur mound by moving the cursor there and clicking
once
6. In the **Feature Attributes** window, you will be asked to type in attribute data in the respective
attribute data fields
7. Type in 1 in the id field
8. Type in **Ur** in the Name field and **1** in the Type field and click OK
9. Note that a new row has been added in the shapefile attribute data table
10. Repeat this exercise for the mounds of Abu Shaharain, Tall al Lahm, and the Murājib Mound, only giving the **Type** for these locations as **2**

### Linking attribute data
As previously noted, the structure of vector data shares many features with **tabular data formats** commonly seen in applications like [Microsoft Excel](https://en.wikipedia.org/wiki/Microsoft_Excel) or [Microsoft Access](https://en.wikipedia.org/wiki/Microsoft_Access), [FileMaker](https://en.wikipedia.org/wiki/FileMaker) or [MySQL](https://en.wikipedia.org/wiki/MySQL). Because the data structure is very similar, this means that you can import and link data in, for example, an Excel-table, to the corresponding spatial data points, lines, or polygons in QGIS (or just about any other GIS). The only thing necessary to link spatial and attribute data is a that the two data collections have a shared and compatible **identifier**, like a name (a text string) or a number (short integer). By linking attribute data to spatial data in GIS, you can analyse and visualise attribute data according to spatial location.

For example, when preparing the point vector data file above, you provided the shapefile with two unique identifiers for this location; one in the field **Name**, and one in the field id, with the value 1. These can be used to link associated attribute data, provided that the data contained in the attribute data table field is compatible with the format of the corresponding field in the shapefile (i.e., you cannot import text strings to a numbers only field).

To obtain a decent workflow in GIS, it is generally easier to keep spatial data in a GIS application and associated attribute data in a tabular file format, like [Excel](https://en.wikipedia.org/wiki/Microsoft_Excel), [Access](https://en.wikipedia.org/wiki/Microsoft_Access), [FileMaker](https://en.wikipedia.org/wiki/FileMaker) or [MySQL](https://en.wikipedia.org/wiki/MySQL), and then import the necessary attribute data when needed. Hence, a lot of tasks involved in working with GIS are actually concerned with cleaning, preparing, and analysing data in attribute tables, without using a GIS application. 

For this exercise, we will attach some simple attribute data to the spatial data files to demonstrate how attribute data can in GIS analysis and visualisation

### Making maps
Maps can be made from anything that can be shown on the map canvas (it is also possible to add tables from attribute table files, for example an Excel sheet, to a map layout, but we will not look into that here). To make a map, you will first need a map layout.
1. Go to **Project > Layout Manager**
2. Choose **Empty layout** from the drop-down menu and click **Create...**
3. Give the map layout a name, for example **daa_map**
4. Go to the **daa_map** tab
5. You will see a blank map canvas, an empty **Items** list, and an **Item properties** panel
6. Mapping functions in GIS generally link directly to what is shown in the main **Viewer** window of your project. In the **daa_map** canvas, you will first need to mark out where the map should be located
7. Go to the toolbar on the left and choose the **Add a New Map** to the layout button
8. Mark out an area on the canvas – the area seen on the project **Viewer** should now appear


