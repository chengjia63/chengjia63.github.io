---
layout: page
title: jiang2021rapid
ispub: true
exclude: true
---

**Background:** Accurate diagnosis of skull base tumors is essential for
providing personalized surgical treatment strategies. Intraoperative diagnosis
can be challenging due to tumor diversity and lack of intraoperative pathology
resources.

**Objective:** To develop an independent and parallel intraoperative pathology
workflow that can provide rapid and accurate skull base tumor diagnoses using
label-free optical imaging and artificial intelligence (AI).

**Method:** We used a fiber laser-based, label-free, non-consumptive,
high-resolution microscopy method (< 60 sec per 1x1 mm2), called stimulated
Raman histology (SRH), to image a consecutive, multicenter cohort of skull base
tumor patients. SRH images were then used to train a convolutional neural
network (CNN) model using three representation learning strategies:
cross-entropy, self-supervised contrastive learning, and supervised contrastive
learning. Our trained CNN models were tested on a held-out, multicenter SRH
dataset.

**Results:** SRH was able to image the diagnostic features of both benign and
malignant skull base tumors. Of the three representation learning strategies,
supervised contrastive learning most effectively learned the distinctive and
diagnostic SRH image features for each of the skull base tumor types. In our
multicenter testing set, cross-entropy achieved an overall diagnostic accuracy
of 91.5%, self-supervised contrastive learning 83.9%, and supervised
contrastive learning 96.6%. Our trained model was able to identify tumor-normal
margins and detect regions of microscopic tumor infiltration in whole-slide SRH
images.

**Conclusion:** SRH with AI models trained using contrastive representation
learning can provide rapid and accurate intraoperative diagnosis of skull base
tumors.

<img class="visabs" src="/assets/images/jiang2021rapid_overview.png" alt="Graphical Abstract">
