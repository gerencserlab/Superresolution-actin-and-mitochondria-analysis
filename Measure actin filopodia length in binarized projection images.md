# Measure actin filopodia length in binarized projection images
## Description
This pipeline measures the length of filopodia protruding from a convex surface in previously binarized images. In this publication we used FIJI/Labkit to binarize maximum intensity projection images of super resolution microscopic phalloidin staining in human PBMC. The pipeline calculates the distance of the farthest point of each protrusion from the concave surface, i.e. the length of each filopodium.  
* Input: image series of binarized maximum intensity projections
* Output: Excel worksheet with individual filopodia length in pixels in columns and frames in rows. Ignore “MASK” values.


[Image Analyst MKII pipeline](https://www.imageanalyst.net) – saved by V2.4.5


## Parameters
| # | Name | Type | Description |
|---|------|------|-------------|


## Structure
![structure](.img\Measure actin filopodia length in binarized projection images.jpg)

[Image Analyst MKII pipeline](https://www.imageanalyst.net) – saved by V4.2.5 (build 838)

