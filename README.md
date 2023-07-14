# Unsupervised Domain Adaptive Object Detection for CCDA(Title to be updated)
Code implementation for CCDA

![LAST COMMIT](https://img.shields.io/github/last-commit/zyfone/UEA)
![ISSUES](https://img.shields.io/github/issues/zyfone/UEA)
![STARS](https://img.shields.io/github/stars/zyfone/UEA)

---
submitting to the XXXX，we will update the code after the paper is officially accepted 





## Requirements
* Ubuntu 18.04.5 LTS
* Python 3.6
* [CUDA 10.0](https://developer.nvidia.com/cuda-toolkit)
* [PyTorch 1.0.0](https://pytorch.org)
* [Faster R-CNN](https://github.com/jwyang/faster-rcnn.pytorch/tree/pytorch-1.0)


## dataset download

We also provide the download URL of the dataset in the future




## Compile the code

Compile the cuda dependencies using following simple commands following [Faster R-CNN](https://github.com/jwyang/faster-rcnn.pytorch/tree/pytorch-1.0):
```bash
cd lib
python setup.py build develop
```


**Note that we find that our code is not stable due to adversarial training,require multiple testing attempts to achieve desired results**



## Pre-trained Models


* **ResNet101:** [Dropbox](https://www.dropbox.com/s/iev3tkbz5wyyuz9/resnet101_caffe.pth?dl=0)  [VT Server](https://filebox.ece.vt.edu/~jw2yang/faster-rcnn/pretrained-base-models/resnet101_caffe.pth)

Tricks：

It is worth noting that the input size is (800, 800)(following UDAT) in a visible-to-thermal benchmark, and the input size of the related comparison method has been changed.
We will release the related logs, in the future. In the visible-to-visible benchmark, the input size is (600, 600) (following TIA).

The anchor parameters are different from the [8,16,32], we update to the [4,8,16,32]. By the ablation experiment, both of these parameters are the same performer in the baseline.


## :pencil:Related repos
Our project references the codes in the following repos:

* Megvii-Nanjing, [CR-DA-DET](https://github.com/Megvii-Nanjing/CR-DA-DET)


other code :
* https://github.com/tiancity-NJU/da-faster-rcnn-PyTorch
* https://github.com/MCG-NJU/TIA/
* https://github.com/harsh-99/SCL
* https://github.com/AmineMarnissi/UDAT



if you have any questions , please contact me at 478756030@qq.com
