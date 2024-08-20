---
title: "Efficient organ localization using multi-label convolutional neural networks in thorax-abdomen CT scans."
authors:
- admin
- Arnaud Setio
- Bram van Ginneken
- Colin Jacobs
date: "2018-04-05"
doi: "10.1088/1361-6560/aab4b3"

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "*Physics in Medicine & Biology*, Volume 63, Number 8, 085003"
publication_short: ""

abstract:
  Automatic localization of organs and other structures in medical images is an important preprocessing step that can improve and speed up other algorithms such as organ segmentation, lesion detection, and registration. This work presents an efficient method for simultaneous localization of multiple structures in 3D thorax-abdomen CT scans.

  Our approach predicts the location of multiple structures using a single multi-label convolutional neural network for each orthogonal view. Each network takes extra slices around the current slice as input to provide extra context. A sigmoid layer is used to perform multi-label classification. The output of the three networks is subsequently combined to compute a 3D bounding box for each structure. We used our approach to locate 11 structures of interest. The neural network was trained and evaluated on a large set of 1884 thorax-abdomen CT scans from patients undergoing oncological workup. Reference bounding boxes were annotated by human observers.

  The performance of our method was evaluated by computing the wall distance to the reference bounding boxes. The bounding boxes annotated by the first human observer were used as the reference standard for the test set. Using the best configuration, we obtained an average wall distance of 3.20 +- 7.33 mm in the test set. The second human observer achieved 1.23 +- 3.39 mm. For all structures, the results were better than those reported in previously published studies.

  In conclusion, we proposed an efficient method for the accurate localization of multiple organs. Our method uses multiple slices as input to provide more context around the slice under analysis, and we have shown that this improves performance. This method can easily be adapted to handle more organs.

# Summary. An optional shortened abstract.
summary: Automatic organ localization using Deep Learning.

tags:
- Localization
- Deep Learning
- Medical imaging
- Computer Vision

featured: true

links:
url_pdf: 'https://iopscience.iop.org/article/10.1088/1361-6560/aab4b3/meta'
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
