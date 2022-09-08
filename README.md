# Awesome-Neural-Tree-Papers <img class="emoji" alt=":art:" height="30" width="30" src="https://github.githubassets.com/images/icons/emoji/unicode/1f3a8.png">
Selected papers and possible corresponding codes in our review paper **"A Survey of Neural Trees" [[arXiv Version]](progressing) [[ResearchGate Version]](https://www.researchgate.net/publication/363349864_A_Survey_of_Neural_Trees)**

*If you find there is a missed paper or a possible mistake in our survey, please feel free to email me or pull a request here. I am more than glad to receive your advice. Thanks!*

## Introduction
Neural networks (NNs) and decision trees (DTs) are both popular models of machine learning, yet coming with mutually
exclusive advantages and limitations. To bring the best of the two worlds, a variety of approaches are proposed to 
integrate NNs and DTs explicitly or implicitly. This survey unifies them into a concept: neural trees (NTs) and present 
a comprehensive review for them. Our keynote is to identify how these approaches enhance the model interpretability and
suggest possible solutions to the remaining challenges. Besides, we provide a discussion about other considerations
like conditional computation and promising directions towards this field, in hope to advance the practice of NTs.

## *News!*
- nothing by now.

### Citation 
If you find this survey useful for your research, please consider citing
```
@article{,
  title={A Survey of Neural Trees},
  author={},
  journal={},
  year={}
}
```

Thanks!

## A Taxonomy of Current Methods
In this survey, we present a thorough taxonomy for NTs that expresses the gradual integration and co-evolution of NNs and DTs.
<p align='center'>
    </br>
    <img src='outline_final.png' width='1000'>
</p>

### 1. Non-hybrid: NNs and DTs Cooperated Approaches.
These approaches are the very first to combine NNs and DTs. It can date back to the early 1990s when DTs were supposed to
provide structural priors for NNs or extract rules from a trained NN. They are perceived implicit combinations of NNs and DTs,
as they do not bring the two worlds into one hybrid model.

#### 1.1 DTs as Structural Priors of NNs.

- **Entropy net:**
  - I.K. Sethi
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/58346/)
  - I.K. Sethi
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/112298)
  - I.K. Sethi, Mike Otten
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/5726783)

- **ID3-based algorithm that converts DTs into hidden layers:**
  - K.J. Cios, N. Liu
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/125869)

- **Soft thresholding of entropy net:**
  - I.K. Sethi
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/398685)

- **Oblique trees version of entropy net:**
  - Youngtae Park
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/374145)
  - Richard P. Brent
  - [[Paper]](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.122.4561&rep=rep1&type=pdf)

- **A knowledge acquisition system that concerns about the knowledge form DTs and NNs prefer:**
  - Katsuhiko Tsujino, Shogo Nishida
  - [[Paper]](https://www.sciencedirect.com/science/article/abs/pii/0954181095000054)

- **Create a disjunctive normal form formula for each class and reformulate the first layer of entropy net:**
  - Arunava Banerjee
  - [[Paper]](https://scholarship.libraries.rutgers.edu/esploro/outputs/technicalDocumentation/Initializing-neural-networks-using-decision-trees/991031549998404646)
  - Irena Ivanova, Miroslav Kubat
  - [[Paper]](https://www.sciencedirect.com/science/article/abs/pii/0950705196819174)
  - R.SetionoW, K.Leow
  - [[Paper]](https://www.sciencedirect.com/science/article/abs/pii/S095070519900009X)















