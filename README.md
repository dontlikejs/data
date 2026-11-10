# FVEI and RRSHID classification data

Dataset inputs and exact partition metadata used for the FVEI and RRSHID experiments
in **DPFO-Net: A Dual-Prior Frequency-Ordinal Network for Fog Visibility Classification**.

| Dataset | Train | Validation | Test | Images provided here |
|---|---:|---:|---:|---|
| FVEI | 3,052 | 311 | 827 | No. Sources, partition manifest and checksums only |
| RRSHID | 2,441 | 308 | 304 | Yes. 3,053 original hazy PNG images |

## Contents

- [FVEI](FVEI/README.md): source information, exact split membership, class mapping,
  image identifiers, byte sizes and SHA-256 checksums. FVEI images are **not included**.
- [RRSHID](RRSHID/README.md): the 3,053 hazy classification inputs, original author
  split, class mapping and per-image SHA-256 checksums.
- [Attribution and terms](ATTRIBUTION.md).

FVEI `outer` denotes the held-out test subset. It is the fixed 4,190-image,
deduplicated date-grouped fold used by the English manuscript, not the full original
FVEI collection. FVEI labels express meter-based visibility categories; RRSHID labels
express haze severity. Their label meanings are not interchangeable.

The manifests retain source filenames and provide image checksums so data obtained
from the original providers can be matched to the experimental partitions. Folder
indices and ordinal ranks are explicitly listed in each dataset's metadata.

This repository contains input data and partition metadata, not trained checkpoints,
model predictions, or a complete archive of all manuscript experiment records.
Seeing Through Fog images are not included.

## Obtaining the data

RRSHID images are in `RRSHID/images/{train,val,test}/{class}/` and can be downloaded
with this repository. For FVEI, obtain the original images from the dataset provider
and match them using `FVEI/manifest.csv`.

No blanket license is granted over all third-party material in this repository.
Please retain source attribution and follow the original dataset terms.
