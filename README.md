

# A survey of label-noise deep learning for medical image analysis

Our manuscript is under review. 

## abstract

There are many factors associated with the success of deep learning. One of the most important is the availability of large-scale datasets with clean annotations. However, it is particularly difficult to obtain such datasets with accurate labels for medical image domain. The reliability and consistency of medical imaging labeling are the issue and there usually exists low-quality annotations with label noise. As the noisy labels degrade the generalization performance of deep neural networks, learning with noisy labels is becoming an important task for medical image analysis. The literatures on this topic have expanded in volume and scope. However, no recent surveys exist to collect and organize this knowledge, impeding the ability of researchers and practitioners to utilize it. In this work, we present an up-to-date survey of label-noise learning for medical image domain. Through the analysis of task characteristic and labeling procedure, we conclude three typical types of label noise: label noise for classification tasks, the morphological noise for segmentation tasks, the inter-observer variability for both classification and segmentation tasks. For every label noise type, we review extensive literatures, illustrate some typical methods and show the unified taxonomies in terms of methodological and task difference. Afterwards, we conduct methodological comparison based on some typically properties of task category, data dimension, organ/disease types and applied strategy. We further analyze existing methods and corresponding pros and cons. Finally, we spark some new directions based on the characteristics of medical images. Our survey aims to provide researchers and practitioners with a solid understanding of existing medical label-noise learning, such as the main algorithms developed over the past few years, which could help them to investigate new methods to combat with the negative effect of label noise.


## Papers 

This article is an introductory review, citing many other articles. For your convenience, here are the relevant links of the tables in the paper



##### **Table 1. Some typical publications for learning with label noise for classification task**

| Taxonomy                    | Method                                           | Typical publications             | Natural image/ Medical image | Paper name                                              | Link                                                     |
| --------------------------- | ------------------------------------------------ | -------------------------------- | ---------------------------- | ------------------------------------------------------- | -------------------------------------------------------- |
| **Noise transition matrix** | Adaptation layer                                 | Goldberger and Ben-Reuven(2016） | Natural image domain         | Training deep neural-networks  using a noise adaptation layer | [link](https://openreview.net/pdf?id=H12GRgcxg)          |
|                             | Gold loss correction                             | Hendrycks et al.(2018)           | Natural image domain         | Using trusted data to train deep  networks on labels corrupted by severe noise, | [link](https://proceedings.neurips.cc/paper_files/paper/2018/file/ad554d8c3b06d6b97ee76a2448bd7913-Paper.pdf) |
|                             | Prior knowledge                                  | Han et al.(2018b)                | Natural image domain         | Co-teaching: Robust training of  deep neural networks with extremely noisy labels | [link](https://proceedings.neurips.cc/paper_files/paper/2018/file/a19744e268754fb0148b017647355b7b-Paper.pdf) |
|                             | Prior knowledge                                  | Cheng et al.(2022)               | Natural image domain         | Instance-dependent label-noise  learning with manifold-regularized transition matrix estimation | [link](https://openaccess.thecvf.com/content/CVPR2022/papers/Cheng_Instance-Dependent_Label-Noise_Learning_With_Manifold-Regularized_Transition_Matrix_Estimation_CVPR_2022_paper.pdf) |
|                             | For medical imaging tasks                        | Dgani et al.(2018)               | Medical image domain         | Training a neural network based  on unreliable human annotation of medical images | [link](https://www.eng.biu.ac.il/goldbej/files/2018/01/ISBI_2016_Yair.pdf) |
| **Regularization**          | Label Smoothing                                  | Lukasik et al.(2020)             | Natural image domain         | Does label smoothing mitigate  label noise?             | [link](http://proceedings.mlr.press/v119/lukasik20a/lukasik20a.pdf) |
|                             | Label Smoothing (Negative label smoothing)       | Wei et al.(2022a)                | Natural image domain         | To smooth or not? when label  smoothing meets noisy labels | [link](https://arxiv.org/pdf/2106.04149.pdf)             |
|                             | Data augmentation (Mixup)                        | Zhang et al. (2017)              | Natural image domain         | mixup: Beyond empirical risk  minimization              | [link](https://arxiv.org/pdf/1710.09412.pdf)             |
|                             | Data augmentation (Weak and strong augmentation) | Nishi et al. (2021)              | Natural image domain         | Augmentation strategies for  learning with noisy labels | [link](https://openaccess.thecvf.com/content/CVPR2021/papers/Nishi_Augmentation_Strategies_for_Learning_With_Noisy_Labels_CVPR_2021_paper.pdf) |
|                             | Data augmentation (MetaCleaner)                  | Zhang et al. (2019)              | Natural image domain         | Metacleaner: Learning to  hallucinate clean representations for noisy-labeled visual recognition | [link](https://openaccess.thecvf.com/content_CVPR_2019/papers/Zhang_MetaCleaner_Learning_to_Hallucinate_Clean_Representations_for_Noisy-Labeled_Visual_Recognition_CVPR_2019_paper.pdf) |
|                             | Pre-training                                     | Hendrycks et al. (2019)          | Natural image domain         | Using pre-training can improve  model robustness and uncertainty, in: International Conference on Machine  Learning | [link](http://proceedings.mlr.press/v97/hendrycks19a/hendrycks19a.pdf) |
|                             | Pre-training (Contrast-to-divide)                | Zheltonozhskii et al. (2022)     | Natural image domain         | Contrast to divide:  Self-supervised pre-training for learning with noisy labels | [link](https://openaccess.thecvf.com/content/WACV2022/papers/Zheltonozhskii_Contrast_To_Divide_Self-Supervised_Pre-Training_for_Learning_With_Noisy_Labels_WACV_2022_paper.pdf) |
|                             | Robust early-learning                            | Liu et al. (2020)                | Natural image domain         | Early-learning regularization prevents  memorization of noisy labels | [link](https://proceedings.neurips.cc/paper/2020/file/ea89621bee7c88b2c5be6681c8ef4906-Paper.pdf) |
|                             | For medical imaging tasks                        | Pham et al. (2019)               | Medical image domain         | Interpreting chest x-rays via  cnns that exploit disease dependencies and uncertainty     labels | [link](https://arxiv.org/pdf/1911.06475.pdf)             |
| **Loss re-designing**       | Generalized cross entropy loss                   | Zhang and Sabuncu (2018)         | Natural image domain         | Generalized cross entropy loss  for training deep neural networks with noisy labels | [link](https://proceedings.neurips.cc/paper_files/paper/2018/file/f2925f97bc13ad2852a7a551802feea0-Paper.pdf) |
|                             | Symmetric cross entropy loss                     | Wang et al. (2019)               | Natural image domain         | Symmetric cross entropy for  robust learning with noisy labels | [link](https://openaccess.thecvf.com/content_ICCV_2019/papers/Wang_Symmetric_Cross_Entropy_for_Robust_Learning_With_Noisy_Labels_ICCV_2019_paper.pdf) |
|                             | Partially Huberized loss                         | Menon et al. (2019)              | Natural image domain         | Can gradient clipping mitigate  label noise?            | [link](https://openreview.net/pdf?id=rklB76EKPr)        |
|                             | Incorporating contrastive learning loss          | Yi et al. (2022)                 | Natural image domain         | On learning contrastive  representations for learning with noisy labels | [link](https://openaccess.thecvf.com/content/CVPR2022/papers/Yi_On_Learning_Contrastive_Representations_for_Learning_With_Noisy_Labels_CVPR_2022_paper.pdf) |
|                             | For medical imaging tasks                        | Karimi et al. (2020)             | Medical image domain         | Deep learning with noisy labels:  Exploring techniques and remedies in medical image analysis | [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7484266) |
| **Loss re-weighting**       | Gradient directions re-weighting                 | Ren et al. (2018)                | Natural image domain         | Learning to reweight examples  for robust deep learning, in: International Conference on Machine Learning | [link](http://proceedings.mlr.press/v80/ren18a/ren18a.pdf) |
|                             | Natural network re-weighting                     | Shu et al. (2019)                | Natural image domain         | Meta-weight-net: Learning an  explicit mapping for sample weighting | [link](https://proceedings.neurips.cc/paper_files/paper/2019/file/e58cc5ca94270acaceed13bc82dfedf7-Paper.pdf) |
|                             | Natural network re-weighting (Faster)            | Xu et al. (2021)                 | Natural image domain         | Faster meta update strategy for  noise-robust deep learning | [link](https://openaccess.thecvf.com/content/CVPR2021/papers/Xu_Faster_Meta_Update_Strategy_for_Noise-Robust_Deep_Learning_CVPR_2021_paper.pdf) |
|                             | Distance re-weighting                            | Lee et al. (2018)                | Natural image domain         | Cleannet: Transfer learning for  scalable image classifier training with label noise | [link](https://openaccess.thecvf.com/content_cvpr_2018/papers/Lee_CleanNet_Transfer_Learning_CVPR_2018_paper.pdf) |
|                             | Angular re-weighting                             | Hu et al. (2019)                 | Natural image domain         | Noise-tolerant paradigm for  training face recognition cnns | [link](https://openaccess.thecvf.com/content_CVPR_2019/papers/Hu_Noise-Tolerant_Paradigm_for_Training_Face_Recognition_CNNs_CVPR_2019_paper.pdf) |
|                             | For medical imaging tasks                        | Xue et al. (2019)                | Medical image domain         | Robust learning at noisy labeled  medical images: Applied to skin lesion classification | [link](https://arxiv.org/pdf/1901.07759.pdf)            |
| **Label correction**        | Predictions-based correction                     | Tanaka et al. (2018)             | Natural image domain         | Joint optimization framework for  learning with noisy labels | [link](https://openaccess.thecvf.com/content_cvpr_2018/papers/Tanaka_Joint_Optimization_Framework_CVPR_2018_paper.pdf) |
|                             | Learning-based correction                        | Yi and Wu (2019)                 | Natural image domain         | Probabilistic end-to-end noise  correction for learning with noisy labels | [link](https://openaccess.thecvf.com/content_CVPR_2019/papers/Yi_Probabilistic_End-To-End_Noise_Correction_for_Learning_With_Noisy_Labels_CVPR_2019_paper.pdf) |
|                             | Prototype-based correction                       | Shi et al. (2021b)               | Natural image domain         | Automatic clinical target volume  delineation for cervical cancer in ct images using deep     learning | [link](https://openaccess.thecvf.com/content_CVPR_2019/papers/Yi_Probabilistic_End-To-End_Noise_Correction_for_Learning_With_Noisy_Labels_CVPR_2019_paper.pdf) |
|                             | Convex combination correction                    | Han et al. (2019)                | Natural image domain         | Deep self-learning from noisy  labels                   | [link](https://openaccess.thecvf.com/content_ICCV_2019/papers/Han_Deep_Self-Learning_From_Noisy_Labels_ICCV_2019_paper.pdf) |
|                             | For medical imaging tasks                        | Qiu et al. (2023)                | Medical image domain         | Hierarchical multimodal fusion  framework based on noisy label learning and attention mechanism for  cancer classification with pathology and genomic features | [link](https://www.sciencedirect.com/science/article/abs/pii/S089561112200146X) |
| **Optimization policy**     | Sample selection (Decoupling)                    | Malach and Shalev-Shwartz (2017) | Natural image domain         | Decoupling” when to update”  from” how to update”       | [link](https://proceedings.neurips.cc/paper_files/paper/2017/file/58d4d1e7b1e97b258c9ed0b37e02d087-Paper.pdf) |
|                             | Sample selection (Co-teaching)                   | Han et al. (2018b)               | Natural image domain         | Co-teaching: Robust training of  deep neural networks with extremely noisy labels | [link](https://proceedings.neurips.cc/paper_files/paper/2018/file/a19744e268754fb0148b017647355b7b-Paper.pdf) |
|                             | Sample selection (Co-teaching+)                  | Yu et al. (2019))                | Natural image domain         | How does disagreement help  generalization against label corruption? | [link](http://proceedings.mlr.press/v97/yu19b/yu19b.pdf) |
|                             | Sample selection (JoCoR)                         | Wei et al. (2020)                | Natural image domain         | Combating noisy labels by  agreement: A joint training method with co-regularization | [link](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wei_Combating_Noisy_Labels_by_Agreement_A_Joint_Training_Method_with_CVPR_2020_paper.pdf) |
|                             | Sample selection (PNP)                           | Sun et al. (2022)                | Natural image domain         | Pnp: Robust learning from noisy  labels by probabilistic noise prediction | [link](https://openaccess.thecvf.com/content/CVPR2022/papers/Sun_PNP_Robust_Learning_From_Noisy_Labels_by_Probabilistic_Noise_Prediction_CVPR_2022_paper.pdf) |
|                             | Hybrid Approach (DivideMix)                      | Li et al. (2020)                 | Natural image domain         | Dividemix: Learning with noisy  labels as semi-supervised learning | [link](https://arxiv.org/pdf/2002.07394.pdf)            |
|                             | Hybrid Approach (MJO)                            | Shi and Wu (2021)                | Natural image domain         | Distilling effective supervision  for robust medical image segmentation with noisy labels | [link](https://arxiv.org/pdf/2106.11099.pdf)            |
|                             | Hybrid Approach (For severe label noise)         | Zhang et al. (2020c)             | Natural image domain         | Distilling effective supervision from severe label noise | [link](https://openaccess.thecvf.com/content_CVPR_2020/papers/Zhang_Distilling_Effective_Supervision_From_Severe_Label_Noise_CVPR_2020_paper.pdf) |
|                             | For medical imaging tasks (Sample selection)     | Ashraf et al. (2022)             | Medical image domain         | A loss-based patch label  denoising method for improving whole-slide image analysis using a  convolutional neural network | [link](https://www.nature.com/articles/s41598-022-05001-8) |
|                             | For medical imaging tasks (Hybrid approach)      | Xue et al. (2022)                | Medical image domain         | Robust medical image     classification from noisy labeled data with global and local  representation     guided co-training. | [link](https://arxiv.org/pdf/2205.04723.pdf)            |



**Table 2. Some typical publications for learning with label noise for natural image segmentation**

| Publications          | Taxonomy                | Pixel-wise noisy labels/Class-level noisy labels | Description                                       | Paper name                                                   | Link                                                         |
| --------------------- | ----------------------- | ------------------------------------------------ | ------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Yi et al. (2021)      | Optimization policy     | Pixel-wise noisy labels                          | Sub-task of semi-supervised semantic segmentation | Learning from pixel-level label  noise: A new perspective for semi-supervised semantic segmentation | [link](https://arxiv.org/pdf/2103.14242.pdf)                 |
| Zheng and Yang (2021) | Regularization          | Pixel-wise noisy labels                          | Sub-task of unsupervised domain  adaptation       | Rectifying pseudo label learning via uncertainty estimation for domain  adaptive semantic segmentation | [link](https://arxiv.org/pdf/2003.03773.pdf)                 |
| Zhang et al. (2021c)  | Label correction        | Pixel-wise noisy labels                          | Sub-task of unsupervised domain adaptation        | Prototypical pseudo label  denoising and target structure learning for domain adaptive semantic  segmentation | [link](https://openaccess.thecvf.com/content/CVPR2021/papers/Zhang_Prototypical_Pseudo_Label_Denoising_and_Target_Structure_Learning_for_Domain_CVPR_2021_paper.pdf) |
| Guo et al. (2021)     | Noise transition matrix | Class-level noisy labels                         | Sub-task of unsupervised domain adaptation        | MetaCorrection: Domain-aware meta loss correction for unsupervised domain  adaptation in semantic segmentation | [link](https://openaccess.thecvf.com/content/CVPR2021/papers/Guo_MetaCorrection_Domain-Aware_Meta_Loss_Correction_for_Unsupervised_Domain_Adaptation_in_CVPR_2021_paper.pdf) |
| Yang et al. (2020)    | Loss re-designing       | Class-level noisy labels                         | Sub-task of instance segmentation                 | Learning with noisy class labels  for instance segmentation  | [link](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123590035.pdf) |



**Table 3. Some typical publications for learning with label noise for medical image segmentation**

| Publications               | Taxonomy                         | paper name                                                   | Link                                                         |
| -------------------------- | -------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Mirikharaji et al. (2019)  | Loss re-weighting                | Learning to segment skin lesions  from noisy annotations     | [link](https://arxiv.org/pdf/1906.03815.pdf)                 |
| Min et al. (2019)          | Optimization policy              | A two-stream mutual attention  network for semi-supervised biomedical segmentation with noisy labels | [link](https://ojs.aaai.org/index.php/AAAI/article/view/4381) |
| Zhang et al. (2020b)       | Optimization policy              | Robust medical image  segmentation from non-expert annotations with tri-network | [link](https://www.researchgate.net/profile/Lequan-Yu/publication/345263627_Robust_Medical_Image_Segmentation_from_Non-expert_Annotations_with_Tri-network/links/601c955192851c4ed54bd593/Robust-Medical-Image-Segmentation-from-Non-expert-Annotations-with-Tri-network.pdf) |
| Wang et al. (2020b)        | Loss re-designing                | A noise-robust framework for  automatic segmentation of covid-19 pneumonia lesions from ct images | [link](https://web.archive.org/web/20201107045237id_/https:/ieeexplore.ieee.org/ielx7/42/9153182/09109297.pdf) |
| Zhu et al. (2019a)         | Loss re-weighting                | Pick-and-learn: Automatic  quality evaluation for noisy-labeled image segmentation | [link](https://arxiv.org/pdf/1907.11835.pdf)                 |
| Shi and Wu (2021)          | Optimization policy              | Distilling effective supervision  for robust medical image segmentation with noisy labels | [link](https://arxiv.org/pdf/2106.11099.pdf)                 |
| Pornvoraphat et al. (2023) | Regularization (Label smoothing) | Real-time gastric intestinal  metaplasia diagnosis tailored for bias and noisy-labeled data with multiple  endoscopic imaging | [link](https://www.sciencedirect.com/science/article/abs/pii/S0010482523000471) |
| Karimi et al. (2023)       | Regularization (Label smoothing) | Learning to segment fetal brain  tissue from noisy annotations. Medical Image Analysis | [link](https://arxiv.org/pdf/2203.14962.pdf)                 |
| Liu et al. (2022a)         | Label correction                 | Adaptive early-learning  correction for segmentation from noisy annotations | [link](https://openaccess.thecvf.com/content/CVPR2022/papers/Liu_Adaptive_Early-Learning_Correction_for_Segmentation_From_Noisy_Annotations_CVPR_2022_paper.pdf) |
| Jin et al. (2022)          | Label correction                 | Deep neural network-based noisy  pixel estimation for breast ultrasound segmentation | [link](https://ieeexplore.ieee.org/abstract/document/9898006) |
| Fang et al. (2023)         | Optimization policy              | Reliable mutual distillation for  medical image segmentation under imperfect annotations | [link](https://ieeexplore.ieee.org/abstract/document/10021263) |



**Table 4. Some typical publications for inter-observer variability for medical image domain**

| Publications              | The  perspective of clean labels/noisy labels | Method                               | Task example   | Full name                                                    | Link                                                         |
| ------------------------- | --------------------------------------------- | ------------------------------------ | -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Menze et al. (2014)       | Clean labels                                  | Majority vote                        |                | The multimodal brain tumor image segmentation benchmark (brats) | [link](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6975210) |
| Warfield et al. (2004)    | Clean labels                                  | Label fusion                         |                | Simultaneous truth and performance level estimation (staple): an  algorithm for the validation of image segmentation | [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1283110/?pagewanted=all) |
| Cardoso et al. (2013)     | Clean labels                                  | Label fusion                         |                | Steps: Similarity and truth estimation for propagated segmentations and  its application to hippocampal segmentation and brain parcelation | [link](https://www.sciencedirect.com/science/article/pii/S1361841513000200) |
| Kohl et al. (2018)        | Clean labels                                  | Modeling multi-annotator  variations | Segmentation   | A probabilistic u-net for segmentation of ambiguous images   | [link](https://proceedings.neurips.cc/paper_files/paper/2018/file/473447ac58e1cd7e96172575f48dca3b-Paper.pdf) |
| Baumgartner et al. (2019) | Clean labels                                  | Modeling multi-annotator  variations | Segmentation   | Phiseg: Capturing uncertainty in medical image segmentation  | [link](https://arxiv.org/pdf/1906.04045.pdf)                 |
| Kohl et al. (2019)        | Clean labels                                  | Modeling multi-annotator  variations | Segmentation   | A hierarchical probabilistic u-net for modeling multi-scale ambiguities | [link](https://arxiv.org/pdf/1905.13077.pdf)                 |
| Zhang et al. (2020a)      | Noisy labels                                  | Noise transition matrix              | Segmentation   | Disentangling human error from the ground truth in segmentation of  medical images | [link](https://proceedings.neurips.cc/paper_files/paper/2020/file/b5d17ed2b502da15aa727af0d51508d6-Paper.pdf) |
| Xiao et al. (2021)        | Noisy labels                                  | Loss re-weighting                    | Segmentation   | Pathological image segmentation with noisy labels            | [link](https://arxiv.org/pdf/2104.02602.pdf)                 |
| Tanno et al. (2019)       | Noisy labels                                  | Noise transition matrix              | Classification | Learning from noisy labels by regularized estimation of annotator  confusion | [link](https://openaccess.thecvf.com/content_CVPR_2019/papers/Tanno_Learning_From_Noisy_Labels_by_Regularized_Estimation_of_Annotator_Confusion_CVPR_2019_paper.pdf) |
| Ju et al. (2022)          | Noisy labels                                  | Loss re-weighting                    | Classification | Improving medical images classification with label noise using  dual-uncertainty estimation | [link](https://arxiv.org/pdf/2103.00528.pdf)                 |
| Liao et al. (2022)        | Noisy labels                                  | Optimization policy                  | Classification | Learning from ambiguous labels for lung nodule malignancy prediction | [link](https://arxiv.org/pdf/2104.11436.pdf)                 |
| Wei et al. (2022b)        | Noisy labels                                  | Optimization policy                  | Classification | To aggregate or not? learning with separate noisy labels     | [link](https://dl.acm.org/doi/pdf/10.1145/3580305.3599522)   |



**Table 5. Methodological comparison for existing typical papers. T, D, O, S represent ‘task category’, ‘Data dimension’, ‘Organ/disease types’, ‘Applied strategy’, respectively.**

| Typical  Papers            | T              | D    | O                                                      | S                                          | Paper name                                                   | Link                                                         |
| -------------------------- | -------------- | ---- | ------------------------------------------------------ | ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Classification with label noise**       |                |      |                                                        |                                            |                                                              |                                                              |
| Dgani et al. (2018)        | Classification | 2D   | Breast microcalcifications                             | Noise transition matrix                    | Training a neural network based on unreliable human annotation of medical  images | [link](https://www.eng.biu.ac.il/goldbej/files/2018/01/ISBI_2016_Yair.pdf) |
| Pham et al. (2019)         | Classification | 2D   | Chest radiography                                      | Regularization                             | Interpreting chest x-rays via  cnns that exploit disease dependencies and uncertainty labels | [link](https://arxiv.org/pdf/1911.06475.pdf)                 |
| Karimi et al. (2020)       | Classification | 2D   | Prostate tissue                                        | Loss re-designing                          | Deep learning with noisy labels: Exploring techniques and remedies in  medical image analysis | [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7484266/) |
| Xue et al. (2019)          | Classification | 2D   | Skin lesion                                            | Loss re-weighting                          | Robust learning at noisy labeled medical images: Applied to skin lesion  classification | [link](https://arxiv.org/pdf/1901.07759.pdf)                 |
| Qiu et al. (2023)          | Classification | 2D   | Pathology of glioma and lung carcinoma                 | Label correction                           | Hierarchical multimodal fusion framework based on noisy label learning  and attention mechanism for cancer classification with pathology and genomic  features | [link](https://www.sciencedirect.com/science/article/abs/pii/S089561112200146X) |
| Ashraf et al. (2022)       | Classification | 2D   | Stomach pathology patch dataset                        | Optimization policy                        | A loss-based patch label denoising method for improving whole-slide image  analysis using a convolutional neural network | [link](https://www.nature.com/articles/s41598-022-05001-8)   |
| Xue et al. (2022)          | Classification | 2D   | 1) Melanoma lesion from  dermoscopy images             | Optimization policy                        | Robust medical image  classification from noisy labeled data with global and local representation  guided co-training | [link](https://arxiv.org/pdf/2205.04723.pdf)                 |
|                            |                |      | 2) Lymph node from  histopathologic images             |                                            |                                                              |                                                              |
|                            |                |      | 3) Chest X-ray with NLP labeled datasets               |                                            |                                                              |                                                              |
|                            |                |      | 4) Prostate cancer with digital  histopathology        |                                            |                                                              |                                                              |
| **Segmentation with lable noise**    |                |      |                                                        |                                            |                                                              |                                                              |
| Pornvoraphat et al. (2023) | Segmentation   | 2D   | Gastric intestinal metaplasia  with endoscopic imaging | Regularization                             | Real-time gastric intestinal  metaplasia diagnosis tailored for bias and noisy-labeled data with  multiple endoscopic imaging | [link](https://www.sciencedirect.com/science/article/abs/pii/S0010482523000471) |
| Karimi et al. (2023)       | Segmentation   | 3D   | Fetal brain tissue with MRI                            | Regularization                             | Learning to segment fetal brain tissue from noisy annotations. Medical  Image Analysis | [link](https://arxiv.org/pdf/2203.14962.pdf)                 |
| Mirikharaji et al. (2019)  | Segmentation   | 2D   | Skin lesion                                            | Loss re-weighting                          | Learning to segment skin lesions  from noisy annotations     | [link](https://arxiv.org/pdf/1906.03815.pdf)                 |
| Min et al. (2019)          | Segmentation   | 3D   | HVSMR 2016 and BRATS 2015                              | Optimization policy                        | A two-stream mutual attention  network for semi-supervised biomedical segmentation with noisy labels | [link](https://ojs.aaai.org/index.php/AAAI/article/view/4381) |
| Zhang et al. (2020b)       | Segmentation   | 2D   | JSRT and Stroke dataset                                | Optimization policy                        | Robust medical image  segmentation from non-expert annotations with tri-network | [link](https://www.researchgate.net/profile/Lequan-Yu/publication/345263627_Robust_Medical_Image_Segmentation_from_Non-expert_Annotations_with_Tri-network/links/601c955192851c4ed54bd593/Robust-Medical-Image-Segmentation-from-Non-expert-Annotations-with-Tri-network.pdf) |
| Wang et al. (2020b)        | Segmentation   | 2D   | COVID-19                                               | Loss re-designing                          | A noise-robust framework for  automatic segmentation of covid-19 pneumonia lesions from ct images | [link](https://web.archive.org/web/20201107045237id_/https:/ieeexplore.ieee.org/ielx7/42/9153182/09109297.pdf) |
| Zhu et al. (2019a)         | Segmentation   | 2D   | JSRT                                                   | Loss re-designing                          | Pick-and-learn: Automatic  quality evaluation for noisy-labeled image segmentation | [link](https://arxiv.org/pdf/1907.11835.pdf)                 |
| Shi and Wu (2021)          | Segmentation   | 3D   | Left Atrial and CTV dataset                            | Loss re-weighting and Label correction     | Distilling effective supervision  for robust medical image segmentation with noisy labels | [link](https://arxiv.org/pdf/2106.11099.pdf)                 |
| Liu et al. (2022a)         | Segmentation   | 3D   | SegTHOR CT dataset                                     | Label correction                           | Adaptive early-learning  correction for segmentation from noisy annotations | [link](https://openaccess.thecvf.com/content/CVPR2022/papers/Liu_Adaptive_Early-Learning_Correction_for_Segmentation_From_Noisy_Annotations_CVPR_2022_paper.pdf) |
| Jin et al. (2022)          | Segmentation   | 2D   | Breast ultrasound                                      | Label correction                           | Deep neural network-based noisy  pixel estimation for breast ultrasound segmentation | [link](https://ieeexplore.ieee.org/abstract/document/9898006) |
| Fang et al. (2023)         | Segmentation   | 3D   | LIDC-IDRI CT; ACDC MRI; BraTS  MRI                     | Optimization policy                        | Reliable mutual distillation for  medical image segmentation under imperfect annotations | [link](https://ieeexplore.ieee.org/abstract/document/10021263) |
| **Inter-observer variability**  |                |      |                                                        |                                            |                                                              |                                                              |
| Zhang et al. (2020a)       | Segmentation   | 2D   | BraTS 2019 and LIDC-IDRI                               | Noise transition matrix and Regularization | Disentangling human error from  the ground truth in segmentation of medical images | [link](https://proceedings.neurips.cc/paper_files/paper/2020/file/b5d17ed2b502da15aa727af0d51508d6-Paper.pdf) |
| Xiao et al. (2021)         | Segmentation   | 2D   | Gleason 2019 dataset                                   | Loss re-weighting                          | Pathological image segmentation  with noisy labels           | [link](https://arxiv.org/pdf/2104.02602.pdf)                 |
| Tanno et al. (2019)        | Classification | 2D   | Ultrasound images                                      | Noise transition matrix and Regularization | Learning from noisy labels by  regularized estimation of annotator confusion | [link](https://openaccess.thecvf.com/content_CVPR_2019/papers/Tanno_Learning_From_Noisy_Labels_by_Regularized_Estimation_of_Annotator_Confusion_CVPR_2019_paper.pdf) |
| Ju et al. (2022)           | Classification | 2D   | ISIC2019 skin cancer and Gleason 2019                  | Loss re-weighting                          | Improving medical images  classification with label noise using dual-uncertainty estimation | [link](https://arxiv.org/pdf/2103.00528.pdf)                 |
| Liao et al. (2022)         | Classification | 3D   | Lung nodule CT                                         | Optimization policy                        | Learning from ambiguous labels  for lung nodule malignancy prediction | [link](https://arxiv.org/pdf/2104.11436.pdf)                 |
| Wei et al. (2022b)         | Classification | 2D   | UCI Breast dataset                                     | Optimization policy                        | To aggregate or not? learning  with separate noisy labels    | [link](https://dl.acm.org/doi/pdf/10.1145/3580305.3599522)   |



We will keep updating for following studies. 


