# **NVivo for Qualitative Data Analysis (Windows)**

*Siti Lei*  
*Data and Visualization Librarian, Duke Kunshan University*

*Last updated: November 11, 2025*

This 1.5-hour tutorial introduces how to conduct qualitative data analysis using a tool called NVivo in Windows devices, starting from importing qualitative data files, coding, running queries, to analyzing and visualizing codes. We will use a selection of text and image files from the project Data Center Energy Efficiency Focus Groups and Interviews (by U.S. Environmental Protection Agency) and the sample project in NVivo in this tutorial for demonstration. 

[Before we start	](#before-we-start)

 - [Introduction	](#introduction)

 - [About the tool	](#about-the-tool)

 - [Setup	](#setup)

 - [Datasets	](#datasets)

[Before we started	](#before-we-started)

[Create a Project	](#create-a-project)

[Import Files	](#import-files)

 - [Files	](#files)

 - [NCapture	](#ncapture)

[Text Coding	](#text-coding)

 - [Deductive Coding	](#deductive-coding)

 - [Inductive Coding	](#inductive-coding)

 - [Mixed Coding	](#mixed-coding)

 - [Parent & Child Code	](#parent--child-code)

 - [Uncoding	](#uncoding)

[Highlighter & Coding Stripes	](#highlighter--coding-stripes)

[Memos & Annotation	](#memos--annotation)

[Image Coding	](#image-coding)

[Save the Project	](#save-the-project)

[Audio & Video Coding	](#audio--video-coding)

[Case Classification & Cases	](#case-classification--cases)

[Query	](#query)

 - [Word Frequency Query	](#word-frequency-query)

 - [Text Search Query	](#text-search-query)

 - [Matrix Coding Query	](#matrix-coding-query)

[Export Codes	](#export-codes)

 - [Code List	](#code-list)

 - [Codebook	](#codebook)

 - [Individual Code	](#individual-code)

[Resources	](#resources)

# 

# Before we start

## Introduction

This tutorial is designed for the Windows version of NVivo 14\. If you are using a Mac device, check out here (coming soon). 

While Lumivero, the company who produces NVivo, has also released a Mac version, it currently includes fewer features than the Windows version. Therefore, it is recommended to use a Windows device for working with NVivo. To learn more about the differences between versions and platforms, see the comparison page [here](https://techcenter.qsrinternational.com/Content/nv12/TOC_older_client_versions.htm).

If you don’t have a device, the Windows computers in the Digital Hub in the 4th floor of the DKU Library have installed NVivo 14 (see [Public Devices](https://library.dukekunshan.edu.cn/public-devices/)). 

In the first half of the tutorial, we will work with open datasets(files) from the project [Data Center Energy Efficiency Focus Groups and Interviews](https://catalog.data.gov/dataset/data-center-energy-efficiency-focus-groups-and-interviews), conducted by U.S. Environmental Protection Agency. The raw data was collected between October 2014 and June 2015\. 

For the second half of the tutorial, we will use the sample project in NVivo. Data in this sample project is drawn from a two-year research study (2008-2009) undertaken by researchers from the Duke University Nicholas School of the Environment at the Duke Marine Laboratory in Beaufort, N.C. The study documented community perceptions of development and land-use change on coastal communities in the Down East area of Carteret County, North Carolina, USA.

By the end of this tutorial, you will understand how NVivo can be used in qualitative research​, and use NVivo to load information, code documents and media files, use cases, make notes, conduct queries, and export information.

For any questions about the NVivo 14, contact the Data and Visualization Librarian, Siti Lei ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)) for support. 

## About the tool

We will use NVivo 14 in this tutorial. Visit the [Qualitative Data Analysis guide](https://library.dukekunshan.edu.cn/qualitative-data-analysis/) for more information about NVivo.

## Setup

Follow the instructions in [Downloading, Installing and Licensing NVivo 14](https://library.dukekunshan.edu.cn/qualitative-data-analysis/) to download the NVivo 14 Windows version on your computer.

## Datasets

Download the sample datasets: [Workshop\_Files.zip](https://duke.box.com/s/91jya5x407qpdql8w1mptu70zqb3h00i)

# Before we started

1. Create a new folder in your computer and name it as **NVivo Workshop**.

<img width="681" height="323" alt="image" src="https://github.com/user-attachments/assets/85f8de07-7692-492b-8b38-3963b3db16e8" />


2. Download the sample dataset [Workshop\_Files.zip](https://duke.box.com/s/91jya5x407qpdql8w1mptu70zqb3h00i).

3. Unzip the file by right-clicking and select **Extra All**. Select where the files are extracted.

<img width="669" height="428" alt="image" src="https://github.com/user-attachments/assets/8d6c894d-02d8-4735-a147-37d03f58ad5b" />


4. Click on **Browse** if you need to adjust the saving path. Once it’s finished, click **Extract**.  
   * Alternatively, you might first install a great little program called [7-Zip](https://www.7-zip.org/) \-  that is helpful to use when working with zip files. Then you should be able to right-click on the zip file and select **7-Zip**, then **Extract** **Here** to extract its files

<img width="856" height="713" alt="image" src="https://github.com/user-attachments/assets/f1364bee-7f3a-416d-a61a-c03ab22665d6" />


5. Copy or move the unzipped sample data folder into the **NVivo Workshop** folder. 

<img width="846" height="295" alt="image" src="https://github.com/user-attachments/assets/81b23c69-c8e4-4bbb-8737-312690f63e89" />


# **Create a Project**

NVivo projects are saved **locally** on your computer. They are not automatically stored or synced to any cloud space, so remember to back up your files regularly.

1. Open NVivo 14 on your desktop. Then, click on **\+ New Project**. Note that NVivo runs locally in your device, so you don’t have to login to your NVivo account to use the software.

<img width="933" height="631" alt="image" src="https://github.com/user-attachments/assets/363435bb-1e76-4364-907d-7c346b1fc679" />


2. First, enter **NVivo Workshop** as the project title.

3. Click **Browse…** to choose where the project file will be saved. Select the **NVivo Workshop** folder we created in the previous section.

4. If the content you plan to analyze is not primarily in English, change the **Text content language** accordingly. Then click **Next** to continue.

<img width="949" height="602" alt="image" src="https://github.com/user-attachments/assets/a8977401-b0d8-444a-89b1-d0fa64788ff9" />


5. In the next pop-up window, review or adjust your saving options as needed, then click **Create Project** to continue.

<img width="950" height="596" alt="image" src="https://github.com/user-attachments/assets/b545c40e-4070-4be3-b1bb-c8d5c21ada08" />


6. When the welcome pop-up appears, click **SKIP TOUR** to close it.

<img width="707" height="475" alt="image" src="https://github.com/user-attachments/assets/1c0def21-16ef-4173-bd3a-7253d47fd01f" />


7. The interface of NVivo includes:  
   1) Ribbon  
   2) Navigation View  
   3) List View  
   4) Detail View  
   5) Find Bar  
   6) Quick Coding Bar  
   7) Status Bar

<img width="663" height="463" alt="image" src="https://github.com/user-attachments/assets/d3069b29-a569-48f1-8c41-f31fffcd5e24" />
 
*Image Source: [The workspace](https://help-nv.qsrinternational.com/14/win/Content/about-nvivo/nvivo-workspace.htm)*

# Import Files

NVivo supports the analysis of various qualitative data file types, including surveys, notes, emails, codebooks, reports, and more. 

## Files

1. Go to **Files** under **Data**, right-click on **Files** and select **New Folder…**.

<img width="461" height="276" alt="image" src="https://github.com/user-attachments/assets/0bb9f4d2-d232-48e7-82c6-0ad387771017" />


2. In the pop-up, enter **Interview** in the “Name” field, and click **OK**.

<img width="656" height="282" alt="image" src="https://github.com/user-attachments/assets/2043ccde-0b34-4ba4-9ec4-8f44be521433" />


3. Make sure the **Interview** under **Files** is selected, then go to the **Import** menu, click on **Files**.

<img width="953" height="325" alt="image" src="https://github.com/user-attachments/assets/cef3e668-c3c5-47ac-b5e8-c8035a2c32ec" />


4. Under ‘File Type’, make sure **Support Files** is selected.

<img width="938" height="286" alt="image" src="https://github.com/user-attachments/assets/5376ef21-c8cc-4559-a6fe-cf767979e65a" />


5. In the pop-up window, navigate to the workshop folder, open the Workshop\_Files folder, select all items that begin with “Interview”, and click **Import**.

<img width="933" height="691" alt="image" src="https://github.com/user-attachments/assets/36ae24e6-beab-4208-b9cf-74280180dfc7" />


6. Repeat the same steps for the focus group files. Create a new folder named **Focus Group**, then go to **Import** \> **Files** \> **Documents**. In the Workshop\_Files folder, select all items that begin with “FG”, and click **Import** to continue.

7. The **Interview** and **Focus Group** folders should now appear under **Files**. Double-click each folder to view all the imported documents within it.

<img width="788" height="432" alt="image" src="https://github.com/user-attachments/assets/f9cb5d6f-b93e-42a7-9c9e-ea0ae829df27" />


## NCapture

**NCapture** is a browser extension that allows collecting web and social media content for import into NVivo for qualitative analysis. Follow the instructions [here](https://help-nv.qsrinternational.com/20/win/Content/ncapture/ncapture.htm) to install and use NCapture, and to import captured files into NVivo.

# Text Coding

NVivo is a tool not only for qualitative data analysis but also for project management. It supports the entire qualitative research process from collecting and organizing materials to coding, analyzing, visualizing, and sharing results. 

While NVivo offers features such as auto-coding and visualization, researchers still **lead** the analysis and interpretation; NVivo is an assistive tool, not an automated one.

## Deductive Coding

Deductive coding is a top-down qualitative analysis approach where you start with a set of predefined codes, and then go through your files, applying those codes to the relevant snippets.

1. To create codes, click **Codes** under **Coding**, then click **Close** to close the introduction page.

<img width="936" height="478" alt="image" src="https://github.com/user-attachments/assets/a36e627c-9aef-44ba-be3d-16e3d5c449cb" />


2. Right-click on **Codes** under **Coding**, select **New Code…** from the menu.

<img width="482" height="199" alt="image" src="https://github.com/user-attachments/assets/6a3b6d1b-e64d-4bc7-b1e6-db1d66efae60" />


3. Enter **Energy** in the ‘Name’ field, then click **OK**. Our first code **Energy** is now created.

<img width="768" height="490" alt="image" src="https://github.com/user-attachments/assets/a612c663-a1fa-470f-a6a4-2323debebce3" />


4. Now, go to **Interview** under the **Files**. Double-click on **Interview dec4\_2014 2\_02pm** to open the file located at the top.

<img width="979" height="573" alt="image" src="https://github.com/user-attachments/assets/c18b5650-4ebf-4103-8ca1-475bc8936d88" />


5. Files imported into NVivo are automatically opened in protected mode, meaning they cannot be edited. To make changes, select **Edit** to turn on editing view.

<img width="504" height="243" alt="image" src="https://github.com/user-attachments/assets/0b54a203-f05f-418b-81a9-b45aa45455e0" />


6. Remember to uncheck it once you’re finished.

<img width="495" height="246" alt="image" src="https://github.com/user-attachments/assets/50128933-b599-43ae-95be-1a0b48c8eb33" />


7. Now, select a text snippet in the **Interview dec4\_2014 2\_02pm** file right-click, and select **Code Selection** from the menu.

<img width="531" height="170" alt="image" src="https://github.com/user-attachments/assets/60f18096-bf4a-4ea5-9ab9-a26b5c323b88" />


8. In the pop-up, select **Energy,** and click **Code Selection to ‘Energy’**.

<img width="506" height="694" alt="image" src="https://github.com/user-attachments/assets/cbbe6afc-06d1-4cbd-956b-469e5c9d104d" />


9. Select another snippet in the same file and right-click to open the content menu. This time, go to **Code to Recent Codes** \> **Energy**.

<img width="901" height="234" alt="image" src="https://github.com/user-attachments/assets/c436bd75-0310-4517-a4ed-ecba8e6d9217" />


10. Alternatively, if you have the **Codes** open in the navigation view, you can drag and drop the text snippet directly onto the corresponding code. Let’s try this method with another new snippet.

<img width="979" height="434" alt="image" src="https://github.com/user-attachments/assets/9045cb24-4f45-4932-a8b4-914577d16465" />


11. Go to **Codes** in the navigation view, you should see the **Imported Products** code has 1 file and 3 references.

<img width="556" height="202" alt="image" src="https://github.com/user-attachments/assets/315bfc97-e3c1-4938-9ead-fee50ba469fc" />


## Inductive Coding

Inductive coding is a bottom-up approach where you may want to read through the material first, let ideas and themes emerge naturally, and then create codes based on what you find in the data.

1. In the **Interview dec4\_2014 2\_02pm** file, select one text snippet and right-click, select **Code Selection…** from the menu.

<img width="796" height="193" alt="image" src="https://github.com/user-attachments/assets/c1b13fdc-1152-4d42-b958-02524ea789fe" />


2. Go to **Top-Level Code** under **Create New**.

<img width="445" height="617" alt="image" src="https://github.com/user-attachments/assets/52e6f0b0-923b-44d2-97fa-914d300f2be0" />


3. Enter **Cost** as the new code, and click **Code Selection to ‘Cost’**.

<img width="450" height="619" alt="image" src="https://github.com/user-attachments/assets/99d82c14-a8c7-485d-be12-d4a576854878" />


4. Select another snippet in the same file, code it to **Cost**.

5. Go to **Codes** in the navigation view, see the **Cost** code has 1 file and 2 references.

<img width="547" height="207" alt="image" src="https://github.com/user-attachments/assets/7ee587a4-8d1d-4f08-b4ea-9e393f2313f6" />


## Mixed Coding

Mixed coding combines deductive and inductive approaches. For example, you can start coding with some predefined codes and then add new ones as patterns and insights while reading through the data. 

## Parent & Child Code

Within NVivo, codes can be organized hierarchically by creating parent and child codes.

1. Go to **Interview** under **Files**, click on **Interview dec4\_2014 2\_02pm** to open the file.

2. Now, select a text snippet and right-click, select **Code Selection…** from the menu.

<img width="896" height="182" alt="image" src="https://github.com/user-attachments/assets/0b2f3c21-8093-4039-b65e-8b2e2d51630f" />


3. Select **Energy**, then click on **Child Code** on the right pane.

<img width="447" height="613" alt="image" src="https://github.com/user-attachments/assets/198565b7-7e3d-4aa0-9904-da0aa97e997c" />


4. Enter **Efficiency** as the new code, then click **Code Selection to ‘Efficiency’**.

<img width="450" height="619" alt="image" src="https://github.com/user-attachments/assets/b4fcc64b-9ec4-4905-a449-e980a00f9132" />


5. Repeat the same steps to create another 2 child codes under **Energy**: **Network**, **Air**, and code 2 snippets under each newly created child code.

6. Go to **Codes** in the navigation view. Click on the **\+** icon next to **Energy** \- 3 child codes will appear.

<img width="552" height="308" alt="image" src="https://github.com/user-attachments/assets/5bed19e4-b550-4b11-a392-5d690b413575" />


7. Double click on a code, the snippet will show up in the detail view with some quantitative information about each snippet.

<img width="979" height="308" alt="image" src="https://github.com/user-attachments/assets/deeb650b-93ac-47ec-b4bf-d64b355729ce" />


8. Now, although the 3 child codes (**Air**, **Efficiency**, **Network**) are underneath one parent code (**Energy**), the counts for **Files** and **References** are not aggregated \- this is because NVivo treats parent code and its child codes separately as defaults. 

<img width="576" height="318" alt="image" src="https://github.com/user-attachments/assets/2622865b-fa5b-43b2-b86d-3bd53db09428" />


9. To aggregate them, right-click on **Energy**, then **Code Properties**.

<img width="610" height="449" alt="image" src="https://github.com/user-attachments/assets/028d351c-fed4-40a8-af24-046f03d2b936" />


10. Check **Aggregate coding from children**, and click **OK**.

<img width="703" height="410" alt="image" src="https://github.com/user-attachments/assets/4ac6b07b-ab77-42bb-b7b0-c523caf0bb5a" />


11. The count of files and references of **Energy** should be updated with the total counts.

<img width="551" height="295" alt="image" src="https://github.com/user-attachments/assets/56b67d30-ceae-45ed-afdb-44224463d4a2" />


## Uncoding

Uncoding means removing a coded snippet from a code that disconnects that piece of data from the theme or category it was assigned to.

1. Double-click on **Network** code \- the snippet of coded text will show up.

<img width="494" height="282" alt="image" src="https://github.com/user-attachments/assets/3375044b-b198-4c0b-89c8-4243e1afcc57" />


2. Select the entire of one snippets, right-click, then select **Uncode From This Code**.

<img width="689" height="405" alt="image" src="https://github.com/user-attachments/assets/a8a482a3-2c82-439f-821d-d53661e7ec33" />


3. The coded text will now be removed. Next, click the **×** on each of the file title tabs to close all open windows.

<img width="726" height="286" alt="image" src="https://github.com/user-attachments/assets/8bc80cc9-8bf6-4f62-82c8-052e62a56bbd" />


# Highlighter & Coding Stripes

The highlighter and coding stripes help visualize and track your coding work in NVivo.

1. Go to **Interview** under **Files**, double-click on **Interview dec4\_2014 2\_02pm** to open the document.

2. In the detail view, click on the highlighter icon, and select **All Coding**.

<img width="256" height="300" alt="image" src="https://github.com/user-attachments/assets/c7988caa-2e4c-4df7-9bbb-65392853e495" />


3. The snippet you’ve coded will be highlighted in yellow.

<img width="831" height="350" alt="image" src="https://github.com/user-attachments/assets/aa998369-dffb-4989-8473-07332c896d52" />


4. In the detail view, click on the coding stripes icon, and select **All**.

<img width="424" height="267" alt="image" src="https://github.com/user-attachments/assets/0f81e43e-006b-43ae-ac48-40209c565fed" />


5. Now, a new pane with multiple colored bars alongside the file shows which part of the text has been coded and which codes were applied.

<img width="840" height="623" alt="image" src="https://github.com/user-attachments/assets/b33724aa-69a1-4180-b170-c45c66af5d86" />


6. To change the color of each code, go to **Codes** under **Coding**, select **Energy** code and right-click, go **Color**, and select **Red** as the new color.

<img width="816" height="547" alt="image" src="https://github.com/user-attachments/assets/2baa2092-d82e-408c-91c2-cdb27a648c10" />


7. Repeat the same steps and change the colors of the Cost code to a color other than red.

8. Now, click the coding stripes icon again, and select **Item Colors**.

<img width="370" height="469" alt="image" src="https://github.com/user-attachments/assets/09e24ed8-95c7-47aa-b8c8-92d9e72ead4d" />


9. The color of each code now will appear as the color you selected.

<img width="245" height="664" alt="image" src="https://github.com/user-attachments/assets/43093dce-6b61-4f07-92e9-6936a41317ed" />


10. Let’s turn off the coding stripes and highlighter by clicking both icons and selecting **None** for now, and close the **Interview dec4\_2014 2\_02pm** file.

<img width="266" height="329" alt="image" src="https://github.com/user-attachments/assets/e09bca7d-edf1-4e8b-a1af-8e5940255873" />


# Memos & Annotation

Memos and annotations help capture your thoughts and insights during analysis. Memos record broader reflections about your data, codes, or project, while annotations act as in-line comments attached to specific text or sections.

1. To create a memo, go to **Interview** under **Files**, right-click on **Interview dec4\_2014 2\_02pm**. Then, **select Link to New Memo…**.

<img width="907" height="455" alt="image" src="https://github.com/user-attachments/assets/b282b1ea-6e46-4bf6-a252-f6f8593e2416" />


2. Enter **Interview Memo** as the name and click **OK**.

<img width="673" height="492" alt="image" src="https://github.com/user-attachments/assets/71902624-de85-4436-a0c8-cd226e035fb5" />


3. A blank page will appear where a detailed memo about the file can be written. For example, noting the interview was conducted in a noisy cafe shop. You can note that here.

<img width="736" height="212" alt="image" src="https://github.com/user-attachments/assets/f99f1222-10e4-4615-a27b-f0a1cd5c31cf" />


4. Once you close the window, the memo will be automatically saved and linked to this file. You should see a small icon next to the interview in the list for the memo link when you have the interview list opened completely (with no other files open to the right of it). 

<img width="812" height="299" alt="image" src="https://github.com/user-attachments/assets/bbc9ea00-e204-45f3-a704-e804584c7089" />


5. To view the memo link, right-click on the file again, select **Memo Link** and then **Open Linked Memo**.

<img width="881" height="593" alt="image" src="https://github.com/user-attachments/assets/97f66c9c-5e68-492c-b78e-5b4997aea5ab" />


6. To create an annotation for a snippet, go to **Interview** under **Files**, double-click on **Interview may13\_2015**.

<img width="830" height="530" alt="image" src="https://github.com/user-attachments/assets/6afae701-0454-4d4b-b4b0-0a7adb77256d" />


7. In the detail view, select a text snippet, then select **New Annotation**.

<img width="842" height="288" alt="image" src="https://github.com/user-attachments/assets/f8d08130-5951-4ead-a90f-12be8e444394" />


8. A new box will appear at the bottom. Enter your annotation for this snippet. For example, “This part hasn't been cleaned yet.” Click anywhere outside of the box to save the annotation.

<img width="685" height="209" alt="image" src="https://github.com/user-attachments/assets/8b9e00c0-7d39-4e04-9943-10ed20d49a4f" />


9. To see memos and annotations you have created all in one place, using the left navigation menu, under **Notes**.

<img width="422" height="235" alt="image" src="https://github.com/user-attachments/assets/1bf8ea5c-8722-4bc6-9792-9f0370cbd0aa" />


10. Finally, you can also create a note that applies to the entire project, for example, maybe some ideas you have about how the research is going or new themes that are emerging. Right-click on **Memos** and select **New Memo**.

<img width="638" height="188" alt="image" src="https://github.com/user-attachments/assets/f2f8115e-3225-4e2c-a820-14b960a141e5" />


11. Give it a name, such as **Project Memo** and click **OK**.

<img width="911" height="609" alt="image" src="https://github.com/user-attachments/assets/7d1dba68-19fc-49c0-93b2-cf2d06dd5d7b" />


12. Type some notes, such as “The project needs to be reviewed” and then close it to save. You can always double click on it from the list of memos to re-open it.

<img width="855" height="242" alt="image" src="https://github.com/user-attachments/assets/595903e6-8583-4c53-8e7d-9e6954ebe3d4" />


# Image Coding

NVivo allows analyzing visual data by selecting and coding specific areas within an image. You can zoom in, highlight relevant parts of an image, and assign them to existing or new codes, making it possible to integrate visual analysis alongside textual and audio data within the same project.

1. Go to **Files** and click on **FG1 Questionnaire 14** to open the PDF file.

<img width="979" height="300" alt="image" src="https://github.com/user-attachments/assets/fba10c70-6e63-4943-9c27-efef75a70f2b" />


2. Note that NVivo 14 does not support **Optical Character Recognition (OCR)**. If your image files contain text that you want to code, make sure they are OCR-processed before importing them into NVivo. For text that cannot be OCRed (like handwriting or signatures), you can manually draw a square around the area you wish to code.

3. Under the **PDF** menu, select **Region**.

<img width="445" height="218" alt="image" src="https://github.com/user-attachments/assets/dc2d25d7-dcd0-4c4b-b2bc-872f9034e5d7" />


4. Draw a square around the area you want to code, then right-click and select **Code to Recent Codes**, then **Energy (Codes)**.

<img width="951" height="217" alt="image" src="https://github.com/user-attachments/assets/7ca0ba16-95da-4bca-bd17-23567ec16031" />


5. Now, go to **Codes** and double-click on **Energy**. In the detail view, instead of showing the image snippet, NVivo will display the coordinates of the selected image area. (On Mac, this will appear as a screenshot of the selected region.)

<img width="821" height="460" alt="image" src="https://github.com/user-attachments/assets/b29169e5-cea4-4dc3-bce0-b4a9eb251bcd" />


# **Save the Project**

1. During your work, the **Save Reminder** pop-up will appear periodically to remind you about the saving. Click **Yes** to confirm.

<img width="607" height="274" alt="image" src="https://github.com/user-attachments/assets/117cc2ad-e728-4da5-98dd-ebab1b79e546" />


2. When you are done working on a project it is important to remember to save manually. First, go to the **File** menu.

<img width="748" height="225" alt="image" src="https://github.com/user-attachments/assets/28b61042-be30-4b3f-82cf-5dad258aca6f" />


3. Select **Save** to save the current project.

<img width="866" height="401" alt="image" src="https://github.com/user-attachments/assets/cbc72e38-9d36-4ccb-a535-d96bd06cc3a6" />


4. Alternatively, you can save a project by clicking on the floppy disk icon on the top right of the menu bar, or pressing **CTRL+S** on your keyboard.

<img width="930" height="118" alt="image" src="https://github.com/user-attachments/assets/ad8540e4-62a6-465d-91f3-3210b0eff725" />


5. Finally, you can close a project to return to the NVivo main screen. Once your project is saved, go back to the **File** menu and select **Close**.

<img width="883" height="442" alt="image" src="https://github.com/user-attachments/assets/9c3197b2-e8b5-4bb1-a88e-d5fbc9d9585f" />


# Audio & Video Coding

NVivo allows the import and analysis of audio and video files through coding specific time segments within those recordings. 

Please note that the **Transcription** feature in NVivo is not included in our software license; however, transcription can be done using alternative tools such as the **Dictate** feature in Microsoft Word.

1. From the main screen, click on **Sample Project (Multi-method)**. We will use this sample project for the rest of the workshop.

<img width="825" height="396" alt="image" src="https://github.com/user-attachments/assets/edf42407-3cbb-457f-9a04-b4f9034a6bac" />


2. When the welcome pop-up appears, click **SKIP TOUR** to close it.

<img width="697" height="485" alt="image" src="https://github.com/user-attachments/assets/0f04cf93-1e11-4461-87a3-8316559301c6" />


3. Go to **Files**, then **Interviews** folder. Double click to open the **Betty and Paul** file \- this is a video recording from an interview.

<img width="640" height="439" alt="image" src="https://github.com/user-attachments/assets/374a90df-9245-4cbc-b126-fc7d509b76b7" />


4. Opening this video recording gives us three panels: the audio waveform, the video playback window, and a content panel showing timestamps along with the transcript. Note that the layout may vary depending on the video \- some files may not include a transcript or have timestamps.

<img width="831" height="624" alt="image" src="https://github.com/user-attachments/assets/eb8fa2ae-2202-4ca8-a471-38068d4ecae0" />


5. Now, go back to the **Interviews** folder, double-click on the **Helen** file \- this is an audio format file. 

<img width="690" height="496" alt="image" src="https://github.com/user-attachments/assets/b6581961-7225-4e57-ae70-77d6e6dc373a" />


6. Unlike the video format file, the audio recording gives us two panels: the audio waveform and a content panel showing timestamps along with the transcript. 

<img width="916" height="641" alt="image" src="https://github.com/user-attachments/assets/7cbadba7-80f7-4fe5-94ed-18dfbc423219" />


7. To code the segment, drag the **playhead** in the waveform window to the starting point, then click the **Start Selection** icon at the bottom to begin selecting the segment.

<img width="720" height="217" alt="image" src="https://github.com/user-attachments/assets/2c5c39a6-e63b-4587-b984-c5b58bc642fc" />


8. When it ends, click the **Finish Selection** icon to complete the coding range.

<img width="722" height="223" alt="image" src="https://github.com/user-attachments/assets/eb275c0f-f4b7-4f02-ba48-5c9499960c4d" />


9. Then, right-click and select **Code Selection**. 

<img width="685" height="413" alt="image" src="https://github.com/user-attachments/assets/5643ffad-3088-4f09-b646-71b3aafca594" />


10. Select the code. For example, let’s select **Memorable quotes** in this case, and click **Code Selection to ‘Memorable qu…’** to confirm.

<img width="422" height="567" alt="image" src="https://github.com/user-attachments/assets/bb6eb6c2-ad51-41f0-a9eb-d2efee69e25d" />


11. Go to **Codes**, **Memorable quotes**. The timestamp of the segment we just coded will appear.

<img width="995" height="606" alt="image" src="https://github.com/user-attachments/assets/cefa0792-b5d5-4cf5-b0c1-98f27be66ca3" />


12. To uncode a segment, click on the segment reference and go back to the source file.

<img width="622" height="204" alt="image" src="https://github.com/user-attachments/assets/5d805391-48bc-413f-a619-f37ac478c451" />


13. From the audio wavement, locate to the coded segment, right-click it and select **Uncode** from the menu.

<img width="676" height="283" alt="image" src="https://github.com/user-attachments/assets/c529f69e-9c1d-4251-a174-9427412e9641" />


14. Select and check **Memorable quotes** from the pop-up, and click **OK**.

<img width="979" height="429" alt="image" src="https://github.com/user-attachments/assets/83915421-59a1-4a82-8b4b-1a274d699d51" />


15. Now the coded segment should be removed.

16. Audio coding follows the same steps as video coding.

# Case Classification & Cases

Cases are a special type of code that represents the individuals in your study. If you have demographics or other important attributes that you want to incorporate into your study, case classifications and cases can help. For example, if you were analyzing interview transcripts, you might want to create a case classification called “Person” with attributes such as their name, age, education, job title, etc. Once your case classification is in place that defines what characteristics you want to capture for your interviewees, you could then create one case for each interviewee with those attributes filled in. 

For example, if you interviewed someone named Barbara, you would create a case called BARBARA (or some ID number if needed for confidentiality) with information about Barbara. You would then use that Barbara case to code all the imported content that are associated with Barbara (where the case acts like a code). Later you can then run queries that incorporate that information to answer questions such as, does Barbara talk more about the environment?

You can manually create case classifications and cases by using the left menu, under **Cases**. You can right click on **Case Classification** and **Create a New Classification** or right click on cases to create a new case. But often times, it is easier and more common to upload a spreadsheet with all the information for the cases. We are not going to try that out in this tutorial, but will show you how that would look like.

1. Under **Cases**, go to **Cases**, then **People.** Expand **Interview Participants** \- this will give us a list of interview participants.

<img width="979" height="673" alt="image" src="https://github.com/user-attachments/assets/c47202d6-a0fa-4f4e-b3aa-0851be7065b3" />


2. Right-click on the name **Barbara**, select **Open Classification Sheet**.

<img width="979" height="404" alt="image" src="https://github.com/user-attachments/assets/e4c8e097-9bd7-4606-8b8f-bf10a12a4607" />


3. A table of all the information about the participants will appear, with different attributes about their background, like the neighborhood they live in, their gender, age range, etc. You can edit the data here.

<img width="979" height="595" alt="image" src="https://github.com/user-attachments/assets/21628576-c97c-4138-9de6-512df4d68bc3" />


4. We can take advantage of NVivo’s autocoding features to identify the parts of interviewee and interviewers in a file and code them automatically into the appropriate case. Using the left menu, under **Data**, then **Files**, go to the **Interviews** folder and right-click on the interview transcript titled “Barbara”. Select **Autocode…**.

<img width="979" height="473" alt="image" src="https://github.com/user-attachments/assets/11159aa4-2fbe-429f-9d6e-182edfd5b149" />


5. A wizard with different autocoding features will appear, which I encourage you to explore on your own. For now, let’s select the **Speaker name**. This is going to automatically code text based on the speaker name. Then click **Next**.

<img width="746" height="661" alt="image" src="https://github.com/user-attachments/assets/1871c00c-bd07-425c-8821-a2bb667d6c72" />


6. The “Barbara” document is formatted in a consistent manner so we can always pick out who is speaking because the person’s name is bolded followed by the words they speak. We need to specify who the unique speakers are in this document. Under **Enter all speakers**, type in **HENRY** and hit **Enter**. Then type in **BARBARA** and hit the **TAB** key. You should check the preview below to confirm that NVivo is picking up each unique speaker by highlighting them in different colours. If it looks correct, click on **Next**.

<img width="620" height="592" alt="image" src="https://github.com/user-attachments/assets/f6432558-0cce-47c6-a032-bd843f2bfee2" />


7. Make sure **Add to existing classification** is selected and from the drop-down next to it, **Person** is selected. Then click on **Finish**. This should code everything that Henry or Barbara said in the transcript with their cases.

<img width="652" height="588" alt="image" src="https://github.com/user-attachments/assets/722ab68e-d9b2-4770-9515-455daa9ff1f4" />


8. Go to **Cases**, then go to **Cases**. 

<img width="373" height="168" alt="image" src="https://github.com/user-attachments/assets/f89a26bc-3be4-4b3e-81b4-e79de4156318" />


9. Double click on the **BARBARA** case. You should see everything that Barbara said in her interview. These words are coded to this case. The BARBARA case code is now linked to Barbara’s interview responses.

<img width="979" height="492" alt="image" src="https://github.com/user-attachments/assets/03f3c2df-d030-45ab-afe9-1adecc848bfd" />


10. Close all the tabs.

# Query

Instead of manually searching through large volumes of coded material, queries in NVivo are powerful tools that help you to quickly grab insight from the data by solving specific questions about your data such as how often certain words/phrases/themes appear, which participants expressed particular attitudes, or how concepts overlap.

This tutorial will not go through all of them in this workshop, but if you are interested in learning more, visit Windows version’s [Queries](https://help-nv.qsrinternational.com/14/win/Content/queries/queries.htm) page for additional resources. 

## Word Frequency Query

Word frequency query allows you to identify and analyze the most frequently used words across your sources.

1. First, let’s see what are the options we have. Go to the **Explore** menu to see all available query options. 

<img width="979" height="112" alt="image" src="https://github.com/user-attachments/assets/d9c12183-29a7-422a-91d7-0f448e9cf15c" />


2. For Windows users, NVivo includes a feature called the **Query Wizard**, which assists in choosing the right query for your task and breaks down each option to help you understand how it works. Let’s try that first. Click on **Query Wizard**.

<img width="530" height="280" alt="image" src="https://github.com/user-attachments/assets/25d988a2-3d24-4947-83e3-64551a3a76ef" />


3. The pop-up gives 4 options corresponding to the four query types. Let’s select the second option \- **Word Frequency** query, which is described as “Identify frequently occurring terms in content.” You can also use Work Frequency query by clicking on **Work Frequency** under the **Explore** menu.

<img width="795" height="395" alt="image" src="https://github.com/user-attachments/assets/7f92b73a-a2cc-429a-915b-889a3d0638a6" />


4. But now, let’s use **Query Wizard**. Select the second option, and click **Next**.

<img width="817" height="586" alt="image" src="https://github.com/user-attachments/assets/c2111ac7-16fe-4983-9079-58199c876e30" />


5. Set the “Display Words” field to 50, and keep the “Minimum Word Length” field set to 3\.

<img width="825" height="593" alt="image" src="https://github.com/user-attachments/assets/f4a9307c-d1b5-49a9-9d2c-335c55dd7282" />


6. The **Grouping** option helps identify and organize similar or related terms in your text data to varying degrees. Same stem means words that share the same root or base form \- for example, talk, talking, talks, and talked all share the stem “talk.” Now, drag the bar to the second level, which groups words by the same stem, and click **Next**.

<img width="794" height="566" alt="image" src="https://github.com/user-attachments/assets/f4a111d9-5d40-4971-bcf9-5118a456bf6e" />


7. For the query scope, check **Selected Items**, then click on **Select…**

<img width="796" height="570" alt="image" src="https://github.com/user-attachments/assets/cba6959a-7434-4426-8b94-a310986c2f11" />


8. In the pop-up, expand **Files**, then click on **Interviews** to select everything in the folder. Next, unselect 2 videos and 1 audio files (with different icons) so that only text transcripts should be selected for our search. Click **OK**.

<img width="979" height="431" alt="image" src="https://github.com/user-attachments/assets/ace40832-9b92-4f54-bb75-5cb36ea42626" />


9. Click **Next**.

<img width="814" height="584" alt="image" src="https://github.com/user-attachments/assets/219f9d17-3fd9-4bd7-981a-ebd6654498aa" />


10. The last window asks you if you just want to run the query once or if you want to save it in your project so that you can later revisit. Let’s leave it as defaults for now and click **Run**.

<img width="814" height="587" alt="image" src="https://github.com/user-attachments/assets/9bde35a7-11ad-4990-91b4-bf7f99480542" />


11. Now we should see the results of our query.

<img width="771" height="613" alt="image" src="https://github.com/user-attachments/assets/90d0aff0-27e7-4a3c-b9ec-45de1c264ffc" />


12. Double-click on the word **people**, you will see the location of where the **people** appeared across all of the selected text transcripts.

<img width="834" height="559" alt="image" src="https://github.com/user-attachments/assets/89780b9d-4357-4b93-8c98-54d2c664466c" />


13. Go back to the **Word Frequency Query Results**, and you will find out that words like ‘a’, ‘and’, ‘the’ are ignored \- these words are treated as **stop words**, which are those really common words and won’t be useful for analysis. When you see a word in the list and you don’t think they’d be helpful, for example, the word ‘things’, you can right-click on ‘things’ and select **Add to Stop Words List**.

<img width="534" height="221" alt="image" src="https://github.com/user-attachments/assets/9514dd16-e471-4074-8f4b-8bf8f0b515ed" />


14. To check or reset the Stop Words List, go to **File** menu, click on **Project Properties**.

<img width="454" height="218" alt="image" src="https://github.com/user-attachments/assets/6f170f9e-f6bb-4f5f-a845-87c4e9eef56c" />


15. Under the **General** tab, you can select text content languages. The default is English (US), but you can switch to other languages. Then, click on **Stop Words…** to see the current list in use. 

<img width="725" height="550" alt="image" src="https://github.com/user-attachments/assets/995ae5b2-d003-4a84-94c8-20aa8dff1b1b" />


16. From here, you can add stop words manually, or reset the list. But for now, let’s click **Cancel**, then **Cancel** again to close the two pop-ups and return back to the result list.

<img width="723" height="558" alt="image" src="https://github.com/user-attachments/assets/350641cf-979d-494d-a6a8-a5b3f1b50653" />


17. Now let's export the list since we only selected **Run the query for once** in the past step. To do that, right-click on any word in the list, and select **Export List**. 

<img width="873" height="556" alt="image" src="https://github.com/user-attachments/assets/af2d8ee4-59e0-4cae-8ef4-cf7e9df26724" />


18. Browse to the workshop folder, give the file a name or keep the default and click on **Save**.

<img width="788" height="570" alt="image" src="https://github.com/user-attachments/assets/7c777ecd-3799-4732-a4d6-360b186a59c0" />


19. NVivo provides several visualization options for word frequency results. For example, click **Word Cloud** in the side tabs to view your results as a cloud.

<img width="801" height="533" alt="image" src="https://github.com/user-attachments/assets/497663fd-cb7c-42f6-8772-b3329fba8bd5" />


20. Under the **Word Frequency Query** menu, you can choose to use another color palette and font style.

<img width="719" height="172" alt="image" src="https://github.com/user-attachments/assets/86311481-b2f2-40bd-91e2-9efea7e4e60b" />


21. Right-click on the visual and select **Export Word Cloud** to save the word cloud in your computer.

<img width="602" height="309" alt="image" src="https://github.com/user-attachments/assets/615aab22-7ab5-4933-a142-614a7d132f83" />


22. Try out the **Tree Map** to see block-sized proportions by term.

<img width="787" height="579" alt="image" src="https://github.com/user-attachments/assets/095785dc-8024-48a7-9801-a7192379b713" />


23. Next, try out the **Cluster Analysis** to view relationships between terms.

<img width="800" height="631" alt="image" src="https://github.com/user-attachments/assets/6a596f2e-fafb-41b1-b682-43b594f7541a" />


24. Close the query to return to the main workspace for now.

<img width="775" height="168" alt="image" src="https://github.com/user-attachments/assets/264be9c2-3507-4da3-afba-844eaeb5df1e" />


## **Text Search Query** 

Text Search Queries allow you to search for specific words or phrases across your project items.

1. Go to the **Explore** menu and select **Text Search Query**.

<img width="558" height="189" alt="image" src="https://github.com/user-attachments/assets/da9cad72-c45a-4e77-9901-e11c4f91f04a" />


2. Keep the search scope as **Files & Externals** \- this includes all imported files in your project. In the search box, enter **water**, and drag the slider to **With stemmed words**.

<img width="979" height="264" alt="image" src="https://github.com/user-attachments/assets/9cbd7e4c-245d-4043-bb74-b5b2e563dc63" />


3. Click **Run Query**.

<img width="979" height="264" alt="image" src="https://github.com/user-attachments/assets/828a3d29-67c9-405f-b959-8ce42736eb65" />


4. A list of files containing the word **water** and its stemmed forms will appear. Double-click **Charles** to view the details.

<img width="795" height="593" alt="image" src="https://github.com/user-attachments/assets/c3ed0a6f-b138-4f47-90f4-08d8dd12e1ea" />


5. In Charles’s interview transcript, you will see the term **water** highlighted.

<img width="882" height="549" alt="image" src="https://github.com/user-attachments/assets/e86a6981-e6b5-4443-adfe-c5520d26e09e" />


6. We can store the results of this query as a new code. To do so, go back to the **Text Search Query – Results Preview** tab and click **Save Results…**. 

<img width="979" height="264" alt="image" src="https://github.com/user-attachments/assets/7019d7a3-cc31-4183-bd23-8cdf5c7e6302" />


7. In the pop-up, click **Select** next to the **Location** field. 

<img width="755" height="361" alt="image" src="https://github.com/user-attachments/assets/bf524f2c-721e-43e8-9291-7a71aa392e03" />


8. Choose **Codes**, then click **OK**.

<img width="500" height="483" alt="image" src="https://github.com/user-attachments/assets/6d192b89-e79d-4e92-aa9c-0979882fcdd8" />


9. Rename the **Name** field to **Water**, and click **OK** again.

<img width="616" height="296" alt="image" src="https://github.com/user-attachments/assets/c60eb100-64e0-48e2-a621-4a1bf1e7df1d" />


10. Go to **Codes** in the navigation view. You will see a new code named **Water**, showing the corresponding files and reference counts from the query.

<img width="798" height="350" alt="image" src="https://github.com/user-attachments/assets/03f071b5-7ff1-4b85-a267-10a88140c254" />


11. If your search phrase contains multiple words, make sure to enclose it in quotation marks (“”). Otherwise, NVivo will treat each word as a separate search term. For example, enter “salt water” in the search box and click **Run Query** again.  
    * For more tips about building search query, visit [Text Search Query](https://help-nv.qsrinternational.com/14/win/Content/queries/text-search-query.htm) page.

<img width="979" height="371" alt="image" src="https://github.com/user-attachments/assets/14ade321-edd5-4164-8c85-ea39a1424731" />


12. Let’s say you want to save this query for future use. To do so, click **Save Criteria…**.

<img width="979" height="223" alt="image" src="https://github.com/user-attachments/assets/f31aa46b-af3d-4b81-91bf-9ec021e75030" />


13. Name the query as **Salt Water**, and click **OK**.

<img width="755" height="687" alt="image" src="https://github.com/user-attachments/assets/6d9349e3-1867-47c5-b226-d57e5e5a4523" />


14. Then, close the query tab.

<img width="833" height="172" alt="image" src="https://github.com/user-attachments/assets/ea32b86c-d50d-49d9-8df3-e54beb354827" />


15. Go to **Queries** in the navigation menu. Under **Query Criteria**, you can find **Salt Water** in the list. Double-click **Salt Water** to reopen the query we just saved.

<img width="979" height="364" alt="image" src="https://github.com/user-attachments/assets/b27d3479-947b-4c45-ab8f-1391f57f97ca" />


## **Matrix Coding Query**

Matrix Coding Query allows you to compare coding across multiple dimensions, such as codes, cases, or attributes, to identify patterns and relationships in your data. The results are displayed as a matrix table, where rows typically represent cases or participants and columns represent codes or themes. Each cell shows the number of references or the amount of coding coverage where the two dimensions intersect. 

For example, we can look at attitudes expressed by different interviewees based on what they said during the interviews. To run this query, we will use the code “Attitude” and the case “Interview Participants."

1. Go to the **Explore** menu and click **Matrix Coding Query**.

<img width="625" height="213" alt="image" src="https://github.com/user-attachments/assets/4976dd3e-f681-48f5-a1fe-2186306017f9" />


2. Under **Cases**, open **People**. In the list view, click the **\+** icon next to **Interview Participants** to expand the name list.

<img width="893" height="665" alt="image" src="https://github.com/user-attachments/assets/d7f4c676-12d4-4cd9-a48f-8f4650a6eb77" />


3. Select all participant names by dragging your cursor over them, then drag the selection into the **Rows** box.

<img width="979" height="533" alt="image" src="https://github.com/user-attachments/assets/78df278e-1803-4a58-89de-667d624b168f" />


4. Next, under **Codes**, expand **Attitude** by clicking the **\+** icon.

<img width="933" height="576" alt="image" src="https://github.com/user-attachments/assets/2c76e8bf-356c-46c0-93ab-f9271588c05a" />


5. Select all items under the **Attitudes** code and drag them into the **Columns** box.

<img width="979" height="534" alt="image" src="https://github.com/user-attachments/assets/12f7ee13-7cc8-46b9-bb32-8c473e13a24c" />


6. Make sure the search scope is set to **Files & Externals**, then click **Run Query**.

<img width="969" height="345" alt="image" src="https://github.com/user-attachments/assets/30c32bf6-17d2-427d-9aa4-eae930b08636" />


7. A matrix table will appear, showing the number of times participants mentioned words related to each attitude.

<img width="964" height="688" alt="image" src="https://github.com/user-attachments/assets/6256e2c0-d2c3-4a04-8828-d9477bc8c3f7" />


8. At the top-left of the page, click the **purple gradient palette** icon to apply color coding for easier visualization.

<img width="921" height="657" alt="image" src="https://github.com/user-attachments/assets/a315710d-5f74-4313-820e-ef00eab89568" />


9. The table currently shows the total count of files where participants mentioned each attitude. To change the view, right-click anywhere on the table, select **Cell Content**, **Words Coded**.

<img width="979" height="387" alt="image" src="https://github.com/user-attachments/assets/54cb56d6-7baf-4fad-b9c8-402e3858b8bd" />


10. This view displays the total count of coded words for each participant and attitude.

<img width="830" height="379" alt="image" src="https://github.com/user-attachments/assets/346728cc-becd-4d59-98ae-ec01d47b8fc5" />



11. Try another view: right-click again, choose **Cell Content**, **Coding Presence**.

<img width="943" height="368" alt="image" src="https://github.com/user-attachments/assets/4f8ca574-8d80-4e10-8c04-0249b0bea03c" />


12. The table now shows **Yes** or **No**, indicating whether a participant mentioned that attitude or not.

<img width="837" height="383" alt="image" src="https://github.com/user-attachments/assets/1c53013b-d784-4b74-af3c-c2d137625d9b" />


13. To improve readability, right-click once more, select **Cell Shading**, **Green-Yellow-Red**.

<img width="942" height="351" alt="image" src="https://github.com/user-attachments/assets/bf75f79b-6dd3-4713-b76b-da7db7649b85" />


14. The table now shows **Yes** in green and **No** in red.

<img width="776" height="352" alt="image" src="https://github.com/user-attachments/assets/e134fad0-162b-4af1-bd00-2abe128d9106" />


15. You can select other visualization. Let’s click on the **Chart** tab to explore this visualization.

<img width="944" height="413" alt="image" src="https://github.com/user-attachments/assets/9fdee341-b13e-4a9b-ad9c-731a21f05411" />


16. While 3D visualizations may look appealing, they can distort data interpretation and obscure important details. For clearer and more accurate results, consider exporting the query data and visualizing it using dedicated tools. See the [Data Visualization](https://library.dukekunshan.edu.cn/data-visualization/) guide for more information.

17. When finished, close the query tab to return to the main workspace.

<img width="861" height="188" alt="image" src="https://github.com/user-attachments/assets/b3e5dbfa-b4b1-4308-9671-915071f28676" />


# **Export Codes** 

When your analysis is complete, you can export your codes from NVivo in various formats \- as a code list, a codebook, or individual code files.

## **Code List** 

1. Go to **Codes** under **Coding** and make sure the list of codes is open.

2. From the **Share** menu, select **Export**, **Export List**.

<img width="873" height="458" alt="image" src="https://github.com/user-attachments/assets/5599bfec-9fae-44a7-a019-c7bbb1a0bd08" />


3. Keep the default file name (**Codes**), choose your workshop folder as the save location, and click **Save**.

<img width="857" height="632" alt="image" src="https://github.com/user-attachments/assets/4fe559e2-5bcc-4b7c-b6d5-18e8c39f2101" />


4. Open the **Codes.xlsx** file in your workshop folder. You should see a list of all codes displayed in NVivo’s code list.

<img width="979" height="506" alt="image" src="https://github.com/user-attachments/assets/435af290-3549-4fe5-9195-b763bbcf623d" />


## **Codebook**

1. Go to **Codes** under **Coding** and make sure the list of codes is open.

2. From the **Share** menu, select **Export**, **Export Codebook**.

<img width="829" height="422" alt="image" src="https://github.com/user-attachments/assets/cdbac5dd-d274-4435-b38b-35157f0b4999" />


3. Keep the default file name (**Codebook – Environmental Change Down East**), check **Include number of files and references**, and click **OK**.

<img width="624" height="643" alt="image" src="https://github.com/user-attachments/assets/fd8af6b2-51ec-46f9-9014-c00ea1adc77e" />


4. Open the **Codebook – Environmental Change Down East.doc** file in your workshop folder. This file displays each code with its description, and the counts of files and references associated with it.

<img width="979" height="552" alt="image" src="https://github.com/user-attachments/assets/03d86ca3-97c7-4e8a-9910-dccb28273569" />


## **Individual Code** 

1. Under **Codes**, select one or more codes to export.

2. Right-click on the selected area and choose **Export,** **Export Codes**.

<img width="902" height="349" alt="image" src="https://github.com/user-attachments/assets/c2aaa44b-7684-4bbd-89c0-d7391ee35833" />


3. In the **Export Options** pop-up, check **Summary View**, then click **OK**.

<img width="527" height="662" alt="image" src="https://github.com/user-attachments/assets/bce17436-f0a0-4169-a514-24b365fd3dd0" />


4. Each selected code will be saved as a separate file in your workshop folder. For example, opening the **Water** file will display the related reference files, their locations, reference counts, and coverage.

<img width="979" height="508" alt="image" src="https://github.com/user-attachments/assets/0056130c-480d-4e03-942c-acbc14cb4010" />


# **Resources**

## **Qualitative Research Theory**

* [SAGE Qualitative Research Methods](https://methods.sagepub.com/book/edvol/sage-qualitative-research-methods/toc) \[Online Book\]​  
* [The Essential Guide to Coding Qualitative Data](https://delvetool.com/guide) by Delve​

## **NVivo**

* [NVivo Tutorials](https://lumivero.com/resources/support/getting-started-with-nvivo/nvivo-tutorials/) by Lumivero​  
* [Lumivero Community](https://lumivero.com/resources/support/getting-started-with-nvivo/nvivo-tutorials/) for browsing resources, sharing knowledge, connecting with other NVivo users.​  
* [Transcribe your recordings](https://support.microsoft.com/en-gb/office/transcribe-your-recordings-7fc2efec-245e-45f0-b053-2a97531ecf57) in Microsoft Word​  
* [What is optical character recognition (OCR)?](https://www.ibm.com/think/topics/optical-character-recognition) By IBM

## **Support**

If you have any questions about the tool or this tutorial, don’t hesitate to reach out to the Data and Visualization Librarian, Siti Lei ([siti.lei@dukekunshan.edu.cn](mailto:siti.lei@dukekunshan.edu.cn)) for further support.
