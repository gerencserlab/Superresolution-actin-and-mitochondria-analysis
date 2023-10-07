# Measure actin filopodia length in binarized projection images
## Description
This pipeline measures the length of filopodia protruding from a convex surface in previously binarized images. In this publication we used FIJI/Labkit to binarize maximum intensity projection images of super resolution microscopic phalloidin staining in human PBMC. The pipeline calculates the distance of the farthest point of each protrusion from the concave surface, i.e. the length of each filopodium.  
* Input: image series of binarized maximum intensity projections
* Output: Excel worksheet with individual filopodia length in pixels in columns and frames in rows. Ignore “MASK” values.




## Parameters
| # | Name | Type | Description |
|---|------|------|-------------|


## Structure
![structure](/img/Measure_actin_filopodia_length_in_binarized_projection_images.jpg)

[Image Analyst MKII](https://www.imageanalyst.net) pipeline – saved by V4.2.5 (build 838)

