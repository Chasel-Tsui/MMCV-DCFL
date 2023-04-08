# MMCV-DCFL

This is the official code for the mmcv-dcfl, which contains necessary components for the paper ''Dynamic Coarse-to-Fine Learning for Oriented Tiny Object Detection''.

## Installation

```shell
git clone https://github.com/Chasel-Tsui/MMCV-DCFL.git
cd MMCV-DCFL
MMCV_WITH_OPS=1 pip install -e .  # package mmcv-full==1.6.1 will be installed after this step
cd ../
```

## Alternative Ways of Installation

If the above steps cannot help you install the mmcv-full of a required version, you can try the following steps.
- Install the mmcv-full following the official [guide](https://github.com/open-mmlab/mmcv)
- Find the directory of mmcv in your environment directory
- Get into the mmcv/ops/ directory
- Replace the following files: [deform_conv.py](mmcv/ops/deform_conv.py), [modulated_deform_conv.py](mmcv/ops/modulated_deform_conv.py)
- Register the 'DeformConvG','ModulatedDeformConvG' classes into the [__init__.py](mmcv/ops/__init__.py)


## Citation
If you find this work helpful, please consider citing:
```bibtex
@inproceedings{xu2023dcfl,
  title={Dynamic Coarse-to-Fine Learning for Oriented Tiny Object Detection},
  author={Xu, Chang and Ding, Jian and Wang, Jinwang and Yang, Wen and Yu, Huai and Yu, Lei and Xia, Gui-Song},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
  year={2023},
```