# Codes CVPR2025 paper ''Improving the Training of Data-Efficient GANs via Quality Aware Dynamic Discriminator Rejection Sampling''

We have provided the codes of QADDRS with StyleGAN2 + Diff-Augment on low-shot datasets. The details are shown as follows.

# Dataset

The low-shot datasets can be found in [[link]](https://drive.google.com/file/d/1rWqaVlms55604jrP5t9ShacL6mZKWL8f/view?usp=sharing).

# Requirement

Please follow the DiffAug-GAN [[link]](https://github.com/mit-han-lab/data-efficient-gans) and ADA [[link]](https://github.com/NVlabs/stylegan2-ada-pytorch) to build the envirment required. 

# Training

To train StyleGAN + Diff-Augment + QADDRS on the 100-shot-obama dataset, run the following 

```
python train.py --outdir=training-runs --mirror=true --data=100-shot-obama.zip --batch=4 --gpus=1

```

It takes about several hours to finish the training. You can also change the --data in the above comments to obtain the results on other datasets. The results of FID values should be close to the reported FID in the paper.

# Important notes

1. The codes of this module is built upon the codes of the DiffAug-GAN [[link]](https://github.com/mit-han-lab/data-efficient-gans) and ADA [[link]](https://github.com/NVlabs/stylegan2-ada-pytorch). We thanks a lot for their great work.

2. We have also found that certain hyperparameters — even those adopted from previous work — as well as inherent properties of the dataset, can influence the performance of QADDRS. If you wish to train or apply QADDRS on your own dataset, we recommend tuning the hyperparameters specifically for your dataset to achieve optimal performance.

3. Feel free to contact me at zzhang55@qub.ac.uk if you have any questions.

# Citation:

```
@inproceedings{zhang2025improving,
  title={Improving the Training of Data-Efficient GANs via Quality Aware Dynamic Discriminator Rejection Sampling},
  author={Zhang, Zhaoyu and Hua, Yang and Sun, Guanxiong and Wang, Hui and McLoone, Se{\'a}n},
  booktitle={Proceedings of the Computer Vision and Pattern Recognition Conference},
  pages={30682--30691},
  year={2025}
}
```

