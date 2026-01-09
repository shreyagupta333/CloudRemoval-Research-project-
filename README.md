# Cloud Removal from Satellite Images: An Image Processing and ML Approach

# Abstract

Cloud cover is a major obstacle in the effective use of optical satellite imagery for remote sensing applications. Clouds obscure surface information and reduce the usability of satellite data for environmental monitoring, land-use analysis, and geographical studies. This research focuses on removing cloud-covered regions from satellite images using classical image processing and interpolation techniques, without relying on machine learning models. The study evaluates Inverse Distance Weighting (IDW) and Fractal Interpolation methods and analyzes their effectiveness in reconstructing cloud-obscured regions.

# Introduction

Satellite imagery plays a crucial role in monitoring environmental changes, land use, and geographical patterns. However, cloud contamination remains a persistent challenge, especially for optical sensors such as Landsat 8 and Landsat 9. This work aims to restore cloud-obscured regions using interpolation-based techniques that are computationally efficient and suitable for limited-data scenarios.

# Motivation

Cloud cover blocks surface information
Deep learning approaches require large datasets and high computational resources
Interpolation methods are training-free and explainable
Provides a strong baseline for future machine learning research

# Literature Review
Existing cloud removal techniques include both learning-based and classical image processing methods. While deep learning approaches offer strong performance, they are often data-intensive and complex. Interpolation-based methods remain relevant due to their simplicity, interpretability, and effectiveness in thick cloud regions.

# Methodology

## Cloud Detection and Masking
Identification of cloud-covered pixels and generation of cloud masks separating valid and missing regions.

## Inverse Distance Weighting (IDW) Interpolation
IDW estimates unknown pixel values using a weighted average of nearby cloud-free pixels, where closer pixels have greater influence.

## Fractal Interpolation
Fractal interpolation leverages self-similarity patterns in satellite imagery using neighborhood averaging and affine transformations.

## Inpainting vs Interpolation
Traditional image inpainting was evaluated and found to be less effective for thick cloud regions due to insufficient contextual information.

# Dataset

Satellite Sources: Landsat 8 & Landsat 9 (Collection 2, Level 2)
Spatial Resolution: 30 meters
Spectral Bands: Visible and Near-Infrared
Multiple geographic locations and acquisition dates

# Results

Significant reduction in cloud coverage
IDW performed well for moderate cloud density
Fractal interpolation preserved texture continuity
Cloud coverage reduced to below 3% in several cases
Processing time ranged from 1 to 5 hours

<img width="1144" height="576" alt="image" src="https://github.com/user-attachments/assets/ea847f88-a0b0-443d-90f1-a44811f2948e" />

<img width="768" height="1086" alt="image" src="https://github.com/user-attachments/assets/daeb5e11-79b7-4dbc-8889-193442261e7a" />



# Challenges

Thick cloud regions lack sufficient neighboring information
Reconstruction accuracy depends on spatial continuity
High computational cost for large satellite scenes
Absence of ground-truth cloud-free images

# Conclusion
This research demonstrates that interpolation-based image processing techniques can effectively reduce cloud coverage in satellite images without requiring training data. While not a replacement for deep learning methods, these techniques serve as reliable baselines and are particularly valuable in data-scarce scenarios.
