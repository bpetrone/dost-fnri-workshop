# dost-fnri-workshop

## Overview

This repository contains materials for a workshop on amplicon sequencing methods held at DOST-FNRI in March, 2023. The workshop contents are organized by topic:

-   **Slides** contains the slide decks presented in lecture format
-   **Hands-on** contains example data and R code notebooks that we'll use in hands-on sessions

The sections below have more information on the schedule and setting up your computer for the hands-on sessions.  Before you get started, please help us by filling out a [pre-workshop survey](https://tinyurl.com/pre-duke-workshop).

## Schedule

| Date   | Time      | Topic                                        |
|--------|-----------|----------------------------------------------|
| 13-Mar | 1:30-2:30 | Lecture: Introduction to amplicon sequencing |
| 14-Mar | Anytime   | On your own: Set up R for hands-on sessions  |
| 15-Mar | 1-1:45    | Lecture: Making a phyloseq object            |
|        | 2-2:45    | Hands-on: Making a phyloseq object           |
|        | 3-3:30    | Lecture: Taxonomic assignment                |
|        | 3:45-4:30 | Hands-on: Taxonomic assignment               |
| 15-Mar | 1-1:45    | Lecture: Making a phyloseq object            |
|        | 1-1:45    | Lecture: Making a phyloseq object            |
| 16-Mar | 10:30-11  | Lecture: Visualization and alpha diversity   |
|        | 11:15-12  | Hands-on: Visualization and alpha diversity  |
|        | 1-1:45    | Lecture: Beta diversity                      |
|        | 2-2:45    | Hands-on: Beta diversity                     |
|        | 3-5       | Office hours                                 |

## Get started

### R

There are two steps to getting started using R on your computer:

-   Install R (the computing language)
-   Install RStudio (a user interface for working with R)

Both are free and easy to download. These instructions assume that you have a computer running Windows. If you have another operating system, let us know.

**To install R:**
1.  In a web browser, go to the [Comprehensive R Archive Network](https://cloud.r-project.org) and click on "Download R for Windows."
2.  Then click the "base" link ("Binaries for base distribution").
3.  Click the first link at the top of the new page, which should say something like "Download R 4.2.2 for Windows" (the version listed will be replaced by the most current version of R over time). The link downloads an installer program, which installs the most up-to-date version of R for Windows.
4.  Run this program and step through the installation wizard that appears. The wizard will install R into your program files folders and place a shortcut in your Start menu. Note that you'll need to have appropriate privileges to install new software on your machine.

**To install RStudio:**
1.  In a web browser, go to the [RStudio homepage](https://posit.co/products/open-source/rstudio/) and clck on "Download RStudio" at the top right.
2.  Click "Download RStudio" under "RStudio Desktop".
3.  Scroll down and click the link for Windows 10/11 to download the Windows installer.
4.  Run this program and step through the installation wizard.

### Install R packages

We'll use a few specialized software packages for analyzing amplicon sequencing data in R. To download these packages, open R Studio, and in the `Console` window (usually on the left), enter and run the following:

    if (!require("BiocManager", quietly = TRUE))
        install.packages("BiocManager")

    BiocManager::install("phyloseq")
    BiocManager::install("dada2")

If you are prompted by the installation to update or install additional required packages, say yes. If you get a message asking `Do you want to install from sources the package which needs compilation?`, say no.

### Download the workshop materials

You can copy the full contents of this repository to your personal computer by "cloning" them. Cloning a repository differs from downloading in that there is still a connection to the remote copy (*i.e.* on GitHub) that you've copied from. This means that if changes happen in the repository, you can run a second command, called a "pull", to update them in your local version as well.

**To clone the workshop repository:**

1.  In a web browser, go to the top of the page you're reading now (the [landing page](https://github.com/bpetrone/dost-fnri-workshop) of the repository.
2.  Click on the blue **Clone** button in the top right part of the repository page.
3.  A dialog box will pop up that says "Clone with SSH", "Clone with HTTPS", etc.
4.  In this case you will want "Clone with HTTPS", so click on the clipboard icon to copy the URL.
5.  Open RStudio, click on the **File** menu, then select **New Project**.
6.  Choose **Version Control** in the *Create Project* dialog box.
7.  Choose **Git** in the *Create Project from Version Control* dialog box.
8.  Paste the repository URL you just copied into the *Repository URL* box.
9.  For *Project directory name* you can use the same repository name that we do (`dost-fnri`), or rename it to something else you prefer.
10. For *Create project as subdirectory of:* click on the **Browse** button
11. In the *Choose Directory* dialog that opens, click on **Home** then **New Folder**
12. In the *New Folder* dialog box type "workshop", then click **OK**.
13. Now in the *Choose Directory* dialog click **Choose**
14. Now that you are back in the *Clone Git Repository* dialog, click **Create Project**.

### Acknowledgements

This workshop borrows extensively from materials shared by Josh Granek.
