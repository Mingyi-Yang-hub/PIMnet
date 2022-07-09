# PIMnet
This work is for video quality enhancement.

We design a learning based post-processing network to enhance the quality of the compressed videos.

We proposed to use use the Quantization Parameter (QP) and Delta Picture Order Count (POC) of multiple input frames in the compressed video to modulate the post-processing network, where QP can reflect the quality of frames and POC can reflect the temporal distance between neighboring frames and the current frame.


# Dataset
Open-source dataset.
We use the open-source dataset used in [MFQE 2.0](https://github.com/RyanXingQL/MFQEv2.0).

Please download raw videos [here](https://github.com/RyanXingQL/MFQEv2.0/wiki/MFQEv2-Dataset). (108 video sequences for training and 18 video sequences for testing)

Please compress all video sequences by H.265/HEVC reference software HM16.5 under Low Delay P (LDP) configuration with QPs set to be 22, 27, 32 and 37.


# Code
The code will be release soon.


# Quantitative performance evaluation
This work only focus on Objective quality, so We adopt the incremental Peak Signal-to-Noise Ratio (PSNR) and Structural Similarity (SSIM) to evaluate quality enhancement performance.


# License
We adopt Apache License v2.0.

We would like to thank the authors of MFQE 2.0 for their open-source dataset and the author of Pytorch implementation of STDF for his open-source implementation and the way to generate training dataset in LMDB format.

If you also find them useful, please cite their works

@article{2019xing,
    doi = {10.1109/tpami.2019.2944806},
    url = {https://doi.org/10.1109%2Ftpami.2019.2944806},
    year = 2021,
    month = {mar},
    publisher = {Institute of Electrical and Electronics Engineers ({IEEE})},
    volume = {43},
    number = {3},
    pages = {949--963},
    author = {Zhenyu Guan and Qunliang Xing and Mai Xu and Ren Yang and Tie Liu and Zulin Wang},
    title = {{MFQE} 2.0: A New Approach for Multi-Frame Quality Enhancement on Compressed Video},
    journal = {{IEEE} Transactions on Pattern Analysis and Machine Intelligence}
}

@misc{2020xing2,
  author = {Qunliang Xing},
  title = {PyTorch implementation of STDF},
  howpublished = "\url{https://github.com/RyanXingQL/STDF-PyTorch}",
  year = {2020}, 
  note = "[Online; accessed 11-April-2021]"
}
