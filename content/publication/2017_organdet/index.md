---
title: "Organ detection in thorax abdomen CT using multi-label convolutional neural networks"
authors:
- admin
- Arnaud Setio
- Bram van Ginneken
- Colin Jacobs
date: "2017-03-03"
doi: "10.1117/12.2254349"

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "Proceedings Volume 10134, Medical Imaging 2017: Computer-Aided Diagnosis (SPIE)"
publication_short: ""

abstract:
  A convolutional network architecture is presented to determine bounding boxes around six organs in thoraxabdomen CT scans. A single network for each orthogonal view determines the presence of lungs, kidneys, spleen and liver. We show that an architecture that takes additional slices before and after the slice of interest as an additional input outperforms an architecture that processes single slices. From the slice-based analysis, a bounding box around the structures of interest can be computed. The system uses 6 convolutional, 4 pooling and one fully connected layer and uses 333 scans for training and 110 for validation. The test set contains 110 scans. The average Dice score of the proposed method was 0.95 and 0.95 for the lungs, 0.59 and 0.58 for the kidneys, 0.83 for the liver and 0.63 for the spleen. This paper shows that automatic localization of organs using multi-label convolution neural networks is possible. This architecture can likely be used to identify other organs of interest as well.

# Summary. An optional shortened abstract.
summary:

tags:
- Computer Vision
- Detection
- Machine Learning
- Deep learning
- CT

featured: false

links:
url_pdf: https://doi.org/10.1117/12.2254349
url_project: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---
