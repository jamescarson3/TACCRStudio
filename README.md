RStudio at TACC
===========

---

#### Objectives
*	Learn to run RStudio on Maverick through the TACC Visualization Portal
*	Import data
*	Run R scripts
*	Save results
*	Visualize results
*	Load R modules

---

R is a programming environment for statistical and data analysis computations. R is an open source GPL licensed (free to anyone) offspring of S, initially written by Ross Ihaka and Robert Gentleman at Dep. of Statistics of U of Auckland, New Zealand during 1990s.  It continues to be in active development; http://www.r-project.org/

### Some things that R can do

* Statistics and analysis
* Plotting and graphics
* Data handling and storage
* Scripting (loops, subroutines, etc)


---

### TACC Visualization Portal

https://vis.tacc.utexas.edu/

Logging in

![](https://github.com/jamescarson3/TACCRStudio/blob/master/vis_login.png)

---

* Wait for authentification
* Will automatically switch to displaying Jobs tab
* Select Maverick
* Select a project that has an allocation on Maverick
* Select RStudio

---

![](https://github.com/jamescarson3/TACCRStudio/blob/master/vis_rstudio_startjob.png)

---

Wait patiently.  Move startup window up with mouse to make sure it did not fail.

---

![](https://github.com/jamescarson3/TACCRStudio/blob/master/vis_rstudio_running.png)

---

Now open RStudio in your browser by clicking the button.

Congratulations!

---

### Challenge

* Use basic linux knowledge to find your working directory path.  Copy it.
* Make and save a tab delimited text data file with some random numbers as ```data.txt```

---

### RStudio Graphical User Interface (GUI)

* Source Editor / Interactive Highlight & Run
* Data Viewer
* Interactive Console
* Workspace / Variable Viewer
* Session History
* File Management
* Plot Viewer
* Package Loader
* Interactive Help

---

### Open your data

In the interactive console type (using your own work directory):

```
workdir="/work/01234/jcarson/maverick"
setwd(workdir)
```

You could also instead use the File Management window on bottom right to set the working directory.  Once it is set, read in the file.

```x = read.delim(“filename.txt”)```

How can you tell it has been read in?

---

### Importing data from URL

Credit to: http://evomics.org/learning/programming/introduction-to-r/

Upper Left Window
* Tools
* Import Dataset
* From Web URL

Repeat for both datasets
* http://evomicsorg.wpengine.netdna-cdn.com/wp-content/uploads/2013/01/healthy_metadata.txt
* http://evomicsorg.wpengine.netdna-cdn.com/wp-content/uploads/2013/01/sick_metadata.txt

```
summary(healthy_metadata)
summary(sick_metadata)
boxplot(healthy_metadata$Age, sick_metadata$Age)
```

Try exporting your plot.  Be sure to specify your working directory in the save window

---

### Saving your workspace

You can use the GUI to save and load your workspace

* Session - save workspace
* Quit RStudio
* Reopen RStudio
* Session - load workspace

----

### Challenge

* Type ```demo()``` to see a list of demos available and try some of them out, e.g. ```demo(graphics)```
* Find a favorite plot and save it as a pdf in your work directory
* Verify that the file is where you wanted to save it
