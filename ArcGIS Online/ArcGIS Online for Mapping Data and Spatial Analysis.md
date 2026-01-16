# **ArcGIS Online for Mapping Data and Spatial Analysis**

*Siti Lei*  
*Data and Visualization Librarian, Duke Kunshan University*

*Last updated: November 21, 2025*

This tutorial introduces how to create, visualize, analyze, and share data-driven interactive maps using ArcGIS Online.

[**Before we start	2**](#before-we-start)

[Introduction	2](#introduction)

[About the tool	2](#about-the-tool)

[Datasets	2](#datasets)

[What is “spatial analysis” and “geoprocessing”?	2](#what-is-“spatial-analysis”-and-“geoprocessing”?)

[**Part 1: Building Maps with Data	3**](#part-1:-building-maps-with-data)

[Sign in to ArcGIS Online	3](#sign-in-to-arcgis-online)

[Create a New Map Project	3](#create-a-new-map-project)

[Toolbars	3](#toolbars)

[Basemap	4](#basemap)

[Add Data	5](#add-data)

[Structured Table Dataset	6](#structured-table-dataset)

[Geospatial Data File	10](#geospatial-data-file)

[Acquire Data from ArcGIS Online	12](#acquire-data-from-arcgis-online)

[Visualize Data	14](#visualize-data)

[Styles	14](#styles)

[Labels	15](#labels)

[Pop-ups	16](#pop-ups)

[Save a Map	17](#save-a-map)

[Share a Map	19](#share-a-map)

[Export Data	22](#export-data)

[**Part 2: Analyzing Data with Maps	25**](#part-2:-analyzing-data-with-maps)

[Tools	25](#tools)

[Join Data	25](#join-data)

[Find by Attributes and Locations	32](#find-by-attributes-and-locations)

[Find Closest	37](#find-closest)

[Extract Data	44](#extract-data)

[Model Builder	47](#model-builder)

[**Resources	57**](#resources)

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




4. Name the new layer as **China Province Boundaries**, then click **Create and add to map**.

<img width="383" height="208" alt="image037" src="https://github.com/user-attachments/assets/04b6197a-d1f5-4a94-82bf-31be3fd8932e" />


5. It may take a moment to process. Once completed, a new layer named **China Province Boundaries** will appear in the **Layers** panel. Locate the **China Province Boundaries** layer, click the ellipsis (3-dot) icon next to it, and select **Zoom to layer**.


<img width="1028" height="744" alt="image039" src="https://github.com/user-attachments/assets/2718f90a-c725-4194-8585-8dc4f2c17721" />


6. This will automatically zoom to the area where your data is displayed on the map.


<img width="382" height="102" alt="image041" src="https://github.com/user-attachments/assets/7ca3c041-4522-49c0-a008-ab1d3fb86fa7" />


7. Go back to the **Layers** panel, and click the eye icon to hide the **China Province Boundaries** layer for now.

<img width="234" height="246" alt="image043" src="https://github.com/user-attachments/assets/2588d5f7-0bfc-4789-a7c5-fb301de58a84" />


### **Acquire Data from ArcGIS Online** {#acquire-data-from-arcgis-online}

Not just a tool, ArcGIS Online is also a rich source of map data, with contributions shared by researchers worldwide. For example, to understand where airports are located within provinces, we need to add a China province layer to the map, which can be directly imported from the ArcGIS Online database.

1. Go to the contents toolbar, then **Add**, **Browse layers.**

<img width="286" height="268" alt="image045" src="https://github.com/user-attachments/assets/9d46f439-96af-46b9-8412-16096f1a8255" />


2. Switch the source from **My content** to **ArcGIS Online**.

<img width="379" height="445" alt="image047" src="https://github.com/user-attachments/assets/7becbcca-dbd2-49fd-905d-cda021ccf076" />


3. Type in the keyword “China province” and press **Enter** on your keyboard.

4. Locate the item **China Province Boundaries** by Esri in the search results, click **\+ Add**.




5. Use the **Zoom In/Out** tool under the viewing and search toolbar to examine the data in detail.

<img width="458" height="290" alt="image049" src="https://github.com/user-attachments/assets/4d6e40fa-c1c3-4642-ae3d-509a576e649a" />



6. Click **Remove** to delete the layer from your map.

<img width="365" height="168" alt="image051" src="https://github.com/user-attachments/assets/5f992c50-f5f2-42d5-af3d-89d132154582" />

## **Visualize Data** {#visualize-data}

### **Styles** {#styles}

1. To customize the appearance of data points, lines, or polygons on the map, first make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

![][image28]

2. Then, select **Styles** under the editing toolbar and use the settings to adjust the appearance of the data points according to your preference. For best practices in selecting colors or patterns for geospatial data and maps, refer to the [Select Visualization Elements](https://library.dukekunshan.edu.cn/data-visualization/#:~:text=4.%20Select%20Visualization%20Elements) section in the [Data Visualization guide](https://library.dukekunshan.edu.cn/data-visualization/). Click **Done** when the edits are complete. 

![][image29]

### **Labels** {#labels}

1. You can configure labels for a map layer. To do so, first, make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

![][image30]

2. Next, select **Labels** under the editing toolbar to start editing. Make sure you toggle on **Enable labels** and select **Name** field as the **Label field** to show the name of each province (since we turned them off in the basemap). You can also adjust the settings to customize their look.

![][image31]

### **Pop-ups** {#pop-ups}

1. Click on a random data point on the map — this will trigger a pop-up displaying all associated information for that specific point.

![][image32]

2. To configure the pop-ups or edit the displayed information in the pop-up, first make sure that you have selected the target layer under **Layers**. A blue strip will appear on the left of the selected layer’s title.

![][image33]

3. Next, go to **Pop-ups** under the editing toolbar to customize the content displayed.

![][image34]

## **Save a Map** {#save-a-map}

ArcGIS Online does **not** save your map project automatically, so be sure to manually save it each time before quitting the page.

1. To save a new-created map project, go to the contents toolbar, click **Save and open**, then **Save as**.

![][image35]

2. Name the project as **China Airport Map Project**, add other details if needed, and click **Save**.

![][image36]

3. Click the hamburger (3-line) icon in the top left corner, then select **Content** \- this is where your saved work will be stored. You can also find it under the main menu.

![][image37]

4. Every time before quitting the project, go to the contents toolbar, click **Save and open**, then click **Save** to apply your changes.

![][image38]

## **Share a Map** {#share-a-map}

One advantage of using ArcGIS Online is that it allows easy sharing of map projects. With an institutional license, DKU members can share their projects with Duke and DKU users, make them public, or keep them private for self-view only.

You can also set up a group to make your project or items visible or editable to group members. Follow the instructions [here](https://doc.arcgis.com/en/arcgis-online/share-maps/create-groups.htm) to create a group. If you have any questions, please contact the Data and Visualization Librarian ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)). 

1. Go to **Content**, then **My content**. Locate the item you want to share, and click on its title.

![][image39]

2. Alternatively, click on the ellipsis (3-dot) icon next to the item and select **View details**.

![][image40]

3. From the right-hand pane, click **Share** to open the sharing options.

![][image41]

4. Choose **Everyone (public)** under sharing options, and click **Save**.

![][image42]

5. Click **Review sharing** to check the items whose sharing permissions will be updated accordingly.

![][image43]

6. Click **Update sharing** to confirm the changes.

![][image44]

7. Now, your map should be visible by the public.

## **Export Data** {#export-data}

For each layer created or added to a map project, you can export it as a shapefile to open in other GIS software or store on your local computer. In this tutorial, we will use the airport layer as an example.

1. Go to **Content**, then **My content**. Make sure the item you select is of the “Feature layer (hosted)” type \- otherwise, it will not support shapefile export.

![][image45]

2. Click on the ellipsis (3-dot) icon next to the item title, select **View details**. You can also do it by clicking on the item title.

![][image46]

3. Under the **Overview** tab, click **Export data** from the right pane.

![][image47]

4. Then, select **Export to shapefile** from the dropdown menu.

![][image48]

5. Name the new file as **China Airport Dataset**, add other details if needed, and click **Export**.

![][image49]

6. Once the export is complete, a new page will appear showing the file type as “Shapefile”. You can also find it under the **Content** tab.

![][image50]

7. Click **Download** on the right pane to save the file in your local computer.

![][image51]

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

![][image52]

2. Select **Tools**. Alternatively, click the tool icon in the header menu.

![][image53]

3. Under **Summarize data**, select **Join Features**.

![][image54]

4. Now, let’s configure our input and output. First, for the **Target layer**, select **China Province Boundaries** layer from the dropdown.

![][image55]

5. For the **Join layer**, select **China Airport Dataset** layer from the dropdown.

![][image56]

6. Under the **Join settings**, toggle on **Use spatial relationship**.

![][image57]

7. For the **Spatial relationship**, select **Completely contains** from the dropdown menu.

![][image58]

8. For the **Join operation**, select **Join one to one** from the dropdown menu.

![][image59]

9. Since we are analyzing the density of airports across provinces, we first need to calculate the number of airports in each province. Under the **Multiple matching records**, select **Calculate count only**.

![][image60]

10. For the **Join type**, make sure **Inner join** is highlighted.

![][image61]

11. Under the **Result layer**, give a name to the new layer in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: **Count of Airports in Provinces\_\[Your NetID\]**.

![][image62]

12. Click **Run** to start processing.

![][image63]

13. To check the progress, click on the history icon in the header menu.

![][image64]

14. Once the analysis is completed successfully, a new layer named **Count of airports in provinces** will appear in the **Layers** and the map. Let’s focus on this layer by hiding the other two layers and keep only the newly created one visible.

![][image65]

15. The new layer called **Count of airports in provinces** will show up in the **Layers** pane. When you click on a province polygon, the pop-up will display a new attribute called **Join\_Count**, followed by the total number of airports in the corresponding province.

![][image66]

16. Click the ellipsis (3-dot) icon next to **Count of airports in provinces** layer and select **Show table**. 

![][image67]

17. The data table attached to this layer will appear with two new attributes named **Join\_Count** and **Admin Name**. **Join\_Count** indicates the number of airports in each corresponding province, **Admin Name** represents the administrative region used in the spatial analysis.

![][image68]

### **Find by Attributes and Locations** {#find-by-attributes-and-locations}

Let’s move to the second question: What and where are the airports in Jiangsu Province?

To answer this, we can use the **Find by Attributes and Location** tool. This tool allows us to set specific query conditions (such as filtering by province name) to automatically extract only the airports that meet our criteria. Once applied, it will generate a subset of the data showing all airports located within Jiangsu.

1. Go to the Editing toolbar, click on **Analysis**.

![][image69]

2. Select **Tools**. Alternatively, click the tool icon in the header menu.

![][image70]

3. Under the **Find locations**, select **Find by Attributes and Location**.

![][image71]

4. Click on **\+ Build new query** under **Criteria**.

![][image72]

5. For **Find features from**, select **China Airport Dataset** layer from the dropdown, then select **Attribute expression**, click **Next**.

![][image73]

6. For **Where** fields, we will define the criteria. First, choose **All of the following are true**. Then, set **Province\_EN** as the field, select **equal** as the operator, and select or enter **Jiangsu** as the value. Once the condition is set, click **Add** to apply it.

![][image74]

7. Under the **Result layer**, give the new item a name in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: Airports in Jiangsu\_\[Your NetID\].

![][image75]

8. Click **Run** to start processing.

![][image76]

9. To check the progress, click on the history icon in the header menu.

![][image77]

10. Once the analysis is completed successfully, a new layer named **Airports in Jiangsu** will appear in the **Layers** and the map. Let’s focus on this layer by hiding the other layers and keep only the newly created one visible.

![][image78]

11. The map will update to show the new layer we just created, automatically zooming into Jiangsu province.

![][image79]

12. Click the ellipsis (3-dot) icon next to **Airports in Jiangsu** layer and select **Show table**. 

![][image80]

13. There should be 11 records in the table, meaning that there are 11 airports in Jiangsu province.

![][image81]

### **Find Closest** {#find-closest}

The third question we want to solve is: what are the 3 closest airports to DKU. To do that, we will first create a new layer with DKU campus’s location data.

1. Click on the **Search** tool in the Searching and Viewing toolbar.

![][image82]

2. Click **Use current location**, Or, enter **Kunshan, Jiangsu**, and select the first option from the dropdown. This will locate you to the Kunshan region on the map. Then, navigate to the Duke Kunshan University.

![][image83]

3. Go to **Add**, then select **Create sketch layer**.

![][image84]

4. Under the **Point feature** in the **Sketch** pane, name the new data point as **DKU**.

![][image85]

5. Make sure the stamp icon is selected in the sketch toolbar, and click on two random places in the campus area on the map.

![][image86]

6. We only need one data point actually, so let’s delete one of them. To do so, click **Select** (cursor icon) from the sketch toolbar. Then click on the point you want to delete, and click on **Delete** or hit **Backspace** on the keyboard.

![][image87]

7. Go to **Layers**, rename the sketch layer as **DKU campus**, and click **OK**.

![][image88]

8. Next, go to **Analysis**, select **Find Closest** under the **Use proximity**.

![][image89]

9. Select **DKU campus (Points)** as input layer, and **Airports in Jiangsu layer** as near layer.

![][image90]

10. For the **Analysis settings**, toggle on **Limit the number of closest locations**, and enter **3** as the max number of input. Make sure **Limited the search range** is toggled off.

![][image91]

11. Under the **Result layer**, give a name to the new layer in the **Output name** field, and select the designated folder to save the output. Note that the name should be unique across the organization no matter where you save the layer. Example: Closest airports to DKU\_\[Your NetID\].

![][image92]

12. Click **Run** to start processing.

![][image93]

13. To check the progress, click on the history icon in the header menu.

![][image94]

14. Once the analysis is completed successfully, a new layer set named **Closest airports to DKU** will appear in the **Layers** and the map. Let’s keep the rest of the layers invisible.

![][image95]

15. Click on the arrow icon next to **Closest airports to DKU** layer set, click on the ellipsis (3-dot) icon next to **Connecting Lines** and select **Show table**. 

![][image96]

16. The data table should display 3 records, along with two new attributes \- **Near Rank** and **FindExistingLocation** \- which indicate the airport names and their rankings by distance.

![][image97]

### **Extract Data** {#extract-data}

Lastly, the analysis tools allow exporting layers in CSV, file geodatabase, shapefile, and KML. Let’s say we want to export the data table attached to our closest airports to the DKU layer in a table csv format. We already know how to view the data table in the map view, but how to download that in a csv format?

1. Go to the Editing toolbar, click on **Analysis**.

![][image98]

2. Select **Tools**. Alternatively, click the tool icon in the header menu.

![][image99]

3. Under **Manage Data**, select **Extra Data**.

![][image100]

4. For **Input layers**, select **Closest airport to DKU \- Nearest Features** and **Closest airport to DKU \- Connecting Lines**. 

![][image101]

5. Under **Result layer,** select CSV as the output data format, name the new output as **Top 3 closest airports**, and select the designated folder to save the output.

![][image102]

6. Click **Run** to start processing.

![][image103]

7. Click on the history icon in the header menu to check the progress. Then, click on the ellipsis (3-dot) icon next to the processing record, and click **View details**. 

![][image104]

8. Click on the ellipsis (3-dot) icon next to **Top 3 closest airports**, then **Open item details**.

![][image105]

9. A new item page will open. Click on the **Download** button in the right pane to download and save the file in your local computer.

![][image106]

10. Open the **Nearest\_Features** file in Excel to view the ranked list of airports closest to the DKU campus. Note that Chinese text may not always export correctly.

![][image107]

## **Model Builder** {#model-builder}

While we just demonstrated how to answer multiple questions by running different analysis tools step by step, there is a way to streamline the entire process without executing each tool manually \- that’s **Model Builder**.

With **Model Builder**, instead of running each tool manually, you can build a workflow where outputs from one step feed directly into the next. This is especially useful when working with large datasets, performing multi-step analyses, or repeating the same workflow with different inputs.

In this demo, we will answer this question: which provinces in China have more than 10 airports?

1. Return to the map project view. If you can’t find it, go to the ArcGIS Online homepage and navigate to **Content** \> **My content**. Open the **Airport within province** web map item.

2. Click on **Analysis**.

![][image108]

3. Select **ModelBuilder**. Alternatively, click the Model Builder icon in the header menu.

![][image109]

4. Click **Connect** to continue.

![][image110]

5. Make sure the **Disconnect** button is showing up, then click **Create model**.

![][image111]

6. For the model, let’s call it **Provinces with over 10 airports**, then click **Save**.

![][image112]

7. In the new window, click on the **Add tools** icon.

![][image113]

8. Select 2 tools: **Join Features** and **Filter by Attributes**, then click **Add**. 

![][image114]

9. The tools will be added to the canvas and displayed in grey. Double-click on the **Join Features** box. 

![][image115]

10. In the pop-up, select **China Province Boundaries** as the target layer, and **China Airport Dataset** as the join layer.

![][image116]

11. Next, toggle on **Use spatial relationship** and select **Completely contains**. For the **Join operation**, choose **Join one to one**, and ensure that **Calculate count only** under the **Multiple matching records** option is selected.

![][image117]

12. For **Join type**, select **Inner join**. For the **Result type**, select **Create intermediate data** from the dropdown \- this means the output from this analysis tool will not be saved as a permanent layer. Click **Confirm**.

![][image118]

13. Now, the canvas should show two additional items in blue, representing the datasets we just configured. In addition, the tool box appears in yellow, and the output box appears in green.

![][image119]

14. Next, double-click on **Filter by Attributes**.

![][image120]

15. For the **Input dataset**, select **Join result**. 

![][image121]

16. Click on **\+ Build new query**.

![][image122]

17. Select **Expression** and click **Next**.

![][image123]

18. For **Where** fields, choose **All of the following are true** first. Then, set **Join Count** as the field, select **is greater than** as the operator, and select or enter **10** as the value. Once the condition is set, click **Add** to apply it.

![][image124]

19. For the result layer, make sure the **Create hosted layer** is selected under the **Result type**, then give a name to the new layer in the **Output name** field. Note that the name should be unique across the organization no matter where you save the layer. Example: Chinese provinces with over 10 airports\_\[Your NetID\].

![][image125]

20. In the canvas, all items are now connected in a workflow with arrows and color-coded accordingly. Click **Run** to execute the model.

![][image126]

21. Once the model runs successfully, a green check mark will appear on both the tool and output boxes. 

![][image127]

22. In the **Layers** pane, a new layer called **Chinese provinces with over 10 airports** will now appear.

![][image128]

23. Click the **Save** icon, then close the tab.

![][image129]

24. Under **Models in this map**, you will find the model we just saved. Click on \+its name to reopen it. You can swap in different datasets and run it again anytime to repeat the same analysis.

![][image130]

25. Remember to save the project manually.

# **Resources** {#resources}

ArcGIS Online offers a wide range of tools for visualizing and analyzing geospatial data, and this tutorial only covers some of them. You are encouraged to continue exploring and experimenting with the tool. For further learning, the following resources are recommended:

* [ArcGIS Online Resources](https://www.esri.com/en-us/arcgis/products/arcgis-online/resources) by Esri;  
* [Perform analysis in Map Viewer](https://learn.arcgis.com/en/paths/data-analysis/) by Esri;  
* ArcGIS Online [Tool Documentation](https://doc.arcgis.com/en/arcgis-online/analyze/aggregate-points-mv.htm)  
* [ArcGIS Online Community](https://community.esri.com/t5/arcgis-online/ct-p/arcgis-online) for browsing resources, sharing knowledge, and connecting with other users.

If you have any questions about the tool or this tutorial, don’t hesitate to reach out to the Data and Visualization Librarian, Siti Lei ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)) for further support.
