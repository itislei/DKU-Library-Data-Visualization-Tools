# **ArcGIS Online for Mapping Data and Spatial Analysis**

*Siti Lei*  
*Data and Visualization Librarian, Duke Kunshan University*

*Last updated: November 21, 2025*

This tutorial introduces how to create, visualize, analyze, and share data-driven interactive maps using ArcGIS Online.

[Before we start	](#before-we-start)

[Introduction	](#introduction)

[About the tool	](#about-the-tool)

[Datasets	](#datasets)

[What is “spatial analysis” and “geoprocessing”?	](#what-is-“spatial-analysis”-and-“geoprocessing”?)

[Part 1: Building Maps with Data	](#part-1:-building-maps-with-data)

[Sign in to ArcGIS Online	](#sign-in-to-arcgis-online)

[Create a New Map Project	](#create-a-new-map-project)

[Toolbars	](#toolbars)

[Basemap	](#basemap)

[Add Data	](#add-data)

[Structured Table Dataset	](#structured-table-dataset)

[Geospatial Data File	](#geospatial-data-file)

[Acquire Data from ArcGIS Online	](#acquire-data-from-arcgis-online)

[Visualize Data	](#visualize-data)

[Styles	](#styles)

[Labels	](#labels)

[Pop-ups	](#pop-ups)

[Save a Map	](#save-a-map)

[Share a Map	](#share-a-map)

[Export Data	](#export-data)

[Part 2: Analyzing Data with Maps	](#part-2:-analyzing-data-with-maps)

[Tools	](#tools)

[Join Data	](#join-data)

[Find by Attributes and Locations	](#find-by-attributes-and-locations)

[Find Closest	](#find-closest)

[Extract Data	](#extract-data)

[Model Builder	](#model-builder)

[Resources	](#resources)

# 

# **Before we start** {#before-we-start}

## **Introduction** {#introduction}

In this tutorial, we will use China’s airport location dataset and provincial boundary dataset to explore the distribution of airports across provinces in China. DKU members may download the original dataset from CnOpenData through [DKU Only E-Resources](https://library.dukekunshan.edu.cn/academic-databases/) by following the instructions.

Tasks covered in this tutorial include:

1. Changing the basemap  
2. Loading and displaying China’s provincial boundaries on a map  
3. Loading and displaying airport locations on a map  
4. Saving the project and exporting data as a shapefile

By the end of this tutorial, you will be able to use ArcGIS Online to create a provincial-level map of China showing the geographic distribution of airports.

## **About the tool** {#about-the-tool}

ArcGIS Online will be used in the tutorial. Visit the [GIS guide](https://library.dukekunshan.edu.cn/geographic-information-system-gis/) for more information about the tool.

## **Datasets** {#datasets}

The sample datasets are derived from [CnOpenData](https://www.cnopendata.com/) and have been cleaned for the purpose of demonstration. Download the sample datasets below:

* [China Airport.csv](https://duke.box.com/shared/static/ycwqlrka3797epk9m0p3svmsocj8fj3c.csv)  
* [China Province Boundary.zip](https://duke.box.com/s/7e2ksv0f7gw156wit9zjxw0stwxo59ws)

## **What is “spatial analysis” and “geoprocessing”?** {#what-is-“spatial-analysis”-and-“geoprocessing”?}

The second part of this tutorial introduces how to use geoprocessing tools to perform spatial analysis. To help ground these concepts, here is a brief overview:

**Spatial analysis** is the process of examining geographic data based on location, relationships, and patterns. It helps answer questions such as where features are located, how they are distributed, and how they interact with other geographic elements. 

**Geoprocessing** refers to the set of operations used to manipulate, analyze, and manage geographic data. These operations include overlaying layers, buffering, clipping, dissolving, intersecting, and converting data formats. In GIS, geoprocessing tools help model spatial relationships, create new datasets from existing ones, and automate complex workflows.

# **Part 1: Building Maps with Data**  {#part-1:-building-maps-with-data}

In Part 1, we will introduce the basics of ArcGIS Online, including how to import and load datasets, visualize your data on a map, and save or export your work.

## **Sign in to ArcGIS Online** {#sign-in-to-arcgis-online}

Follow the instructions in [Signing in to ArcGIS Online](https://library.dukekunshan.edu.cn/signing-in-to-arcgis/) to sign in to [ArcGIS Online](https://www.arcgis.com/index.html). 

## **Create a New Map Project** {#create-a-new-map-project}

### **Toolbars** {#toolbars}

1. Once you successfully sign in to ArcGIS Online, you will see the view shown below. To start creating a map, go to the **Map** tab in the main menu — this opens a new map view where you can begin a new map project.

<img width="1015" height="410" alt="image001" src="https://github.com/user-attachments/assets/6c0cfa04-f6ac-46f2-a7d3-97b5c5c9dc54" />



2. The interface provides a variety of tools, organized in these toolbars:  
1) Contents toolbar  
2) Editing toolbar  
3) Viewing and Search toolbar


<img width="1232" height="782" alt="image003" src="https://github.com/user-attachments/assets/18f93cbc-27f9-4c12-9c4e-93c919a98951" />



### **Basemap** {#basemap}

1. The main map at the center serves as the basemap. By default, ArcGIS Online applies the “Topographic” map as the basemap.   
     
2. To select an alternative, navigate to the contents toolbar, select **Basemap**, and a list of available options will be displayed.


<img width="437" height="591" alt="image005" src="https://github.com/user-attachments/assets/5335de4b-8eca-45a1-8441-4172704b58a9" />



3. Scroll down and select **Light Gray Canvas**.


<img width="371" height="323" alt="image007" src="https://github.com/user-attachments/assets/fffc861e-5c39-4b3d-b899-e9124c11d0c9" />



4. The reference system for China is not accurate. To correct this, we will create a new labeling system. First, close the current one by clicking the arrow to expand the details of the selected basemap.

<img width="383" height="114" alt="image009" src="https://github.com/user-attachments/assets/e20089ae-b8a9-4d23-b53c-667e33e24090" />



5. Then, click on the eye icon next to **Light Gray Reference** to hide it.



<img width="380" height="343" alt="image011" src="https://github.com/user-attachments/assets/f4b0e31d-8d5e-4a9e-bfd9-3d841832d28b" />



## **Add Data** {#add-data}

There are multiple ways to add data to a map project in ArcGIS Online \- you can add datasets with location data, upload images, connect to external sources via URL, or create your own sketches directly in the map.

ArcGIS Online supports importing data from structured table formats such as comma-separated values files (.csv), Excel files (.xslx) with location fields (e.g., coordinates, addresses), and geospatial file formats including shapefile (.shp), GeoJSON, KML (.kml), and GeoPackage (.gpkg), and Geodatabase (.gdb).

### **Structured Table Dataset** {#structured-table-dataset}

[China Airport.csv](https://duke.box.com/shared/static/ycwqlrka3797epk9m0p3svmsocj8fj3c.csv) is a data table containing information about every airport in China, including their names, addresses, coordinates, and year of construction. Let’s map this data on the map\! Before we begin, make sure you have downloaded the file to your computer.

1. Go to the contents toolbar, select **Add**, then **Add layer from file**.

<img width="232" height="245" alt="image013" src="https://github.com/user-attachments/assets/5feb6e57-81d8-4c28-89fe-89c9ea9bd5a6" />



2. Click **Your device** button, then select **China Airport Dataset.csv** file (downloaded from the setup files) from its saved location and click **Open**. Alternatively, drag and drop the file into the pop-up window.

<img width="1345" height="675" alt="image015" src="https://github.com/user-attachments/assets/b1fd7d91-1f1f-40ed-b951-c79be705ffa7" />



3. Select **Create a hosted feature layer and add it to the map**, click **Next**.


<img width="1085" height="633" alt="image017" src="https://github.com/user-attachments/assets/2d2ec344-a905-4396-bc1d-e0879d52a5e3" />



4. Confirm data type for each variable, and click **Next**.

<img width="1084" height="632" alt="image019" src="https://github.com/user-attachments/assets/98dad15c-2cb8-4c0d-bf45-481035abd965" />



5. Click the arrow icon to expand the options, select **Latitude and longtitude**, click **Next**.

<img width="1085" height="633" alt="image021" src="https://github.com/user-attachments/assets/07089a55-2a75-4d3d-afd8-2f506c028986" />



6. Open the dropdown, then select **LAT** for the “Latitude” field and **LNG** for the “Longitude” field, click **Next**.

<img width="1084" height="632" alt="image023" src="https://github.com/user-attachments/assets/1d7b4c73-cbdf-439d-a12b-224b79e4700f" />




7. Name the new layer as **China Airport Dataset**, then click **Create and add to map**.


<img width="1084" height="632" alt="image025" src="https://github.com/user-attachments/assets/293443dc-eeb1-4b3a-8eb9-7c59d720da03" />



8. A map layer with all airport data points in China has been added to your map\!


<img width="891" height="596" alt="image027" src="https://github.com/user-attachments/assets/7f8f154b-0ba8-4c7d-b908-845b1fc05b0d" />


9. Go to **Layers** in the contents toolbar to check the items that have been added to the project.

<img width="393" height="171" alt="image029" src="https://github.com/user-attachments/assets/bdbb389e-81a3-45f2-9fa8-497b88f5f455" />



### **Geospatial Data File** {#geospatial-data-file}

A shapefile is one of the most common geospatial data formats used in GIS, which stores geographic features (such as points, lines, or polygons) along with their associated attributes. Despite its name, a shapefile is actually a collection of several related files (e.g., .shp, .shx, .dbf) that must stay together for the data to function properly. ArcGIS Online can only read a shapefile directly from a zipped folder, which is why you should upload the .zip file without unzipping it.

[China Province Boundary.zip](https://duke.box.com/s/7e2ksv0f7gw156wit9zjxw0stwxo59ws) is a compressed folder containing a shapefile and its supporting files. It provides provincial-level boundary data for China, with each province represented as a polygon. Let’s add this data to the map\! Before we begin, make sure you have downloaded the file to your computer, and **do not** unzip it.

1. After download, go to the contents toolbar, select **Add** \> **Add layer from file**.

![image031](https://github.com/user-attachments/assets/ebc014cb-5a83-4559-8364-0c814e4f1211)


2. Select **Your device** option, then locate and click on the **China Province Boundaries.zip** file (downloaded from the setup files) from its saved location and click **Open**. Alternatively, drag and drop the file into the pop-up window. Click **Next** to continue.

![image032](https://github.com/user-attachments/assets/7304da18-9316-41cf-afd0-7233dbcf7bd6)



3. Make sure “Shapefile” is selected, then click **Next**.

<img width="1344" height="674" alt="image114" src="https://github.com/user-attachments/assets/79dca8b4-5055-41ba-9dd6-4964c8afea1f" />



4. Name the new layer as **China Province Boundaries**, then click **Create and add to map**.

<img width="1346" height="677" alt="image115" src="https://github.com/user-attachments/assets/0870c93d-afb9-48cd-9f17-604f16e3f07d" />


5. It may take a moment to process. Once completed, a new layer named **China Province Boundaries** will appear in the **Layers** panel. Locate the **China Province Boundaries** layer, click the ellipsis (3-dot) icon next to it, and select **Zoom to layer**.


<img width="383" height="208" alt="image116" src="https://github.com/user-attachments/assets/066b3d9c-5d86-4c27-a402-9ed41d88b7c9" />


6. This will automatically zoom to the area where your data is displayed on the map.


<img width="1028" height="744" alt="image75" src="https://github.com/user-attachments/assets/ff475502-9edd-4ed5-8d92-857a41216ab0" />



7. Go back to the **Layers** panel, and click the eye icon to hide the **China Province Boundaries** layer for now.

<img width="382" height="102" alt="image76" src="https://github.com/user-attachments/assets/1732087b-7369-472e-8c21-af6fd6c48d87" />



### **Acquire Data from ArcGIS Online** {#acquire-data-from-arcgis-online}

Not just a tool, ArcGIS Online is also a rich source of map data, with contributions shared by researchers worldwide. For example, to understand where airports are located within provinces, we need to add a China province layer to the map, which can be directly imported from the ArcGIS Online database.

1. Go to the contents toolbar, then **Add**, **Browse layers.**

<img width="234" height="246" alt="image77" src="https://github.com/user-attachments/assets/aba653c9-2295-41a1-beac-ca53677cac50" />


2. Switch the source from **My content** to **ArcGIS Online**.

<img width="286" height="268" alt="image79" src="https://github.com/user-attachments/assets/37912fbe-d485-4c0c-a99c-8ade956d828e" />



3. Type in the keyword “China province” and press **Enter** on your keyboard.

4. Locate the item **China Province Boundaries** by Esri in the search results, click **\+ Add**.

<img width="379" height="445" alt="image80" src="https://github.com/user-attachments/assets/b4523b4f-5dfb-4d3b-8dac-1272ee5dfe26" />



5. Use the **Zoom In/Out** tool under the viewing and search toolbar to examine the data in detail.


<img width="458" height="290" alt="image81" src="https://github.com/user-attachments/assets/78ad587e-999e-4504-b9fa-32fb08df0a2a" />



6. Click **Remove** to delete the layer from your map.

<img width="365" height="168" alt="image82" src="https://github.com/user-attachments/assets/43f13759-7076-43da-a6de-499874738363" />


## **Visualize Data** {#visualize-data}

### **Styles** {#styles}

1. To customize the appearance of data points, lines, or polygons on the map, first make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

<img width="430" height="263" alt="image84" src="https://github.com/user-attachments/assets/14cc6b70-2405-47dc-a072-57cfd4477ed4" />


2. Then, select **Styles** under the editing toolbar and use the settings to adjust the appearance of the data points according to your preference. For best practices in selecting colors or patterns for geospatial data and maps, refer to the [Select Visualization Elements](https://library.dukekunshan.edu.cn/data-visualization/#:~:text=4.%20Select%20Visualization%20Elements) section in the [Data Visualization guide](https://library.dukekunshan.edu.cn/data-visualization/). Click **Done** when the edits are complete. 

<img width="393" height="171" alt="image23" src="https://github.com/user-attachments/assets/50a2a43a-56d8-4cd0-8c72-8e207bfd722b" />


### **Labels** {#labels}

1. You can configure labels for a map layer. To do so, first, make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

<img width="394" height="344" alt="image83" src="https://github.com/user-attachments/assets/0087abba-7597-4752-8c57-28eb056c2690" />


2. Next, select **Labels** under the editing toolbar to start editing. Make sure you toggle on **Enable labels** and select **Name** field as the **Label field** to show the name of each province (since we turned them off in the basemap). You can also adjust the settings to customize their look.

<img width="699" height="531" alt="image20" src="https://github.com/user-attachments/assets/f7593b1e-b031-494e-b795-47a4e47256dd" />


### **Pop-ups** {#pop-ups}

1. Click on a random data point on the map — this will trigger a pop-up displaying all associated information for that specific point.

<img width="564" height="422" alt="image22" src="https://github.com/user-attachments/assets/7349595b-a457-4987-af5e-7c9beba0f8f0" />


2. To configure the pop-ups or edit the displayed information in the pop-up, first make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

<img width="393" height="171" alt="image113" src="https://github.com/user-attachments/assets/093281f5-b5ff-4646-8d18-7eb93dae73dd" />


3. Next, go to **Pop-ups** under the editing toolbar to customize the content displayed.

<img width="392" height="431" alt="image24" src="https://github.com/user-attachments/assets/4da2cf5c-6a21-4ee0-a627-adaeb09fd8c8" />


## **Save a Map** {#save-a-map}

ArcGIS Online does **not** save your map project automatically, so be sure to manually save it each time before quitting the page.

1. To save a new-created map project, go to the contents toolbar, click **Save and open**, then **Save as**.

<img width="223" height="266" alt="image25" src="https://github.com/user-attachments/assets/9db69e5c-f4e2-4616-bede-481c1863aa30" />


2. Name the project as **China Airport Map Project**, add other details if needed, and click **Save**.

<img width="516" height="578" alt="image26" src="https://github.com/user-attachments/assets/71d2245e-1537-469a-8cd2-f7cc4aa2eb7b" />


3. Click the hamburger (3-line) icon in the top left corner, then select **Content** \- this is where your saved work will be stored. You can also find it under the main menu.

<img width="351" height="607" alt="image27" src="https://github.com/user-attachments/assets/66c12702-9231-4728-ae69-b6b3a3914a27" />


4. Every time before quitting the project, go to the contents toolbar, click **Save and open**, then click **Save** to apply your changes.

<img width="199" height="242" alt="image28" src="https://github.com/user-attachments/assets/e50079af-8837-4845-ab14-39834aa1e9a5" />


## **Share a Map** {#share-a-map}

One advantage of using ArcGIS Online is that it allows easy sharing of map projects. With an institutional license, DKU members can share their projects with Duke and DKU users, make them public, or keep them private for self-view only.

You can also set up a group to make your project or items visible or editable to group members. Follow the instructions [here](https://doc.arcgis.com/en/arcgis-online/share-maps/create-groups.htm) to create a group. If you have any questions, please contact the Data and Visualization Librarian ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)). 

1. Go to **Content**, then **My content**. Locate the item you want to share, and click on its title.

<img width="1281" height="347" alt="image29" src="https://github.com/user-attachments/assets/e75fa705-98c5-43ee-b806-aeb260d95c36" />


2. Alternatively, click on the ellipsis (3-dot) icon next to the item and select **View details**.

<img width="222" height="296" alt="image30" src="https://github.com/user-attachments/assets/d45c9701-113d-4a7a-9d9c-e82072285328" />


3. From the right-hand pane, click **Share** to open the sharing options.

<img width="312" height="368" alt="image1" src="https://github.com/user-attachments/assets/c1554cd2-7cbe-45ca-9a71-e765414f2e6e" />


4. Choose **Everyone (public)** under sharing options, and click **Save**.

<img width="509" height="624" alt="image2" src="https://github.com/user-attachments/assets/aa6cd518-e98d-4838-8479-cf2855439564" />


5. Click **Review sharing** to check the items whose sharing permissions will be updated accordingly.

<img width="509" height="177" alt="image3" src="https://github.com/user-attachments/assets/c1e44369-7431-4dac-b8db-ad5910d1825e" />


6. Click **Update sharing** to confirm the changes.

<img width="1005" height="453" alt="image4" src="https://github.com/user-attachments/assets/80b03445-fa19-4edd-bef5-cf08341c6655" />


7. Now, your map should be visible by the public.

## **Export Data** {#export-data}

For each layer created or added to a map project, you can export it as a shapefile to open in other GIS software or store on your local computer. In this tutorial, we will use the airport layer as an example.

1. Go to **Content**, then **My content**. Make sure the item you select is of the “Feature layer (hosted)” type \- otherwise, it will not support shapefile export.

<img width="1494" height="348" alt="image5" src="https://github.com/user-attachments/assets/a4eef91c-3543-441b-956e-708073dbbf0e" />


2. Click on the ellipsis (3-dot) icon next to the item title, select **View details**. You can also do it by clicking on the item title.

<img width="183" height="300" alt="image6" src="https://github.com/user-attachments/assets/8b4f2fef-aa92-40cd-9e2f-c07872489eec" />


3. Under the **Overview** tab, click **Export data** from the right pane.

<img width="318" height="503" alt="image7" src="https://github.com/user-attachments/assets/4c876f64-e0a9-44c7-a2d9-a442dc58ec1f" />


4. Then, select **Export to shapefile** from the dropdown menu.

<img width="317" height="337" alt="image8" src="https://github.com/user-attachments/assets/42a4fea0-b029-42c6-9ed6-f64d38ef606e" />


5. Name the new file as **China Airport Dataset**, add other details if needed, and click **Export**.

<img width="514" height="572" alt="image9" src="https://github.com/user-attachments/assets/2ccc4cf5-b228-48f1-aa83-97a0de549ba7" />


6. Once the export is complete, a new page will appear showing the file type as “Shapefile”. You can also find it under the **Content** tab.

<img width="871" height="315" alt="image10" src="https://github.com/user-attachments/assets/0c0107b2-84b7-49b9-9f53-5db0e3fb73c2" />


7. Click **Download** on the right pane to save the file in your local computer.

<img width="323" height="330" alt="image41" src="https://github.com/user-attachments/assets/f3cbf523-ea48-4464-9dbb-9986e219764c" />


# **Part 2: Analyzing Data with Maps** {#part-2:-analyzing-data-with-maps}

In Part 2, we will use some geoprocessing tools in ArcGIS Online to gain insights from China’s airport and province boundary datasets. By the end, you will be able to use maps to answer these questions:

1. How are airports distributed across the provinces of the country? Which provinces have higher or lower densities of airports?  
2. How many airports are there in Jiangsu province? What are these airports, and where are they located?  
3. Which 3 airports in Jiangsu province are closest to DKU campus?  
4. How to export the layer into a format that is shareable and downloadable (e.g., Shapefile, CSV)?  
5. Which provinces have more than 10 airports?

## **Tools** {#tools}

### **Join Data** {#join-data}

The first question “How are airports distributed across the provinces of the country? Which provinces have higher or lower densities of airports?” focuses on the distribution and density of airport locations across the country. 

Since the two datasets we need to answer this question are currently separate, we need to merge them into a single layer. Many of the geoprocessing tools can achieve this (like **Aggregate Points**), but the tool that will be introduced in this tutorial is **Join Features**. 

1. Go to the Editing toolbar, click on **Analysis**.

<img width="386" height="532" alt="image15" src="https://github.com/user-attachments/assets/49d2a774-27a2-4e39-9bf0-7a11f77c680c" />


2. Select **Tools**. Alternatively, click the tool icon in the header menu.

<img width="327" height="481" alt="image39" src="https://github.com/user-attachments/assets/f8e09fe9-508f-4d12-a552-98cd988a2666" />


3. Under **Summarize data**, select **Join Features**.

<img width="778" height="283" alt="image42" src="https://github.com/user-attachments/assets/2ce9e158-923f-43f6-930f-8ef7a245f588" />


4. Now, let’s configure our input and output. First, for the **Target layer**, select **China Province Boundaries** layer from the dropdown.

<img width="701" height="537" alt="image43" src="https://github.com/user-attachments/assets/4a98475e-ce0a-4b91-b63a-5764ebf1856d" />


5. For the **Join layer**, select **China Airport Dataset** layer from the dropdown.

<img width="699" height="536" alt="image44" src="https://github.com/user-attachments/assets/edb2e595-8187-4027-9287-d2e943418e9b" />


6. Under the **Join settings**, toggle on **Use spatial relationship**.

<img width="366" height="180" alt="image45" src="https://github.com/user-attachments/assets/bc104541-69cd-46aa-81e5-ce98cc182481" />


7. For the **Spatial relationship**, select **Completely contains** from the dropdown menu.

<img width="363" height="156" alt="image46" src="https://github.com/user-attachments/assets/dd074114-dda6-430c-ae7e-00c74960dc84" />


8. For the **Join operation**, select **Join one to one** from the dropdown menu.

<img width="365" height="127" alt="image47" src="https://github.com/user-attachments/assets/49700d62-789f-441c-9bce-a9e86dfb4781" />


9. Since we are analyzing the density of airports across provinces, we first need to calculate the number of airports in each province. Under the **Multiple matching records**, select **Calculate count only**.

<img width="366" height="134" alt="image48" src="https://github.com/user-attachments/assets/6ac3d9da-8be8-4f84-b57f-4f8db3fee39a" />


10. For the **Join type**, make sure **Inner join** is highlighted.

<img width="363" height="82" alt="image40" src="https://github.com/user-attachments/assets/d199fa8e-f712-4f12-bc3c-1a4770bb24f7" />


11. Under the **Result layer**, give a name to the new layer in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: **Count of Airports in Provinces\_\[Your NetID\]**.

<img width="370" height="247" alt="image33" src="https://github.com/user-attachments/assets/4525c84f-abf4-4115-b8cd-f21135ae3eb1" />


12. Click **Run** to start processing.

<img width="382" height="117" alt="image21" src="https://github.com/user-attachments/assets/8da86f3e-c2de-4f3d-947b-d5326cea43eb" />


13. To check the progress, click on the history icon in the header menu.

<img width="382" height="108" alt="image34" src="https://github.com/user-attachments/assets/bbcca6f5-151d-41e7-af7b-50d2d15baf8c" />


14. Once the analysis is completed successfully, a new layer named **Count of airports in provinces** will appear in the **Layers** and the map. Let’s focus on this layer by hiding the other two layers and keep only the newly created one visible.

<img width="432" height="289" alt="image35" src="https://github.com/user-attachments/assets/f1fdc83d-b19c-404a-9ae7-37ef0ee8304b" />


15. The new layer called **Count of airports in provinces** will show up in the **Layers** pane. When you click on a province polygon, the pop-up will display a new attribute called **Join\_Count**, followed by the total number of airports in the corresponding province.

<img width="1022" height="617" alt="image36" src="https://github.com/user-attachments/assets/34265b67-3cf2-446f-bc25-b1c7de0fe8d7" />


16. Click the ellipsis (3-dot) icon next to **Count of airports in provinces** layer and select **Show table**. 

<img width="162" height="180" alt="image37" src="https://github.com/user-attachments/assets/7ed00588-0633-4d04-9ca2-7babf98e0d9b" />


17. The data table attached to this layer will appear with two new attributes named **Join\_Count** and **Admin Name**. **Join\_Count** indicates the number of airports in each corresponding province, **Admin Name** represents the administrative region used in the spatial analysis.

<img width="992" height="548" alt="image38" src="https://github.com/user-attachments/assets/f7602074-aa70-41ea-856b-3cbfeb6c3c3c" />


### **Find by Attributes and Locations** {#find-by-attributes-and-locations}

Let’s move to the second question: What and where are the airports in Jiangsu Province?

To answer this, we can use the **Find by Attributes and Location** tool. This tool allows us to set specific query conditions (such as filtering by province name) to automatically extract only the airports that meet our criteria. Once applied, it will generate a subset of the data showing all airports located within Jiangsu.

1. Go to the Editing toolbar, click on **Analysis**.

<img width="386" height="532" alt="image15" src="https://github.com/user-attachments/assets/77560eb1-dc65-4bfd-a170-f1856acf8708" />


2. Select **Tools**. Alternatively, click the tool icon in the header menu.

<img width="327" height="481" alt="image39" src="https://github.com/user-attachments/assets/522b2623-fb37-4b46-8e10-5191d2c3f9d5" />


3. Under the **Find locations**, select **Find by Attributes and Location**.

<img width="820" height="424" alt="image31" src="https://github.com/user-attachments/assets/e3ebd615-ff67-4ab1-8d4d-6e4a1c253aa1" />


4. Click on **\+ Build new query** under **Criteria**.

<img width="367" height="257" alt="image32" src="https://github.com/user-attachments/assets/8f847450-480a-41ef-80c5-7c734e813eae" />


5. For **Find features from**, select **China Airport Dataset** layer from the dropdown, then select **Attribute expression**, click **Next**.

<img width="956" height="431" alt="image61" src="https://github.com/user-attachments/assets/483372ec-c2e7-486c-b9aa-7fb649bd6946" />


6. For **Where** fields, we will define the criteria. First, choose **All of the following are true**. Then, set **Province\_EN** as the field, select **equal** as the operator, and select or enter **Jiangsu** as the value. Once the condition is set, click **Add** to apply it.

<img width="953" height="429" alt="image62" src="https://github.com/user-attachments/assets/df777c36-8479-4f67-afc6-2a7c8340872b" />


7. Under the **Result layer**, give the new item a name in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: Airports in Jiangsu\_\[Your NetID\].

<img width="371" height="280" alt="image63" src="https://github.com/user-attachments/assets/880c7c3a-036a-4c84-80a5-e92fba03f43d" />


8. Click **Run** to start processing.

<img width="382" height="117" alt="image21" src="https://github.com/user-attachments/assets/848b0642-3ea6-496f-b762-5f4735356c97" />


9. To check the progress, click on the history icon in the header menu.

<img width="382" height="108" alt="image34" src="https://github.com/user-attachments/assets/7ce58704-2a81-4f35-b7ab-88d1f4416e45" />


10. Once the analysis is completed successfully, a new layer named **Airports in Jiangsu** will appear in the **Layers** and the map. Let’s focus on this layer by hiding the other layers and keep only the newly created one visible.

<img width="282" height="267" alt="image64" src="https://github.com/user-attachments/assets/d88c55ae-d6f8-4033-8373-87cb8690c88a" />


11. The map will update to show the new layer we just created, automatically zooming into Jiangsu province.

<img width="1358" height="859" alt="image65" src="https://github.com/user-attachments/assets/f52135b1-53c4-47a4-a3f3-6ffdfe2f984c" />


12. Click the ellipsis (3-dot) icon next to **Airports in Jiangsu** layer and select **Show table**. 

<img width="162" height="180" alt="image37" src="https://github.com/user-attachments/assets/4982341f-0d35-4b58-980d-3201a181d31b" />


13. There should be 11 records in the table, meaning that there are 11 airports in Jiangsu province.

<img width="948" height="525" alt="image58" src="https://github.com/user-attachments/assets/2db9e1f8-46af-4760-895b-e589980597c2" />


### **Find Closest** {#find-closest}

The third question we want to solve is: what are the 3 closest airports to DKU. To do that, we will first create a new layer with DKU campus’s location data.

1. Click on the **Search** tool in the Searching and Viewing toolbar.

<img width="131" height="184" alt="image59" src="https://github.com/user-attachments/assets/0d4e9da5-4a38-41ec-acb7-c8645f032f37" />


2. Click **Use current location**, Or, enter **Kunshan, Jiangsu**, and select the first option from the dropdown. This will locate you to the Kunshan region on the map. Then, navigate to the Duke Kunshan University.

<img width="577" height="444" alt="image60" src="https://github.com/user-attachments/assets/d071dfa5-ad2c-4591-b755-d79bd3099380" />


3. Go to **Add**, then select **Create sketch layer**.

<img width="285" height="297" alt="image51" src="https://github.com/user-attachments/assets/cb31c685-40fa-42c2-9b1f-1e32f9148e5f" />


4. Under the **Point feature** in the **Sketch** pane, name the new data point as **DKU**.

<img width="370" height="485" alt="image52" src="https://github.com/user-attachments/assets/f4ea5688-0460-49e6-a1d0-a7be6ef484f5" />


5. Make sure the stamp icon is selected in the sketch toolbar, and click on two random places in the campus area on the map.

<img width="962" height="693" alt="image53" src="https://github.com/user-attachments/assets/b8a283b4-6c81-44d2-ad01-b03a4353bdfe" />


6. We only need one data point actually, so let’s delete one of them. To do so, click **Select** (cursor icon) from the sketch toolbar. Then click on the point you want to delete, and click on **Delete** or hit **Backspace** on the keyboard.

<img width="581" height="231" alt="image54" src="https://github.com/user-attachments/assets/19b935a7-b4ff-4c30-ba69-264257c14d29" />


7. Go to **Layers**, rename the sketch layer as **DKU campus**, and click **OK**.

<img width="165" height="264" alt="image55" src="https://github.com/user-attachments/assets/514112ca-10d3-4258-8267-f2bee7a877d8" />


8. Next, go to **Analysis**, select **Find Closest** under the **Use proximity**.

<img width="888" height="273" alt="image56" src="https://github.com/user-attachments/assets/4a54e360-496a-45ad-a449-d70424d43373" />


9. Select **DKU campus (Points)** as input layer, and **Airports in Jiangsu layer** as near layer.

<img width="362" height="429" alt="image57" src="https://github.com/user-attachments/assets/d84f48b0-00d1-4ef2-aaed-952fe5e278c4" />


10. For the **Analysis settings**, toggle on **Limit the number of closest locations**, and enter **3** as the max number of input. Make sure **Limited the search range** is toggled off.

<img width="369" height="375" alt="image49" src="https://github.com/user-attachments/assets/0877de0b-5706-420b-bfa0-ecb8efbd980b" />


11. Under the **Result layer**, give a name to the new layer in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: Closest airports to DKU\_\[Your NetID\].

<img width="365" height="271" alt="image50" src="https://github.com/user-attachments/assets/24b8f3b4-1719-496e-b158-7dc1046f7e4b" />


12. Click **Run** to start processing.

<img width="382" height="117" alt="image21" src="https://github.com/user-attachments/assets/c58d3baa-a779-4138-a5b6-13523119ac88" />


13. To check the progress, click on the history icon in the header menu.

<img width="382" height="108" alt="image34" src="https://github.com/user-attachments/assets/5fc609a9-54f4-434c-9707-45d2b70983eb" />


14. Once the analysis is completed successfully, a new layer set named **Closest airports to DKU** will appear in the **Layers** and the map. Let’s keep the rest of the layers invisible.

<img width="295" height="357" alt="image96" src="https://github.com/user-attachments/assets/98e7742c-5f6e-4acc-8315-944e6f9300d6" />


15. Click on the arrow icon next to **Closest airports to DKU** layer set, click on the ellipsis (3-dot) icon next to **Connecting Lines** and select **Show table**. 

<img width="378" height="365" alt="image99" src="https://github.com/user-attachments/assets/e2aea17a-8d2a-45ab-839e-5d2ff041f97a" />


16. The data table should display 3 records, along with two new attributes \- **Near Rank** and **FindExistingLocation** \- which indicate the airport names and their rankings by distance.

<img width="1134" height="552" alt="image102" src="https://github.com/user-attachments/assets/6933fb36-1d5a-4174-bc3a-732ba5d80f99" />


### **Extract Data** {#extract-data}

Lastly, the analysis tools allow exporting layers in CSV, file geodatabase, shapefile, and KML. Let’s say we want to export the data table attached to our closest airports to the DKU layer in a table csv format. We already know how to view the data table in the map view, but how to download that in a csv format?

1. Go to the Editing toolbar, click on **Analysis**.

<img width="386" height="532" alt="image15" src="https://github.com/user-attachments/assets/eaf3cc18-9401-46a9-a52e-244f66aa97a5" />


2. Select **Tools**. Alternatively, click the tool icon in the header menu.

<img width="327" height="481" alt="image39" src="https://github.com/user-attachments/assets/1ce6a7c5-0c79-42c7-8aa8-f111539455e6" />


3. Under **Manage Data**, select **Extra Data**.

<img width="831" height="319" alt="image108" src="https://github.com/user-attachments/assets/fb96c7e9-5753-4080-956d-7648af8f0580" />


4. For **Input layers**, select **Closest airport to DKU \- Nearest Features** and **Closest airport to DKU \- Connecting Lines**. 

<img width="702" height="427" alt="image18" src="https://github.com/user-attachments/assets/f1f1ef13-4385-4b3a-87a9-57fe439df89a" />


5. Under **Result layer,** select CSV as the output data format, name the new output as **Top 3 closest airports**, and select the designated folder to save the output.

<img width="358" height="373" alt="image17" src="https://github.com/user-attachments/assets/74a9c0e7-076a-449a-b544-5d3ba6c6eaba" />


6. Click **Run** to start processing.

<img width="382" height="117" alt="image21" src="https://github.com/user-attachments/assets/dc2248ff-7c3d-4346-93f9-190676358023" />


7. Click on the history icon in the header menu to check the progress. Then, click on the ellipsis (3-dot) icon next to the processing record, and click **View details**. 

<img width="368" height="242" alt="image19" src="https://github.com/user-attachments/assets/f0c72f6c-74f0-4fa2-a84e-736e2d8a0e1e" />


8. Click on the ellipsis (3-dot) icon next to **Top 3 closest airports**, then **Open item details**.

<img width="944" height="524" alt="image14" src="https://github.com/user-attachments/assets/2c55d640-0ce4-4308-8d37-3e8fa4b5490c" />


9. A new item page will open. Click on the **Download** button in the right pane to download and save the file in your local computer.

<img width="1294" height="426" alt="image13" src="https://github.com/user-attachments/assets/3cae393d-28e5-4015-99ad-336b05dc4466" />


10. Open the **Nearest\_Features** file in Excel to view the ranked list of airports closest to the DKU campus. Note that Chinese text may not always export correctly.

<img width="431" height="141" alt="image16" src="https://github.com/user-attachments/assets/b782b7d0-cf41-43a4-ac3c-f34a10284428" />


## **Model Builder** {#model-builder}

While we just demonstrated how to answer multiple questions by running different analysis tools step by step, there is a way to streamline the entire process without executing each tool manually \- that’s **Model Builder**.

With **Model Builder**, instead of running each tool manually, you can build a workflow where outputs from one step feed directly into the next. This is especially useful when working with large datasets, performing multi-step analyses, or repeating the same workflow with different inputs.

In this demo, we will answer this question: which provinces in China have more than 10 airports?

1. Return to the map project view. If you can’t find it, go to the ArcGIS Online homepage and navigate to **Content** \> **My content**. Open the **Airport within province** web map item.

2. Click on **Analysis**.

<img width="386" height="532" alt="image15" src="https://github.com/user-attachments/assets/924b979a-e0c4-4a47-a1d6-9d9455e8f9e2" />


3. Select **ModelBuilder**. Alternatively, click the Model Builder icon in the header menu.

<img width="380" height="435" alt="image12" src="https://github.com/user-attachments/assets/f26deab3-072b-45ec-91a7-772689806abc" />


4. Click **Connect** to continue.

<img width="380" height="397" alt="image11" src="https://github.com/user-attachments/assets/48df63ea-57b5-49e7-af5d-c6007c57a6fd" />


5. Make sure the **Disconnect** button is showing up, then click **Create model**.

<img width="375" height="307" alt="image78" src="https://github.com/user-attachments/assets/afb24f68-0a4d-4bcc-90b7-4c4a52bfbaf5" />


6. For the model, let’s call it **Provinces with over 10 airports**, then click **Save**.

<img width="507" height="470" alt="image72" src="https://github.com/user-attachments/assets/b9704b12-7ca3-445c-9147-483e49462d42" />


7. In the new window, click on the **Add tools** icon.

<img width="278" height="192" alt="image71" src="https://github.com/user-attachments/assets/c974c048-6eb5-4b39-a699-1cac19bb0989" />


8. Select 2 tools: **Join Features** and **Filter by Attributes**, then click **Add**. 

<img width="509" height="557" alt="image74" src="https://github.com/user-attachments/assets/9e0599dd-fe60-4325-8342-08c703730f46" />


9. The tools will be added to the canvas and displayed in grey. Double-click on the **Join Features** box. 

<img width="511" height="247" alt="image73" src="https://github.com/user-attachments/assets/3b5ec593-28fa-4e9b-8503-35eb3f230848" />


10. In the pop-up, select **China Province Boundaries** as the target layer, and **China Airport Dataset** as the join layer.

<img width="287" height="317" alt="image68" src="https://github.com/user-attachments/assets/382cb152-f30b-4825-8d8c-8c0265ab299e" />


11. Next, toggle on **Use spatial relationship** and select **Completely contains**. For the **Join operation**, choose **Join one to one**, and ensure that **Calculate count only** under the **Multiple matching records** option is selected.

<img width="289" height="399" alt="image67" src="https://github.com/user-attachments/assets/61efa4f6-97bf-4a83-8a24-527c532f5c29" />


12. For **Join type**, select **Inner join**. For the **Result type**, select **Create intermediate data** from the dropdown \- this means the output from this analysis tool will not be saved as a permanent layer. Click **Confirm**.

<img width="285" height="316" alt="image70" src="https://github.com/user-attachments/assets/556b858f-2c0d-410e-934b-bc978774c8ff" />


13. Now, the canvas should show two additional items in blue, representing the datasets we just configured. In addition, the tool box appears in yellow, and the output box appears in green.

<img width="733" height="332" alt="image69" src="https://github.com/user-attachments/assets/0574d18c-aa79-49e3-b344-c367d89508d1" />


14. Next, double-click on **Filter by Attributes**.

<img width="960" height="427" alt="image" src="https://github.com/user-attachments/assets/78223674-a7c0-4b99-8243-1a9e4a7de63b" />


15. For the **Input dataset**, select **Join result**. 

<img width="682" height="759" alt="image" src="https://github.com/user-attachments/assets/fe019d5b-e409-4fdb-a1fa-e1f37e6672a2" />


16. Click on **\+ Build new query**.

<img width="501" height="614" alt="image" src="https://github.com/user-attachments/assets/e88013e5-284f-4816-aeeb-5c3dc35fcba3" />


17. Select **Expression** and click **Next**.

<img width="966" height="433" alt="image" src="https://github.com/user-attachments/assets/7293f4ac-d884-4cc1-8c77-e2b734addaa5" />


18. For **Where** fields, choose **All of the following are true** first. Then, set **Join Count** as the field, select **is greater than** as the operator, and select or enter **10** as the value. Once the condition is set, click **Add** to apply it.

<img width="908" height="421" alt="image" src="https://github.com/user-attachments/assets/d1c1cb6c-9bf0-466b-aeb6-fd534277da27" />


19. For the result layer, make sure the **Create hosted layer** is selected under the **Result type**, then give a name to the new layer in the **Output name** field. Note that the name should be unique across the organization no matter where you save the layer. Example: Chinese provinces with over 10 airports\_\[Your NetID\].

<img width="455" height="620" alt="image" src="https://github.com/user-attachments/assets/57bbddbb-02ed-4716-b371-a8770c0af7fa" />


20. In the canvas, all items are now connected in a workflow with arrows and color-coded accordingly. Click **Run** to execute the model.

<img width="918" height="386" alt="image" src="https://github.com/user-attachments/assets/b129aac0-f2b0-4d4d-a957-074234a585eb" />


21. Once the model runs successfully, a green check mark will appear on both the tool and output boxes. 

<img width="919" height="336" alt="image" src="https://github.com/user-attachments/assets/14328854-329c-494c-8600-b2694b78a4bf" />


22. In the **Layers** pane, a new layer called **Chinese provinces with over 10 airports** will now appear.

<img width="578" height="312" alt="image" src="https://github.com/user-attachments/assets/76c98348-7152-47e9-8ae5-236e93d5455b" />


23. Click the **Save** icon, then close the tab.

<img width="652" height="332" alt="image" src="https://github.com/user-attachments/assets/9095d711-8cc4-4348-9aff-45808bd03e2a" />


24. Under **Models in this map**, you will find the model we just saved. Click on \+its name to reopen it. You can swap in different datasets and run it again anytime to repeat the same analysis.

<img width="631" height="237" alt="image" src="https://github.com/user-attachments/assets/b6a550c7-3e5c-4d51-975c-5b017b3f6423" />


25. Remember to save the project manually.

# **Resources** {#resources}

ArcGIS Online offers a wide range of tools for visualizing and analyzing geospatial data, and this tutorial only covers some of them. You are encouraged to continue exploring and experimenting with the tool. For further learning, the following resources are recommended:

* [ArcGIS Online Resources](https://www.esri.com/en-us/arcgis/products/arcgis-online/resources) by Esri;  
* [Perform analysis in Map Viewer](https://learn.arcgis.com/en/paths/data-analysis/) by Esri;  
* ArcGIS Online [Tool Documentation](https://doc.arcgis.com/en/arcgis-online/analyze/aggregate-points-mv.htm)  
* [ArcGIS Online Community](https://community.esri.com/t5/arcgis-online/ct-p/arcgis-online) for browsing resources, sharing knowledge, and connecting with other users.

If you have any questions about the tool or this tutorial, don’t hesitate to reach out to the Data and Visualization Librarian, Siti Lei ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)) for further support.
