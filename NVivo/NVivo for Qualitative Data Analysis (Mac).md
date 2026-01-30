# **NVivo for Qualitative Data Analysis (Mac)**

*Siti Lei*  
*Data and Visualization Librarian, Duke Kunshan University*

*Last updated: November 13, 2025*

This 1.5-hour tutorial introduces how to conduct qualitative data analysis using a tool called NVivo in Mac devices, starting from importing qualitative data files, coding, running queries, to analyzing and visualizing codes. We will use a selection of text and image files from the project Data Center Energy Efficiency Focus Groups and Interviews (by U.S. Environmental Protection Agency) and the sample project in NVivo in this tutorial for demonstration. 

**[Before we start	](#before-we-start)**

 - [Introduction	](#introduction)

 - [About the tool	](#about-the-tool)

 - [Setup	](#setup)

 - [Datasets	](#datasets)

**[Before we started	](#before-we-started)**

**[Create a Project	](#create-a-project)**

**[Import Files	](#import-files)**

 - [Files	](#files)

 - [NCapture	](#ncapture)

**[Text Coding	](#text-coding)**

 - [Deductive Coding	](#deductive-coding)

 - [Inductive Coding	](#inductive-coding)

 - [Mixed Coding	](#mixed-coding)

 - [Parent & Child Code	](#parent--child-code)

 - [Uncoding	](#uncoding)

**[Highlighter & Coding Stripes	](#highlighter--coding-stripes)**

**[Memos & Annotation	](#memos--annotation)**

**[Image Coding	](#image-coding)**

**[Save the Project	](#save-the-project)**

**[Audio & Video Coding	](#audio--video-coding)**

**[Case Classification & Cases	](#case-classification--cases)**

**[Query	](#query)**

 - [Word Frequency Query	](#word-frequency-query)

 - [Text Search Query	](#text-search-query)

 - [Matrix Coding Query	](#matrix-coding-query)

**[Export Codes	](#export-codes)**

 - [Code List	](#code-list)

 - [Codebook	](#codebook)

 - [Individual Code	](#individual-code)

**[Resources	](#resources)**

# Before we start

## Introduction

This tutorial is designed for the Mac version of NVivo 14\. If you are using a Windows device, check out [the Windows tutorial here](https://docs.google.com/document/d/1esYrHgOCILlQWpgB5S-ImPCj6XCOwmn4pq6RiV3tD3E/edit?usp=sharing). 

While Lumivero, the company who produces NVivo, has released both Mac and Windows versions, the Mac version currently includes fewer features than the Windows version. Therefore, it is recommended to use a Windows device for working with NVivo. To learn more about the differences between versions and platforms, see the comparison page [here](https://techcenter.qsrinternational.com/Content/nv12/TOC_older_client_versions.htm).

If you don’t have a Windows device, the computers in the Digital Hub in the 4th floor of the DKU Library have installed NVivo 14 (see [Public Devices](https://library.dukekunshan.edu.cn/public-devices/)). 

In the first half of the tutorial, we will work with open datasets(files) from the project [Data Center Energy Efficiency Focus Groups and Interviews](https://catalog.data.gov/dataset/data-center-energy-efficiency-focus-groups-and-interviews), conducted by U.S. Environmental Protection Agency. The raw data was collected between October 2014 and June 2015\. 

For the second half of the tutorial, we will use the sample project in NVivo. Data in this sample project is drawn from a two-year research study (2008-2009) undertaken by researchers from the Duke University Nicholas School of the Environment at the Duke Marine Laboratory in Beaufort, N.C. The study documented community perceptions of development and land-use change on coastal communities in the Down East area of Carteret County, North Carolina, USA.

By the end of this tutorial, you will understand how NVivo can be used in qualitative research​, and use NVivo to load information, code documents and media files, use cases, make notes, conduct queries, and export information.

For questions about the NVivo 14, contact the Data and Visualization Librarian, Siti Lei ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)) for support.

## About the tool

We will use NVivo 14 in this tutorial. Visit the [Qualitative Data Analysis guide](https://library.dukekunshan.edu.cn/qualitative-data-analysis/) for more information about NVivo.

## Setup

Follow the instructions in [Downloading, Installing and Licensing NVivo 14](https://library.dukekunshan.edu.cn/qualitative-data-analysis/) to download, install and activate NVivo 14 Mac version on your computer.

## Datasets

Download the sample datasets below:

* [Workshop\_Files.zip](https://duke.box.com/s/91jya5x407qpdql8w1mptu70zqb3h00i)

# Before we started

1. Create a new folder in your computer and name it as **NVivo Workshop**. We will be using this folder to store all the files created in this tutorial.

<img width="223" height="205" alt="image" src="https://github.com/user-attachments/assets/0bfb412c-770a-4311-92d4-6bb995e33ada" />


2. Download the sample dataset [Workshop\_Files.zip](https://duke.box.com/s/91jya5x407qpdql8w1mptu70zqb3h00i).

3. Go to the place where the dataset is saved, right-click on the zip file and select **Quick Look “Workshop\_Files.zip”**.

<img width="828" height="501" alt="image" src="https://github.com/user-attachments/assets/dc2412d6-38f7-4ba2-93c0-2de0c43dad1b" />


4. Click on **Uncompress**.

<img width="723" height="413" alt="image" src="https://github.com/user-attachments/assets/c276600b-1962-403d-ba17-1413505704f2" />


5. Copy or move the unzipped **Workshop\_Files** folder into the **NVivo Workshop** folder. 

<img width="1017" height="322" alt="image" src="https://github.com/user-attachments/assets/bca30b4f-57b1-43c0-b374-825f29f17a91" />


# Create a Project

NVivo projects are saved **locally** on your computer. They are not automatically stored or synced to any cloud space, so remember to back up your files regularly.

1. Go to Launchpad and find NVivo 14\. Double click on the icon to open NVivo 14\.

<img width="410" height="198" alt="image" src="https://github.com/user-attachments/assets/cd083817-cb4d-4634-af04-f262e658da3f" />


2. A launch window will appear. Click **Create New Project**.

<img width="981" height="587" alt="image" src="https://github.com/user-attachments/assets/0bcf616f-e760-45f9-a34e-3d0199bf101b" />


3. If the window does not appear automatically, hover over the top toolbar. When the menu appears, click **File**, then **New Project**.

<img width="624" height="554" alt="image" src="https://github.com/user-attachments/assets/a9565823-69a9-4565-a70c-a2b894f945b4" />


4. In the pop-up window, enter **NVivo Workshop** in the “Save As” field, and make sure that the workshop folder is selected as the save location.

<img width="937" height="315" alt="image" src="https://github.com/user-attachments/assets/b06e0bc3-7cd5-4d5f-9bf9-cafd4c7c98d1" />


5. For the “Project Title” field, enter **NVivo Workshop**.

<img width="939" height="359" alt="image" src="https://github.com/user-attachments/assets/fa0b9938-2ea5-4647-ad42-ab1e729f2b61" />


6. If the data you plan to analyze is not primarily in English, change the **Text Content Language** field accordingly. Then click **Create Project** to continue.

<img width="944" height="353" alt="image" src="https://github.com/user-attachments/assets/2dd96023-7fc3-440a-8cf9-800330c9cd76" />


7. When the welcome pop-up appears, click **SKIP TOUR** to close it.

<img width="681" height="458" alt="image" src="https://github.com/user-attachments/assets/f0ab6a66-dddd-46a2-be53-db7ab8ebd9fa" />


8. The interface of NVivo includes:  
   1) Ribbon  
   2) Navigation View  
   3) List View  
   4) Detail View  
   5) Find Bar  
   6) Quick Coding Bar  
   7) Status Bar

<img width="663" height="463" alt="image" src="https://github.com/user-attachments/assets/2c4f3d66-bd68-493f-be68-dc6c32337a28" />
*Image Source: [The workspace](https://help-nv.qsrinternational.com/14/win/Content/about-nvivo/nvivo-workspace.htm)*

# Import Files

NVivo supports organizing files in a hierarchical structure and analyzing a wide range of qualitative data types, including surveys, notes, emails, codebooks, reports, and more.

## Files

1. Go to **Files** under **Data**, right-click on **Files** and select **New Folder…**.

<img width="345" height="157" alt="image" src="https://github.com/user-attachments/assets/e2d52ba9-87ac-4d38-88a3-8963617fc8e4" />


2. In the pop-up, enter **Interview** in the “Name” field, and click **Done**.

<img width="448" height="402" alt="image" src="https://github.com/user-attachments/assets/1e3c03d9-9a70-40f9-9098-8baeb947ec2d" />


3. Make sure the **Interview** under **Files** is selected, then go to the **Import** menu, click on **Files**.

<img width="930" height="333" alt="image" src="https://github.com/user-attachments/assets/143bc23e-7f28-4908-bd3d-d900af1f4681" />


4. In the dropdown, select **Documents…**.

<img width="228" height="236" alt="image" src="https://github.com/user-attachments/assets/82a815b6-7028-4967-84df-953d37d2a6e0" />


5. In the pop-up window, navigate to the workshop folder, open the Workshop\_Files folder, select all items that begin with “Interview”, and click **Import**.

<img width="864" height="484" alt="image" src="https://github.com/user-attachments/assets/55f17e3d-8e8e-4f68-9bf9-855e1249f8ed" />


6. Repeat the same steps for the focus group files. Create a new folder named **Focus Group**, then go to **Import** \> **Files** \> **Documents**. In the Workshop\_Files folder, select all items that begin with “FG”, and click **Import** to continue.

7. The **Interview** and **Focus Group** folders should now appear under **Files**. Double-click each folder to view all the imported documents within it.

<img width="635" height="247" alt="image" src="https://github.com/user-attachments/assets/60df74bc-d0a1-427e-8adb-79806dea79af" />


8. Hover over the icon next to each file title to see its corresponding file format appears as “Shortcut to \[file format\]”.

<img width="384" height="118" alt="image" src="https://github.com/user-attachments/assets/952a03af-5624-4dd9-a2d7-36512f54505a" />


## NCapture

If you want to capture content from online sources (e.g., websites, social media posts)and import those into NVivo, **NCapture** is a browser extension that streamlines the process. With NCapture, you can collect online content and import it directly into NVivo. Follow the instructions [here](https://help-nv.qsrinternational.com/20/win/Content/ncapture/ncapture.htm) to install and use NCapture.

# 

# Text Coding

NVivo is a tool not only for qualitative data analysis but also for project management. It supports the entire qualitative research process from collecting and organizing materials to coding, analyzing, visualizing, and sharing results. 

## Deductive Coding

Deductive coding is a top-down qualitative analysis approach where you start with a set of predefined codes, and then go through your files, applying those codes to the relevant snippets.

1. To create codes, click **Codes** under **Coding**, then click **Close** to close the introduction page.

<img width="789" height="482" alt="image" src="https://github.com/user-attachments/assets/d344043e-a987-435d-87e5-7e5bc0ca1f14" />


2. In the blank area, right-click and select **New Top-Level Code…**.

<img width="317" height="341" alt="image" src="https://github.com/user-attachments/assets/7e4ec5dc-cf26-4c7a-92ff-2ed338d95fbf" />


3. In the pop-up, enter **Energy** in the “Name” field, and click **Done**.

<img width="442" height="458" alt="image" src="https://github.com/user-attachments/assets/c93651f4-eaac-4b09-a0b0-7443c9ece722" />


4. Go to **Interview** under **Files**, and double-click to open the **Interview Transcript dec4\_2014 2\_02pm** file.

<img width="690" height="282" alt="image" src="https://github.com/user-attachments/assets/22f4df89-c04e-4c8c-a009-11f4b6e53146" />


5. Files imported into NVivo are automatically opened in protected mode, meaning they cannot be edited. To make changes, check **Edit** to turn on editing view.

<img width="346" height="103" alt="image" src="https://github.com/user-attachments/assets/0f355a5d-3b7c-496e-b77a-c9a7d87b6e3e" />


6. Remember to uncheck it once you’re finished editing.

<img width="346" height="104" alt="image" src="https://github.com/user-attachments/assets/34a246da-54c2-4e50-8736-8ff315ffb78b" />


7. Now, select a text snippet in the **Interview Transcript dec4\_2014 2\_02pm** file, right-click, and select **Code Selection** \> **To Existing Codes or Cases…** from the menu.

<img width="623" height="370" alt="image" src="https://github.com/user-attachments/assets/2173c4c1-d1a5-4c23-8ff9-931213c1bec1" />


8. In the pop-up, select **Imported Products,** and click **Code Selection to ‘Imported Pro…’**.

<img width="784" height="434" alt="image" src="https://github.com/user-attachments/assets/2341ac71-f991-497b-8c14-dbee30233f2b" />


9. Select another snippet in the same file and right-click to open the content menu. This time, go to **Code Selection** \> **Energy (Codes)**.

<img width="861" height="498" alt="image" src="https://github.com/user-attachments/assets/70b2329c-8289-4e88-a968-0b906508a97e" />


10. Alternatively, you can drag and drop the text snippet directly onto the corresponding code in the code list. Let’s try this method with another new snippet.

<img width="971" height="368" alt="image" src="https://github.com/user-attachments/assets/8a97e45e-f7ce-4881-8ac4-08b80f97e50c" />


11. Now, go to **Codes** in the navigation view, you should see the **Energy** code has 1 file and 3 references.

<img width="645" height="155" alt="image" src="https://github.com/user-attachments/assets/b488c9ca-0f49-4341-897a-627accb99507" />


## Inductive Coding

Inductive coding is a bottom-up approach where you may want to read through the material first, let ideas and themes emerge naturally, and then create codes based on what you find in the data.

1. In the **Interview dec4\_2014 2\_02pm** file, select one text snippet and right-click, select **Code Selection**, then **To New Code…**.

<img width="747" height="529" alt="image" src="https://github.com/user-attachments/assets/93296936-d070-40e6-9a32-c1b8583da93f" />


2. In the pop-up, enter **Cost** in the “Name” field, and click **Done**.

<img width="458" height="527" alt="image" src="https://github.com/user-attachments/assets/07b63300-41ff-4307-991e-f31733798c85" />


3. Select another snippet in the same file, code it to **Cost**.

4. Go to **Codes** in the navigation view, you should see the **Cost** code has 1 file and 2 references.

<img width="728" height="175" alt="image" src="https://github.com/user-attachments/assets/7d18f75f-98a2-4b16-a0a3-77865dbca483" />


## Mixed Coding

Mixed coding combines deductive and inductive approaches. For example, you can start coding with some predefined codes and then add new ones as patterns and insights while reading through the data. 

## Parent & Child Code

Within NVivo, codes can be organized hierarchically by creating parent and child codes.

1. Now, in the **Interview dec4\_2014 2\_02pm** file, select one text snippet and right-click, select **Code Selection**, then **To New Code…**.

<img width="954" height="554" alt="image" src="https://github.com/user-attachments/assets/c763a71e-a714-4ff9-9800-6232785a925f" />


2. Enter **Efficiency**, then click the arrow icon.

<img width="500" height="581" alt="image" src="https://github.com/user-attachments/assets/47de0b1b-e83e-4a85-ad44-5eccd83d786f" />


3. Then, expand **Codes** by clicking on the arrow icon, select **Energy**, and then click **Done**.

<img width="553" height="606" alt="image" src="https://github.com/user-attachments/assets/cc92b517-f591-439b-9399-0aebd593d661" />


4. Repeat the same steps to create another 2 child codes under **Energy**: **Network**, **Air**, and code 2 snippets under each newly created child code.

5. Go to **Codes** in the navigation view. Click on the **\+** icon next to **Energy** \- 3 child codes will appear.

<img width="615" height="283" alt="image" src="https://github.com/user-attachments/assets/fc7b44aa-ca9b-4c6a-b849-b321285e5b17" />


6. Double click on a code, the snippet will show up in the detail view with some quantitative information about each snippet.

<img width="979" height="368" alt="image" src="https://github.com/user-attachments/assets/1decea0e-b9f1-4fbf-92ea-580784162ee6" />


7. Now, although the 3 child codes (**Air, Efficiency, Network**) are underneath one parent code (**Energy**), the counts for **Files** and **References** are not aggregated \- this is because NVivo treats parent code and its child codes separately as defaults. 

<img width="579" height="267" alt="image" src="https://github.com/user-attachments/assets/2f0c4da9-8706-4c6c-bab9-066f602fabc8" />


8. To aggregate them, right-click on **Energy**, then **Get Info**.

<img width="622" height="300" alt="image" src="https://github.com/user-attachments/assets/d07c04c3-6d17-4e46-84ab-3091ec1fae0e" />


9. Check **Aggregate coding from child codes**, and click **Done**.

<img width="653" height="587" alt="image" src="https://github.com/user-attachments/assets/184c987d-8af8-4cdf-8f38-857ee5c2258f" />


10. The count of files and references of **Energy** should be updated with the total counts.

<img width="615" height="256" alt="image" src="https://github.com/user-attachments/assets/3c401277-4d6f-45a6-912b-4ef1ca06bf32" />


## Uncoding

Uncoding means removing a coded snippet from a code that disconnects that piece of data from the theme or category it was assigned to.

1. Double-click on **Chemicals** code \- the snippet of coded text will show up.

<img width="527" height="213" alt="image" src="https://github.com/user-attachments/assets/085d8e3a-9ea8-41d0-b2dd-360ed50adbd0" />


2. Select the entire of one snippet, right-click and select **Uncode Selection** \> **From this Code**.

<img width="715" height="424" alt="image" src="https://github.com/user-attachments/assets/4561abd7-0ebc-48ea-8322-bb04a0ab8a7b" />


3. The coded text will now be removed. Next, click the hamburger icon, then **Close All** to close all tabs.

<img width="812" height="315" alt="image" src="https://github.com/user-attachments/assets/9eabb78d-9313-438d-b527-af5d610d311a" />


# Highlighter & Coding Stripes

The highlighter and coding stripes help visualize and track your coding work in NVivo.

1. Go to **Interview** under **Files**, click on **Interview dec4\_2014 2\_02pm** to open the file.

2. In the detail view, click on the **Highlight** icon, and select **All Coding**.

<img width="353" height="233" alt="image" src="https://github.com/user-attachments/assets/0ab630c6-efa4-496a-aca6-3b64140505cb" />


3. The snippet you’ve coded will be highlighted in yellow.

<img width="795" height="272" alt="image" src="https://github.com/user-attachments/assets/8a97651c-0d02-4aec-991a-41a5a7b20c65" />


4. Next, in the detail view, click on the **Coding Stripes** icon, and select **All**.

<img width="313" height="475" alt="image" src="https://github.com/user-attachments/assets/747a17c1-78fc-4269-98be-aa1ee7378c1c" />


5. Now, a new pane with multiple colored stripes alongside the file shows which part of the text has been coded and which codes were applied.

<img width="893" height="422" alt="image" src="https://github.com/user-attachments/assets/8cd10b15-a849-414a-ae07-a689bd56ff84" />


6. We can change the color of these bars to visualize our coded content more clearly. To do this, go to **Codes** under **Coding**, select a code and right-click, go to **Color**, then select **Red** as the new color for the code Energy.

<img width="598" height="673" alt="image" src="https://github.com/user-attachments/assets/761d98f9-b10d-4726-913a-a231cf07b02c" />


7. Repeat the same steps and change the colors of the child codes under the **Energy** code to colors other than red.

8. Now, click the **Coding Stripes** icon again, and make sure **Item Colors** is selected.

<img width="251" height="430" alt="image" src="https://github.com/user-attachments/assets/c6bd2acd-c856-4eec-90b1-29ac2ed867e2" />


9. The color of each code now will appear as the color you selected.

<img width="363" height="697" alt="image" src="https://github.com/user-attachments/assets/eb2c9d5f-9d12-42f4-9f60-2d6ba7493f64" />


10. Let’s turn off the coding stripes and highlighter by clicking both icons and selecting **None** for now.

<img width="338" height="455" alt="image" src="https://github.com/user-attachments/assets/b488c743-2058-48d2-a28f-8819876642a3" />


# Memos & Annotation

Memos and annotations help capture your thoughts and insights during analysis. Memos record broader reflections about your data, codes, or project, while annotations act as in-line comments attached to specific text or sections.

1. To create a memo, go to **Interview** under **Files**, right-click on **Interview dec4\_2014 2\_02pm**. Then, select **Link to New Memo…**.

<img width="876" height="435" alt="image" src="https://github.com/user-attachments/assets/4ac19835-ff1b-458a-a1e3-e907b948d083" />


2. Enter **Interview Memo** as the name in the pop-up and click **Done**.

<img width="383" height="572" alt="image" src="https://github.com/user-attachments/assets/311cc2d2-ae71-4383-a82e-5285192ecd48" />


3. A blank page will appear where a detailed memo about the file can be written. For example, noting the interview was conducted in a noisy cafe shop. You can note that here.

<img width="685" height="276" alt="image" src="https://github.com/user-attachments/assets/28a077bf-ce75-47bc-b33b-ab8dabc465d2" />


4. Once you close the window, the memo is saved and linked to this file. You should see a small icon next to the interview in the list for the memo link when you have the interview list opened completely (with no other files open to the right of it). 

<img width="402" height="211" alt="image" src="https://github.com/user-attachments/assets/0d2469d5-92dc-4dff-b441-3529e3527f14" />


5. To view the memo, right-click on the file again, select **Memo Link** \> **Open Linked Memo**.

<img width="849" height="502" alt="image" src="https://github.com/user-attachments/assets/f512b8b1-ea08-4d08-915e-44f34ad3c2e2" />


6. To create an annotation for a snippet, go to **Interview** under **Files**, double-click on **Interview may13\_2015**.

<img width="552" height="187" alt="image" src="https://github.com/user-attachments/assets/495ff2dd-4243-409f-8f7e-e2b93fb8cb8d" />


7. In the detail view, select a text snippet, then select **New Annotation**.

<img width="743" height="366" alt="image" src="https://github.com/user-attachments/assets/39542d08-b6ba-4ce1-a0b9-add04234931a" />


8. A new box will appear next to the selected text. Enter your annotation for this snippet. For example, “This part hasn’t been cleaned yet.”

<img width="796" height="348" alt="image" src="https://github.com/user-attachments/assets/9dad69ef-d848-462e-8833-194b2a77ac83" />


9. To see memos and annotations you have created all in one place, using the left navigation menu, under **Notes**.

<img width="512" height="235" alt="image" src="https://github.com/user-attachments/assets/07746aea-d65b-4ce6-91e6-66070755d121" />


10. Finally, you can also create a note that applies to the entire project. For example, maybe some ideas you have about how the research is going or new themes that are emerging. Double-click on **Memos** under **Notes**. In the detail view, right-click on the blank area and select **New Memo**.

<img width="712" height="335" alt="image" src="https://github.com/user-attachments/assets/59e346e0-7b99-441d-9717-be61a6935253" />


11. Give it a name, such as **Project Memo** and click **Done**.

<img width="444" height="671" alt="image" src="https://github.com/user-attachments/assets/4f117da9-2b98-4ef7-821f-79b92f239e5b" />


12. Type some notes, such as “The project needs to be reviewed” and then close it to save. You can always double-click on **Project** from the list of memos to re-open it.

<img width="784" height="406" alt="image" src="https://github.com/user-attachments/assets/779d5025-5f49-4bd8-ba14-c9000d9edbda" />


# Image Coding

NVivo allows analyzing visual data by selecting and coding specific areas within an image. You can zoom in, highlight relevant parts of an image, and assign them to existing or new codes, making it possible to integrate visual analysis alongside textual and audio data within the same project.

1. Go to **Focus Group** under **Files** and click on **FG1 Questionnaire 14** to open the PDF file.

<img width="663" height="256" alt="image" src="https://github.com/user-attachments/assets/c2e7dcc9-a7d8-4829-a44d-06143fa18c2f" />


2. Note that NVivo 14 does not support **Optical Character Recognition (OCR)**. If your image files contain text that you want to code, make sure they are OCR-processed before importing them into NVivo. For text that cannot be OCRed (like handwriting or signatures), you can manually draw a square around the area you wish to code.

3. Next to **Selection Mode**, select **Region**.

<img width="379" height="161" alt="image" src="https://github.com/user-attachments/assets/99e49654-d00b-40c1-8e22-da5e39a5f7eb" />


4. Draw a square around the area you want to code, then right-click and select **Code Selection**, then **To Existing Codes or Cases**.

<img width="759" height="331" alt="image" src="https://github.com/user-attachments/assets/c26d9c76-80e9-48fa-93c2-12186da741cd" />


5. Check **Energy**, and click **Select** to continue.

<img width="918" height="507" alt="image" src="https://github.com/user-attachments/assets/9b361969-d6c5-48be-bdcb-c5ff06cbabde" />


6. Now, go to **Codes** and select **Energy**. In the detail view, instead of showing the image snippet, NVivo will display a screenshot of the selected region. (On Windows, this will appear as the coordinates of the selected image area.)

<img width="907" height="526" alt="image" src="https://github.com/user-attachments/assets/9ef521ed-3573-4435-8512-41f6c40a68b5" />


# Save the Project

1. Every time when you are done working on editing the project, it is important to remember to save manually. First, hover over the top toolbar and go to the **File** menu.

<img width="577" height="244" alt="image" src="https://github.com/user-attachments/assets/529f6b29-c829-4eaf-b374-edfc62e44d03" />


2. Select **Save** to save the current project.

<img width="617" height="383" alt="image" src="https://github.com/user-attachments/assets/19b06a0d-26f3-45a0-bab0-15c5c2dbbda7" />


3. Finally, you can close a project to return to the NVivo main screen. Once your project is saved, go to the **File** menu in the top toolbar and select **Close**.

<img width="622" height="389" alt="image" src="https://github.com/user-attachments/assets/02adb649-a962-4d6c-8c34-88effbbee766" />


# Audio & Video Coding

NVivo allows the import and analysis of audio and video files through coding specific time segments within those recordings. Please note that the **Transcription** feature in NVivo is not included in our software license; however, transcription can be done using alternative tools such as the **Dictate** feature in Microsoft Word.

1. Go to the **File** menu in the top toolbar and click on **Create Copy of Sample Project**. We will use this sample project for the rest of the workshop.

<img width="375" height="438" alt="image" src="https://github.com/user-attachments/assets/9bef5a56-9245-49c7-be0e-08fd28c05c5e" />


2. Name the project as its default **Sample Project**. For the saving path, select the workshop folder, and click **Save**.

<img width="693" height="506" alt="image" src="https://github.com/user-attachments/assets/f801e594-f449-45b8-9364-3ec0ed5c9618" />


3. When the welcome pop-up appears, click **SKIP TOUR** to close it.

<img width="783" height="536" alt="image" src="https://github.com/user-attachments/assets/01667599-2f07-4e9a-93e9-89745ab1d64d" />


4. Go to **Files**, then **Interviews** folder. Double click to open the **Betty and Paul** file \- this is a video recording from an interview.

<img width="900" height="586" alt="image" src="https://github.com/user-attachments/assets/922346dd-10e4-428f-a78d-5f6da3d02a34" />


5. Opening this video recording gives us three panels: the audio waveform, the playback window, and a content panel showing timestamps along with the transcript. 

<img width="933" height="634" alt="image" src="https://github.com/user-attachments/assets/7acd8789-f7c9-4fb8-872d-aea5de377b8c" />


6. Now, go back to the **Interviews** folder, double-click on the **Helen** file \- this is an audio format file. 

<img width="845" height="431" alt="image" src="https://github.com/user-attachments/assets/e50dc9ce-e25a-4efc-a732-932ceefb957c" />


7. Like a video format file, the audio recording gives us three panels: the audio waveform, the playback window, and a content panel showing timestamps along with the transcript. 

<img width="821" height="612" alt="image" src="https://github.com/user-attachments/assets/83e06559-bf6a-4738-b51c-f97789e6a274" />


8. To code the segment, drag the **playhead** in the waveform window to the starting point, then click the **Start Selection** icon at the bottom to begin selecting the segment.

<img width="565" height="219" alt="image" src="https://github.com/user-attachments/assets/b0af83f6-6d87-4a26-a91f-1f900529f59d" />


9. When it ends, click the **Finish Selection** icon to complete the coding range.

<img width="564" height="225" alt="image" src="https://github.com/user-attachments/assets/6de422fa-6b67-4635-ae5f-9e0768f27164" />


10. Then, right-click and select **Code Selection**, then **At Existing Codes or Cases**.

<img width="599" height="351" alt="image" src="https://github.com/user-attachments/assets/f6c0dcf0-22db-4535-bdbe-7ee4ddc44529" />


11. Select **Memorable quotes** in this case, and click **Select** to confirm.

<img width="801" height="445" alt="image" src="https://github.com/user-attachments/assets/87273b13-5b04-457b-a7a4-6649914041e6" />


12. Go to **Codes**, **Memorable quotes**. The timestamp of the segment we just coded will appear.

<img width="923" height="365" alt="image" src="https://github.com/user-attachments/assets/5f3cc0b9-783b-4248-ab90-86812c1f5a6b" />


13. To uncode a segment, click on the segment reference to go back to the source file.

<img width="785" height="192" alt="image" src="https://github.com/user-attachments/assets/9080f84d-a91a-4b9a-b907-a693ca716337" />


14. From the audio wavement, find the coded segment, right-click and select **Uncode Selection**, then **Memorable quotes (Codes)**.

<img width="723" height="573" alt="image" src="https://github.com/user-attachments/assets/3347856f-d816-4fd1-92d3-5c04d7f49722" />


15. Now the coded segment should be removed.

16. Video coding follows the same steps as audio coding.

# Case Classification & Cases

Cases are a special type of code that represents the individuals in your study. If you have demographics or other important attributes that you want to incorporate into your study, case classifications and cases can help. For example, if you were analyzing interview transcripts, you might want to create a case classification called “Person” with attributes such as their name, age, education, job title, etc. Once your case classification is in place that defines what characteristics you want to capture for your interviewees, you could then create one case for each interviewee with those attributes filled in. 

For example, if you interviewed someone named Barbara, you would create a case called BARBARA (or some ID number if needed for confidentiality) with information about Barbara. You would then use that Barbara case to code all the imported content that are associated with Barbara (where the case acts like a code). Later you can then run queries that incorporate that information to answer questions such as, does Barbara talk more about the environment?

You can manually create case classifications and cases by using the left menu, under **Cases**. You can right click on **Case Classification** and **Create a New Classification** or right click on cases to create a new case. But often times, it is easier and more common to upload a spreadsheet with all the information for the cases. We are not going to try that out in this tutorial, but will show you how that would look like.

1. Under **Cases**, go to **Case Classifications**.

<img width="319" height="327" alt="image" src="https://github.com/user-attachments/assets/b262b3cd-1a40-4271-9a50-680bd21161cc" />


2. Double-click to open **Person**, then switch the view from **Attributes** to **Classification Sheet**.

<img width="913" height="394" alt="image" src="https://github.com/user-attachments/assets/230c452a-37bf-47eb-b427-e0d73f47fa2f" />


3. A table of all the information about the participants will appear, with different attributes about their background, like the neighborhood they live in, their gender, age range, etc. You can edit the data here.

<img width="970" height="457" alt="image" src="https://github.com/user-attachments/assets/39bf091d-e40e-4b4e-8613-08cd6040dc58" />


4. We can take advantage of NVivo’s autocoding features to identify the parts of interviewee and interviewers in a file and code them automatically into the appropriate case. Using the left menu, under **Data**, then **Files**, go to the **Interviews** folder, and open the interview transcript titled “Barbara”. Then, go to **Home** menu \> **Autocode** \> **By Speaker**. You can also right-click on “Barbara” and select **Autocode** \> **By Speaker** to continue.

<img width="943" height="527" alt="image" src="https://github.com/user-attachments/assets/9c252f53-4ac1-4fa9-812c-77d35a9a61aa" />


5. An **Autocode by Speaker** pop-up will appear.

<img width="879" height="576" alt="image" src="https://github.com/user-attachments/assets/05fd8112-614f-468d-afe3-b11d5fe8a16c" />


6. The “Barbara” document is formatted in a consistent manner so we can always pick out who is speaking because the person’s name stands on its own line followed by the words they speak. We need to specify who the unique speakers are in this document. In the entering field in the **Autocode by Speaker** pop-up, type in **HENRY** and hit **Enter**. Then type in **BARBARA** and hit the **TAB** key. You should double-check the preview on the right pane to confirm that NVivo is picking up each unique speaker by highlighting them in different colours.

<img width="861" height="406" alt="image" src="https://github.com/user-attachments/assets/7ee27e52-aaee-4ac5-a9e2-ddba7d3bc484" />


7. Make sure **Cases** is selected for the saving location (**Create cases in** field), and **Person** is selected under **Existing classification**. Then click on **Autocode**. This should code everything that Henry or Barbara said in the transcript with their cases. 

<img width="877" height="575" alt="image" src="https://github.com/user-attachments/assets/2653012a-4c1f-42d2-b55d-72dfd8c6f2e8" />


8. Go to **Cases** under **Cases**. 

<img width="323" height="559" alt="image" src="https://github.com/user-attachments/assets/eac79088-dad7-4a00-8a91-cd8a3ad19c79" />


9. Double click on the **BARBARA** case. You should see everything that Barbara said in her interview. These words are coded to this case. The **BARBARA** case code is now linked to Barbara’s interview responses.

<img width="756" height="448" alt="image" src="https://github.com/user-attachments/assets/b9896a11-0227-4906-9954-673e0580d47e" />


10. Close all the tabs.

# Query

Instead of manually searching through large volumes of coded material, queries in NVivo are powerful tools that help you to quickly grab insight from the data by solving specific questions about your data such as how often certain words/phrases/themes appear, which participants expressed particular attitudes, or how concepts overlap.

This tutorial will not go through all of them in this workshop, but if you are interested in learning more, visit Mac version’s [Queries](https://help-nv.qsrinternational.com/14/mac/Content/queries/queries.htm) page for additional resources. 

## Word Frequency Query

Word frequency query allows you to find the most commonly used words in your sources.

1. First, let’s see how queries can help with making sense of this project. Go to the **Explore** menu to see all available query options.

<img width="681" height="163" alt="image" src="https://github.com/user-attachments/assets/f0b30ed6-653b-49c7-aa93-64061c41fc4b" />


2. Select **Word Frequency** query, which helps with finding the most frequently used words in the data.

<img width="666" height="160" alt="image" src="https://github.com/user-attachments/assets/d31a0bfd-e685-44d6-b945-f7881da94cbf" />


3. Let’s set the search scope limited to the interview script. Next to **Search in**, click on **Selected Items**.

<img width="706" height="200" alt="image" src="https://github.com/user-attachments/assets/26715c76-84bf-4976-a9f6-4c9bcbf301b3" />


4. In the pop-up, expand **Files**, then click on **Interviews** to select everything in the folder. Next, unselect 2 videos and 1 audio files (with different icons) so that only text transcripts are selected for our search. Click **Select** to continue.

<img width="866" height="477" alt="image" src="https://github.com/user-attachments/assets/d3605753-95aa-4cbf-996c-ab6958671326" />


5. The **Finding matches** option helps identify and organize similar or related terms in your text data to varying degrees. Stemmed words means words that share the same root or base form \- for example, talk, talking, talks, and talked all share the stem “talk.” Now, let’s check on **Include stemmed words**, which groups words by the same stem.

<img width="946" height="175" alt="image" src="https://github.com/user-attachments/assets/d78f4cc7-6df8-48ad-9ca6-51606bf10aa9" />


6. Set the “Display Words” field to **50**, and keep the “Minimum Word Length” field set to **3**. 

<img width="952" height="175" alt="image" src="https://github.com/user-attachments/assets/d830d622-05f8-449d-990e-82db4b94ff1e" />


7. Click **Run Query**.

<img width="954" height="176" alt="image" src="https://github.com/user-attachments/assets/5f8433e8-acd4-446c-9f9a-d85189a170ed" />


8. Now, we should see the results of our query.

<img width="931" height="568" alt="image" src="https://github.com/user-attachments/assets/42593d60-208c-420a-9cdd-5b207d57f00b" />


9. Double-click on the word **people**, you will see the location of where the **people** appeared across all of the selected text transcripts.

<img width="834" height="559" alt="image" src="https://github.com/user-attachments/assets/ad30c287-db7c-4a4f-8175-870ef976c125" />


10. Go back to the first **Unsaved Query**, and you will find out that words like ‘a’, ‘and’, ‘the’ are ignored \- these words are treated as **stop words**, which are those really common words and won’t be useful for analysis. When you see a word in the list and you don’t think they’d be helpful, for example, the word ‘things’, you can right-click on ‘things’ and select **Add to Stop Words List**.

<img width="838" height="435" alt="image" src="https://github.com/user-attachments/assets/434f1751-da50-4977-ad31-acd39a677971" />


11. To check or reset the stop words list, go to the top toolbar, hover over **Files** and select **Project Properties** from the menu. 

<img width="487" height="563" alt="image" src="https://github.com/user-attachments/assets/0957ec1b-d6dd-49bb-83f3-328fe800c559" />


12. Under the **General** tab, you can select text content languages. The default is English (US), but you can switch to other languages. Click on **Stop Words…** to see the current list in use. 

<img width="917" height="529" alt="image" src="https://github.com/user-attachments/assets/130d3c4b-a4e4-46be-8559-c2683cbb8f28" />


13. From here, you can add stop words manually, or reset the list. But for now, let’s click **Cancel**, then **Cancel** again to close the two pop-ups and return back to the result list.

<img width="873" height="473" alt="image" src="https://github.com/user-attachments/assets/a42659e8-359e-4643-bd0a-6e9e193de7d2" />


14. Now let's export the list, since the query results are not saved automatically \- once you close the tab, they will be lost. To save the list as a file on your computer, right-click any word in the list and select **Export**.

<img width="963" height="554" alt="image" src="https://github.com/user-attachments/assets/76a76ef3-c254-41b0-8ecd-452970f7010b" />


15. In the pop-up, give the file a name or keep the default, then browse to the workshop folder. Modify the file format if needed, and click on **Save**.

<img width="759" height="418" alt="image" src="https://github.com/user-attachments/assets/f9e5b583-b72e-4047-9648-7490ba1be1a7" />


16. NVivo provides several visualization tools to help you explore your codes. For example, click the **Word Cloud** tab to view our results as a cloud visualization. The Mac version of NVivo offers limited visualization and style options for word frequency queries, whereas the Windows version includes additional visualizations such as Tree Map and Cluster Analysis diagrams.

<img width="843" height="624" alt="image" src="https://github.com/user-attachments/assets/62863fb0-4331-4ddb-8da9-9c5416abe7f7" />


17. Click **Gallery** to change the appearance of the visualization.

<img width="831" height="672" alt="image" src="https://github.com/user-attachments/assets/69028deb-94a4-4c79-af97-dcc429cd4dce" />


18. Right-click on the visual and select **Export** to save the word cloud in your computer.

<img width="834" height="539" alt="image" src="https://github.com/user-attachments/assets/b8b642d7-a676-40d0-98d4-740ae022ffaf" />


19. Close all tabs for now.

<img width="825" height="206" alt="image" src="https://github.com/user-attachments/assets/56668358-e6c4-4e9a-aa35-522d187b8d36" />


## Text Search Query

Text Search Queries allow you to search for specific words or phrases across your project items.

1. Go to the **Explore** menu and select **Text Search Query**.

<img width="762" height="174" alt="image" src="https://github.com/user-attachments/assets/1013a5d3-46f9-49f4-83c8-bfe837b947a1" />


2. Keep the search scope as **Files & Externals** \- this includes all imported files in your project. In the search box, enter **water**, and check **Include stemmed words**.

<img width="872" height="224" alt="image" src="https://github.com/user-attachments/assets/621516c3-de65-4720-b0f3-815c27dd4576" />


3. Click **Run Query**.

<img width="874" height="223" alt="image" src="https://github.com/user-attachments/assets/9e3a0e4d-241e-43b4-b4b8-57c98395678d" />


4. A list of files containing the word **water** and its stemmed forms will appear. Double-click **Charles** to view the details.

<img width="829" height="352" alt="image" src="https://github.com/user-attachments/assets/801428b5-5f57-4f58-aab9-cdb135fd479e" />


5. In Charles’s interview transcript, you will see the term **water** highlighted.

<img width="837" height="514" alt="image" src="https://github.com/user-attachments/assets/14ca9cf8-624e-4c71-896c-06e84df5d242" />


6. We can store the results of this query as a new code. To do so, go back to the **Unsaved Query** tab and click **Save Results…**. 

<img width="885" height="211" alt="image" src="https://github.com/user-attachments/assets/c6016f11-b363-4e11-95d9-1a6081e64907" />


7. In the pop-up, click on the **arrow** icon next to the **Location** field. 

<img width="587" height="314" alt="image" src="https://github.com/user-attachments/assets/d72a1172-0e25-4dfd-aad2-85bbd684ce84" />


8. Choose **Codes**, then click **Select**.

<img width="502" height="484" alt="image" src="https://github.com/user-attachments/assets/7ea9b105-851e-43fd-a5e3-95d21105d477" />


9. Rename the **Name** field to **Water**, and click **Save Results**.

<img width="598" height="325" alt="image" src="https://github.com/user-attachments/assets/8b505a57-895f-4bb2-a224-fa98e189b14e" />


10. Go to **Codes** in the navigation view. You will see a new code named **Water**, showing the corresponding files and reference counts from the query.

<img width="906" height="490" alt="image" src="https://github.com/user-attachments/assets/747d77f1-8119-4bef-9a7f-416fab79169d" />


11. If your search phrase contains multiple words, make sure to enclose it in quotation marks (“”). Otherwise, NVivo will treat each word as a separate search term. For example, enter “salt water” in the search box and click **Run Query** again. This new query should return 3 results.  
    * For more tips about building search query, visit [Text Search Query](https://help-nv.qsrinternational.com/14/win/Content/queries/text-search-query.htm) page.

<img width="924" height="486" alt="image" src="https://github.com/user-attachments/assets/135c2f9d-32a4-4f2f-bae8-cc68593d6df5" />


12. Let’s say you want to save this query for future use. To do so, click **Save Criteria…**.

<img width="979" height="238" alt="image" src="https://github.com/user-attachments/assets/eac60957-e06e-4a8d-9b98-faf029fa08a8" />


13. Name the query as **Salt Water**, and click **Save Criteria**.

<img width="520" height="271" alt="image" src="https://github.com/user-attachments/assets/54d9bdbe-af19-434c-866d-944d40f7eb41" />


14. Then, close all tabs.

15. Go to **Queries** under **Explore** in the navigation menu. Under **Query Criteria**, you will find **Salt Water** listed. Double-click it to reopen the saved query.

<img width="530" height="492" alt="image" src="https://github.com/user-attachments/assets/8cb189ea-c0e9-4173-9ffd-a977ddba78a6" />


16. Close the tab to continue.

## Matrix Coding Query

Matrix Coding Query allows you to compare coding across multiple dimensions, such as codes, cases, or attributes, to identify patterns and relationships in your data. The results are displayed as a matrix table, where rows typically represent cases or participants and columns represent codes or themes. Each cell shows the number of references or the amount of coding coverage where the two dimensions intersect. 

For example, we can look at attitudes expressed by different interviewees based on what they said during the interviews. To run this query, we will use the code “Attitude” and the case “Interview Participants."

1. Go to the **Explore** menu and click **Matrix Coding Query**.

<img width="654" height="197" alt="image" src="https://github.com/user-attachments/assets/139ee266-c7cd-42c9-bfae-541c26faecf5" />


2. Under **Cases**, open **People**. In the list view, click the **\+** icon next to **Interview Participants** to expand the name list.

<img width="917" height="609" alt="image" src="https://github.com/user-attachments/assets/72ac7d0f-f563-44bf-b73a-46ac36fb00f2" />


3. Select all participant names by dragging your cursor over them, then drag the selection into the **Rows** box.

<img width="970" height="582" alt="image" src="https://github.com/user-attachments/assets/eaac595e-b66c-42c9-bc23-4f97898eb5e6" />


4. Next, under **Codes**, expand **Attitude** by clicking the **\+** icon.

<img width="953" height="560" alt="image" src="https://github.com/user-attachments/assets/719508b7-2864-4415-ab01-9e827889e27e" />


5. Select all items under the **Attitudes** code and drag them into the **Columns** box.

<img width="972" height="615" alt="image" src="https://github.com/user-attachments/assets/a1f82220-4ca9-409d-b393-4b28d022a561" />


6. Make sure the search scope is set to **Files & Externals**, then click **Run Query**.

<img width="935" height="450" alt="image" src="https://github.com/user-attachments/assets/e496b349-e32b-4b89-b8ab-720654646da8" />


7. A matrix table will appear, showing the number of times participants mentioned words related to each attitude.

<img width="713" height="612" alt="image" src="https://github.com/user-attachments/assets/01e5b48b-420e-42a4-922c-3e3674b52483" />


8. We can color-coded the table to make it more visual. To do that, right-click on the table and go to **Cell Shading**, then **Blue-White**. 

<img width="848" height="618" alt="image" src="https://github.com/user-attachments/assets/27f006d8-e505-4825-bc43-14fbf44cd797" />


9. Now the table is color-coded — the deeper the color, the higher the count of coded references.

<img width="582" height="548" alt="image" src="https://github.com/user-attachments/assets/7f747620-a68c-4aeb-aeff-9087f4e5cb38" />


10. We can also visualize other data within this table. To change data sources in the view, right-click anywhere on the table and select **Cell Content** \> **Files Coded** \> **All**. Note that the Windows version offers additional options for displaying data sources, such as words coded, coding presence, and more.

<img width="929" height="509" alt="image" src="https://github.com/user-attachments/assets/7e7735f3-7be1-4beb-b849-c751e19a2c65" />


11. This visualization shows the total number of files in which the coded snippet(s) appear.

<img width="608" height="570" alt="image" src="https://github.com/user-attachments/assets/771d286c-d849-4779-bcc4-f2d3e7517c4f" />


12. You can export the table by right-clicking the visualization and selecting **Share**. From the available options, choose **Print** to export the visual as a PDF file or **Spreadsheet** to visualize the data using other tools.

<img width="782" height="539" alt="image" src="https://github.com/user-attachments/assets/6d50777a-a840-41fa-a162-afbbc2347ae5" />


13. When finished, close all tabs to return to the main workspace.

# Export Codes

When your analysis is complete, you can export your codes from NVivo in various formats \- as a code list, a codebook, or individual code files.

## Code List

1. Go to **Codes** under **Coding,** make sure the list of codes is open and unselected.

2. From the **Share** menu, select **Export** \> **Export List**.

<img width="359" height="340" alt="image" src="https://github.com/user-attachments/assets/49469ebd-81e3-465b-8310-386df57b3a32" />


3. Keep the default file name (**Codes**), choose your workshop folder as the save location, and click **OK**.

<img width="765" height="575" alt="image" src="https://github.com/user-attachments/assets/52553001-ddad-416e-86c9-7cf6ffc0e942" />


4. Open the **Codes.docx** file in your workshop folder. You should see a list of all codes displayed in NVivo’s code list.

<img width="979" height="604" alt="image" src="https://github.com/user-attachments/assets/a8231c5f-889f-4192-9ee9-8ad749a5a7da" />


## Codebook

1. Ensure you are in the **Codes** pane and the list of codes is open.

2. From the **Share** menu, select **Export** \> **Export Codebook**.

<img width="372" height="356" alt="image" src="https://github.com/user-attachments/assets/1432f544-73af-44cc-b350-8774037078b6" />


3. Keep the default file name (**Codebook \- Sample Project**) and make sure MS Word (.docx) is selected as the file format. Click **OK**.

<img width="788" height="590" alt="image" src="https://github.com/user-attachments/assets/5ae4f212-6f88-4f21-b841-4921d7c8b3f1" />


4. Open the **Codebook – Environmental Change Down East.doc** file in your workshop folder. This file displays each code with its description, and the counts of files and references associated with it.

<img width="979" height="584" alt="image" src="https://github.com/user-attachments/assets/9b21f033-38b1-496f-a394-8802741e3932" />


## Individual Code

1. Under **Codes**, select one or more codes to export.

<img width="902" height="244" alt="image" src="https://github.com/user-attachments/assets/3aca5208-52ea-4bb9-818d-b63bac2bb211" />


2. From the **Share** menu, select **Export** \> **Export Item**.

<img width="384" height="352" alt="image" src="https://github.com/user-attachments/assets/cfb373ba-46d1-456d-a0b5-712e4b89a38c" />


3. Make sure the workshop folder is selected, then click **OK**.

<img width="800" height="445" alt="image" src="https://github.com/user-attachments/assets/65823577-d7b4-408f-8e47-61bfe804c45c" />


4. Each selected code will be saved as a separate file in your workshop folder. For example, opening the **Water** file will display the related reference files, their locations, reference counts, and coverage.

<img width="979" height="579" alt="image" src="https://github.com/user-attachments/assets/c17c8751-b3cf-464d-bd83-cff10cafbd5c" />


# 

# Resources

## Qualitative Research Theory

* [SAGE Qualitative Research Methods](https://methods.sagepub.com/book/edvol/sage-qualitative-research-methods/toc) \[Online Book\]​  
* [The Essential Guide to Coding Qualitative Data](https://delvetool.com/guide) by Delve​

## NVivo

* [NVivo Tutorials](https://lumivero.com/resources/support/getting-started-with-nvivo/nvivo-tutorials/) by Lumivero​  
* [Lumivero Community](https://lumivero.com/resources/support/getting-started-with-nvivo/nvivo-tutorials/) for browsing resources, sharing knowledge, connecting with other NVivo users.​  
* [Transcribe your recordings](https://support.microsoft.com/en-gb/office/transcribe-your-recordings-7fc2efec-245e-45f0-b053-2a97531ecf57) in Microsoft Word​  
* [What is optical character recognition (OCR)?](https://www.ibm.com/think/topics/optical-character-recognition) By IBM

## Support

If you have any questions about the tool or this tutorial, don’t hesitate to reach out to the Data and Visualization Librarian, Siti Lei ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)) for further support.
