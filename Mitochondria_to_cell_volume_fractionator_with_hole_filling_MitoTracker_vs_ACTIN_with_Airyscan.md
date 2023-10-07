# Mitochondria to cell volume fractionator with hole filling MitoTracker vs ACTIN with Airyscan
## Description
Analysis of Mitochondria:cell volume fraction from confocal microscopic recordings of a cytosolic or cellular stain and a mitochondrial stain. This pipeline is specifically applicable for cells with swollen mitochondria. Image processing in the original volume fractionator captures swollen mitochondria with a hole in the middle. This pipeline has additional components to fill in these holes. In addition, hole filling can repair holes introduced by saturation of images. Holes in the cytosolic stain, e.g. vacuoles are also filled in, thus estimated as cell area. Post-hoc images are recordings of the same view fields as the live cell recording, but after fixation and immunofluorescence staining. 

This pipeline was tuned to work with Airyscan2 super resolution images.

The volume fraction is given by the 2/3 times the ratio of the sum of mitochondrial pixels over the sum of all cellular (including mitochondrial) pixels, where the sum is calculated for all recorded images. The sum and ratio calculations take place in an Excel template.
The algorithm is based on the one described in J Physiol. 2012 590:12 2845-71. Handling of saturation and spectral unmixing has been removed compared to the original version (Mitochondria:cell volume fractionator (original)).
Note: The "Sensitivity scaling for the cytosolic stain (percentile)" may need to be adjusted. A lower value (slightly below 100) increases sensitivity, and estimates bigger cell size.

Keywords: volume fraction, volume density, mitochondrial biogenesis, mitochondrial abundance, mitochondrial mass, amounts of mitochondria, confocal microscopic stereology, mitochondrial membrane potential measurement

Version history:
V2: An Erase All ROIs command was added to the start to ensure that no user-drawn ROIs interfere with the analysis.
V3: The first version of the "hole filling" flavor of the volume fractionator is based on V2 basic volume fractionator.



## Parameters
| # | Name | Type | Description |
|---|------|------|-------------|
| 0 | Channel number for cytoplasmic stain (actin) | Integer | This is the channel number shown in the Multi-Dimensional Open dialog or in the Image Window caption, e.g. Ch2. |
| 1 | Channel number for mitochondrial stain (MitoTracker) | Integer | This is the channel number shown in the Multi-Dimensional Open dialog or in the Image Window caption, e.g. Ch1. |
| 2 | Image acutance cutoff for the cytoplasmic stain | Real | Frames with acutance smaller than this value will be omitted. See frame-by-frame acutance values in the Image Property Window. |
| 3 | Sensitivity scaling for the cytosolic stain (percentile) | Real | A lower value (slightly below 100) increases sensitivity. Cells aggregating the probe in lysosomes need a lower percentile value to select cells and not lysosomes. |
| 4 | Otsu factor for cytoplasmic stain | Real | This factor times Otsu optimal threshold value will be used as an automatic threshold value |
| 5 | Hole filling: maximal hole area in the cytosol | Integer | Holes smaller than this in pixel are will be filled. |
| 6 | Hole filling: maximal hole area in mitochondria | Integer | Holes smaller than this in pixel are will be filled. |
| 7 | Hole filling: close this size of gaps before filling holes | Integer | This wide gaps will be closed before hole filling  |


## Structure
![structure](/img/Mitochondria_to_cell_volume_fractionator_with_hole_filling_MitoTracker_vs_ACTIN_with_Airyscan.jpg)

[Image Analyst MKII](https://www.imageanalyst.net) pipeline - saved by V4.2.5 (build 917)

