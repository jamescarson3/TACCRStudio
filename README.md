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

Now open RStudio in your browser by clicking the button

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

Commands to try




---

Session - save workspace

Quit RStudio

Reopen

Session - load workspace

----

  history(Inf)
–  To review the command lines entered during the
sessions
•  savehistory(“history.txt”)
–  Save the history of command lines to a text file
•  loadhistory(“history.txt”) –  read it back into R
•  save(list=ls(),file=“all.Rdata”)
–  The session as a whole can be saved as a binary file.
•  load(“c:\\temp\\ all.Rdata”) – Read back saved sessions.

---

demo()


---

Importing and exporting data
There are many ways to get data into R and out of R.
Most programs (e.g. Excel), as well as humans, know how to deal with rectangular tables in the form of tab- delimited text files.
> x = read.delim(“filename.txt”) also: read.table, read.csv
> write.table(x, file=“x.txt”, sep=“\t”)



setwd("/work/02570/jcarson/maverick")



Source - http://evomics.org/learning/programming/introduction-to-r/
Tools
Import Dataset
From Web URL
http://evomicsorg.wpengine.netdna-cdn.com/wp-content/uploads/2013/01/healthy_metadata.txt
http://evomicsorg.wpengine.netdna-cdn.com/wp-content/uploads/2013/01/sick_metadata.txt

summary(healthy_metadata)
summary(sick_metadata)
boxplot(healthy_metadata$Age, sick_metadata$Age)

Plots - Export
  Set your directory


Files window 
...
Files - More - Set as working directory

/work/02570/jcarson/maverick

---

### Challenges

---



