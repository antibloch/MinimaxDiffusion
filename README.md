# Efficient Dataset Distillation via Minimax Diffusion (CIFAR-10 and ImageWoof Benchmarking)
<h2>Abstract</h2>

<div style="background-color:#2f2f2f; color:#f0f0f0; padding:16px; border-radius:8px; font-size:15px; line-height:1.5em;">
Dataset distillation reduces the storage and computational consumption of training a network by generating a small surrogate dataset that encapsulates rich information of the original large-scale one. However, previous distillation methods heavily rely on the sample-wise iterative optimization scheme. As the images-per-class (IPC) setting or image resolution grows larger, the necessary computation will demand overwhelming time and resources. In this work, we intend to incorporate generative diffusion techniques for computing the surrogate dataset. Observing that key factors for constructing an effective surrogate dataset are representativeness and diversity, we design additional minimax criteria in the generative training to enhance these facets for the generated images of diffusion models. We present a theoretical model of the process as hierarchical diffusion control demonstrating the flexibility of the diffusion process to target these criteria without jeopardizing the faithfulness of the sample to the desired distribution. The proposed method achieves state-of-the-art validation performance while demanding much less computational resources. Under the 100-IPC setting on ImageWoof, our method requires less than one-twentieth the distillation time of previous methods, yet yields even better performance.
</div>


# CIFAR-10 (500 samples per class)
```code
git clone https://github.com/algebraicdianuj/MinimaxDiffusion.git
cd MinimaxDiffusion
chmod +x initiator.sh
chmod +x commands.sh

./initiator.sh
./commands.sh
```

# Image Woof
```code
chmod +x initialize_woof.sh
chmod +x commands_woof.sh

./initialize_woof.sh
./commands_woof.sh
```


## Reference
```
@inproceedings{gu2024efficient,
  title={Efficient Dataset Distillation via Minimax Diffusion},
  author={Gu, Jianyang and Vahidian, Saeed and Kungurtsev, Vyacheslav and Wang, Haonan and Jiang, Wei and You, Yang and Chen, Yiran},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
  year={2024}
}
```
