---
title: "DAMI Lab - fidelity"
layout: textlay
excerpt: "fidelity"
sitemap: false
permalink: /fidelity
---

## Robust fidelity ( Fidα )  [paper](https://openreview.net/pdf?id=up6hr4hIQH) [code](https://github.com/AslanDing/Fidelity) 

### abstract

Graph Neural Networks (GNNs) are neural models that leverage the dependency
structure in graphical data via message passing among the graph nodes. GNNs
have emerged as pivotal architectures in analyzing graph-structured data, and their
expansive application in sensitive domains requires a comprehensive understanding of their decision-making processes necessitating a framework for GNN
explainability. An explanation function for GNNs takes a pre-trained GNN along
with a graph as input, to produce a ‘sufficient statistic’ subgraph with respect to
the graph label. A main challenge in studying GNN explainability is to provide
fidelity measures that evaluate the performance of these explanation functions.
This paper studies this foundational challenge, spotlighting the inherent limitations
of prevailing fidelity metrics, including  Fid+, Fid−, and Fid∆. Specifically, a
formal, information-theoretic definition of explainability is introduced and it is
shown that existing metrics often fail to align with this definition across various
statistical scenarios. The reason is due to potential distribution shifts when subgraphs are removed in computing these fidelity measures. 
Subsequently, a robust
class of fidelity measures are introduced, and it is shown analytically that they are
resilient to distribution shift issues and are applicable in a wide range of scenarios.
Extensive empirical analysis on both synthetic and real datasets are provided to
illustrate that the proposed metrics are more coherent with gold standard metrics

### illustration
We provide an illustration to understand how our method works.

<center class="ba2">
<table>
  <tr>
    <td><img src="../images/fidelity/fid_alpha.jpg"  width = "100%" alt="" align=center /> </td>
  </tr>
 </table>

</center>



### Experiments
#### Probability ori. Fidelity results of Ba2Motifs dataset, the x-axis means adding non-explanation edges to GT, y-axis means remove edges from GT. The following three figures are Original Fid+, Fid−, and Fid∆.

<center class="ba2">
<table>
  <tr>
    <td><img src="../images/fidelity/GNN_ba2_results_ori_fid_1fid_plus prob.png"  width = "100%" alt="" align=center /> </td>
    <td><img src="../images/fidelity//GNN_ba2_results_ori_fid_1fid_minus prob.png"  width = "100%" alt="" align=center /></td>
    <td><img src="../images/fidelity//GNN_ba2_results_ori_fid_1fid_Delta prob.png"  width = "100%" alt="" align=center /></td>
  </tr>
 </table>

</center>



#### Probability our Fidelity results of Ba2Motifs dataset. The following three figures are Ours Fid+, Fid−, and Fid∆.
<center class="ba2">

<table>
  <tr>
    <td><img src="../images/fidelity/GNN_ba2_results_new_fid_0_0_seeds_1_fid_plus prob.png"  width = "100%" alt="" align=center /> </td>
    <td><img src="../images/fidelity/GNN_ba2_results_new_fid_0_0_seeds_1_fid_minus prob.png"  width = "100%" alt="" align=center /></td>
    <td><img src="../images/fidelity/GNN_ba2_results_new_fid_0_0_seeds_1_fid_Delta prob.png"  width = "100%" alt="" align=center /></td>
  </tr>
 </table>
</center>

#### Probability ori. Fidelity results of TreeCycles dataset. The following three figures are Original Fid+, Fid−, and Fid∆.
<center class="ba2">
<table>
  <tr>
    <td><img src="../images/fidelity/GNN_syn3_results_ori_fid_1fid_plus prob.png"  width = "100%" alt="" align=center /> </td>
    <td><img src="../images/fidelity/GNN_syn3_results_ori_fid_1fid_minus prob.png"  width = "100%" alt="" align=center /></td>
    <td><img src="../images/fidelity/GNN_syn3_results_ori_fid_1fid_Delta prob.png"  width = "100%" alt="" align=center /></td>
  </tr>
 </table>
</center>

#### Probability our Fidelity results of TreeCycles dataset. The following three figures are Ours Fid+, Fid−, and Fid∆.
<center class="ba2">

<table>
  <tr>
    <td><img src="../images/fidelity/GNN_syn3_results_new_fid_0_0_seeds_1_fid_plus prob.png"  width = "100%" alt="" align=center /> </td>
    <td><img src="../images/fidelity/GNN_syn3_results_new_fid_0_0_seeds_1_fid_minus prob.png"  width = "100%" alt="" align=center /></td>
    <td><img src="../images/fidelity/GNN_syn3_results_new_fid_0_0_seeds_1_fid_Delta prob.png"  width = "100%" alt="" align=center /></td>
  </tr>
 </table>
</center>



### If this work is helpful for you, please consider citing our paper.

```angular2html
@article{zheng2023towards,
  title={Towards robust fidelity for evaluating explainability of graph neural networks},
  author={Zheng, Xu and Shirani, Farhad and Wang, Tianchun and Cheng, Wei and Chen, Zhuomin and Chen, Haifeng and Wei, Hua and Luo, Dongsheng},
  journal={arXiv preprint arXiv:2310.01820},
  year={2023}
}
```

