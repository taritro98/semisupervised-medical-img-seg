

---

# Semi-Supervised Medical Image Segmentation via Feature-level Cross-teaching between CNN and Transformer
**Notebook Author - Taritro Ghoshal**

## Introduction

This dissertation explores the development and application of a novel semi-supervised learning framework for medical image segmentation based on cross-teaching between Convolutional Neural Networks (CNN) and Transformers at the feature level. CNNs and Transformers, individually, suffer from certain limitations while performing medical image segmentation tasks. CNNs lack the ability to model global and long-range semantic information interaction due to the intrinsic locality of convolution operations. In contrast, Transformers require large datasets for recognition tasks, acting as a data-hungry solution. The proposed framework combines the strength of both architectures by introducing a novel feature-level cross-teaching technique. This technique employs intermediate feature map representations of unlabelled images generated by one architecture (CNN or Transformer) to update the parameters of the other, enhancing the robustness and accuracy of the segmentation process.

The experimental results indicate a significant improvement in segmentation accuracy, demonstrating the effectiveness of feature-level cross-teaching. It also shows that this approach is capable of capturing both local information, which is the strength of CNNs, and long-range relations, which is the strength of Transformers. This successful combination offers a promising approach to enhance the performance of semi-supervised medical image segmentation, especially in settings where labelled data are scarce.

## Conclusion

The objective of this dissertation was to investigate the merits of collaborative learning in neural networks, specifically via a cross-teaching mechanism that leverages feature-level loss. The empirical studies and subsequent analyses have not only illuminated the strengths and areas of potential refinement but also underscored the vast promise this approach holds for the broader domain of deep learning.
The comparative analysis drew sharp distinctions between standalone architectures, such as U-Net and Swin U-Net, and their performance within a feature-level cross-teaching framework. The standalone models, reputable in their own right, exhibited commendable results in segmentation tasks. However, the cross-teaching approach's superior performance, both quantitatively and qualitatively, provided compelling evidence in favour of collaborative learning mechanisms.
The backbone of this research—the feature-level loss—demonstrated its centrality and efficacy. Its convergence, as evidenced in the results, alluded to its instrumental role in guiding the model's learning trajectory. Moreover, the refined and noise-free predictions obtained under the cross-teaching paradigm vis-à-vis standalone configurations attested to the inherent benefits of introducing feature supervision within a collaborative learning framework.

## Results

SNo | Model | Validation Dice Score | Validation IOU Score
------------- | ------------- | ----------- | ---------------
1 | U-Net | 0.869 | 0.793
2 | Swin U-Net | 0.850	| 0.768
3 | Feature Cross-teaching (U-Net + Swin U-Net) | 0.889 | 0.825

In summation, the empirical outcomes provide a lucid narrative. While standalone models, such as U-Net and Swin U-Net, deliver robust results, their amalgamation within a feature-level cross-teaching paradigm elevates their performance to a superior plane. This is a salient testament to the efficacy of collaborative learning and the pivotal role of feature supervision. Given the demonstrated improvements, this novel approach heralds significant implications for future segmentation tasks, potentially setting a new benchmark in the field.

##  Future Work
While the current research provides substantive insights into the benefits of the feature-level cross-teaching paradigm, several avenues remain unexplored, offering fertile ground for future endeavours:
- Model Expansion: Future endeavours might explore the integration of other neural network architectures, pushing the envelope on what collaborative learning can achieve across diverse neural configurations.
- Hyperparameter Optimization: While the present study did involve various parameter configurations, a more exhaustive hyperparameter search, potentially using automated tools, could further hone the model's performance.
- Broader Application: The efficacy of this approach could be assessed across different datasets and tasks, moving beyond the current scope to gauge its universality and scalability.
- Enhanced Feature Supervision Mechanisms: The novelty of feature-level loss presents opportunities for iterative refinement. Future research might probe into more sophisticated or adaptive feature supervision mechanisms, possibly integrating dynamic loss weighting based on the training stage or dataset characteristics.
- Integration of Transfer Learning: The potential of combining transfer learning with the cross-teaching mechanism could be another frontier to explore, potentially further augmenting performance, especially in scenarios with limited labelled data.
In conclusion, this dissertation has systematically explored feature representation in semi-supervised learning methods. The advancements made in this study mark an initial step in a broader field of research. The potential for further exploration in collaborative learning suggests opportunities for enhanced understanding, improved methodologies, and more robust performance outcomes.


----
