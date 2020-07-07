PiaNO
=====

PIA file reader/writer.

A reference library for opening and modifying AutoDesk® plot files (.pc3, .pmp, .stb, .ctb).

#### Example Usages:

##### Reading and Saving Plotter Configurations (.PC3)
```csharp
string supportPath = @"C:\Plot Support";
string configName = Path.Combine(supportPath, "DWG To PDF.pc3");
var pdfConfig = new PlotterConfiguration(configName);

pdfConfig.TruetypeAsText = true;
pdfConfig.SetCustomValue("Include_Layer", false);
pdfConfig.SetCustomValue("Create_Bookmarks", false);

pdfConfig.Write(Path.Combine(supportPath, "DWG To PDF - NoLayersOrBookmarks.pc3"));
```

## *CADbloke edits*
- more info on the file format and a Viewer at http://www.noliturbare.com/plot-print/print-ctbs-and-more
- details of the file format at http://www.noliturbare.com/more/faq#Q5 and also on the below Swamp thread...
- a thread on pc3 files etc https://www.theswamp.org/index.php?topic=52070.0