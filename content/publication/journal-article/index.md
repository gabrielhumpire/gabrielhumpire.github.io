---
title: "Fully Automatic Volume Measurement of the Spleen at CT Using Deep Learning"
authors:
- admin
- Joris Bukala
- Ernst T Scholten
- Mathias Prokop
- Bram van Ginneken
- Colin Jacobs
date: "2020-07-22"
doi: "10.1148/ryai.2020190102"

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "*Radiology: Artificial Intelligence,* 2020;2(4):e190102"
publication_short: ""

abstract:
  Purpose
  To develop a fully automated algorithm for spleen segmentation and to assess the performance of this algorithm in a large dataset.
  
  Materials and Methods
  In this retrospective study, a three-dimensional deep learning network was developed to segment the spleen on thorax-abdomen CT scans. Scans were extracted from patients undergoing oncologic treatment from 2014 to 2017. A total of 1100 scans from 1100 patients were used in this study, and 400 were selected for development of the algorithm. For testing, a dataset of 50 scans was annotated to assess the segmentation accuracy and was compared against the splenic index equation. In a qualitative observer experiment, an enriched set of 100 scan-pairs was used to evaluate whether the algorithm could aid a radiologist in assessing splenic volume change. The reference standard was set by the consensus of two other independent radiologists. A Mann-Whitney U test was conducted to test whether there was a performance difference between the algorithm and the independent observer.
  
  Results
  The algorithm and the independent observer obtained comparable Dice scores (P = .834) on the test set of 50 scans of 0.962 and 0.964, respectively. The radiologist had an agreement with the reference standard in 81% (81 of 100) of the cases after a visual classification of volume change, which increased to 92% (92 of 100) when aided by the algorithm.
  
  Conclusion
  A segmentation method based on deep learning can accurately segment the spleen on CT scans and may help radiologists to detect abnormal splenic volumes and splenic volume changes.

# Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Segmentation
featured: false
- Deep Learning
- Medical imaging

# links:
# - name: ""
#   url: ""
url_pdf: 'https://pubs.rsna.org/doi/full/10.1148/ryai.2020190102'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: 'https://grand-challenge.org/algorithms/spleen-segmentation/'
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
projects: [pandas]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---
