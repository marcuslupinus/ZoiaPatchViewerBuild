# ZoiaPatchViewerBuild

Already-build distribution of ZoiaPatchViewer and ZoiaFileExplorer desktop apps For Windows.

Both apps are intended to help in managing Zoia Patch Files.  For those who don't know, Zoia is an electronic
device created by Empress Effects Inc. (Canada!!!) that is more or less a guitar effect pedal...

## Requirements

The package include two desktop apps in executable form.  They target a Windows environment - sorry no Mac.

They are build in C# .Net Core 6 and use WPF. They were tested under Windows 11 but should work fine under
Windows 7+.

The apps are very lightweight, they won't take over your computer in any significant way.  No background processes,
no huge files...

They are provided free to be used as is.

## How to Install

Download the ZIP file found in the Builds folder.  Extract it's content then execute the .msi or setup file.

## What is ZoiaPatchViewer

ZoiaPatchViewer allow users to open a ZOIA patch file from their computer to see the modules, connections, etc. of the patch. 

It's important to note that this app was created using some knowledge of the patch file formats used by the ZOIA that was obtained mainly through reverse engineering.  This software was not created nor verified by Empress Effects Inc.  Thus it might contain errors and is certainly not able to decode 100% of the patch data.  Some reverse engineering is still required to be able to do that.

There is a documentation file in the GitHub project meanmediamoge/zoia_lib that contains the details for the ZOIA patch file format that has been used to create this software.

## Main Features of ZoiaPatchViewer

From a patch file, the app is able to display the following :
- The list of modules in a patch with it's name, it's color and it's position (page and grid position).
- The page names.
- The selected value for each module's option.
- The list of blocks (parameter blocks) of the module, based on the selected module's options, with their name.
- The connections between module parameter blocks with the connection strength.
- The modules parameters that are starred with the optionnal MIDI CC number.
- The connections that are starred with the optionnal MIDI CC number.

Furthermore, the app give the user access to some documentation on the module types available in the ZOIA when creating a patch along with some description, the available options and the available parameter blocks.

### What is NOT available in ZoiaPatchViewer (yet...)

In its current state, the app is unable to display the CV values set for the parameter block.  For example, if a patch has a Reverb module, the value of the Mix parameter is not decoded and displayed.

The intention is to add those details later but it will require some more reverse engineering and that is quite time consuming and uncertain.

## How to use ZoiaPatchViewer (ZoiaFileExplorer described further down)

You will find some screen shots of the app in the following location: https://github.com/marcuslupinus/ZoiaPatchViewerBuild/tree/main/Screen%20Shots

To view a patch file, you have two options:
- Click on the «Open Patch File...» button in the toolbar next to the app menu (top left of the window).
- Click on the grey encoder button in the ZOIA graphic view.

### Patch Page

You can select a module by clicking on one of it's block in the graphic view or by selecting the module from the list on the right side.  The currently selected module is shown in the graphic view by a yellow rectangle around each of its parameter blocks.

When selecting a module from the list on the right, the corresponding page is displayed in the graphics view.

The details of the currently selected module appears below the graphic view.  

You can go to the previous and next page by clicking the top-most left and top-most right utitlity button in the graphig view.  The utility buttons are the 4 red buttons under the display.

The current page number and name if any, is displayed in the text block under the encoder button in the graphic view.

In the Patch page, the connections appearing as lines in the graphics view and appearing as text in the bottom part of the current module details are color coded.  White/Gray is used for audio connections and green for CV connections.

Selecting a connection from the connection list will hilight the corresponding block and it is possible to select the module at the origin or destination of the selected connection.

### Patch Summary Page

The Summary page show some information from the patch in a textual form.  The goal here is to display information that is helpfull in understanding how to use the patch.

It shows whether audio in and out are present, in stereo or mono, etc.

It shows any stompswitch or button present in the patch.

It lists all the 'values' modules in the patch.

It lists all the MIDI related modules in the patch.

It list also starred elements present in the patch with corresponding MIDI CC number if any.

When creating a patch, keep in mind that if you set any name for any of the module type used above, it's name will be shown thus making it much easier to understand, at a glance, how the patch is intended to be used.

### Errors with patch files

Any error or warning detected when the patch was loaded will appear in the Errors page.  If any are present, the Errors text will appear in red.  If that's the case, it's most likely that the patch will not display correctly.

Usually, errors occurs because you are trying to open a patch made with a rather old version of the ZOIA firmware.  The easiest way to fix this is to select that patch in the ZOIA (with a recent firmware) and save it again.  ZOIA seems to automatically convert old patches to current module definition when a patch is loaded.  You can the retransfer the patch to your computer and try openning it again.

### Help Page

The help page allow access to the list of module types that the ZOIA supports along with details on each one of them.

Note the search at the bottom of the list of modules.  It allow to search modules documentation by their name.

## Main Features of ZoiaFileExplorer

ZoiaFileExplorer operation is similar to the Windows File Explorer app.  It allow you to browse your folders and display their content.  It allow for creating sub folders, renaming files and folders and also moving and copying files around just like the File Explorer.

In addition, ZoiaFileExplorer has some features that makes managing the Zoia files easier, like reorganizing the order of the patches in a folder using drag and drop.  There are many other features.  Read the integrated help for more details.

There is also a silent video giving you a quick video demo of the app in the Screen Shots folder (on Github).

## Help, Comments, Suggestions

Can be made by sending email to lupinskysoft@gmail.com.

Only serious, polite and constructive emails will be answered.

**end**