# A Guide to the Code

Scripts for image analysis softwares  
Written by Kristina M. Sattler

Notes:
- See document comments for further explanations of how to tailor code to your experiment - Adjust pathways, labels, and settings to fit your experiment! 
- To add or remove a line of code, DO NOT delete it- add “//” at the beginning of the line so it is read as a comment rather than code to be executed
  - Any text with “//” in front will be interpreted as a comment and ignored. This is useful for taking notes on lines of code or toggling switches to include/exclude arguments
- Pay close attention to punctuation in code! Make sure the code of each line ends in a semicolon (not comments) and quotes are correctly placed

Completed code
- **ImageJ Macros**
  - Batch Image Merge - Complete
    - For 2-4 channels, this macro will merge, color, adjust brightness/contrast, scale, flatten (optional), and save images 
  - Batch Fluorescence Quantification - Complete
    - This macro will open one image, set scale, set measurements, measure, close, save measurement results as a .csv file, and loop for all images in the folder 
  - Batch Image Scale - Complete
    - This macro will set the scales and save sets of images either in a single folder or separated into multiple subfolders
  - Batch Cell Area Quantification - Complete, but would take some ImageJ macro know-how to edit to fit a different experiment
    - This macro will measure the area of an image covered by fluorescence above a set threshold
- **FIJI Macros**
  - MorphoLibJ Processing Cellpose Masks - Complete
    - This macro will process mask images created in Cellpose to remove the border ROIs and filter ROIs by size to eliminate small ROIs
- **QuPath Scripts**
  - Image Setup
  - Batch Colocalization Quantification
    - This script will use DAPI to detect nuclei, create ROIs around the nuclei, measure the mean gray value of all channels in the image, classify each ROI based on mean gray value measurements, and save individual and summaryvalues to a .txt file
  - Batch Cell Detection
  - Classifiers
