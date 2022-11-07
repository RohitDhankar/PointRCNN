
#### This is a FORK of the Original - PointRCNN

- https://github.com/sshaoshuai/PointRCNN

#
<br>

#



| Own Note - Header| Description - Detail Remarks | Related URL Link |
| :--- | :---: | :---: |
| `Primary Paper - PointRCNN` | Primary Paper - PointRCNN | https://github.com/sshaoshuai/PointRCNN |
| `Primary Data` | KITTI | KITTI.org |


<!-- | `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged | -->

#
<br>

```bash
(base) dhankar@dhankar-1:~/.../original_PointRCNN$ git clone --recursive https://github.com/sshaoshuai/PointRCNN.git
Cloning into 'PointRCNN'...
remote: Enumerating objects: 88, done.
remote: Total 88 (delta 0), reused 0 (delta 0), pack-reused 88
Unpacking objects: 100% (88/88), done.
Submodule 'pointnet2_lib' (https://github.com/sshaoshuai/Pointnet2.PyTorch.git) registered for path 'pointnet2_lib'
Cloning into '/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/pointnet2_lib'...
remote: Enumerating objects: 45, done.        
remote: Total 45 (delta 0), reused 0 (delta 0), pack-reused 45        
Submodule path 'pointnet2_lib': checked out '5a4416f51ceaeba242828cabf39133433336850d'
(base) dhankar@dhankar-1:~/.../original_PointRCNN$ 
```

#
<br>

```bash
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ sh build_and_install.sh
Traceback (most recent call last):
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/pointnet2_lib/pointnet2/setup.py", line 2, in <module>
    from torch.utils.cpp_extension import BuildExtension, CUDAExtension
ModuleNotFoundError: No module named 'torch'
Traceback (most recent call last):
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/lib/utils/iou3d/setup.py", line 2, in <module>
    from torch.utils.cpp_extension import BuildExtension, CUDAExtension
ModuleNotFoundError: No module named 'torch'
Traceback (most recent call last):
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/lib/utils/roipool3d/setup.py", line 2, in <module>
    from torch.utils.cpp_extension import BuildExtension, CUDAExtension
ModuleNotFoundError: No module named 'torch'
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ 
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia
Collecting package metadata (current_repodata.json): done
Solving environment: done

```
#
<br>

#### See File -- 'Errors_Install.md'

- ``` bash src/ball_query.cpp:3:10: fatal error: THC/THC.h: No such file or directory ```
- ``` src/iou3d.cpp:7:23: error: ‘AT_CHECK’ was not declared in this scope ```
- below could be the solution for the -- AT_CHECK


#
<br>

_Originally posted by @guni9191 in https://github.com/mrlooi/rotated_maskrcnn/issues/31#issuecomment-631416601_

        I've found out the solution. add the code below
```
#ifndef AT_CHECK
#define AT_CHECK TORCH_CHECK 
#endif
```

at the top of the two srcs,
rotated_maskrcnn/maskrcnn_benchmark/csrc/cuda/deform_conv_cuda.cu
rotated_maskrcnn/maskrcnn_benchmark/csrc/cuda/deform_pool_cuda.cu


      


#
<br>


#
<br>


#
<br>

#### below own notes for the -- 
> PRIMARY PAPER - “Pointrcnn: 3d object proposal generation
and detection from point cloud,”

- https://arxiv.org/abs/1907.03670
- https://github.com/sshaoshuai/PointRCNN


> S. Shi, X. Wang, and H. Li, “Pointrcnn: 3d object proposal generation
and detection from point cloud,”
- Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, 2019, pp. 770–779.
- https://ieeexplore.ieee.org/document/8954080
> PointRCNN: 3D Object Proposal Generation and Detection From Point Cloud
#
> Abstract:
In this paper, we propose PointRCNN for 3D object detection from raw point cloud. The whole framework is composed of two stages: stage-1 for the bottom-up 3D proposal generation and stage-2 for refining proposals in the canonical coordinates to obtain the final detection results. Instead of generating proposals from RGB image or projecting point cloud to bird's view or voxels as previous methods do, our stage-1 sub-network directly generates a small number of high-quality 3D proposals from point cloud in a bottom-up manner via segmenting the point cloud of the whole scene into foreground points and background. The stage-2 sub-network transforms the pooled points of each proposal to canonical coordinates to learn better local spatial features, which is combined with global semantic features of each point learned in stage-1 for accurate box refinement and confidence prediction. Extensive experiments on the 3D detection benchmark of KITTI dataset show that our proposed architecture outperforms state-of-the-art methods with remarkable margins by using only point cloud as input. The code is available at https://github.com/sshaoshuai/PointRCNN.

#
<br>

> PRIMARY PAPER CITATIONS -- 
- https://ieeexplore.ieee.org/document/8954080/citations?tabFilter=papers#citations




#
<br>


- python -m torch.distributed.launch 
- https://pytorch.org/tutorials/intermediate/dist_tuto.html
- https://github.com/pytorch/examples/blob/main/distributed/ddp/README.md

> then collectively synchronizing gradients using the AllReduce primitive. In HPC terminology, this model of execution is called Single Program Multiple Data or SPMD since the same application runs on all application but each one operates on different portions of the training dataset.

#
<br>

- https://discuss.pytorch.org/t/the-right-way-to-distribute-the-training-over-multiple-gpus-and-nodes/29277


#
<br>

#### FASTER -- RCNN -->> https://arxiv.org/pdf/2208.04171.pdf
DCNN architectures can be categorized into two groups:
two-stage detectors and one-stage detectors. Two-stage detec-
tors have a proposal detection stage where a set of bounding
box candidates are generated and a verification stage where
these bounding boxes are separately evaluated whether they
contain an object of a specific class. Examples of these
networks are R-CNN [54], SPPNet [55], Fast R-CNN [56],
Faster R-CNN [6].

#### One STAGE DETECTORS -->> https://arxiv.org/pdf/2208.04171.pdf
On the other hand, in the case of one-stage detectors, a
single neural network is applied to the full image that predicts
the bounding boxes straight away. The slow detection time
which is the biggest disadvantage of the two-stage detectors,
can be overcome with the one-stage approach. Detection time
is crucial for many applications especially but not exclusively
in the field of robotics or self-driving cars. 


#### DATA GENERATION Framework -->> https://arxiv.org/pdf/2208.04171.pdf
For data generation, the PyBullet [25] physics simulator was
used since it has an easy-to-use, intuitive API, including an
image renderer tool, and an integrated physics simulator where
the gravitational force can be easily simulated. It is important
to mention that one of the biggest advantages of domain
randomization over domain adaptation is that it is generally
faster as images do not need to be photo-realistic. In our case,
we could achieve less than 0.5s per image (generation) on a
GeForce RTX 2080 Ti GPU. With 4000 images it is around
33 minutes. In general, the time of dataset generation is an
important aspect of the method as in the industry, on many
occasions, it is not feasible to wait long hours or even days
to start the training.


#### SUMMARY OF RELATED WORKS -->> https://arxiv.org/pdf/2208.04171.pdf
Work Problem Input Domain DR/DA Base Model Simulator Synthetic
Images
Real Im-
ages
Results
Tobin [14] Detection RGB Shapes DR VGG-16 MuJoCo [20] 5K-50K 0 1.5 cm
Tobin [21] Grasping Depth YCB [48] DR CNNs MuJoCo [20] 2K / obj 0 80% success
Borrego [22] Detection RGB Shapes DR Faster R-CNN Gazebo [23] 9K 0 82% mAP50
9K 121 83% mAP50
SSD 9K 0 64% mAP50
9K 121 62% mAP50
Pashevich [12] Detection Depth Cubes DR ResNet-18 PyBullet [25] 2K 0 1.09±0.73 cm
Cup placing Cups - 0 15/20
James [28] Pick-and-place RGB,
joints
Cube DR CNNs V-REP [49] 100K-1M 0 ≥41% success
Devo [29] Navigation 2xRGB - DR CNNs UE4 [30] 540K 0 46% success
Chen [31] Detection RGB Street DA Faster RCNN - 10K 3K(unlab.) 38.97 AP50
Sankarana-
rayanan [34]
Segmentation RGB Street DA GAN - 25K 5K(unlab.) 37.1 mIOU
Tremblay [37] Detection RGB Street DR Faster R-CNN UE4 [30] 100K 0 78.1 AP50
100
