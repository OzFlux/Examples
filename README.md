# Examples
Welcome to the PyFluxPro Examples repository!

The repository contains ZIP files for 3 TERN Ecosystem Processes/OzFlux sites; Calperum, Cumberland Plain and Loxton.  These files are intended to be used as examples for using PyFluxPro.  Each ZIP file contains all of the files required to complete processing the site data from ingestion (L1) to partitioning (L6), including L1 data files (as Excel workbooks), control files for all levels of processing and alternate data (AWS, ACCESS and ERA5) for gap filing meteorological data at L4.

## Downloading

You can download the example files for a site by following these steps:

1. Click on the ZIP file for a site.  GitHub will open a page saying it "can't show files this big".
2. Click on the **Download** button at the top right corner of the window displaying this message.
3. The file will start downloading after a delay of several seconds.

## Using the Examples

### A note about folders

The control files for each site in the examples assume a particular folder structure.  You're welcome to use any folder structure that makes sense to you but if you stick with the one described below then you wont have to change anything in the example control files in order to run them.

The screenshot below shows the default folder structure used in the example files.

![](/home/peter/Examples/folder_structure.png)

The main points are:

1. The example files for each site are in separate folders under the **PFP_examples** folder.
2. The **PFP_examples** and **PyFluxPro** folders are at the same level.
3. Keep your own data and control files separate from both **PFP_examples** and **PyFluxPro**.  In the example shown above, your sites go in the **mySites** folder which is also at the same level as the **PyFluxPro** folder.

If you use the folder structure described above then you can use the example control files with modification.

### Running the examples

We will use the level 1 (L1) processing for Loxton as a basic demonstration for how to use the examples.  A more detailed description of how to use the examples can be found in the PyFluxPro wiki.

Before you start, make sure:

1. You have installed PyFluxPro and checked that it starts correctly.
2. You have installed the example files for Loxton using the folder structure shown above.

To run the L1 processing for Loxton, follow these steps:

1. Open a command window (Windows) or a terminal (macOS and Linux), use **cd** to navigate to your PyFluxPro folder and start PyFluxPro by typing:
   1. Windows;
      1. If you installed PyFluxPro from the single file installer, just type **PyFluxPro** at the command line.
      2. If you installed PyFluxPro by cloning from the GitHub repository, type **"python PyFluxPro"** at the command line or just **"pfp"**.
   2. macOS;
      1. If you installed PyFluxPro by uncompressing the ZIP file, just type **./PyFluxPro** at the command line.
      2. If you installed PyFluxPro by cloning from the GitHub repository, type **"python3 PyFluxPro"** at the command line or just **"./pfp"**.
   3. Linux;
      1. You know what to do ...
2. When the PyFluxPro GUI opens, use the **File/Open** menu option to open the Loxton L1 control file (L1.txt), see the screenshot below;
   ![](/home/peter/Examples/file_open_loxton_l1.png)
3. Once the Loxton L1 control file has loaded in the GUI, take a few minutes to review its contents.  The PyFluxPro wiki entry on L1 (see https://github.com/OzFlux/PyFluxPro/wiki/Level-1) has a description of the L1 control file contents.  Below is a screenshot of the Loxton L1 control file loaded into the GUI.
   ![](/home/peter/Examples/loxton_l1_open_in_gui.png)
4. If you have followed the folder structure suggested above then this control file will run without changes.  If you have used a different folder structure, you will need to change the **file_path** entry in the **Files** section so that is refers to the folder containing the Loxton L1 workbook.  A right click on the **file_path** entry (in the **Value** column) will allow you to browse to the appropriate folder.
5. To run the L1 processing for Loxton, use the **Run/Current** menu option, see below:
   ![](/home/peter/Examples/loxton_l1_run_current.png)
6. If the Loxton L1 processing runs successfully, you should see the output below:
   ![](/home/peter/Examples/loxton_l1_run_output.png)

That's it, you're all done for Loxton L1.  Now try the same process for Loxton L2 to L3.  Then try **Utilities/Climatology** and **Utilities/u* threshold/CPD (McHugh)** to run the climatology (needed for L4) and the CPD u* threshold detection routine (needed for L5).  Then run L4 to L6.  Try the other example sites, they all do something different that displays the various features of PyFlyxPro.

The PyFluxPro Wiki, see https://github.com/OzFlux/PyFluxPro/wiki, has more information on the processing.
