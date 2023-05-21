# Examples
Welcome to the PyFluxPro Examples repository!

The repository contains files for 3 TERN Ecosystem Processes/OzFlux sites; Calperum, Cumberland Plain and Loxton.  These files are intended to be used as examples for using PyFluxPro.  Each site folder contains all of the files required to complete processing the site data from ingestion (L1) to partitioning (L6), including L1 data files (as Excel workbooks), control files for all levels of processing and alternate data (AWS, ACCESS and ERA5) for gap filing meteorological data at L4.

## Downloading

1. The easiest way to download the example files is to clone this repository using **git**.  This is the same method suggested for installing PyFluxPro.  The process is as follows:
   1. Open a command line window or terminal session and use the **cd** (shorthand for "change directory") command to navigate to the directory into which you want to install the example folders. Note that the installation process will create a folder called **Examples** in the directory where the installation is run.
   2. Clone the **Examples** repository by typing **git clone https://github.com/OzFlux/Examples.git** at the command prompt.
   3. This process will create a folder called **Examples** in the current folder.  The **Examples** folder itself contains 4 folders, 1 for each example site (**Calperum**, **Cumberland Plain** and **Loxton**) and 1 called **controlfiles**.

## Using the Examples

### A note about folders

The control files for each site in the examples assume a particular folder structure.  You're welcome to use any folder structure that makes sense to you but if you stick with the one described below then you wont have to change anything in the example control files in order to run them.

The screenshot below shows the default folder structure used in the example files.

![](images/examples_folder_structure.png?raw=true)

The main points are:

1. The example files for each site are in separate folders under the **Examples** folder.
2. The **Examples** and **PyFluxPro** folders are at the same level.
3. Keep your own data and control files separate from both **Examples** and **PyFluxPro**.  In the example shown above, your sites go in the **mySites** folder which is also at the same level as the **PyFluxPro** folder.

If you use the folder structure described above then you can use the example control files with modification.

### Running the examples

We will use the level 1 (L1) processing for Loxton as a basic demonstration for how to use the examples.  A more detailed description of how to use the examples can be found in the PyFluxPro wiki.

Before you start, make sure:

1. You have installed PyFluxPro and checked that it starts correctly.
2. You have installed the example files for Loxton using the folder structure shown above.

To run the L1 processing for Loxton, follow these steps:

1. Open a command window (Windows) or a terminal (macOS and Linux), use **cd** to navigate to your PyFluxPro folder and start PyFluxPro by typing:
   1. Windows;
      1. Type **"pfp"** at the command line.
   2. macOS;
      1. Type **"./pfp"** at the command line.
   3. Linux;
      1. Don't be cute, you know what to do ...
2. When the PyFluxPro GUI opens, use the **File/Open** menu option to open the Loxton L1 control file (L1.txt), see the screenshot below;
   ![](images/file_open_loxton_l1.png?raw=true)
3. Once the Loxton L1 control file has loaded in the GUI, take a few minutes to review its contents.  The PyFluxPro wiki entry on L1 (see https://github.com/OzFlux/PyFluxPro/wiki/Level-1) has a description of the L1 control file contents.  Below is a screenshot of the Loxton L1 control file loaded into the GUI.
   ![](images/loxton_l1_open_in_gui.png?raw=true)
4. If you have followed the folder structure suggested above then this control file will run without changes.  If you have used a different folder structure, you will need to change the **file_path** entry in the **Files** section so that is refers to the folder containing the Loxton L1 workbook.  A right click on the **file_path** entry (in the **Value** column) will allow you to browse to the appropriate folder.
5. To run the L1 processing for Loxton, use the **Run/Current** menu option, see below:
   ![](images/loxton_l1_run_current.png?raw=true)
6. If the Loxton L1 processing runs successfully, you should see the output below:
   ![](images/loxton_l1_run_output.png?raw=true)

That's it, you're all done for Loxton L1.  Now try the same process for Loxton L2 to L3.  Then try **Utilities/Climatology** and **Utilities/u\* threshold/CPD (McHugh)** to run the climatology (needed for L4) and the CPD u* threshold detection routine (needed for L5).  Then run L4 to L6.  Try the other example sites, they all do something different that displays the various features of PyFlyxPro.

The PyFluxPro Wiki, see https://github.com/OzFlux/PyFluxPro/wiki, has more information on the processing.
