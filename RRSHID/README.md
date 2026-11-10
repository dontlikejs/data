# RRSHID hazy-image classification subset

This directory contains 3,053 original 256 x 256 PNG hazy images from RRSHID,
retaining the author's split: 2,441 train, 308 validation and 304 test.

Official project and dataset access: https://github.com/AeroVILab-AHU/RRSHID

Citation: Zhu, Z.-H.; Lu, W.; Chen, S.-B.; Ding, C. H. Q.; Tang, J.; Luo, B.
*Real-World Remote Sensing Image Dehazing: Benchmark and Baseline*.
IEEE Transactions on Geoscience and Remote Sensing 63 (2025), 1-14.
https://doi.org/10.1109/TGRS.2025.3584234

## Layout and labels

`images/{train,val,test}/{moderate_fog,thick_fog,thin_fog}/`

The alphabetical classification-loader indices are moderate_fog=0, thick_fog=1,
thin_fog=2. Increasing haze-severity ranks in this loader order are [1, 2, 0].
These are haze-severity labels, not meter-based visibility intervals.

`manifest.csv` contains source and local paths, split, class, loader index, byte size
and SHA-256 for every image. `dataset_metadata.json` contains counts and mappings.
Only hazy classification inputs are included, not the complete paired dehazing archive.
All image bytes were verified against the experiment-server manifest and were not
resized, enhanced or otherwise modified. This repository only reorganizes them into
the original classification split and adds metadata.

## Dataset terms

The upstream project's README states that use is subject to **Creative Commons
Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** and commercial use
requires permission. See the upstream README for the source notice and
https://creativecommons.org/licenses/by-nc/4.0/ for the license and legal text.
Retain attribution and comply with its noncommercial and other conditions.

The upstream repository also contains an MIT code-license file; this does not replace
the separate dataset-use terms stated in its README. The original authors retain
rights in their material. No broader license is granted by this redistribution.
