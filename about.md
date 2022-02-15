---
layout: page
title: About
permalink: /about/
---

The Gadgetron is an open source framework for medical image reconstruction. It has been developed at the National Heart, Lung, and Blood Institute, NIH, Bethesda, MD, USA and at the Department of Computer Science and Department of Clinical Medicine, Aarhus University, Denmark. It is made freely available to the medical image reconstruction community.

If you find the Gadgetron useful in your research, please cite this [paper](http://onlinelibrary.wiley.com/doi/10.1002/mrm.24389/abstract):

Hansen MS, S&#0248;rensen TS. Gadgetron: An Open Source Framework for Medical Image Reconstruction. Magn Reson Med. 2013 Jun;69(6):1768-76.

---

# What is Gadgetron

Gadgetron is a streaming data processing framework for medical image reconstruction. It has been developed to make it easier to prototype, test, and deploy new image reconstruction algorithms.

The framework features a number of reconstruction applications that can be employed directly. Moreover, it contains a wide range of toolboxes with common data structures and algorithms designed for a much broader use. These toolboxes can be used within the streaming framework to create new dedicated reconstruction components or used as shared libraries in standalone (or third party) applications.

This document serves as an introduction to the Gadgetron framework and provides some "getting started" examples of using it. A scientific paper is also available ([Magn Reson Med. 2013 Jun;69(6):1768-76](http://www.ncbi.nlm.nih.gov/pubmed/22791598)). Gadgetron is further extended to support cluster/cloud [Magn Reson Med. 2015 March;73(3):1015-1025](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.25213).

Although Gadgetron is a generic, multi-modality image reconstruction framework, it was initially developed to support the work of the authors in the field of advanced MRI reconstruction. Specifically to support work on fast image reconstruction, not only on traditional CPU architectures, but also using commodity graphics hardware (GPUs). Some examples that are made publicly available through the Gadgetron
framework include fast (re)gridding on the GPU ([IEEE Trans Med Imaging. 2008 Apr;27(4):538-47](http://www.ncbi.nlm.nih.gov/pubmed/18390350)), Cartesian parallel
imaging on the GPU ([Magn Reson Med. 2008 Mar;59(3):463-8](http://www.ncbi.nlm.nih.gov/pubmed/18306398)), and non-Cartesian parallel imaging on the GPU ([IEEE Trans Med Imaging. 2009 Dec;28(12):1974-85](http://www.ncbi.nlm.nih.gov/pubmed/19628452)), and free-breathing cardiac cine imaging [JCMR 2013; 15:102](https://jcmr-online.biomedcentral.com/articles/10.1186/1532-429X-15-102).

