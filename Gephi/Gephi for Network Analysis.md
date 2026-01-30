# **Gephi for Network Analysis**

*Siti Lei*  
*Data and Visualization Librarian, Duke Kunshan University*

*Last updated: December 8, 2025*

This tutorial introduces the basics of network analysis and how to use Gephi to import and visualize data, apply different layouts, install and use plugins, and export the graphs. For demonstration, we will use a subset of character relationships from Sherlock Holmes stories.

[Before we start	](#before-we-start)

 - [Introduction	](#introduction)

 - [Glossary	](#glossary)

 - [About the tool	](#about-the-tool)

 - [Setup	](#setup)

 - [Datasets	](#datasets)

 - [Node Table	](#node-table)

 - [Edge Table	](#edge-table)

[Install Plugins	](#install-plugins)

[Import Network Data	](#import-network-data)

[Visualize Data	](#visualize-data)

 - [Left Toolbar	](#left-toolbar)

 - [Appearance	](#appearance)

 - [Bottom Toolbar	](#bottom-toolbar)

 - [Layout	](#layout)

[Filters & Statistics	](#filters--statistics)

 - [Filters	](#filters)

 - [Statistics	](#statistics)

[Export the Graph	](#export-the-graph)

 - [Capture the current view	](#capture-the-current-view)

 - [Save the graph	](#save-the-graph)

 - [Export as a website	](#export-as-a-website)

 - [Publish to GitHub	](#publish-to-github)

[Learning Resources	](#resources)

# Before we start

## Introduction

In this tutorial, you will learn the basic concepts of network analysis and how to use Gephi to create network graphs for qualitative research,from importing and visualizing data to installing plugins, applying different layouts, and exporting the final graphs. For demonstration purposes, we will use a subset of character relationships from the Sherlock Holmes stories.

To give you a sense of its wide applicability, network analysis can be used in many contexts, such as social relationships, communication patterns, transportation systems, biological interactions, or character connections in a story. Some project examples include [DKU’s Natural and Applied Sciences Research](https://dnas.dukekunshan.edu.cn/research/), [Map of the Interstate Highway System in the United States](https://wiki.aaroads.com/wiki/Interstate_Highway_System#/media/File:Map_of_current_Interstates.svg), and [Map of Scientific Paradigms](https://scimaps.org/map/2/9). 

For any questions about network analysis and Gephi, contact the Data and Visualization Librarian, Siti Lei ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)) for support. 

## Glossary

**Network analysis** is a method used to study how different items (**nodes**) and their connections (**edges**) form patterns and relationships. A network graph visually represents these connections, helping audiences understand how things are linked, how information or influence flows, and which nodes play important roles within a system.

**Nodes** (aka. actors, vertices, points, or entities) are individual items that participate in relationships or are connected to others in a network. They can represent many things, such as people, groups, organizations, locations, events, or concepts. Each node can also have additional information attached to it, such as a category, a location, or a size value.

**Edges** (aka. links, connections, ties, relations) refer to the relationships or interactions between nodes in a network. They show how two nodes are connected and can represent many types of relationships, such as communication or influence. Each edge can also include additional information, such as the type of relationship. Multiple edges between a pair of items is allowed.

**Link direction** in a network can be either **directed** or **undirected**. A **directed edge** shows a one-way relationship, such as an email sent or a citation from one paper to another. An **undirected edge** refers to a two-way or mutual relationship, such as friendship or co-authorship.

**Degree** refers to the number of edges connected to a node which shows how many direct relationships that node has within the network. A node with a high degree is more connected, while a node with a low degree has fewer connections. 

**Weight** refers to the strength, frequency, or importance of an edge between two nodes. A higher weight means the two nodes interact more often or have a stronger relationship. 

## About the tool

We will use Gephi, an open-source and free software compatible with Windows, Mac, and Linux devices, in this workshop. Visit [Gephi](https://gephi.org/about/) for more information about the tool. 

## Setup

Download [Gephi](https://gephi.org/desktop/) and complete the installation on your local computer.

## Datasets

Download the sample datasets: [Workshop\_Files.zip](https://duke.box.com/s/91jya5x407qpdql8w1mptu70zqb3h00i)

**Prepare Data**

In network analysis, it is recommended to have a node table and an edge table that complement each other. A node table lists all the individual elements in your network. An edge table describes how those nodes are connected.

## Node Table

Each row in the node table describes a single node and should include a node label. You can also add a unique identifier (such as the **ID** column shown in the example sheet below), which helps simplify the creation of the edge table. Additional relevant attributes can be added as needed.

Example:  
<img width="981" height="469" alt="image" src="https://github.com/user-attachments/assets/fb5b4b92-606b-48ed-af2e-cdd220967146" />


## **Edge Table** 

Each row describes a single edge between a **Source** and a **Target** node. If you assigned unique identifiers in the node table, you can use those identifiers as the **Source** and **Target** (see  the example sheet below). If not, you can use the node labels instead.

Example:  
<img width="978" height="433" alt="image" src="https://github.com/user-attachments/assets/3680c55d-7ab2-4098-b74c-7166c5828320" />


# **Install Plugins** 

Gephi provides a series of plugins that allows better experience and function in working with network analysis. Let’s try some of them in this tutorial.

1. Open **Gephi** on your computer. In the welcome popup, click on **New Project**.

<img width="975" height="540" alt="image" src="https://github.com/user-attachments/assets/17c955ad-9e20-4ec7-bf7f-8707c16f55f0" />


2. In the top menu, click on **Tools** then select **Plugins**. Note that you can also change the language in the **Tools** menu.

<img width="975" height="475" alt="image" src="https://github.com/user-attachments/assets/66f08a9a-7498-4a9d-9e36-cd4ae3462b06" />


3. Under **Available Plugins**, select **Publish your network to the web**, **SigmaExporter**, and **Circular Layout**. Then click **Install**.

<img width="975" height="598" alt="image" src="https://github.com/user-attachments/assets/bfca9c6f-5959-443a-a61f-a5f1d987382a" />


4. Click **Next**.

<img width="819" height="738" alt="image" src="https://github.com/user-attachments/assets/a76b70e5-d049-4b75-aac0-af32db9d2d77" />


5. Check **I accept the terms in all of the license agreements**, then click **Install**.

<img width="820" height="744" alt="image" src="https://github.com/user-attachments/assets/f8eb924e-3d16-49df-8352-32487fffa7b3" />


6. When finished, select **Restart Now**, then click **Finish**.

<img width="819" height="742" alt="image" src="https://github.com/user-attachments/assets/94cff951-4398-439c-a282-307f98cf6ac5" />


7. In the new pop-up, click on **Do not save for** now.

<img width="514" height="286" alt="image" src="https://github.com/user-attachments/assets/1e02a5a2-46ab-415a-bf55-0818a4ece5a7" />


8. Gephi will then relaunch on your computer. In the welcome window, click **New Project**.

<img width="975" height="540" alt="image" src="https://github.com/user-attachments/assets/c674ee69-ea99-41ba-9974-072a55f62f4a" />


9. Next, go to **Tools** in the top menu and select **Plugins**. Under the **Installed** tab, you will find **Publish your network to the web**, **SigmaExporter**, and **Circular Layout** listed.

<img width="975" height="600" alt="image" src="https://github.com/user-attachments/assets/3a03bb99-2864-4bf7-9f34-824bd1cfad0a" />


# **Import Network Data**

Gephi allows you to import network data from various file types, including CSV files, Excel sheets, and graph files such as GEXF, GML, and GraphML. In this tutorial, we will demonstrate how to import the nodes and edges tables in CSV file format. 

1. Go to the **File** tab, then select **Import spreadsheet** from the menu.

<img width="975" height="638" alt="image" src="https://github.com/user-attachments/assets/4bee3314-ede1-45fc-9836-cb5f985b99ce" />


2. Select the **nodes.csv** from the sample datasets downloaded in your computer, then click **Open**.

<img width="780" height="159" alt="image" src="https://github.com/user-attachments/assets/7ed5848f-2388-448d-a6ce-17c3aa709f60" />


3. Click **Next \>**.

<img width="975" height="621" alt="image" src="https://github.com/user-attachments/assets/f2f59646-461a-49cc-abcf-1c4d9f393ad4" />


4. Review the data type for each column, then click **Finish**.

<img width="975" height="625" alt="image" src="https://github.com/user-attachments/assets/0f776f2f-5dcc-4a41-825f-eb1567903b1a" />


5. Check **Append to existing workspace**, then click **OK**.

<img width="975" height="675" alt="image" src="https://github.com/user-attachments/assets/07b930b2-f763-4cde-961f-32889dcb4c49" />


6. A few dots will now appear on the canvas, with each dot representing a node. Note that the exact layout may differ, as the positioning of data is randomly assigned.

<img width="979" height="637" alt="image" src="https://github.com/user-attachments/assets/03b328c4-b078-440d-bbac-dc4f1124d3dc" />


7. Next, go to the **File** tab again, select **Import spreadsheet** from the menu.

<img width="975" height="652" alt="image" src="https://github.com/user-attachments/assets/b33ecf19-b0ba-405f-b7ff-8d617caef99c" />


8. Select the **edges.csv** from the sample datasets downloaded on your computer, then click **Open**.

<img width="792" height="161" alt="image" src="https://github.com/user-attachments/assets/2c2c956b-ea2f-4702-a42c-66e0cd48a1ad" />


9. Click **Next \>**.

<img width="975" height="627" alt="image" src="https://github.com/user-attachments/assets/d0f53007-3741-4ba3-a22d-cb1fd21e6aca" />


10. Review the data type for each column, then click **Finish**.

<img width="975" height="625" alt="image" src="https://github.com/user-attachments/assets/f489021a-efa7-49a9-8dd6-034602fdd4e3" />


11. Check **Append to existing workspace**, then click **OK**.

<img width="975" height="677" alt="image" src="https://github.com/user-attachments/assets/cbd6ae86-a4e1-4fb5-9a69-3053d01b6d2d" />


12. Now, few connection lines will show up connecting each dot in the canvas. Each line represents one edge. Note that the exact layout may differ, as the positioning of data is randomly assigned.

<img width="979" height="639" alt="image" src="https://github.com/user-attachments/assets/e5c82f0d-a5e8-4b07-abd4-4bf78449520d" />


13. Click the arrow on the right side of the bottom panel.

<img width="951" height="146" alt="image" src="https://github.com/user-attachments/assets/bf5577b5-e072-4f06-a1f2-6b6e569ad446" />


14. Drag the scale bar under **Zoom** to zoom in and view more detail. You can also use your mouse wheel to zoom. Note that you can also change the background color here.

<img width="975" height="692" alt="image" src="https://github.com/user-attachments/assets/65758779-5612-436e-aa13-f3d186947c53" />


15. Click the arrow on the right side of the bottom panel again to hide it.

<img width="895" height="235" alt="image" src="https://github.com/user-attachments/assets/10a5a480-9e51-4437-b2ff-dad484807f66" />


16. To reset the view, click on the **Center on graph** icon on the left-bottom toolbar. 

<img width="979" height="481" alt="image" src="https://github.com/user-attachments/assets/b1aa3075-c05b-4117-b898-513144655c85" />


# **Visualize Data** 

In Gephi, you can customize the visual appearance of your network by adjusting the nodes, edges, background, and layout positions using a variety of built-in and plugin tools.

## **Left Toolbar** 

1. The left toolbar provides editing tools for modifying the visuals of the nodes and edges in the graph. We will only cover some of the tools here, but it is encouraging to explore and try them on your own after the tutorial.

<img width="472" height="509" alt="image" src="https://github.com/user-attachments/assets/e7d7ce47-5b58-4678-be09-ec7be4c4dfa8" />


2. Click on the **Rectangle selection** icon on the left toolbar. 

<img width="73" height="159" alt="image" src="https://github.com/user-attachments/assets/1bce6506-7974-4a9a-8550-a5c2439029c8" />


3. Click and drag to draw a square that selects all the imported items.

<img width="979" height="667" alt="image" src="https://github.com/user-attachments/assets/fc679c9d-4508-4bc0-bb24-91cdfd4db909" />


4. Select the Size icon in the toolbar.

<img width="76" height="250" alt="image" src="https://github.com/user-attachments/assets/c14e3876-0638-401f-86ed-5e91f6dabac7" />


5. Click anywhere on the canvas, then drag the mouse vertically to adjust the node size. Click again to confirm the change. The updated size value will appear in the top-right corner.

<img width="975" height="665" alt="image" src="https://github.com/user-attachments/assets/27553b86-829d-46e4-85da-939a2a02ba7b" />


6. Now, select the **Direct selection** icon and **Painter** icon in the toolbar. 

<img width="73" height="308" alt="image" src="https://github.com/user-attachments/assets/feae4ec4-7808-4890-aa12-fe9239a8c646" />


7. Click on any node to apply a color to it.

<img width="975" height="663" alt="image" src="https://github.com/user-attachments/assets/7825b4e4-e368-43ac-b72d-713ec51969b4" />


8. Double-click the same node to intensify the color. Each additional click makes the color more vibrant.

<img width="975" height="663" alt="image" src="https://github.com/user-attachments/assets/71af8f0c-690f-4988-8b25-53f3d7a7b93e" />


9. Move the cursor away. The selected node and all edges directed toward it will now be highlighted in color.

<img width="975" height="665" alt="image" src="https://github.com/user-attachments/assets/e002b921-c8fa-4f55-99c9-37363baa4d8b" />


10. Click on the Reset color icon at the bottom of the toolbar. This will reset the color setting.

<img width="97" height="254" alt="image" src="https://github.com/user-attachments/assets/fcb72a58-c679-4d90-ac2b-7bd12ae5c38e" />


11. Next, select the **Brush** icon and switch the color to green. Then click a node to apply the color. This will color the selected node, all connected nodes, and the edges between them.

<img width="975" height="665" alt="image" src="https://github.com/user-attachments/assets/f0dac57b-05e9-472d-ae34-27a1e6cfbd94" />


12. To reset the color setting, click on the **Reset colors** icon in the left-bottom toolbar.

<img width="979" height="481" alt="image" src="https://github.com/user-attachments/assets/cd89d3ef-dd15-4162-8821-9b2eb2ef95b0" />


## **Appearance** 

1. As default, the **Appearance** window appears in the top left of the workplace.

<img width="975" height="477" alt="image" src="https://github.com/user-attachments/assets/c7328082-38d1-4ec8-acf4-ab2dbaf2ed93" />


2. If you don’t have that open, go to the **Window** tab, then select **Appearance**. The **Appearance** window should appear in the workplace again. You can also select **Reset Windows** to go back to the default view.

<img width="331" height="646" alt="image" src="https://github.com/user-attachments/assets/339009af-7c58-49cd-9e5d-bb01b941d69a" />


3. In the Appearance window, select **Nodes**, then **Partition**, choose the role types as the attribute.

<img width="376" height="657" alt="image" src="https://github.com/user-attachments/assets/3415fadb-bc3a-4cee-aa2c-be65c213b035" />


4. The system will automatically assign colors to different values. To adjust a single color, click the color block and choose a new color from the pop-up.

<img width="695" height="709" alt="image" src="https://github.com/user-attachments/assets/166afd19-91e6-4469-86f4-c1e2bcd3113e" />


5. Alternatively, you can click **Palette…** in the bottom-right corner and select a new color scale from the list.

<img width="376" height="312" alt="image" src="https://github.com/user-attachments/assets/f421ebf2-6cc2-4b10-9a2f-365fe6da97d5" />


6. Once the color selection is complete, click **Apply**. The nodes on the canvas should now be colored.

<img width="374" height="660" alt="image" src="https://github.com/user-attachments/assets/001b4f10-bb99-4fab-b7be-f27e920b76a1" />


7. Now, let’s switch to the **Size** tab, then **Ranking**, select **Degree** as the attribute. 

<img width="374" height="359" alt="image" src="https://github.com/user-attachments/assets/13b63a96-3000-4a98-9fde-01eb5129ac81" />


8. Set the minimal size to **20**, and maximal size to **60**. Then, click **Apply**.

<img width="367" height="656" alt="image" src="https://github.com/user-attachments/assets/be93b4f6-e6f3-4d68-a00f-20b37d90cf08" />


9. The graph should now appear similar to the example below. Note that the exact layout may differ, as the positioning of nodes and edges is randomly assigned.

<img width="975" height="633" alt="image" src="https://github.com/user-attachments/assets/669d6907-107c-4b84-b235-9327eff58d8e" />


10. Now, switch to the **Ranking** tab, and select **Degree** as the attribute.

<img width="374" height="326" alt="image" src="https://github.com/user-attachments/assets/8949a26d-53ee-4c3e-8764-a22d184e0cd0" />


11. Click on the link icon next to the **Apply** button \- this will enable the auto apply feature.

<img width="371" height="102" alt="image" src="https://github.com/user-attachments/assets/ac9fd2b1-223d-42bc-862c-9e43595d2b7e" />


12. Click on **Auto Apply**. 

<img width="374" height="101" alt="image" src="https://github.com/user-attachments/assets/3445dd11-bf10-4055-ae60-a38b113bfd3e" />


13. Double-click the arrows to adjust the colors, then click **OK** to confirm the changes. 

<img width="705" height="759" alt="image" src="https://github.com/user-attachments/assets/90ee92ce-219f-46a8-b4a9-7335961093cf" />


14. The nodes should update their colors automatically. You can delete an arrow by selecting it and dragging it downward, or add a new arrow by clicking anywhere along the bar.

<img width="979" height="544" alt="image" src="https://github.com/user-attachments/assets/dc6f2dc9-065f-4a7a-9801-8d2e98dbb87d" />


15. Next, we will configure and categorize the edges based on the relationship type, which is the **Label** field in our dataset. In the **Appearance** window, switch to **Edges**, then select **Partition**, and click the arrow to expand the attribute list.

<img width="371" height="281" alt="image" src="https://github.com/user-attachments/assets/e44e6209-21e7-46c7-b677-fd281c2fe9cd" />


16. You will notice that **Label** is not in the list. This is because we did not set its data type during import (see Step 11 in **Import Data**). To correct this, we need to assign the appropriate data type to the column. Switch to the **Data Laboratory** view, where all imported datasets are displayed.

<img width="979" height="639" alt="image" src="https://github.com/user-attachments/assets/c532cc6d-be4e-4f62-8101-d286c633abd7" />


17. In the top-left corner, click **Edges** to switch to the edges data.

<img width="257" height="138" alt="image" src="https://github.com/user-attachments/assets/9b78e865-c3eb-43f5-a9cf-44b93609ceab" />


18. In the button toolbar, click on the **Duplicate column**, then select **Label**.

<img width="692" height="257" alt="image" src="https://github.com/user-attachments/assets/8d8608d8-7ac3-46db-a968-36eb5a146e45" />


19. In the pop-up, enter a new name for the column and set the type to **String**, then click **Ok**.

<img width="501" height="332" alt="image" src="https://github.com/user-attachments/assets/12a7baeb-41d6-4093-95e3-8f82d25b039d" />


20. A new column **Label\_copy** now appears. You may delete the original **Label** column, but we will leave it in this tutorial.

<img width="979" height="355" alt="image" src="https://github.com/user-attachments/assets/446fb8bf-353f-4f03-8de5-ee047cbcb67d" />


21. Go back to the **Overview** tab. In the **Appearance** window, select **Edges** \> **Partition**, then choose **Label\_copy** as the attribute from the dropdown menu.

<img width="548" height="357" alt="image" src="https://github.com/user-attachments/assets/5bb03113-2a62-4473-8cdd-8a8e585cfb8e" />


22. Confirm the color setting, then click **Apply**.

<img width="345" height="624" alt="image" src="https://github.com/user-attachments/assets/7856c2ca-6283-4493-9e48-fe48c5096b12" />


23. The graph now displays edges in different colors representing different relationship categories. Thicker lines indicate higher weights.

<img width="979" height="623" alt="image" src="https://github.com/user-attachments/assets/a6d0cac0-00c5-45b3-9416-1badc78cf15a" />


## **Bottom Toolbar**

1. The bottom toolbar provides annotating tools for adding or deleting elements, such as the label and edges to the graph. We will only cover some of the tools here, but it is encouraging to explore and try them on your own after the tutorial.

<img width="917" height="76" alt="image" src="https://github.com/user-attachments/assets/6d98bd79-90c6-4693-8e76-3f18d82508ea" />


2. First, the **Background color** icon (the lightbulb symbol) allows you to switch the background from bright white to dark black.

<img width="834" height="484" alt="image" src="https://github.com/user-attachments/assets/2ad8a6cf-b60a-4bd5-82d4-2dc840ab70ac" />


3. Click on the **Attributes** icon in the toolbar.

<img width="345" height="104" alt="image" src="https://github.com/user-attachments/assets/c9fa2021-77b5-4c0e-9d88-97370649a079" />


4. For the nodes, select **name** as the attributes, then click **OK**.

<img width="523" height="535" alt="image" src="https://github.com/user-attachments/assets/03151390-a240-4696-be0e-909a607e95d7" />


5. Next, click on the **Show Node Labels** icon.

<img width="356" height="110" alt="image" src="https://github.com/user-attachments/assets/b8c0452e-cfd1-4f54-9b87-5ab6466072e9" />


6. You will notice that the labels appear too large in the graph, but we can adjust them. To do so, click on the font settings (**Arial Bold, 32**) or drag the scale bar next to it to change the label size.

<img width="818" height="324" alt="image" src="https://github.com/user-attachments/assets/d04f128c-48b3-462d-b42d-164c91115c53" />


7. If you click on the font settings (**Arial Bold, 32**), you can change the font, style, and size of the labels there. Let’s set the size to **10**, then click **OK**.

<img width="663" height="640" alt="image" src="https://github.com/user-attachments/assets/b7d3f859-32ef-4767-82e3-34a35845ec8f" />


8. You can also use the **Size mode** or **Color mode** icons to control how the label size and color adjust based on the placement and size of the nodes.

<img width="223" height="109" alt="image" src="https://github.com/user-attachments/assets/042e3485-19e3-468c-a5c1-e6afdc55893c" />


## **Layout** 

1. As default, the **Layout** window appears in the bottom left of the workplace. We will only cover some of the tools here, but it is encouraging to explore and try them on your own after the tutorial.

<img width="979" height="483" alt="image" src="https://github.com/user-attachments/assets/7d6ed3e5-282c-4ca5-b65d-9a01cd57881e" />


2. Click on the arrow to expand the menu, select **Circular Layout**. 

<img width="524" height="685" alt="image" src="https://github.com/user-attachments/assets/2d42d29d-2649-4345-b35b-a9b2c42abbff" />


3. Let’s say we want the nodes arranged alphabetically by the characters’ names, we can set **Order Nodes by (decreasing)** to the **name (Attribute)**. 

<img width="521" height="679" alt="image" src="https://github.com/user-attachments/assets/5f23c457-ab7a-4c89-b17f-a29ff095de6b" />


4. Click **Run**. 

<img width="521" height="679" alt="image" src="https://github.com/user-attachments/assets/fe1ac899-85bd-47e0-a3d8-cff7206538cb" />


5. Now the nodes should be arranged in a circle, with the edges displayed within the circular arrangement.

<img width="979" height="764" alt="image" src="https://github.com/user-attachments/assets/d322dad0-1615-4086-8b56-504bf3284803" />


6. However, some labels may now overlap. To refine this, we can try another layout tool. Go to the **Layout** window, click the arrow to expand the menu, and select **Label Adjust**.

<img width="515" height="687" alt="image" src="https://github.com/user-attachments/assets/7f049428-a3d5-4d52-a7d1-75fa6954f571" />


7. Click **Run**. 

<img width="517" height="673" alt="image" src="https://github.com/user-attachments/assets/fae355b4-9926-45fe-aa3d-4da563b4e4ae" />


8. The labels will now adjust to clearer positions, creating better spacing and improving readability.

<img width="979" height="762" alt="image" src="https://github.com/user-attachments/assets/0991b6ca-fc21-46bf-ba7f-447f68def84b" />


9. Now the graph looks a bit squeezed. Let’s say we want to expand it, so go back to the **Layout** window, click the arrow to expand the menu, then select **Expansion**.

<img width="520" height="765" alt="image" src="https://github.com/user-attachments/assets/1db57d27-92bf-43c5-9ec0-e612800d02f8" />


10. Click **Run** once (or multiple times) to expand the layout and reduce the squeezed appearance.

<img width="520" height="756" alt="image" src="https://github.com/user-attachments/assets/28f3202c-02cd-4924-90c8-53d0310a2b6b" />


11. The graph now has a better spatial arrangement and is no longer squeezed.

<img width="975" height="706" alt="image" src="https://github.com/user-attachments/assets/4272463a-2de0-4755-b702-8e0f00a28b95" />

12. The graph returns to the default state after clicking on the button.

<img width="958" height="747" alt="Frame 54" src="https://github.com/user-attachments/assets/652e3419-310d-424b-8ef6-7ec6876bf54e" />


# **Filters & Statistics** 

Gephi provides filtering and statistical tools that allow you to narrow down the data for closer examination and perform statistical calculations on the imported dataset. The **Filters & Statistics** window is located at the bottom right of the workspace.  

<img width="975" height="479" alt="image" src="https://github.com/user-attachments/assets/e223a343-895e-49ae-9a62-090dd00272d5" />

## **Filters** 

1. Let’s say we want to look only at the network between protagonists and supporting characters instead of all role types. We can use the filtering tools to build a query to isolate and visualize just these connections. Go to **Filters** \> **Attributes** \> **Partition** \> **role type (Node)**.

<img width="588" height="560" alt="image" src="https://github.com/user-attachments/assets/c5824af7-333e-482c-9e84-6eb11b60d23a" />


2. Double-click on **role type (Node)**, then select **Supporting character (23.53%)** and **Protagonist (11.76%)**.

<img width="585" height="437" alt="image" src="https://github.com/user-attachments/assets/52ff08c3-8d1e-4578-9ba7-b495848edf83" />


3. Next, click on the **Select** button.

<img width="584" height="437" alt="image" src="https://github.com/user-attachments/assets/acd3f05f-f224-4577-867f-f7c03b9240e0" />


4. The selected roles will be highlighted, while the unselected ones will appear faded in the background.

<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/327af1db-ec8a-4470-934f-10e407f576a2" />


5. Next, let’s try out the **Filter** button.

<img width="584" height="437" alt="image" src="https://github.com/user-attachments/assets/c38a9198-156d-4316-acb4-af27b231378b" />


6. Only the selected roles will now remain visible in the workspace. 

<img width="979" height="581" alt="image" src="https://github.com/user-attachments/assets/988460a0-69fa-44ed-9200-7b10a6d52b69" />


7. Click **Stop** to return to the original, unfiltered graph.

<img width="582" height="363" alt="image" src="https://github.com/user-attachments/assets/2c09fcd8-5d07-4237-bae6-f44c11935bc4" />


## **Statistics**

Gephi includes a range of built-in statistical tools that help you analyze the structure and characteristics of your network. The results can be visualized directly within the interface or exported for further analysis. We won’t cover all tools here, but it is encouraging to explore and try them on your own after the tutorial.

1. Let’s say we want to analyze the network’s average degree. First, navigate to the **Statistics** tab in the bottom-right **Filters & Statistics** window. 

<img width="975" height="475" alt="image" src="https://github.com/user-attachments/assets/31159a21-def0-4d22-a797-3a443c4cdba1" />


2. Then, click **Run** next to **Average Degree**.

<img width="590" height="487" alt="image" src="https://github.com/user-attachments/assets/1fc95b18-ae3e-4b56-87fb-2b56a651eb50" />


3. A pop-up window will appear displaying a line graph of the degree distribution.

<img width="979" height="846" alt="image" src="https://github.com/user-attachments/assets/ba465657-7e95-4fb5-bc81-8ca182d98c5e" />


4. You can print, copy, or save the results from the pop-up window. Click **Close** when you’re finished.

<img width="638" height="69" alt="image" src="https://github.com/user-attachments/assets/b681bffd-b0a3-4c1c-a457-b83f1bf354ad" />


# **Export the Graph** 

There are multiple ways to export a project from Gephi. You can export the graph as static image files (e.g.,PNG, SVG, PDF) for use in reports or presentations, or generate an interactive dashboard that allows users to explore the network online.

## **Capture the current view**

1. Click on the **Take screenshot** icon (the camera symbol), then go **Configure**.

<img width="296" height="123" alt="image" src="https://github.com/user-attachments/assets/4754e767-8481-4337-b65c-33724aca3062" />


2. Configure the saving settings, such as adjusting the export size, enabling the **Transparent Background** option, and selecting a directory for **Autosave**. Once complete, click **Ok**.

<img width="398" height="426" alt="image" src="https://github.com/user-attachments/assets/a615eae5-887f-43e3-a4e4-c0241b3121e3" />


3. Go back to the toolbar and click on the **Take screenshot** icon (the camera symbol) again.

<img width="257" height="109" alt="image" src="https://github.com/user-attachments/assets/878768c5-9b58-4910-b1b3-e1e96ee0b8ef" />


4. Go to the directory where saved as the saving path, you will find the image exported

<img width="459" height="193" alt="image" src="https://github.com/user-attachments/assets/b3944375-ada4-45cf-a020-d9f6a0e0ce8a" />


## **Save the graph** 

1. Go to **Preview** view first. 

<img width="874" height="246" alt="image" src="https://github.com/user-attachments/assets/10531746-02b7-42f7-8f4f-050eb21ba4d0" />


2. Now you will see the graph has no label or colored edges we previously set. This is because some settings have not been applied, and we can configure those using the **Preview Settings** pane. 

<img width="979" height="489" alt="image" src="https://github.com/user-attachments/assets/c67cfe5a-f1f2-4b3c-9c14-53c7303fe408" />


3. For example, let’s check **Show Labels**, and change the **Font** size to **3** and click **OK**.

<img width="979" height="514" alt="image" src="https://github.com/user-attachments/assets/6f88858f-694f-4671-b07a-17f638b23c25" />


4. Click the **Refresh** button at the bottom. 

<img width="515" height="118" alt="image" src="https://github.com/user-attachments/assets/4397fd3d-5ff7-42a8-9f2f-bd22c46188a6" />


5. The graph is now updated with the characters’ names displayed as labels.

<img width="979" height="585" alt="image" src="https://github.com/user-attachments/assets/921108e1-dba6-4df3-ae01-e49a269c3da7" />


6. Next, we will change the color of the edges. Under **Edges**, in the **Color** field, click the ellipsis (3-dot icon) next to **mixed**.

<img width="506" height="307" alt="image" src="https://github.com/user-attachments/assets/d47105c1-443c-4fe8-b35a-a846627df459" />


7. In the pop-up, check **Original**, then click **OK**.

<img width="822" height="414" alt="image" src="https://github.com/user-attachments/assets/9f8e6f0f-4aee-4311-bee4-61d380bb5093" />


8. Click the **Refresh** button at the bottom again. 

<img width="515" height="118" alt="image" src="https://github.com/user-attachments/assets/54c51f87-b851-4057-b70a-57ef7a23e08a" />


9. Now we have essentially recreated the visualization from the **Overview** tab, even though it may not be an exact match. The preview graph is ready to be exported. To export it, click the **SVG/PDF/PNG** button next to **Export** at the bottom of the **Preview Settings** pane.

<img width="506" height="118" alt="image" src="https://github.com/user-attachments/assets/78542ca8-0eb5-4393-93ab-ca9078ed26a9" />


10. In the pop-up window, choose the save location, enter a file name, and select the desired format. Then click **Save**.

<img width="794" height="596" alt="image" src="https://github.com/user-attachments/assets/77737222-2d14-44ee-98d2-5f45f05c6533" />


11. The file should now be saved in the designated location.

<img width="834" height="343" alt="image" src="https://github.com/user-attachments/assets/342bf1d0-afba-48b3-98a9-92ba31343f77" />


## **Export as a website** 

1. In the workspace, go to **File** \> **Export** \> **Sigma.js.template**.

<img width="568" height="621" alt="image" src="https://github.com/user-attachments/assets/c7d4fbb6-fa95-4c63-948f-df664033ef5d" />


2. In the pop-up window, set the saving path and fill in the details you want to include about the nodes, edges, colors, author, and the graph title. Next, complete the short and long descriptions, and then click **OK**.  
3. Now, go to the folder where we just saved the file \- this will be a folder called **network**.  
4. Open network folder, you should find a HTML file titled **index**. Double-click to open it in your browser.  
5. Unfortunately, if you try to open the newly exported index.html file directly, it will not display correctly. This happens because modern web browsers block local HTML files from running JavaScript. There are several ways to work around this, but in this tutorial we will introduce two options. Let’s begin with the first one.  
6. Install a free software package called [Visual Studio Code](https://code.visualstudio.com/).  
7. Start it up on your computer.  
8. In the left toolbar, go to **Extension**, and search for **Live Server** and install it.  
9. Next, go to **File** \> **Open Folder** and select the **network** folder that contains the **index.html** file, click **Open** to continue.  
10. Once the files are imported, right-click **index.html** in the folder pane and select **Open with Live Server**.  
11. This should open up the file in your default browser, and you should be able to view it and interact with it.  
12. Note that this link cannot be shared with others because it runs locally on your machine and is not hosted on the internet. To create a shareable version, consider using the **Publish to GitHub** option in the next section.

## **Publish to GitHub** 

1. In the workspace, go to **File** \> **Export** \> **Publish to the web**.

<img width="507" height="613" alt="image" src="https://github.com/user-attachments/assets/600f1bc9-731f-413a-8b9b-370159c49ba8" />


2. First, complete the steps under the **Set up (to do just once)** tab.   
3. Next, go to the **Publish** tab and click **Publish your network to the web\!**  
4. Then, under **Link to the network visualization**, click **Open in web browser**. You may also copy and paste the link into any browser.  
5. Your project is now hosted on the Retina platform, where you can interact with the graph, adjust visual settings, and download the dataset.  
6. Most importantly, you can now share your network using the URL or use the embed code to display the graph as an asset on other websites.

# **Resources** 

## **Network Analysis Theory**

* [*Networks, crowds, and markets : reasoning about a highly connected world*](https://dukekunshan.userservices.exlibrisgroup.com.cn/discovery/openurl?institution=86DKU_INST&rfr_id=info:sid%2Fsummon&rft_dat=ie%3D5174659060008931,ie%3D217708680008931,language%3DEN&svc_dat=CTO&u.ignore_date_coverage=true&vid=86DKU_INST:Services&Force_direct=false) by David Easley and Jon Kleinberg  
* [*Visual Insights: A Practical Guide to Making Sense of Data*](https://dukekunshan.userservices.exlibrisgroup.com.cn/discovery/openurl?institution=86DKU_INST&rfr_id=info:sid%2Fsummon&rft_dat=ie%3D21119927750008931,ie%3D51123384730008931,language%3DEN&svc_dat=CTO&u.ignore_date_coverage=true&vid=86DKU_INST:Services) by Katy Börner and David E. Polley  
* [*Network data mining and analysis*](https://dukekunshan.userservices.exlibrisgroup.com.cn/discovery/openurl?institution=86DKU_INST&rfr_id=info:sid%2Fsummon&rft_dat=ie%3D217621590008931,language%3DEN&svc_dat=CTO&u.ignore_date_coverage=true&vid=86DKU_INST:Services&Force_direct=false) by Ming Gao, Ee-Peng Lim, David Lo  
* [*Fundamentals of big data : network analysis for research and industry*](https://dukekunshan.userservices.exlibrisgroup.com.cn/discovery/openurl?institution=86DKU_INST&rfr_id=info:sid%2Fsummon&rft_dat=ie%3D5182638120008931,language%3DEN&svc_dat=CTO&u.ignore_date_coverage=true&vid=86DKU_INST:Services) by Hyunjoung Lee and Il Sohn

## **Gephi**

* [Gephi Quickstart](https://gephi.org/quickstart/)  
* [Gephi Documentation](https://docs.gephi.org/desktop/)  
* [Workshops](https://seinecle.github.io/gephi-tutorials/generated-html/using-filters-en.html) by Clément Levallois

## **Network Data Preparation**

* [Preparing Data 1: Making an Edge List](https://github.com/miriamposner/cytoscape_tutorials/blob/master/preparing-data-1-making-an-edge-list.md)  
* [Preparing Data 2: Making a Node List from an Edge List](https://github.com/miriamposner/cytoscape_tutorials/blob/master/preparing-data-2-making-a-node-list-from-an-edge-list.md)

## **Network Datasets**

* [Duke Network Analysis Center](https://sites.duke.edu/dnac/resources/datasets/)  
* [Index of Complex Networks](https://icon.colorado.edu/#!/networks)  
* [UCIrvine Network Data Repository](https://networkdata.ics.uci.edu/)  
* [Stanford Large Network Dataset Collection](https://snap.stanford.edu/data/index.html)  
* [UCINET Datasets](https://sites.google.com/site/ucinetsoftware/datasets)  
* [Network Datasets](http://networkrepository.com/networks.php)





