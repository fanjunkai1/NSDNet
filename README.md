# Non-aligned Supervision for Real Image Dehazing

[Junkai Fan](https://fanjunkai1.github.io/), Fei Guo, Jianjun Qian, [Xiang Li](http://implus.github.io/), [Jun li](https://sites.google.com/view/junlineu/) and Jian Yang

[Paper Download (Arxiv)](https://arxiv.org/pdf/2303.04940.pdf) 

<hr />

**Abstract:** *Removing haze from real-world images is challenging due to unpredictable weather conditions, resulting in misaligned hazy and clear image pairs. In this paper, we propose a non-aligned supervision framework that consists of three networks - dehazing, airlight, and transmission. In particular, we explore a non-alignment setting by utilizing a clear reference image that is not aligned with the hazy input image to supervise the dehazing network through a multi-scale reference loss that compares the features of the two images. Our setting makes it easier to collect hazy/clear image pairs in real-world environments, even under conditions of misalignment and shift views. To demonstrate this, we have created a new hazy dataset called ”Phone-Hazy”, which was captured using mobile phones in both rural and urban areas. Additionally, we present a mean and variance self-attention network to model the infinite airlight using dark channel prior as position guidance, and employ a channel attention network to estimate the three-channel transmission. Experimental results show that our framework outperforms current state-of-the-art methods in the real-world image dehazing. Phone-Hazy and code will be available at  https://fanjunkai1.github.io/projectpage/NSDNet/index.html*
<hr />

## Network Architecture

<img src = "figs/framework.png">

Overall pipeline of our non-aligned supervision framework with physical priors for the real-world image dehazing. It includes the mvSA and non-aligned supervision modules. mvSA can effectively estimate the infinite airlight A∞ in real scenes. Our framework is different from the supervised dehazing models as it does not require aligned ground truths.

## Video Demo

<img src = "figs/demo.gif">

## Phone-Hazy Dataset

<img src = "figs/phone-hazy.png" width='970' height='300'>

Our phone-hazy dataset contains 415 non-aligned image pairs with four primary scenes: buildings, urban highways, rural cement roads, and outdoor landscapes. The haze levels mainly vary within a visibility range of 0 to 50 meters.

## Our Environment
- Ubuntu 18.04
- Python == 3.9
- PyTorch == 1.11 with CUDA 11.2
- torchvision ==0.12.0
- numpy == 1.22.3)

## Citation
If you are interested in this work, please consider citing:

    @article{fan2023non,
      title={Non-aligned supervision for Real Image Dehazing},
      author={Fan, Junkai and Guo, Fei and Qian, Jianjun and Li, 
          Xiang and Li, Jun and Yang, Jian},
      journal={arXiv preprint arXiv:2303.04940},
      year={2023}
    }

## Acknowledgment
This code is based on the [CycleGAN](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix). Thank them for their outstanding work.

## Contact
Should you have any question or suggestion, please contact junkai.fan@njust.edu.cn.
