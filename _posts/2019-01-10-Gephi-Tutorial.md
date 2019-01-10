---
layout: post
title: Gephi Tutorial  
categories: Gephi
---

# How to use Gephi for Data Analysis

Gephi is a visualization and exploration software for graphs and networks. Like Photoshop but for graph data, the user interacts with the representation, manipulate the structures, shapes and colors to reveal hidden patterns. This tutorial will provide you an overview of Gephi.

<hr />

## **Installation**

Gephi is open-source, free to download and runs on Windows, Mac OS X and Linux. For installation, you can visit [Gephi](https://gephi.org/).


![Gephi 0.9.2]({{"/static/img/1.png" | prepend: site.baseurl}})

<hr />

## **Data Processing** 

Two kinds of data files:

+ **"Nodes" list**: Contains the identifiers of each nodes, their label and their id. 
<br/>
<br/>
![Nodes list]({{"/static/img/2.png" | prepend: site.baseurl}})
<br/>
<br/>

+ **"Edges" list**: The first two columns are the node ID and the other column is the correlation coefficient.
<br/><br/>
![Edges list]({{"/static/img/3.png" | prepend: site.baseurl}})
<br/><br/>

<hr />

## **Importing Data into Gephi**

Run the application on your computer, click **"New Project"** to create a new Gephi project in the start menu.
<br/>
![Create Project]({{"/static/img/create_project.png" | prepend: site.baseurl}})
<br/>

Click **"File"** -> **"Import spreadsheet"** -> Choose your data file and click **"Open"** to import your data files.
<br/>
![Import spreadsheet]({{"/static/img/file.png" | prepend: site.baseurl}})
<br/>

Specify all information that is required:
+ **Separator**: Specify the separation (comma, semicolon, tab or space) between your data. 
+ **Import as**: Choose the kind of data file you are importing (Nodes table, Edges table, adjacency list or matrix)
+ **Charset**: Select the encoding of your data.
<br/>
![Import spreadsheet]({{"/static/img/spreadsheet.png" | prepend: site.baseurl}})
<br/>

Click **"Next"** and **"Finish"**. You should now see a graph.
<br/>
![Overview]({{"/static/img/overview.png" | prepend: site.baseurl}})
<br/>

<hr />

## Visualization

The action now takes place on the overview panel. The software produces an overview of the graph, spatialized randomly (and completely unreadable). We need to set some layout styles to make it readable.

<br/>
### Run a layout

Layout algorithms set the graph shape, it is the most essential operation. Gephi offers a variety of layout algorithms including **ForceAtlas, OpenOrd, Circular Layout** and etc. After choosing a layout, there are multiple properties you can change to control the algorithm in order to make a readable representation.
<br/>
![Various Layout]({{"/static/img/variouslayout.png" | prepend: site.baseurl}})
<br/>

You should select one layout algorithm according to the feature of the topology you want to highlight. Gephi provides a detailed [Tutorial Layouts](https://gephi.org/tutorials/gephi-tutorial-layouts.pdf) which explains all kinds of layout algorithms and how to control them.

Here I will take the ForceAtlas as an example:

+ Locate the Layout module on the left panel.
<br/>
![Layout Panel]({{"/static/img/layoutpanel.png" | prepend: site.baseurl}})
<br/>

+ Choose **"Force Atlas"**. And you can see the layout properties below.
+ Click **"Run"** to launch the algorithm. You can see now the positions of nodes changeing in real time. Let tha algorithm run until the graph is stablilized.
+ Click **"Stop"** to stop the algorithm. You should now see a graph with the layout applied. Use the little blue magnifying glass (bottom left of the graph panel) to re-center the zoom.
+ Then you can run **"Noverlap"** and **"Expansion"** algorithms to prevent nodes overlapping.
<br/>
![ForceAtlas Graph]({{"/static/img/forceatlas.png" | prepend: site.baseurl}})
<br/>

### **Set Appearance**

Next we can change the size, color of the nodes and edges to make the graph more readable.

+ Locate the Appearance module on the left panel.
+ Click **"Nodes"** -> **"Ranking"** -> **"Choose an attribute"** -> **"Degree"**
+ Then you can choose a color that you like.
+ Click **"Apply"**.
+ Do the same with Edges.
<br/>
![Appearance Panel]({{"/static/img/appearance.png" | prepend: site.baseurl}})
<br/>

Now you can see a colorful Force Atlas graph.
<br/>
![Set Color]({{"/static/img/setcolor.png" | prepend: site.baseurl}})
<br/>

### **Set Labels**

There is a tiny black arror at the right bottom of the graph display. Click that arrow and you can find the Label panel. Then click the black **"T"** to add labels. 
<br/>
![Set Label]({{"/static/img/labelpanel.png" | prepend: site.baseurl}})
<br/>

You can set different font styles, colors and sizes. You can also choose to add labels to the nodes, edges or both. If wanted, you can also click on the “Configure” link to set the data you want to get displayed.
<br/>
![]({{"/static/img/label.png" | prepend: site.baseurl}})
<br/>

### **Preview and Export**

Before export graphs, you can go to the **Preview** panel and check the final details. You can change properties on the left **Preview Settings** panel. Changing settings in this menu is reversible, and do not affect the structure of the graph.  The graph may take a few seconds to update after each change (click on **Refresh** to apply the changes).
<br/>
![Preview]({{"/static/img/preview.png" | prepend: site.baseurl}})
<br/>

At the bottom of this preview column, you find an export link. Note that exporting in .png produces figure with a poor resolution. You may want to output for .svg or .pdf, which have the advantage of being modifiable by your own image/drawing software.

<hr />

## Community Detection

The visualization only is not enough for data analysis as it often needs other mathematical means to provide the researcher with a satisfactory result. The **Statistics** menu on the right provides more options: degree measures, density, path length, modularity and etc...

In this tutorial, I will show you how to generate a community detection graph.

+ Locate the **Statistic** panel on the right of the **Overview** page.
+ Find "Modularity" and click "Run"
+ Set **Resolution** value (default 1.0). Lower to get more communities and higher than 1.0 to get less communities.
+ Click **OK** to view the modularity report. You can see the number of communities on the report.

<br/>
![Modularity Panel]({{"/static/img/modularity.png" | prepend: site.baseurl}})
<br/>

![Modularity Report]({{"/static/img/modularityreport.png" | prepend: site.baseurl}})
<br/>

The next step takes place in the Partition menu situated in the left column of the Overview page. Select **"Nodes"**, **"Partition"** and **"Modularity Class"** (rolling menu). You will be then able to modify the colors attributed to the detected communities by clicking on them.
<br/>
![Partition Panel]({{"/static/img/partition.png" | prepend: site.baseurl}})
<br/>

Once you have set up a color for each community, click **"Apply"** and you can see the community detection graph.
<br/>
![Community detection graph]({{"/static/img/communitydetection.png" | prepend: site.baseurl}})
<br/>
<hr />

## **Conclusion**

I hope this tutorial can help you start with Gephi. Gephi also provides various [tutorials](https://gephi.org/users/) which you can refer to. There are also plenty of wonderful video tutorials on Youtube. I list one here if you are interested.

[Video Tutorial](https://www.youtube.com/watch?v=2FqM4gKeNO4)

<hr />

### Reference

[Introduction to Network Visualization with GEPHI](http://www.martingrandjean.ch/introduction-to-network-visualization-gephi/)

[Gephi Tutorial Layouts](https://gephi.org/users/tutorial-layouts/)
