# Guiding Monocular Depth Estimation Using Depth Attention-Volume
-----
This repository contains the PyTorch implementation of our ECCV 2020 paper:  

[Guiding Monocular Depth Estimation Using Depth Attention-Volume](https://arxiv.org/abs/2004.02760)  
[Lam Huynh](https://lamhuynh.info/), 
[Phong Nguyen-Ha](https://scholar.google.fi/citations?user=030WAOoAAAAJ&hl=en),
[Jiří Matas](http://cmp.felk.cvut.cz/~matas/), 
[Esa Rahtu](http://esa.rahtu.fi/), 
[Janne Heikkilä](https://www.oulu.fi/university/researcher/janne-heikkila)  
[University of Oulu](https://huynhlam.github.io/mono-depth-DAV/figures/oulu_univ.png),
[Tampere University](https://research.tuni.fi/vision), 
[Czech Technical University in Prague](http://www.fel.cvut.cz/en/)  

| [Project page](https://bit.ly/dav-project) 
| [Arxiv]((https://arxiv.org/abs/2004.02760)) 
| [Demo video](https://drive.google.com/file/d/1c8by8GZUUoPLBMeySkH8WkZtTFUgEH-K/view) |

### Abstract
Recovering the scene depth from a single image is an ill-posed problem that requires additional priors, often referred to as monocular depth cues, to disambiguate different 3D interpretations. In recent works, those priors have been learned in an end-to-end manner from large datasets by using deep neural networks. In this paper, we propose guiding depth estimation to favor planar structures that are ubiquitous especially in indoor environments. This is achieved by incorporating a non-local coplanarity constraint to the network with a novel attention mechanism called depth-attention volume (DAV). Experiments on two popular indoor datasets, namely NYU-Depth-v2 and ScanNet, show that our method achieves state-of-the-art depth estimation results while using only a fraction of the number of parameters needed by the competing methods.

### Network architecture
The pipeline of our proposed network. An image is passed through the encoder,then  the  non-local  depth-attention  module, and finally the decoder to  produce the estimated depth map. The model is trained using L_attention and L_depth losses, which are described in the paper.

![Overview architecture](./figures/overview_architecture.png?raw=true)

Details structure of the depth attention module.

![Depth attention module](./figures/dav_module.png?raw=true)

### Results

Evaluation on NYU-v2 test set.

![Depth attention module](./figures/eval_nyu.png?raw=true)

Comparison between number of parameters and model performance.

![Depth attention module](./figures/params_chart.png?raw=true)

Qualitative results on NYU.

![Depth attention module](./figures/qualitative_nyu.png?raw=true)

Cross-dataset evaluation on SUN-RGBD.

![Depth attention module](./figures/cross_dataset_sunrgbd.png?raw=true)

Result video on unseen data from the real world: 

[![Unseen data](./figures/unseen_data.png?raw=true)](https://drive.google.com/file/d/1c8by8GZUUoPLBMeySkH8WkZtTFUgEH-K/view)


