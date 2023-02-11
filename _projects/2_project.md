---
layout: page
title: lesion detection
description: Detectron2 based pipeline to detect lesions present in undersampled MRI images.
img: assets/img/lesion_detection.png
importance: 2
category: all
---

To save MRI image generation time from raw MRI measurements, deep learning algorithms have emerged as a viable method for MRI reconstruction with higher rates of acceleration. Recent reconstruction problems have shown various shortcomings in current deep learning approaches, including the loss of fine image details even when employing models that score well in terms of global quality criteria. This study provided an end-to-end deep learning framework for pathology detection present in MRI images.

The proposed system accepts as input MRI images obtained using MRI reconstruction algorithms (such as [VarNet](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.26977)), then conducts lesion identification. Using publicly available [fastMRI](https://arxiv.org/abs/1811.08839) dataset, this is the first study to establish an automated lesion identification pipeline for MRI images reconstructed using undersampled raw MRI measurements with comparable identification performance at undersampling factors upto 8.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/lesion_data_distribution.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: Distribution of lesions in fastMRI knee dataset.
</div>

The lesion identification pipeline consisted of three different variants of faster-rcnn models present in Detectron2 library: (1) faster_rcnn_R_50_FPN_3x; (2) faster_rcnn_R_50_DC5_3x; and (3) faster_rcnn_R_50_C4. The identified lesions from all these model variants were then ensembled for final output.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/inference_pipeline.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2: Overview of the lesion identification pipeline.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/joint_effusion_varnet_acc.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3: Joint effusion identification in VarNet reconstructed MRI images with fully sampled data and images reconstructed with undersampling factors of 4 and 8.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/joint_effusion_f1_score.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3: f1-score values for joint effusion identification in VarNet reconstructed MRI images with fully sampled data and images reconstructed with undersampling factors of 4 and 8.
</div>

It was observed that the developed lesion identification pipeline was able to detect common and as well some rare lesions with comparable identification performance for MRI images reconstructed at various undersampling rates. More information can be found in the presentation [here](https://docs.google.com/presentation/d/1e4rnnw2IUy727KgfCO0DB9T7aSrqSTNl/edit?usp=sharing&ouid=101805083213502751228&rtpof=true&sd=true).
