---
title: "The Liver Tumor Segmentation Benchmark (LiTS)"
authors:
- Patrick Bilic
- Patrick Christ
- Hongwei Bran Li
- Eugene Vorontsov
- Avi Ben-Cohen
- Georgios Kaissis
- Adi Szeskin
- Colin Jacobs
- admin
- Gabriel Chartrand
- Fabian Lohöfer
- Julian Walter Holch
- Wieland Sommer
- Felix Hofmann
- Alexandre Hostettler
- Naama Lev-Cohain
- Michal Drozdzal
- Michal Marianne Amitai
- Refael Vivanti
- Jacob Sosna
- Ivan Ezhov
- Anjany Sekuboyina
- Fernando Navarro
- Florian Kofler
- Johannes C Paetzold
- Suprosanna Shit
- Xiaobin Hu
- Jana Lipková
- Markus Rempfler
- Marie Piraud
- Jan Kirschke
- Benedikt Wiestler
- Zhiheng Zhang
- Christian Hülsemeyer
- Marcel Beetz
- Florian Ettlinger
- Michela Antonelli
- Woong Bae
- Míriam Bellver
- Lei Bi
- Hao Chen
- Grzegorz Chlebus
- Erik B Dam
- Qi Dou
- Chi-Wing Fu
- Bogdan Georgescu
- Xavier Giró-i-Nieto
- Felix Gruen
- Xu Han
- Pheng-Ann Heng
- Jürgen Hesser
- Jan Hendrik Moltz
- Christian Igel
- Fabian Isensee
- Paul Jäger
- Fucang Jia
- Krishna Chaitanya Kaluva
- Mahendra Khened
- Ildoo Kim
- Jae-Hun Kim
- Sungwoong Kim
- Simon Kohl
- Tomasz Konopczynski
- Avinash Kori
- Ganapathy Krishnamurthi
- Fan Li
- Hongchao Li
- Junbo Li
- Xiaomeng Li
- John Lowengrub
- Jun Ma
- Klaus Maier-Hein
- Kevis-Kokitsi Maninis
- Hans Meine
- Dorit Merhof
- Akshay Pai
- Mathias Perslev
- Jens Petersen
- Jordi Pont-Tuset
- Jin Qi
- Xiaojuan Qi
- Oliver Rippel
- Karsten Roth
- Ignacio Sarasua
- Andrea Schenk
- Zengming Shen
- Jordi Torres
- Christian Wachinger
- Chunliang Wang
- Leon Weninger
- Jianrong Wu
- Daguang Xu
- Xiaoping Yang
- Simon Chun-Ho Yu
- Yading Yuan
- Miao Yue
- Liping Zhang
- Jorge Cardoso
- Spyridon Bakas
- Rickmer Braren
- Volker Heinemann
- Christopher Pal
- An Tang
- Samuel Kadoury
- Luc Soler
- Bram van Ginneken
- Hayit Greenspan
- Leo Joskowicz
- Bjoern Menze
date: "2023-02-01"
doi: "10.1016/j.media.2022.102680"

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Medical Image Analysis 84, 102680"
publication_short: ""

abstract:
  In this work, we report the set-up and results of the Liver Tumor Segmentation Benchmark (LiTS), which was organized in conjunction with the IEEE International Symposium on Biomedical Imaging (ISBI) 2017 and the International Conferences on Medical Image Computing and Computer-Assisted Intervention (MICCAI) 2017 and 2018. The image dataset is diverse and contains primary and secondary tumors with varied sizes and appearances with various lesion-to-background levels (hyper-/hypo-dense), created in collaboration with seven hospitals and research institutions. Seventy-five submitted liver and liver tumor segmentation algorithms were trained on a set of 131 computed tomography (CT) volumes and were tested on 70 unseen test images acquired from different patients. We found that not a single algorithm performed best for both liver and liver tumors in the three events. The best liver segmentation algorithm achieved a Dice score of 0.963, whereas, for tumor segmentation, the best algorithms achieved Dices scores of 0.674 (ISBI 2017), 0.702 (MICCAI 2017), and 0.739 (MICCAI 2018). Retrospectively, we performed additional analysis on liver tumor detection and revealed that not all top-performing segmentation algorithms worked well for tumor detection. The best liver tumor detection method achieved a lesion-wise recall of 0.458 (ISBI 2017), 0.515 (MICCAI 2017), and 0.554 (MICCAI 2018), indicating the need for further research. LiTS remains an active benchmark and resource for research, e.g., contributing the liver-related segmentation tasks in [http://medicaldecathlon.com/](http://medicaldecathlon.com/). In addition, both data and online evaluation are accessible via [https://competitions.codalab.org/competitions/17094](https://competitions.codalab.org/competitions/17094).

# Summary. An optional shortened abstract.
summary: Automatic detection and segmentation of battery cells of Electric Vehicles.

tags:
- Segmentation
- Deep Learning
- CT scans
- Computer Vision

featured: false

links:
url_pdf: 'https://www.sciencedirect.com/science/article/pii/S1361841522003085'
url_project: ''
url_code: ''
url_dataset: 'https://competitions.codalab.org/competitions/17094'
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
