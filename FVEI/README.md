# FVEI: source and partition metadata only

**Original FVEI images are not redistributed here.** Public redistribution permission
has not been confirmed, so this directory provides only provenance, split membership
and per-image checksums.

Source: Yang, W. *Multi visual feature fusion based fog visibility estimation for
expressway surveillance using deep learning network*. Expert Systems with Applications
234 (2023), 121151. https://doi.org/10.1016/j.eswa.2023.121151

The exact subset contains 4,190 deduplicated images: 3,052 training, 311 validation
and 827 held-out test images. `outer` in the manifest is the test partition.
This is the English-manuscript date-grouped fold2, not a different 918-image test split.

`manifest.csv` records each image's original relative path, split, class, loader index,
byte size and SHA-256. The `relative_path` column describes the Windows-compatible
local layout used during packaging; those image files are not part of this repository.
The original class names include < and >, so compatible local names and the exact
mapping are recorded in `dataset_metadata.json`. Image bytes and memberships were
not altered. Loader index order is 0-50 m, 100-200 m, 200-500 m, 50-100 m, above 500 m;
increasing-visibility ranks in this order are [0, 2, 3, 1, 4].

Obtain the images from the original rights holder/provider under their access terms,
then use the source filenames and checksums to reconstruct the listed partitions.
The metadata provided here does not grant rights to redistribute the original images.
