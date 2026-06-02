---
# =============================================================================
# PUBLICATION TEMPLATE
# =============================================================================
# Copy this file and rename it to match your paper, e.g.:
#   2024-01-15-my-paper-title.md
#
# The filename date determines sort order on the Publications page.
# The category must match a key in _config.yml under publication_category.
# =============================================================================

title:      "Image to attribute model for trees (ITAM-T): individual tree detection and classification in Alberta boreal forest for wildland fire fuel characterization."
collection: publications
category:   manuscripts         # Use: manuscripts OR conferences
permalink:  /publication/itam-t
excerpt:    "This paper develops a deep learning workflow that detects and classifies individual trees from high-resolution RGB drone imagery, enabling the creation of accurate tree inventory and fuel maps that can support wildfire hazard assessment, management, and response."
date:       2022-02-25         # Publication date: YYYY-MM-DD
venue:      "International Journal of Remote Sensing"

# Optional links — delete any lines you don't need
paperurl:   "https://doi.org/10.1080/01431161.2022.2048914"
# bibtexurl:  "https://wildfire-ml.github.io/files/paper1.bib"
# slidesurl:  ""

# Full citation text shown at the bottom of the paper page
citation:   "Bennett, L., Wilson, B., Selland, S., Qian, L., Wood, M., Zhao, H., & Boisvert, J. (2022). Image to attribute model for trees (ITAM-T): individual tree detection and classification in Alberta boreal forest for wildland fire fuel characterization. International Journal of Remote Sensing, 43 (5), 1848–1880. https://doi.org/10.1080/01431161.2022.2048914"
---

Regional and municipal decision makers rely on fuel (vegetation) maps to inform decisions on tree stand management related to wildfire management and response. Remote sensing of trees is used in commercial applications but has limited uptake in the fire management community. A two-stage detection and identification convolutional network for high-resolution RGB drone imagery is developed to address this limitation. The detection routine is based on DeepForest, an existing convolutional neural network implementation designed to recognize trees in aerial imagery. Retraining the model and implementing an adaptive window-size workflow improves tree detection, with F1 scores reaching 85% and averaging 72% for k-fold cross-validation in boreal forest. For classification, a VGG19 network with added data augmentation and dropout layers is trained. When this network is implemented, manually annotated trees are recognized as coniferous with an average F1 of 97% and deciduous with an 87% F1. Overall, the developed image-to-attribute model for trees reaches a maximum F1 score of 85% considering classification after identification, with averages of 72% for coniferous trees and 57% for deciduous trees over six sites. Tree height, size, and stem density are extracted from the tree location output and geometric data. The calculated density is compared to the density of manual annotations, with an average R2 of 0.90. A remote preliminary proximity-based hazard assessment is performed on a rural property in Alberta, demonstrating the model’s ability to detect and classify trees near values-at-risk. The results indicate a potential extension to low-cost decision support in enterprise and fire-related applications.
