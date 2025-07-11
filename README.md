# A Guide to the Code

Scripts for image analysis softwares  
Written by Kristina M. Sattler

### Notes:
- Only change code in sections with EDIT
- See comments for further explanations of how to tailor code to your experiment - Adjust pathways, labels, and settings to fit your experiment! 
- To add or remove a line of code, DO NOT delete it- add “//” at the beginning of the line so it is read as a comment rather than code to be executed
  - Any text with “//” in front will be interpreted as a comment and ignored. This is useful for taking notes on lines of code or toggling switches to include/exclude arguments
- Pay close attention to punctuation in code! Make sure the code of each line ends in a semicolon (not comments) and quotes are correctly placed

### Completed code
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
    - This macro will process mask images created in Cellpose 
      - Remove the border ROIs 
      - Filter by size to eliminate small ROIs
- **QuPath Scripts**
  - Automatic Batch Cell Detection - Complete
  - Semi-Automatic Satellite Cell Quantification - Complete
  - Automatic Batch Colocalization Quantification - Complete
    - This script will use DAPI to:
      - Detect nuclei
      - Create ROIs around the nuclei
      - Measure the mean gray value of all channels in the image
      - Classify each ROI based on mean gray value measurements
      - Save individual and summary values to a .txt file
  - Classifiers
 
### File Organization:
- Parent Folder = folder containing subfolders of one sample
  - e.g. 7088_L_Scan_29-22
- Subfolders = group of folders in the parent folder containing images 
  - Name the subfolders with SampleID_SampleType_#
    - e.g. 7088_L_1 (sample 7088, left muscle, image 1)
    - *Note: Keep Subfolder names very simple. These will be used to name the final output files when applicable
- Images = images that code will be applied to
- Oraganize files like this for:
  - ImageJ: Batch Image Merge
  - ImageJ: Fluorescence Quantification
  - ImageJ: Set Scales
<img width="742" alt="File_Organization" src="https://github.com/user-attachments/assets/a0482e32-7d65-4393-84f7-1afe462844e9" />
