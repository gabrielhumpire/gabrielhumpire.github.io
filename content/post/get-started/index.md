---
title: Winning Brazil's National COVID-19 AI Challenge
summary: How I built an automated CT scan segmentation system that won 1st place in Brazil's government-sponsored national AI competition.
date: 2020-08-07

authors:
  - admin

tags:
  - Deep Learning
  - Medical Imaging
  - Segmentation
  - COVID-19
---

In August 2020, during my PhD at Radboud University Medical Center, I won 1st place in Brazil's national COVID-19 CT segmentation challenge, organised by the Government of the State of São Paulo. The challenge drew entries from 30 teams across the country. This post describes the approach, the lessons learned, and what it meant to ship a system that could actually help clinicians during the pandemic.

## The Problem

COVID-19 was overwhelming hospitals in Brazil. Radiologists were drowning in CT scans, manually assessing ground-glass opacities and consolidations that indicated infection severity. The challenge: build an automated system to detect and segment COVID-19 lesions in thorax CT scans - accurately enough to be useful in a clinical setting.

## The Approach

My solution built on the organ segmentation expertise I had developed during my PhD. The key components were:

- **Preprocessing**: Normalisation and lung field extraction using a pretrained segmentation model to focus the network on relevant anatomy.
- **Architecture**: A 3D U-Net variant trained on the challenge dataset with heavy augmentation to compensate for limited annotated data.
- **Post-processing**: Connected component analysis and probability thresholding tuned to maximise sensitivity for clinical screening.

The entire pipeline was containerised with Docker to ensure reproducible results and easy deployment.

## What Made the Difference

Several factors contributed to winning:

1. **Domain knowledge**: Understanding CT imaging physics and anatomy let me choose sensible preprocessing steps that generic approaches miss.
2. **Transfer learning**: Weights pretrained on the large LIDC-IDRI dataset gave a strong starting point before fine-tuning on COVID data.
3. **Validation discipline**: Using a strict held-out validation set and not tuning on it - a basic principle that is easy to violate under competition pressure.

## Aftermath

The system was featured by the [University of São Paulo](https://jornal.usp.br/universidade/sistema-que-identifica-covid-19-em-tomografias-e-selecionado-em-desafio-internacional/) and went on to become one of two finalists in the IdeiaGov innovation challenge. It reinforced something I already believed: the gap between research accuracy and clinical utility is closed by engineering discipline, not just better architectures.
