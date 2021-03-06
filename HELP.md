![4Quant](http://4quant.com/LungStageAnnotator/imgs/logo.png)

# Getting Started

- To get more comfortable using 3D Slicer have a look at our tutorials on basic 3D Slicer usage and annotation techniques on [YouTube](https://www.youtube.com/playlist?list=PLor6_v5dt2SjdX-jds-OshNKHhehJOmov).
- To use the Annotator tool a custom command will have been provided to you to start the tool. A full tutorial is available on [YouTube](https://www.youtube.com/watch?v=Euu2pQ0Ecjk)

# Load PETCT Data
The starting point for a new patient is the `Load PETCT Data` panel. The scans from the currently loaded DICOM database are shown to load a different database or import data see the `DICOM` panel and Slicer documentation.

- The scans are prioritized according to the criteria given in the next panel (modality), basically a  list of regular expression based rules.
- The _load_ button will match the best PET scan with the best CT scan (if available), select a standard window and display the fusion images in the 'Slice Viewer' panel

# Modality/Scan Priority

This panel shows the different scans which are acceptable as part of the PET/CT input. The order specifies the priority.

# Slice Viewer

- Once a patient has been loaded change to the 'Slice Viewer' panel browse the images.
- Keyboard Shortcuts
 - _Shift+N_ for showing the slice number in all planes 
 - _Shift+J_ for jumping to and centering on the currently highlighted lesion 
- Mouse Operation  
 - holding left mouse and moving vertical and horizontal will change window and level
 - holding down the shift key while moving the mouse in slice views will scroll all slice viewers to that RAS coordinate
 - holding down the shift key and holding down the left button while moving will pan the slice view (or views, if linked)
 - control click + drag to zoom in and out
- See annotating for information about making annotations
- More mouse and keyboard guides are available [here](https://www.slicer.org/wiki/Documentation/4.6/SlicerApplication/MouseandKeyboardShortcuts)

- The _Create Label Table_ creates a table from the labels which have already been applied to the image. It will calculate the corresponding CT and PET values for the region as well

# Annotating

While the primary annotations are done in the 'Slice Viewer' the information for the annotations can be seen in the segmentation panel. The tool creates a new segmentation group at the beginning after loading each patient. This can have unlimited numbers of individual segments are labels added to it.

In the slice viewer there are a few shortcuts which have been setup to ease operation and keep the labeling consistent. The tools open in another window and are the same (currently) as the 3D Slicer [SegmentEditor](https://www.slicer.org/wiki/Documentation/4.6/Modules/SegmentEditor#Effects), currently the focus is on using the 3D sphere brush but other quicker tools (optimized for 2D slices) are available.


# Segmentations

The segmentations are described in detail [here](https://www.slicer.org/wiki/Documentation/Nightly/Modules/SegmentEditor). The default brush is the sphere, but there are many others which can be useful for segmenting larger or homogenous regions quickly.
