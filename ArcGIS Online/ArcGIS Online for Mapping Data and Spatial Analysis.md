# **ArcGIS Online for Mapping Data and Spatial Analysis**

*Siti Lei*  
*Data and Visualization Librarian, Duke Kunshan University*  
*Last updated: November 21, 2025*

This tutorial introduces how to create, visualize, analyze, and share data-driven interactive maps using ArcGIS Online.

**[Before we start](#before-we-start)**

- [Introduction	](#introduction)

- [About the tool	](#about-the-tool)

- [Datasets	](#datasets)

- [What is “spatial analysis” and “geoprocessing”?	](#what-is-spatial-analysis-and-geoprocessing)

**[Part 1: Building Maps with Data](#part-1-building-maps-with-data)**

- [Sign in to ArcGIS Online	](#sign-in-to-arcgis-online)

- [Create a New Map Project	](#create-a-new-map-project)

- [Toolbars	](#toolbars)

- [Basemap	](#basemap)

- [Add Data](#add-data)

  - [Structured Table Dataset](#structured-table-dataset)

  - [Geospatial Data File](#geospatial-data-file)

- [Acquire Data from ArcGIS Online	](#acquire-data-from-arcgis-online)

- [Visualize Data	](#visualize-data)

  - [Styles	](#styles)

  - [Labels	](#labels)

  - [Pop-ups	](#pop-ups)

[Save a Map	](#save-a-map)

[Share a Map	](#share-a-map)

[Export Data	](#export-data)

**[Part 2: Analyzing Data with Maps](#part-2-analyzing-data-with-maps)**

- [Tools	](#tools)

- [Join Data	](#join-data)

- [Find by Attributes and Locations	](#find-by-attributes-and-locations)

- [Find Closest	](#find-closest)

- [Extract Data	](#extract-data)

- [Model Builder	](#model-builder)

**[Resources	](#resources)**

# 

# Before we start

## Introduction

In this tutorial, we will use China’s airport location dataset and provincial boundary dataset to explore the distribution of airports across provinces in China. DKU members may download the original dataset from CnOpenData through [DKU Only E-Resources](https://library.dukekunshan.edu.cn/academic-databases/) by following the instructions.

Tasks covered in this tutorial include:

1. Changing the basemap  
2. Loading and displaying China’s provincial boundaries on a map  
3. Loading and displaying airport locations on a map  
4. Saving the project and exporting data as a shapefile

By the end of this tutorial, you will be able to use ArcGIS Online to create a provincial-level map of China showing the geographic distribution of airports.


## About the tool

ArcGIS Online will be used in the tutorial. Visit the [GIS guide](https://library.dukekunshan.edu.cn/geographic-information-system-gis/) for more information about the tool.

## Datasets

The sample datasets are derived from [CnOpenData](https://www.cnopendata.com/) and have been cleaned for the purpose of demonstration. Download the sample datasets below:

* [China Airport.csv](https://duke.box.com/shared/static/ycwqlrka3797epk9m0p3svmsocj8fj3c.csv)  
* [China Province Boundary.zip](https://duke.box.com/s/7e2ksv0f7gw156wit9zjxw0stwxo59ws)

## What is “spatial analysis” and “geoprocessing”?

The second part of this tutorial introduces how to use geoprocessing tools to perform spatial analysis. To help ground these concepts, here is a brief overview:

**Spatial analysis** is the process of examining geographic data based on location, relationships, and patterns. It helps answer questions such as where features are located, how they are distributed, and how they interact with other geographic elements. 

**Geoprocessing** refers to the set of operations used to manipulate, analyze, and manage geographic data. These operations include overlaying layers, buffering, clipping, dissolving, intersecting, and converting data formats. In GIS, geoprocessing tools help model spatial relationships, create new datasets from existing ones, and automate complex workflows.

# Part 1: Building Maps with Data

In Part 1, we will introduce the basics of ArcGIS Online, including how to import and load datasets, visualize your data on a map, and save or export your work.

## Sign in to ArcGIS Online

Follow the instructions in [Signing in to ArcGIS Online](https://library.dukekunshan.edu.cn/signing-in-to-arcgis/) to sign in to [ArcGIS Online](https://www.arcgis.com/index.html). 

## Create a New Map Project

### Toolbars

---

1. Once you successfully sign in to ArcGIS Online, you will see the view shown below. To start creating a map, go to the **Map** tab in the main menu — this opens a new map view where you can begin a new map project.

<img width="1019" height="414" alt="image115" src="https://github.com/user-attachments/assets/2e889907-58c4-4079-91d0-db442a9bd495" />


---

2. The interface provides a variety of tools, organized in these toolbars:  
   1) Contents toolbar  
   2) Editing toolbar  
   3) Viewing and Search toolbar
 

<img width="1236" height="786" alt="image91" src="https://github.com/user-attachments/assets/36fb5336-9e70-46d2-b4f4-495d2e14154f" />



### Basemap

---

1. The main map at the center serves as the basemap. By default, ArcGIS Online applies the “Topographic” map as the basemap.   

---

     
2. To select an alternative, navigate to the contents toolbar, select **Basemap**, and a list of available options will be displayed.

<img width="441" height="595" alt="image15" src="https://github.com/user-attachments/assets/a3eadb16-0a11-4258-9950-3d3d14aecfef" />


---

3. Scroll down and select **Light Gray Canvas**.

<img width="375" height="327" alt="image34" src="https://github.com/user-attachments/assets/40f762cf-f38f-41ee-8c57-fccb0760e3a8" />


---

4. The reference system for China is not accurate. To correct this, we will create a new labeling system. First, close the current one by clicking the arrow to expand the details of the selected basemap.

<img width="387" height="118" alt="image93" src="https://github.com/user-attachments/assets/094c90c6-c3e4-45d3-8c4f-a7e18664f592" />


---

5. Then, click on the eye icon next to **Light Gray Reference** to hide it.

<img width="384" height="347" alt="image92" src="https://github.com/user-attachments/assets/a135738f-8f46-49ca-ac91-ea9c1bed153a" />



## Add Data

There are multiple ways to add data to a map project in ArcGIS Online \- you can add datasets with location data, upload images, connect to external sources via URL, or create your own sketches directly in the map.

ArcGIS Online supports importing data from structured table formats such as comma-separated values files (.csv), Excel files (.xslx) with location fields (e.g., coordinates, addresses), and geospatial file formats including shapefile (.shp), GeoJSON, KML (.kml), and GeoPackage (.gpkg), and Geodatabase (.gdb).


### Structured Table Dataset

[China Airport.csv](https://duke.box.com/shared/static/ycwqlrka3797epk9m0p3svmsocj8fj3c.csv) is a data table containing information about every airport in China, including their names, addresses, coordinates, and year of construction. Let’s map this data on the map\! Before we begin, make sure you have downloaded the file to your computer.

---

1. Go to the contents toolbar, select **Add**, then **Add layer from file**.

<img width="236" height="249" alt="image72" src="https://github.com/user-attachments/assets/9ad6151d-955f-4971-9538-eba556ea71c4" />


---

2. Click **Your device** button, then select **China Airport Dataset.csv** file (downloaded from the setup files) from its saved location and click **Open**. Alternatively, drag and drop the file into the pop-up window.

<img width="1349" height="679" alt="image11" src="https://github.com/user-attachments/assets/3c58feaf-daaa-4c91-868d-9e077eb43c56" />


---

3. Select **Create a hosted feature layer and add it to the map**, click **Next**.

<img width="1089" height="637" alt="image37" src="https://github.com/user-attachments/assets/ef335169-f8b3-40ec-9ed2-bfa7d3c29e5a" />


---

4. Confirm data type for each variable, and click **Next**.

<img width="970" height="559" alt="image" src="https://github.com/user-attachments/assets/eae04bb4-85e5-48e8-8fcb-2b4d3ca91fd2" />


---

5. Click the arrow icon to expand the options, select **Latitude and longtitude**, click **Next**.

<img width="968" height="561" alt="image" src="https://github.com/user-attachments/assets/2a25427c-2e0b-43d6-94af-8c1ffd51691d" />


---

6. Open the dropdown, then select **LAT** for the “Latitude” field and **LNG** for the “Longitude” field, click **Next**.

<img width="968" height="564" alt="image" src="https://github.com/user-attachments/assets/c1796a19-e0bc-4251-871a-5ccd89607f5e" />


---

7. Name the new layer as **China Airport Dataset**, then click **Create and add to map**.

<img width="968" height="561" alt="image" src="https://github.com/user-attachments/assets/8986e596-025f-42fe-b786-034251b70d37" />


---

8. A map layer with all airport data points in China has been added to your map\!

<img width="950" height="636" alt="image" src="https://github.com/user-attachments/assets/ffeac3d1-2354-4119-8f59-7deffda683cb" />


---

9. Go to **Layers** in the contents toolbar to check the items that have been added to the project.

<img width="645" height="283" alt="image" src="https://github.com/user-attachments/assets/00407b26-6ea4-4d3e-bf2e-12e7989f350c" />



### Geospatial Data File

A shapefile is one of the most common geospatial data formats used in GIS, which stores geographic features (such as points, lines, or polygons) along with their associated attributes. Despite its name, a shapefile is actually a collection of several related files (e.g., .shp, .shx, .dbf) that must stay together for the data to function properly. ArcGIS Online can only read a shapefile directly from a zipped folder, which is why you should upload the .zip file without unzipping it.

[China Province Boundary.zip](https://duke.box.com/s/7e2ksv0f7gw156wit9zjxw0stwxo59ws) is a compressed folder containing a shapefile and its supporting files. It provides provincial-level boundary data for China, with each province represented as a polygon. Let’s add this data to the map\! Before we begin, make sure you have downloaded the file to your computer, and **do not** unzip it.

---

1. After download, go to the contents toolbar, select **Add** \> **Add layer from file**.

<img width="391" height="411" alt="image" src="https://github.com/user-attachments/assets/04f54bc4-d2ca-4859-adaf-6d9b3715be36" />


---

2. Select **Your device** option, then locate and click on the **China Province Boundaries.zip** file (downloaded from the setup files) from its saved location and click **Open**. Alternatively, drag and drop the file into the pop-up window. Click **Next** to continue.

<img width="697" height="363" alt="image" src="https://github.com/user-attachments/assets/00916077-9fe7-464e-ae3d-48cad66acec4" />


---

3. Make sure “Shapefile” is selected, then click **Next**.

<img width="707" height="366" alt="image" src="https://github.com/user-attachments/assets/e9d612f7-048a-484d-8a0b-2f5d6ac0160c" />


---

4. Name the new layer as **China Province Boundaries**, then click **Create and add to map**.

<img width="706" height="367" alt="image" src="https://github.com/user-attachments/assets/f24586b3-6869-424b-9f0c-fe33ec91365b" />


---

5. It may take a moment to process. Once completed, a new layer named **China Province Boundaries** will appear in the **Layers** panel. Locate the **China Province Boundaries** layer, click the ellipsis (3-dot) icon next to it, and select **Zoom to layer**.

<img width="460" height="202" alt="image" src="https://github.com/user-attachments/assets/7eb921d3-5f96-44e6-b6b5-11246df15ab0" />


---

6. This will automatically zoom to the area where your data is displayed on the map.

<img width="604" height="395" alt="image" src="https://github.com/user-attachments/assets/23cdf9d3-8a81-4413-a1b8-51bbf8197ae1" />


---

7. Go back to the **Layers** panel, and click the eye icon to hide the **China Province Boundaries** layer for now.

<img width="578" height="158" alt="image" src="https://github.com/user-attachments/assets/7ae2e6bb-0ceb-4006-b68b-07984f643b0f" />




### Acquire Data from ArcGIS Online

Not just a tool, ArcGIS Online is also a rich source of map data, with contributions shared by researchers worldwide. For example, to understand where airports are located within provinces, we need to add a China province layer to the map, which can be directly imported from the ArcGIS Online database.

1. Go to the contents toolbar, then **Add**, **Browse layers.**

<img width="381" height="235" alt="image" src="https://github.com/user-attachments/assets/8eb8bd9b-827d-4e53-903f-7df71213bde7" />


---

2. Switch the source from **My content** to **ArcGIS Online**.

<img width="420" height="393" alt="image" src="https://github.com/user-attachments/assets/aa08206b-471e-4c21-873e-02189b9a4def" />


---

3. Type in the keyword “China province” and press **Enter** on your keyboard.

---

4. Locate the item **China Province Boundaries** by Esri in the search results, click **\+ Add**.

<img width="383" height="448" alt="image" src="https://github.com/user-attachments/assets/d2c866bd-08e1-4625-820a-a97eb60466a6" />


---

5. Use the **Zoom In/Out** tool under the viewing and search toolbar to examine the data in detail.

<img width="632" height="402" alt="image" src="https://github.com/user-attachments/assets/cdc0de55-ad33-4f75-9660-adac0e40129a" />


---

6. Click **Remove** to delete the layer from your map.

<img width="454" height="212" alt="image" src="https://github.com/user-attachments/assets/f0d2393d-5248-46ee-acf7-5e7a10433589" />



## Visualize Data

### Styles

1. To customize the appearance of data points, lines, or polygons on the map, first make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

<img width="590" height="259" alt="image" src="https://github.com/user-attachments/assets/9b847049-3387-49d0-a01a-0866d52572b6" />


---

2. Then, select **Styles** under the editing toolbar and use the settings to adjust the appearance of the data points according to your preference. For best practices in selecting colors or patterns for geospatial data and maps, refer to the [Select Visualization Elements](https://library.dukekunshan.edu.cn/data-visualization/#:~:text=4.%20Select%20Visualization%20Elements) section in the [Data Visualization guide](https://library.dukekunshan.edu.cn/data-visualization/). Click **Done** when the edits are complete. 

<img width="588" height="514" alt="image" src="https://github.com/user-attachments/assets/55796198-9f7c-4ffb-94e1-63320a6fb988" />



### Labels

1. You can configure labels for a map layer. To do so, first, make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

<img width="618" height="232" alt="image" src="https://github.com/user-attachments/assets/3bb66930-0894-4766-89ac-4166487bbdc1" />


---

2. Next, select **Labels** under the editing toolbar to start editing. Make sure you toggle on **Enable labels** and select **Name** field as the **Label field** to show the name of each province (since we turned them off in the basemap). You can also adjust the settings to customize their look.

<img width="774" height="483" alt="image" src="https://github.com/user-attachments/assets/97e32f36-04af-4f8e-bbd8-cacd60fe6864" />


---

### Pop-ups

1. Click on a random data point on the map — this will trigger a pop-up displaying all associated information for that specific point.

<img width="758" height="568" alt="image" src="https://github.com/user-attachments/assets/3d1a6be5-f16d-4185-9591-4bd0e6b60fa2" />


---

2. To configure the pop-ups or edit the displayed information in the pop-up, first make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

<img width="481" height="212" alt="image" src="https://github.com/user-attachments/assets/5206f3a3-2a2b-4494-ad89-a6d43d7032ad" />


---

3. Next, go to **Pop-ups** under the editing toolbar to customize the content displayed.

<img width="470" height="386" alt="image" src="https://github.com/user-attachments/assets/472f89c0-475b-425b-87fb-934cd9797b6b" />




## Save a Map

ArcGIS Online does **not** save your map project automatically, so be sure to manually save it each time before quitting the page.

1. To save a new-created map project, go to the contents toolbar, click **Save and open**, then **Save as**.

<img width="377" height="272" alt="image" src="https://github.com/user-attachments/assets/b0ac4aee-1f6b-427f-bc93-638c88a9e096" />


---

2. Name the project as **China Airport Map Project**, add other details if needed, and click **Save**.

<img width="539" height="601" alt="image" src="https://github.com/user-attachments/assets/d5680744-f35b-4442-96a6-65d04aea5fcc" />


---

3. Click the hamburger (3-line) icon in the top left corner, then select **Content** \- this is where your saved work will be stored. You can also find it under the main menu.

<img width="346" height="543" alt="image" src="https://github.com/user-attachments/assets/21f5e3fc-f1b4-41b9-88e6-387c7eae3343" />


---

4. Every time before quitting the project, go to the contents toolbar, click **Save and open**, then click **Save** to apply your changes.

<img width="351" height="383" alt="image" src="https://github.com/user-attachments/assets/dae71ce6-cf11-44c3-a93e-6958a7c6e935" />



## Share a Map

One advantage of using ArcGIS Online is that it allows easy sharing of map projects. With an institutional license, DKU members can share their projects with Duke and DKU users, make them public, or keep them private for self-view only.

You can also set up a group to make your project or items visible or editable to group members. Follow the instructions [here](https://doc.arcgis.com/en/arcgis-online/share-maps/create-groups.htm) to create a group. If you have any questions, please contact the Data and Visualization Librarian ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)). 

1. Go to **Content**, then **My content**. Locate the item you want to share, and click on its title.

<img width="1007" height="410" alt="image" src="https://github.com/user-attachments/assets/858bc49d-92ee-4268-967a-d483ffca35e2" />


---

2. Alternatively, click on the ellipsis (3-dot) icon next to the item and select **View details**.

<img width="402" height="460" alt="image" src="https://github.com/user-attachments/assets/2ef4f0a5-f32d-4628-afe7-0f31140b7fbf" />


---

3. From the right-hand pane, click **Share** to open the sharing options.

<img width="550" height="648" alt="image" src="https://github.com/user-attachments/assets/f7baeea1-00d3-415e-b828-0346c79af654" />


---

4. Choose **Everyone (public)** under sharing options, and click **Save**.

<img width="630" height="772" alt="image" src="https://github.com/user-attachments/assets/ca793e90-be83-47b1-95a5-5554a56a2f37" />


---

5. Click **Review sharing** to check the items whose sharing permissions will be updated accordingly.

<img width="915" height="321" alt="image" src="https://github.com/user-attachments/assets/a6e5e618-97ba-474c-a264-988885568a0b" />


---

6. Click **Update sharing** to confirm the changes.

<img width="979" height="444" alt="image" src="https://github.com/user-attachments/assets/68f38439-2bb0-4a75-aa7f-b2f92b1166ec" />


---

7. Now, your map should be visible for the public.



## Export Data

For each layer created or added to a map project, you can export it as a shapefile to open in other GIS software or store on your local computer. In this tutorial, we will use the airport layer as an example.

1. Go to **Content**, then **My content**. Make sure the item you select is of the “Feature layer (hosted)” type \- otherwise, it will not support shapefile export.

<img width="987" height="380" alt="image" src="https://github.com/user-attachments/assets/b269d42b-ee47-4f83-889c-677c1ac4cf0e" />


---

2. Click on the ellipsis (3-dot) icon next to the item title, select **View details**. You can also do it by clicking on the item title.

<img width="274" height="219" alt="image" src="https://github.com/user-attachments/assets/49c5e2b7-946e-4432-80a7-d6a4df30db55" />


---

3. Under the **Overview** tab, click **Export data** from the right pane.

<img width="378" height="474" alt="image" src="https://github.com/user-attachments/assets/759b838b-f4b5-4901-9d15-15e4a4dcea1b" />


---

4. Then, select **Export to shapefile** from the dropdown menu.

<img width="390" height="414" alt="image" src="https://github.com/user-attachments/assets/10e97299-3a4e-44d4-adbb-a32cc22ff01e" />


---

5. Name the new file as **China Airport Dataset**, add other details if needed, and click **Export**.

<img width="639" height="706" alt="image" src="https://github.com/user-attachments/assets/dbde12b7-baf8-4cc8-83ae-861999ed29a7" />


---

6. Once the export is complete, a new page will appear showing the file type as “Shapefile”. You can also find it under the **Content** tab.

<img width="898" height="392" alt="image" src="https://github.com/user-attachments/assets/e6d412a4-1c1a-4b3d-9e01-166d6369e7e8" />


---

7. Click **Download** on the right pane to save the file in your local computer.

<img width="421" height="431" alt="image" src="https://github.com/user-attachments/assets/6b66da3c-c79e-4fa4-8582-ba308cc60a5c" />



# Part 2: Analyzing Data with Maps

In Part 2, we will use some geoprocessing tools in ArcGIS Online to gain insights from China’s airport and province boundary datasets. By the end, you will be able to use maps to answer these questions:

1. How are airports distributed across the provinces of the country? Which provinces have higher or lower densities of airports?  
2. How many airports are there in Jiangsu province? What are these airports, and where are they located?  
3. Which 3 airports in Jiangsu province are closest to DKU campus?  
4. How to export the layer into a format that is shareable and downloadable (e.g., Shapefile, CSV)?  
5. Which provinces have more than 10 airports?

## Tools

### Join Data

The first question “How are airports distributed across the provinces of the country? Which provinces have higher or lower densities of airports?” focuses on the distribution and density of airport locations across the country. 

Since the two datasets we need to answer this question are currently separate, we need to merge them into a single layer. Many of the geoprocessing tools can achieve this (like **Aggregate Points**), but the tool that will be introduced in this tutorial is **Join Features**. 

---

1. Go to the Editing toolbar, click on **Analysis**.

<img width="457" height="625" alt="image" src="https://github.com/user-attachments/assets/01159cb3-6379-4076-bf03-da1ed4218cec" />


---

2. Select **Tools**. Alternatively, click the tool icon in the header menu.

<img width="422" height="586" alt="image" src="https://github.com/user-attachments/assets/b2e3f758-5824-4af1-84a1-b48cc235b0b4" />


---

3. Under **Summarize data**, select **Join Features**.

<img width="971" height="374" alt="image" src="https://github.com/user-attachments/assets/98f648d5-290e-4d66-b27f-872fdc6e84b6" />


---

4. Now, let’s configure our input and output. First, for the **Target layer**, select **China Province Boundaries** layer from the dropdown.

<img width="965" height="741" alt="image" src="https://github.com/user-attachments/assets/9574d300-8100-412e-994e-5e45d12d643e" />


---

5. For the **Join layer**, select **China Airport Dataset** layer from the dropdown.

<img width="900" height="694" alt="image" src="https://github.com/user-attachments/assets/6cd0b809-d6ab-4ce2-8405-e1f2119ba8b9" />


---

6. Under the **Join settings**, toggle on **Use spatial relationship**.

<img width="606" height="298" alt="image" src="https://github.com/user-attachments/assets/7c1097f3-8200-4590-bbcc-df3c0ac59ca1" />


---

7. For the **Spatial relationship**, select **Completely contains** from the dropdown menu.

<img width="662" height="285" alt="image" src="https://github.com/user-attachments/assets/c186f494-899f-4c4a-9a27-5806326ce205" />


---

8. For the **Join operation**, select **Join one to one** from the dropdown menu.

<img width="669" height="233" alt="image" src="https://github.com/user-attachments/assets/be7065a0-be6c-411a-98bf-b4146bc61aea" />


---

9. Since we are analyzing the density of airports across provinces, we first need to calculate the number of airports in each province. Under the **Multiple matching records**, select **Calculate count only**.

<img width="681" height="251" alt="image" src="https://github.com/user-attachments/assets/1b757b76-c113-47d1-b5ad-c9a0b2054029" />


---

10. For the **Join type**, make sure **Inner join** is highlighted.

<img width="714" height="164" alt="image" src="https://github.com/user-attachments/assets/b5163a6b-9344-4248-a42f-408a16fa5cb0" />


---

11. Under the **Result layer**, give a name to the new layer in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: **Count of Airports in Provinces\_\[Your NetID\]**.

<img width="604" height="433" alt="image" src="https://github.com/user-attachments/assets/586c18ba-3258-4bfd-b63a-ab8e78f31302" />


---

12. Click **Run** to start processing.

<img width="607" height="215" alt="image" src="https://github.com/user-attachments/assets/cc3357da-da49-4a5a-a212-fcbd2c8960e0" />


---

13. To check the progress, click on the history icon in the header menu.

<img width="657" height="207" alt="image" src="https://github.com/user-attachments/assets/83ab0690-b346-4c3c-83b9-eba3cf1891eb" />


---

14. Once the analysis is completed successfully, a new layer named **Count of airports in provinces** will appear in the **Layers** and the map. Let’s focus on this layer by hiding the other two layers and keep only the newly created one visible.

<img width="656" height="440" alt="image" src="https://github.com/user-attachments/assets/3fc31d6a-131b-4218-8a54-a1c91acf6d9e" />


---

15. The new layer called **Count of airports in provinces** will show up in the **Layers** pane. When you click on a province polygon, the pop-up will display a new attribute called **Join\_Count**, followed by the total number of airports in the corresponding province.

<img width="907" height="620" alt="image" src="https://github.com/user-attachments/assets/07cd4e6d-b500-4a1f-ab1f-d0fbfe19e4f1" />


---

16. Click the ellipsis (3-dot) icon next to **Count of airports in provinces** layer and select **Show table**.

<img width="271" height="299" alt="image" src="https://github.com/user-attachments/assets/97b93e83-f182-4cfd-ba38-007f739de7dd" />


---

17. The data table attached to this layer will appear with two new attributes named **Join\_Count** and **Admin Name**. **Join\_Count** indicates the number of airports in each corresponding province, **Admin Name** represents the administrative region used in the spatial analysis.

<img width="981" height="510" alt="image" src="https://github.com/user-attachments/assets/ac35e1fc-9cbe-4733-b99d-9122d4f0d529" />



### Find by Attributes and Locations

Let’s move to the second question: What and where are the airports in Jiangsu Province?

To answer this, we can use the **Find by Attributes and Location** tool. This tool allows us to set specific query conditions (such as filtering by province name) to automatically extract only the airports that meet our criteria. Once applied, it will generate a subset of the data showing all airports located within Jiangsu.

---

1. Go to the Editing toolbar, click on **Analysis**.

<img width="452" height="620" alt="image" src="https://github.com/user-attachments/assets/50f76682-9429-433b-a1ca-253b1daf2ea9" />


---

2. Select **Tools**. Alternatively, click the tool icon in the header menu.

<img width="432" height="606" alt="image" src="https://github.com/user-attachments/assets/60a1b648-0019-4872-bbb1-64f5f4e5a660" />


---

3. Under the **Find locations**, select **Find by Attributes and Location**.

<img width="920" height="421" alt="image" src="https://github.com/user-attachments/assets/618af60a-b943-4b58-a7a4-716666b8b49d" />


---

4. Click on **\+ Build new query** under **Criteria**.

<img width="492" height="346" alt="image" src="https://github.com/user-attachments/assets/6e4528e2-320a-455b-a22e-31ea353a121f" />


---

5. For **Find features from**, select **China Airport Dataset** layer from the dropdown, then select **Attribute expression**, click **Next**.

<img width="796" height="360" alt="image" src="https://github.com/user-attachments/assets/9d71adaf-4809-443b-8cbf-47b8f3609235" />


---

6. For **Where** fields, we will define the criteria. First, choose **All of the following are true**. Then, set **Province\_EN** as the field, select **equal** as the operator, and select or enter **Jiangsu** as the value. Once the condition is set, click **Add** to apply it.

<img width="930" height="418" alt="image" src="https://github.com/user-attachments/assets/d91470dd-cfa1-4016-b929-7d836b33acfd" />


---

7. Under the **Result layer**, give the new item a name in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: Airports in Jiangsu\_\[Your NetID\].

<img width="491" height="370" alt="image" src="https://github.com/user-attachments/assets/70f4d85a-82f7-49bf-aabc-daf0a0360270" />


---

8. Click **Run** to start processing.

<img width="657" height="204" alt="image" src="https://github.com/user-attachments/assets/43aad186-7d73-4795-a548-ae47318a850a" />


---

9. To check the progress, click on the history icon in the header menu.

<img width="626" height="181" alt="image" src="https://github.com/user-attachments/assets/4013f5a9-1167-40cc-923a-704f144dbd91" />


---

10. Once the analysis is completed successfully, a new layer named **Airports in Jiangsu** will appear in the **Layers** and the map. Let’s focus on this layer by hiding the other layers and keep only the newly created one visible.

<img width="400" height="378" alt="image" src="https://github.com/user-attachments/assets/b4c94a82-9c48-4840-be7a-c6d575af78f5" />


---

11. The map will update to show the new layer we just created, automatically zooming into Jiangsu province.

<img width="868" height="497" alt="image" src="https://github.com/user-attachments/assets/307d765c-b1fd-4bd6-93fe-753504a80972" />


---

12. Click the ellipsis (3-dot) icon next to **Airports in Jiangsu** layer and select **Show table**. 

<img width="249" height="277" alt="image" src="https://github.com/user-attachments/assets/103b73b3-fce1-4656-b0d6-efb44737f14a" />


---

13. There should be 11 records in the table, meaning that there are 11 airports in Jiangsu province.

<img width="985" height="432" alt="image" src="https://github.com/user-attachments/assets/7fa138ae-86f3-4df7-9ebc-6f08ab9a8431" />



### Find Closest

The third question we want to solve is: what are the 3 closest airports to DKU. To do that, we will first create a new layer with DKU campus’s location data.

---

1. Click on the **Search** tool in the Searching and Viewing toolbar.

<img width="245" height="247" alt="image" src="https://github.com/user-attachments/assets/7f363956-0be2-4608-8a28-1f53f7557745" />


---

2. Click **Use current location**, Or, enter **Kunshan, Jiangsu**, and select the first option from the dropdown. This will locate you to the Kunshan region on the map. Then, navigate to the Duke Kunshan University.

<img width="881" height="679" alt="image" src="https://github.com/user-attachments/assets/e1d5cb9b-7f3f-45c3-8e9a-975516e11ca3" />


---

3. Go to **Add**, then select **Create sketch layer**.

<img width="429" height="446" alt="image" src="https://github.com/user-attachments/assets/0e0a67a2-6acb-4bbd-a58e-bbab5de22354" />


---

4. Under the **Point feature** in the **Sketch** pane, name the new data point as **DKU**.

<img width="441" height="501" alt="image" src="https://github.com/user-attachments/assets/4668a594-5657-4f67-9058-b437173b15eb" />


---

5. Make sure the stamp icon is selected in the sketch toolbar, and click on two random places in the campus area on the map.

<img width="928" height="667" alt="image" src="https://github.com/user-attachments/assets/e88083a6-307d-4638-b98a-10f0ff150542" />


---

6. We only need one data point actually, so let’s delete one of them. To do so, click **Select** (cursor icon) from the sketch toolbar. Then click on the point you want to delete, and click on **Delete** or hit **Backspace** on the keyboard.

<img width="777" height="311" alt="image" src="https://github.com/user-attachments/assets/d7145cca-ab4c-48e6-8688-b7b5130bb4a8" />


---

7. Go to **Layers**, rename the sketch layer as **DKU campus**, and click **OK**.

<img width="286" height="452" alt="image" src="https://github.com/user-attachments/assets/f0c2c55e-a9dd-4771-bb29-dcd9ccb0660e" />


---

8. Next, go to **Analysis**, select **Find Closest** under the **Use proximity**.

<img width="911" height="283" alt="image" src="https://github.com/user-attachments/assets/4acc6da7-27dc-483c-bc87-28f3114e9778" />


---

9. Select **DKU campus (Points)** as input layer, and **Airports in Jiangsu layer** as near layer.

<img width="516" height="611" alt="image" src="https://github.com/user-attachments/assets/3467b380-a7a4-4b9e-b92a-ae53d3f890b6" />


---

10. For the **Analysis settings**, toggle on **Limit the number of closest locations**, and enter **3** as the max number of input. Make sure **Limited the search range** is toggled off.

<img width="523" height="530" alt="image" src="https://github.com/user-attachments/assets/c8f4e936-1597-42f3-8583-d708c5db304a" />


---

11. Under the **Result layer**, give a name to the new layer in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: Closest airports to DKU\_\[Your NetID\].

<img width="396" height="294" alt="image" src="https://github.com/user-attachments/assets/6cc45631-916b-4f59-9df1-68a2b8eecf77" />


---

12. Click **Run** to start processing.

<img width="480" height="123" alt="image" src="https://github.com/user-attachments/assets/dc9be530-e4e2-4ebc-975c-229d00b67fac" />


---

13. To check the progress, click on the history icon in the header menu.

<img width="471" height="136" alt="image" src="https://github.com/user-attachments/assets/0e73fec8-bb11-4a4f-be2a-0de708061466" />


---

14. Once the analysis is completed successfully, a new layer set named **Closest airports to DKU** will appear in the **Layers** and the map. Let’s keep the rest of the layers invisible.

<img width="333" height="405" alt="image" src="https://github.com/user-attachments/assets/ed765143-de72-4051-a910-6a5cc4110c02" />


---

15. Click on the arrow icon next to **Closest airports to DKU** layer set, click on the ellipsis (3-dot) icon next to **Connecting Lines** and select **Show table**. 

<img width="510" height="492" alt="image" src="https://github.com/user-attachments/assets/e6505c6b-85b6-41f0-bcd1-f2ab026be312" />


---

16. The data table should display 3 records, along with two new attributes \- **Near Rank** and **FindExistingLocation** \- which indicate the airport names and their rankings by distance.

<img width="957" height="525" alt="image" src="https://github.com/user-attachments/assets/1acc4a57-0bc0-48ba-8d4c-3349bbf69322" />



### Extract Data

Lastly, the analysis tools allow exporting layers in CSV, file geodatabase, shapefile, and KML. Let’s say we want to export the data table attached to our closest airports to the DKU layer in a table csv format. We already know how to view the data table in the map view, but how to download that in a csv format?

---

1. Go to the Editing toolbar, click on **Analysis**.

<img width="370" height="297" alt="image" src="https://github.com/user-attachments/assets/594f85e1-f73c-4488-a22e-e30e66169f42" />


---

2. Select **Tools**. Alternatively, click the tool icon in the header menu.

<img width="349" height="359" alt="image" src="https://github.com/user-attachments/assets/edb2a2e7-8276-4512-8aae-833c3116c15b" />


---

3. Under **Manage Data**, select **Extra Data**.

<img width="789" height="306" alt="image" src="https://github.com/user-attachments/assets/ef1df760-5088-4e6a-9a0a-bef56dd1d3d0" />


---

4. For **Input layers**, select **Closest airport to DKU \- Nearest Features** and **Closest airport to DKU \- Connecting Lines**. 

<img width="729" height="447" alt="image" src="https://github.com/user-attachments/assets/e89707b5-a6fd-4f21-9d56-223e5305cc39" />


---

5. Under **Result layer,** select CSV as the output data format, name the new output as **Top 3 closest airports**, and select the designated folder to save the output.

<img width="404" height="420" alt="image" src="https://github.com/user-attachments/assets/891aebf7-76e4-45f2-9992-bee4c1e67f1e" />


---

6. Click **Run** to start processing.

<img width="556" height="174" alt="image" src="https://github.com/user-attachments/assets/45183db8-242b-4120-b52d-d22d5b424613" />


---

7. Click on the history icon in the header menu to check the progress. Then, click on the ellipsis (3-dot) icon next to the processing record, and click **View details**.

<img width="497" height="329" alt="image" src="https://github.com/user-attachments/assets/e9d53d1e-bf7b-415c-ad5f-b57c5a514dd3" />


---

8. Click on the ellipsis (3-dot) icon next to **Top 3 closest airports**, then **Open item details**.

<img width="918" height="389" alt="image" src="https://github.com/user-attachments/assets/1d1e8bd4-b61b-4f97-8064-49ed2f21f2b7" />


---

9. A new item page will open. Click on the **Download** button in the right pane to download and save the file in your local computer.

<img width="979" height="325" alt="image" src="https://github.com/user-attachments/assets/3878a0a5-ad83-4b92-9482-a4cb9454a681" />


---

10. Open the **Nearest\_Features** file in Excel to view the ranked list of airports closest to the DKU campus. Note that Chinese text may not always export correctly.

<img width="548" height="182" alt="image" src="https://github.com/user-attachments/assets/d8cb9cd6-fbc2-4ebe-a1ce-82141c9e02cc" />




## Model Builder

While we just demonstrated how to answer multiple questions by running different analysis tools step by step, there is a way to streamline the entire process without executing each tool manually \- that’s **Model Builder**.

With **Model Builder**, instead of running each tool manually, you can build a workflow where outputs from one step feed directly into the next. This is especially useful when working with large datasets, performing multi-step analyses, or repeating the same workflow with different inputs.

In this demo, we will answer this question: which provinces in China have more than 10 airports?

---

1. Return to the map project view. If you can’t find it, go to the ArcGIS Online homepage and navigate to **Content** \> **My content**. Open the **Airport within province** web map item.

---

2. Click on **Analysis**.

<img width="398" height="500" alt="image" src="https://github.com/user-attachments/assets/49c063cb-7245-49ad-ac87-451a85dbb87c" />


---

3. Select **ModelBuilder**. Alternatively, click the Model Builder icon in the header menu.

<img width="399" height="360" alt="image" src="https://github.com/user-attachments/assets/4902ad3a-3d04-475e-9f2b-21681fd03e3a" />


---

4. Click **Connect** to continue.

<img width="409" height="417" alt="image" src="https://github.com/user-attachments/assets/454c72c5-bafe-4b8f-8a1d-b27973c9dd1c" />


---

5. Make sure the **Disconnect** button is showing up, then click **Create model**.

<img width="440" height="362" alt="image" src="https://github.com/user-attachments/assets/343e85de-122f-48ab-b331-4d1002a6aa69" />


---

6. For the model, let’s call it **Provinces with over 10 airports**, then click **Save**.

<img width="770" height="714" alt="image" src="https://github.com/user-attachments/assets/27df2c1c-e2e5-4c83-969c-5eb10200e297" />


---

7. In the new window, click on the **Add tools** icon.

<img width="619" height="356" alt="image" src="https://github.com/user-attachments/assets/3591bc48-d179-426d-abce-eb8ed9029f07" />


---

8. Select 2 tools: **Join Features** and **Filter by Attributes**, then click **Add**. 

<img width="644" height="704" alt="image" src="https://github.com/user-attachments/assets/92e0edc9-2370-4151-b337-e21e1926eee5" />


---

9. The tools will be added to the canvas and displayed in grey. Double-click on the **Join Features** box. 

<img width="930" height="435" alt="image" src="https://github.com/user-attachments/assets/8fac3bf1-c311-453d-83b7-38b9af7625e4" />


---

10. In the pop-up, select **China Province Boundaries** as the target layer, and **China Airport Dataset** as the join layer.

<img width="480" height="521" alt="image" src="https://github.com/user-attachments/assets/ec45cb37-71e2-448c-a247-89a354ecdd34" />


---

11. Next, toggle on **Use spatial relationship** and select **Completely contains**. For the **Join operation**, choose **Join one to one**, and ensure that **Calculate count only** under the **Multiple matching records** option is selected.

<img width="486" height="598" alt="image" src="https://github.com/user-attachments/assets/1308d9e9-e5e4-48d5-861f-bb6a71f6034e" />


---

12. For **Join type**, select **Inner join**. For the **Result type**, select **Create intermediate data** from the dropdown \- this means the output from this analysis tool will not be saved as a permanent layer. Click **Confirm**.

<img width="523" height="582" alt="image" src="https://github.com/user-attachments/assets/f102c26c-9d6e-4e76-b0ca-6c1fb99b612a" />


---

13. Now, the canvas should show two additional items in blue, representing the datasets we just configured. In addition, the tool box appears in yellow, and the output box appears in green.

<img width="969" height="433" alt="image" src="https://github.com/user-attachments/assets/a8bb0b95-ce24-4fb8-b722-c22b45323900" />


---

14. Next, double-click on **Filter by Attributes**.

<img width="960" height="427" alt="image" src="https://github.com/user-attachments/assets/12b94550-8b68-4593-9a60-52686a2a72a3" />


---

15. For the **Input dataset**, select **Join result**. 

<img width="682" height="759" alt="image" src="https://github.com/user-attachments/assets/dadce1e4-1d8c-4a65-bf31-6e8d9d7e8eca" />


---

16. Click on **\+ Build new query**.

<img width="501" height="614" alt="image" src="https://github.com/user-attachments/assets/e88013e5-284f-4816-aeeb-5c3dc35fcba3" />

---

17. Select **Expression** and click **Next**.

<img width="966" height="433" alt="image" src="https://github.com/user-attachments/assets/7293f4ac-d884-4cc1-8c77-e2b734addaa5" />

---

18. For **Where** fields, choose **All of the following are true** first. Then, set **Join Count** as the field, select **is greater than** as the operator, and select or enter **10** as the value. Once the condition is set, click **Add** to apply it.

<img width="908" height="421" alt="image" src="https://github.com/user-attachments/assets/d1c1cb6c-9bf0-466b-aeb6-fd534277da27" />

---

19. For the result layer, make sure the **Create hosted layer** is selected under the **Result type**, then give a name to the new layer in the **Output name** field. Note that the name should be unique across the organization no matter where you save the layer. Example: Chinese provinces with over 10 airports\_\[Your NetID\].

<img width="455" height="620" alt="image" src="https://github.com/user-attachments/assets/57bbddbb-02ed-4716-b371-a8770c0af7fa" />

---

20. In the canvas, all items are now connected in a workflow with arrows and color-coded accordingly. Click **Run** to execute the model.

<img width="918" height="386" alt="image" src="https://github.com/user-attachments/assets/b129aac0-f2b0-4d4d-a957-074234a585eb" />

---

21. Once the model runs successfully, a green check mark will appear on both the tool and output boxes. 

<img width="919" height="336" alt="image" src="https://github.com/user-attachments/assets/14328854-329c-494c-8600-b2694b78a4bf" />

---

22. In the **Layers** pane, a new layer called **Chinese provinces with over 10 airports** will now appear.

<img width="578" height="312" alt="image" src="https://github.com/user-attachments/assets/76c98348-7152-47e9-8ae5-236e93d5455b" />

---

23. Click the **Save** icon, then close the tab.

<img width="652" height="332" alt="image" src="https://github.com/user-attachments/assets/9095d711-8cc4-4348-9aff-45808bd03e2a" />

---

24. Under **Models in this map**, you will find the model we just saved. Click on \+its name to reopen it. You can swap in different datasets and run it again anytime to repeat the same analysis.

<img width="631" height="237" alt="image" src="https://github.com/user-attachments/assets/b6a550c7-3e5c-4d51-975c-5b017b3f6423" />

---

25. Remember to save the project manually.



# Resources

ArcGIS Online offers a wide range of tools for visualizing and analyzing geospatial data, and this tutorial only covers some of them. You are encouraged to continue exploring and experimenting with the tool. For further learning, the following resources are recommended:

* [ArcGIS Online Resources](https://www.esri.com/en-us/arcgis/products/arcgis-online/resources) by Esri;  
* [Perform analysis in Map Viewer](https://learn.arcgis.com/en/paths/data-analysis/) by Esri;  
* ArcGIS Online [Tool Documentation](https://doc.arcgis.com/en/arcgis-online/analyze/aggregate-points-mv.htm)  
* [ArcGIS Online Community](https://community.esri.com/t5/arcgis-online/ct-p/arcgis-online) for browsing resources, sharing knowledge, and connecting with other users.

If you have any questions about the tool or this tutorial, don’t hesitate to reach out to the Data and Visualization Librarian, Siti Lei ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)) for further support.
