# Awesome-Neural-Tree-Papers <img class="emoji" alt=":art:" height="30" width="30" src="https://github.githubassets.com/images/icons/emoji/unicode/1f3a8.png">
Selected papers and possible corresponding codes in our review paper **"A Survey of Neural Trees" [[arXiv Version]](https://arxiv.org/abs/2209.03415) [[ResearchGate Version]](https://www.researchgate.net/publication/363349864_A_Survey_of_Neural_Trees)**

*If you find there is a missed paper or a possible mistake in our survey, please feel free to email me or pull a request here. I am more than glad to receive your advice. Thanks!*

## Introduction
Neural trees (NTs) refers to a school of methods that combine neural networks (NNs) and decision trees (DTs), for which
we present a comprehensive review in this survey. Our keynote is to identify how these approaches enhance the model
interpretability and suggest possible solutions to the remaining challenges. Besides, we provide a discussion about
other considerations like conditional computation and promising directions towards this field, in hope to advance
the practice of NTs.

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
These approaches are the very first to combine NNs and DTs. They employ DTs as auxiliaries for NNs as well as using
NNs as tools to improve the design of DTs. In these approaches, "neural" and "tree" are separated, *i.e.*, one of NN
and DT is assigned to accomplish a specific task, while the other performs as its assistant or interpreter. It can 
date back to the early 1990s when DTs were supposed to provide structural priors for NNs or extract rules from a 
trained NN. They are perceived implicit combinations of NNs and DTs, because NNs and DTs still operate on their 
own paradigms and no hybrid model is produced.

#### 1.1 DTs as Structural Priors of NNs.
Adopt DTs to approximate the target concept of NNs in terms of logical descriptions, *i.e.*, use DTs to design NNs 
with structural priors.
<p align='center'>
    </br>
    <img src='shortened_structural_prior.png' width='1000'>
</p>

- **Entropy net: the first practice**
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

#### 1.2 DTs for Approximating NNs.
Apply DTs to interpret trained NNs by approximating the network (mostly in terms of input-output mapping) and mimic
the decision boundaries implicitly learned by the hidden layers.

##### *1.2.1 Pedagogical Techniques.*
Treat NNs as black-box approaches, and extract the input-output rule directly form NNs regardless of its intermediate
layers.

<p align='center'>
    </br>
    <img src='shortened_rule_extract.png' width='1000'>
</p>

- **TREPAN: the first practice of DT-based interpretation**
  - Mark Craven, Jude Shavlik
  - [[Paper]](https://proceedings.neurips.cc/paper/1995/hash/45f31d16b1058d586fc3be7207b58053-Abstract.html)
  - Mark Craven, Jude Shavlik
  - [[Paper]](https://www.sciencedirect.com/science/article/pii/B9781558603356500131)

- **Remove insignificant input neurons from the trained network before inducing the DT**
  - Nikola Vasilev, Zheni Mincheva, Ventsislav Nikolov
  - [[Paper]](https://pdfs.semanticscholar.org/9528/ece5f2a9c71fac8ac258d6812ff5cc75da63.pdf)

- **Turn the 𝑚-of-𝑛 type splits into standard splitting tests such as C4.5**
  - Darren Dancey, Dave McLean, Zuhair Bandar (CART tree)
  - [[Paper]](https://www.aaai.org/Papers/FLAIRS/2004/Flairs04-089.pdf)
  - Olcay Boz *(propose discretization algorithms to handle continuous features)*
  - [[Paper]](https://www.proquest.com/openview/11cd66e5b5aab652403e370ca7bf1eef/1?pq-origsite=gscholar&cbl=18750&diss=y)
  - Olcay Boz 
  - [[Paper]](https://dl.acm.org/doi/abs/10.1145/775047.775113)
  - Zhi-Hua Zhou, Yuan Jiang *(use NN ensembles)*
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/1294896)
  - R.Krishnan, G.Sivakumar, P.Bhattacharya *(adapt genetic algorithms to generate artificial examples)*
  - [[Paper]](https://www.sciencedirect.com/science/article/abs/pii/S0031320398001812)

- **generalize the TREPAN algorithm**
  - William A Young *et al.* *(develop DTs derived from continuous-based models)*
  - [[Paper]](https://www.researchgate.net/profile/William-Young-10/publication/227441144_An_investigation_of_TREPAN_utilising_a_continuous_oracle_model/links/00b495258560f7e8d3000000/An-investigation-of-TREPAN-utilising-a-continuous-oracle-model.pdf?_sg%5B0%5D=started_experiment_milestone&origin=journalDetail)
  - M Rangwala, G Weckman, J Marvel, W Young *(extend TREPAN to multi-class regression problems)*
  - [[Paper]](https://d1wqtxts1xzle7.cloudfront.net/47121083/TREPAN-PLUS_AN_EXTENSION_OF_A_DECISION_T20160708-16395-1sj4ete-with-cover-page-v2.pdf?Expires=1662702200&Signature=D7KxjY-G2yD3m~srwPsFdkZ3FRjaKdgnqsKnvIN8emqFzbFXKH1Z17-3UrdC9iUobcT-t1plwsUNdW61Ex0p6W74Z~h8FVBXpvhVuACLZSZFlH5CzMsjNc03N5JKXCPrGMVJrwCHdrT59KAEHNrXMkJa7D5hYM~M5mzPjyiH1RCkZdzQDmaJAnk2vH7ylpMhkPOUmt2jKFRM2f8abiHTnrwdfgo4JMcyC1RfBYmcBa~Jqb9nCqOcZn-4QYrH6oglWhqWc-KcTtcUEuT9bQVPyCL-IcHO88GALXiHZ6ios0NLq1wOAupKJ-9WaXY-QOS-VgdvzYMS6AqzRPX5xcrSIw__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)
  - Maciej Faifer, Cezary Z Janikow, Krzysztof Krawiec *(use fuzzy representation during the tree-induction process)*
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/781764)
  - Peter Müller, Lukas Faber, Karolis Martinkus, Roger Wattenhofer *(incorporate DTs into graph neural networks)*
  - [[Paper]](https://arxiv.org/abs/2205.13234)

- **NNs perform significance analysis to select attributes**
  - Gregor PJ Schmitz, Chris Aldrich, Francois S Gouws.
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/809084)


##### *1.2.2 Decompositional Techniques.*
Decompositional techniques concern units in the hidden layers. They extract rules from the trained NN at the level of 
individual neurons, thus gaining insight into their inner structures.

- **Extract axis-aligned trees**
  - Makoto Sato, Hiroshi Tsukimoto *(CRED algorithm that deals with NNs with one hidden layer)*
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/938448)
  - Jan Ruben Zilke, Eneldo Loza Mencía, Frederik Janssen *(Extend CRED algorithm by deriving intermediate rules for every additional hidden layer)*
  - [[Paper]](https://link.springer.com/chapter/10.1007/978-3-319-46307-0_29)
  - MD. Ridwan Al Iqbal *(Simplify rules by logical simplification)*
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/6471502)

- **Extract oblique and multivariate trees**
  - Rudy Setiono, Huan Liu *(oblique trees)*
  - [[Paper]](https://www.sciencedirect.com/science/article/abs/pii/S0925231297000386)
  - Duy T Nguyen, Kathryn E Kasmarik, Hussein A Abbass *(multivariate trees)*
  - [[Paper]](http://arxiv-export-lb.library.cornell.edu/abs/2003.04675)

##### *1.2.3 Eclectic Techniques.*
Typically, eclectic techniques model the relationship between the last hidden layer and the outputs, then infer the
input-output relationship from the magnitudes of the weights in a NN. However, few of them are based on DTs. Therefore,
this survey comprises approaches that extract **partial knowledge** contained in the hidden layers and do not demand
their approximation target is the input-output relationship

- **Extended C-Net algorithm**
  - Duy T Nguyen, Kathryn E Kasmarik, Hussein A Abbass *(a typical eclectic technique)*
  - [[Paper]](http://arxiv-export-lb.library.cornell.edu/abs/2003.04675)
  - Chengliang Yang, Anand Rangarajan, Sanjay Ranka *(CART tree learned from the contribution matrix and applied to scene understanding tasks)*
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/8622994)
  - Quanshi Zhang, Yu Yang, Haotian Ma, Ying Nian Wu *(encodes all potential decision modes of the CNN in a coarse-to-fine manner)*
  - [[Paper]](https://openaccess.thecvf.com/content_CVPR_2019/html/Zhang_Interpreting_CNNs_via_Decision_Trees_CVPR_2019_paper.html)

##### *1.2.4 Optional: DTs for Regularizing NNs.*
These approaches train NNs that resemble compact DTs through crafted regularization terms, so that they can be well-approximated by small DTs.

- **Tree regularization**
  - Mike Wu, Michael Hughes, Sonali Parbhoo, Maurizio Zazzi, Volker Roth, Finale Doshi-Velez *(a complexity penalty function that aims to optimize the deep model for interpretability and human-simulatability)*
  - [[Paper]](https://ojs.aaai.org/index.php/AAAI/article/view/11501)
  - Mike Wu *et al. (extended work of tree regularization that encourage a deep model to be approximated by several separate DTs specific to pre-defined regions of the input space.)*
  - [[Paper]](https://ojs.aaai.org/index.php/AAAI/article/view/6112)
  - [[Paper]](https://www.jair.org/index.php/jair/article/view/12558)

- **L1-orthogonal regularization**
  - Nina Schaaf, Marco Huber, Johannes Maucher *(so that they do not need a surrogate network to estimate the tree loss)*
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/8999213)

#### 1.3 NNs for Designing DTs.
NNs specialized for designing more reasonable DTs and do not benefit from it, which is rare in practice.

- **Induce DTs from more valid data filtered by the trained NNs**
  - Xiao-Ye Wang, Xiu-Xia Liang, and Ji-Zhou Sun
  - [[Paper]](https://ieeexplore.ieee.org/abstract/document/1527283)

### 2. Semi-hybrid: NNs Leveraging Class Hierarchies.
DT algorithms have two key ideas: "decision" and "tree". We view that "decision" is decision branches implemented by
routing functions, and "tree" is the model topology that identifies a class hierarchy. This survey tries to include
NNs that draw on a part of ideas from DTs, either the class hierarchy or the decision branches, but not both. These 
approaches are considered to be half and implicit integration of NNs and DTs. They borrow some inherent ideas from DTs
for NNs, instead of designing a NN that works like a DT. However, we only concern about the former in our taxonomy, 
*i.e.*, NNs leveraging class hierarchies. These approaches can not implement the class hierarchy in the network
structure due to the absence of decision branches, so they resort to incorporating the hierarchical relations into a NN
directly. There are three lines of research: hierarchical architecture, hierarchical loss function and label embedding
based methods, corresponding to different strategies of employing class hierarchies.

<p align='center'>
    </br>
    <img src='class_hierarchy.png' width='1000'>
</p>





  
  




















