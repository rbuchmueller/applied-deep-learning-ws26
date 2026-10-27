# Applied Deep Learning Coursework WS26
## Task 1 - Reference at least two scientific papers that are related to your topic
[1] Zhao, Wentao, Jiang, Wei, Qiu, Xinguo, Big Transfer Learning for Fine Art Classification, Computational Intelligence and Neuroscience, 2022, 1764606, 19 pages, 2022. https://doi.org/10.1155/2022/1764606
[2] Liangyu Wei, Qianheng Li, Dandan Wang. Multitask Art Painting Categorization by Convolution and Transformer Hybrid Architecture. Knowl. Organ. 2026, 53(2), 48360. https://doi.org/10.31083/KO48360
[3] Fanelli, Nicola, Gennaro Vessio, and Giovanna Castellano. "ArtSeek: Deep artwork understanding via multimodal in-context reasoning and late interaction retrieval." arXiv preprint arXiv:2507.21917 (2025) https://arxiv.org/abs/2507.21917?utm_source=chatgpt.com
[4] Melis, Federico, et al. "Harnessing Self-Supervised Features for Art Classification." arXiv preprint arXiv:2605.18974 (2026).

## Task 2 - topic of your choice
Classification of Artist of Fine Art 

## Task 3 - decision of which type of project you want to do 
Reaching for the stars 
Alternative: Bring your own method

## Task 4 - a written summary
### a. Short description of your project idea and the approach you intend to use
The overall idea of this project is to create a deep learning model for the classification of fine art. After initial research*, training a competitive vision model from scratch does not appear feasible. Given the description of the assignment, we hope that the development of a base model is sufficient for the coursework: DinoV3 appears to be an interesting candidate as a base model. Melis et al. (2026) [4] evaluated DINO-family and CLIP representations for artwork classification but focused on genre and style classification; artist classification is not reported. However, there is potential to pursue this direction, also given the effectiveness of DinoV3 in other tasks of similar complexity. We begin by deploying DinoV3 and the respective evaluation pipeline as initial proof-of-concept, given an DinoV3 embeddings and training a simple artist classification head. Given my research and the course information, multi-class classification could be a relevant method, assigning each painting to one of the known artists and building an optimization strategy by determining a cross-entropy loss function. Both models should be compared to find initial improvements. The final model should include relevant characteristics of the data at hand. Edge cases with overlapping classification caused by artistic similarity might be the biggest issue leading to general loss of accuracy in painting classification. I plan to experiment with contrastive learning of HD embeddings of the given paintings to segregate paintings in the HD space and explore applying clustering techniques (such as spectral clustering or kNN) to most accurately specify artist clusters. 
Extending this project's scope, I plan to extend this work: I want to use the model to focus on integrating visual analytics into a supervised training process. If art historical expert could use their knowledge to identify dimensions missed by the model (such as background knowledge), it would lead to novel techniques combining Visual Analytics, symbolic and subsymbolic knowledge to a first use case of "Neurosymbolic VA". A convincing evaluation pipeline is required.  

### b. Description of the dataset you are about to use (or collect)
We need to use a large dataset to learn meaningful representations. The wikiart dataset (https://huggingface.co/datasets/huggan/wikiart) should be used to make the work comparable to related work. Interestingly, I did not find any work that evaluates their model on the complete wikiart dataset. In detail, the dataset is composed of XXX high-resolution figures and relevant target data plus genre and style information.

### c. A work-breakdown structure for the individual tasks with time estimates in hours for dataset collection; designing and building an appropriate network; training and fine-tuning that network; building an application to present the results; writing the final report; preparing the presentation of your work.
- data collection: 10 hours
- designing and building an appropriate network (networks): 30 hours
- training and fine-tuning that network: 40 hours
- building an applixation to present the results: 30 hours
- writing the final report: 10 hours
- preparing the presentation of the work: 6 hours


## Note to AI usage
ChatGPT 6.1 Sol was used particularly and only for the initial literature search (see chat here for transparency: https://chatgpt.com/share/6ae084c1-2028-83ed-82dd-8cdf2a72dd24). Given those results, the literature search was extended by employing catalog search engines, Google Scholar, keyword search and snowballing.
Grammarly was used for proofreading only. 
