# modular-spatial-analysis
A modular series of scripts made for performing spatially-dependent image analysis on batches of images, producing a heuristic map. Intended for use on defect detection in strain maps.


Test Functions Examples:
SA_Test - unified script to test all methods and varying parameters on a set of imported images
SA_Test2 - tests FEA strain data w/ spatial analysis

Modular functions:
1) SA_Defect - creates a defect in an image, intended for use on strain maps
2) SA_ErrorRate - computes sensitivity and specificity for an analyzed image when trying
3) SA_Gradient - computes intensity gradient and vector map
4) SA_Lacunarity - computes lacunarity. Implemented from: https://www.researchgate.net/publication/13324182_Lacunarity_analysis_A_general_technique_for_the_analysis_of_spatial_patterns
5) SA_MoransI - computes Moran's I (spatial autocorrelation). Implemented from: https://www.jstor.org/stable/2332142?origin=crossref
6) SA_VMRatio - computed variance-mean ratio (VMR). Also known as index of dispersion. Implemented from Cox & Lewis 1966


Helper functions:
1) SA_EdgeHelper - removes boundaries of an image using a mask, intended for use with SA_Gradient
2) SA_FindDefects - finds outlier in an analyzed heuristic map, based on a flat level of exclusion
3) SA_GradientHelper - erodes edges of a mask, intended to be used with Gradient. Has 'fast' and 'slow' modes
4) SA_Helper - coordinates calls to modular functions, main function called by other scripts
5) SA_Identify - finds outlier values in an analyzed heuristic map based on standard deviation
6) SA_Overlay - tiny script to overlay plusses on an image, for visualization
7) SA_QuiverOverlay - overlays quiver/vector maps on a normal image for gradiate visualization
8) SA_RoiVal - computes the value of an ROI using the desired heuristic and a mask
9) SA_WindowAnalysis - some SA methods require windowing. Grabs all points from a moving window
