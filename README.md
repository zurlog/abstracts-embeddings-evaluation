# `Abstracts Embeddings Evaluation`
[![Made withJupyter][jupyter-shield]][jupyter-url]
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Issues][issues-shield]][issues-url]
[![DOI](https://zenodo.org/badge/675144631.svg)](https://zenodo.org/doi/10.5281/zenodo.13336504)




### **Data and Code for the paper:**

*Zurlo, G., Ronchieri, E. (2024). Abstracts Embeddings Evaluation: A Case Study of Artificial Intelligence and Medical Imaging for the COVID-19 Infection. In: Foresti, G.L., Fusiello, A., Hancock, E. (eds) Image Analysis and Processing - ICIAP 2023 Workshops. ICIAP 2023. Lecture Notes in Computer Science, vol 14365. Springer, Cham. https://doi.org/10.1007/978-3-031-51023-6_18*

***


## **Summary**
The SARS-CoV-2 pandemic triggered unprecedented research efforts across various disciplines. Notably, the field of artificial intelligence (AI) applied to medical imaging has been prominently involved. Given the scarcity of resources in facing this devious disease, AI-based tools have emerged as potentially valuable assets to be harnessed. Natural Language Processing (NLP) offers a means to expedite the analysis of scientific articles on a larger scale, and has long been recognized as a solution to mitigate information overload in biomedical research. Since the beginning of the pandemic, the natural language processing (NLP) community has been consistently addressing the needs of domain experts by applying cutting-edge methods to enhance comprehension and knowledge discovery.

The primary objective of this study is to assess the adequacy of commonly employed biomedical transformer-based models, trained on pre-pandemic corpora, in capturing the semantic features present in medical imaging literature. Concurrently, we aim to observe the potential advantage of continual and citation-informed pretraining on COVID-19 literature.

To accomplish this, we introduce a unique and independent test set specifically focused on the medical imaging domain. This novel dataset serves as a valuable resource for the extrinsic evaluation of contextual embeddings, comprising realistic text classification tasks based on 560 gold labels referred to two target variables: the clinical task and imaging modality.


## **Installation**
This project depends on Python ($\geq$ 3.7). The project script can be installed via `pip install .` in the project root, i.e.:
```
git clone https://github.com/zurlog/abs-embeddings-eval
cd abs-embeddings-eval
pip install -e .
```

## **Contents**

Notebooks in `scripts/`: 
- `Embeddings_Extraction`: Compute the abstracts embeddings from 15 BERT models.  [<img src="https://img.shields.io/badge/Kaggle-20BEFF?logo=kaggle&logoColor=fff&style=flat" alt="Kaggle Badge">](https://www.kaggle.com/code/zurlog/abstracts-embeddings-extraction)
-  `Embeddings_Comparison_Modality`: Metrics calculations in the prediction of the imaging modality employed. 
-  `Embeddings_Comparison_Task`: Metrics calculations in the prediction of the clinical task. 
-  `Setup`: Dependencies and utility functions.

Files in `results/`:
- `Modality_accuracy.csv` and `Modality_balanced_acc.csv` : Results of the imaging modality prediction comparison.
-  `Task_(primary)_accuracy.csv` and `Task_(primary_balanced_acc.csv` : Results of the clinical task prediction comparison.
-  📁 `embeddings`: Pre-computed vectors stored as serialized *Pandas Series*. 

Files in `data/`: 
- `subset_wlabels.csv` : 560 records subset with gold labels.

<br>

## **3D Visualization** 
###### With the [TensorBoard Embedding Projector](https://projector.tensorflow.org/?config=https://gist.githubusercontent.com/zurlog/cc320ae6380d8ca5914aa0773a2f3034/raw/3a248d41fc265f0729e4e57cd3886da37714e368/projector_config.json), we graphically represented SPECTER embeddings against the corresponding labels. The interactive dashboard allows users to search for specific terms in abstracts, and highlights articles that are adjacent to each other in the embedding (low-dimensional) space. The user can choose and tune three popular dimensionality reduction methods (*UMAP, T-SNE, PCA*).
<p align="center">
  <img src=viz_preview.PNG alt="Embeddings 3D Visualization" width="500"/>
</p>


## **Acknowledgments** 
*References, Inspiration, Code Snippets, etc.*

- Classification Framework from [Born et al. (2021). **On the role of artificial intelligence in medical imaging of COVID-19**. Patterns (New York, N.Y.), 2(6), 100269.](https://pubmed.ncbi.nlm.nih.gov/33969323/)
- Labels from *Detailed results of systematic meta-analysis* [`[Direct Link]`](https://www.cell.com/cms/10.1016/j.patter.2021.100269/attachment/e921e84c-3d7f-4183-bb6c-d42f5b59f3d9/mmc2.csv)
- Inspiration from [González-Márquez et al. (2023). **The Landscape of Biomedical Research**. bioRxiv, 2023.04.10.536208.](https://www.biorxiv.org/content/10.1101/2023.04.10.536208v2)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/zurlog/abs-embeddings-eval.svg?style=for-the-badge
[contributors-url]: https://github.com/zurlog/abs-embeddings-eval/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/zurlog/abs-embeddings-eval.svg?style=for-the-badge
[forks-url]: https://github.com/zurlog/abs-embeddings-eval/network/members
[issues-shield]: https://img.shields.io/github/issues/zurlog/abs-embeddings-eval.svg?style=for-the-badge
[issues-url]: https://github.com/zurlog/abs-embeddings-eval/issues
[license-shield]: https://img.shields.io/github/license/zurlog/abs-embeddings-eval.svg?style=for-the-badge
[license-url]: https://github.com/zurlog/dpc-covid19/blob/master/LICENSE.txt
[jupyter-shield]: https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter
[jupyter-url]: https://jupyter.org/try
[kaggle-shield]:(https://img.shields.io/badge/Kaggle-20BEFF?logo=kaggle&logoColor=fff&style=flat)
[kaggle-url]:https://www.kaggle.com/code/zurlog/abstracts-embeddings-extraction
