

cudatoolkit=


#### https://github.com/Turoad/lanedet/issues/29
pip install torch==1.10.0+cu102 torchvision==0.10.0+cu102 torchaudio==0.9.0 -f https://download.pytorch.org/whl/torch_stable.html


pip install torch==1.10.0+cu102 torchvision==0.10.0+cu102 -f https://download.pytorch.org/whl/torch_stable.html

#
<br>

#### https://stackoverflow.com/questions/72139806/pytorch-with-cuda-local-installation-fails
- https://stackoverflow.com/questions/72139806/pytorch-with-cuda-local-installation-fails

```bash
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 450.51.05    Driver Version: 450.51.05    CUDA Version: 11.0 
```

#
<br>


```bash
$ nvcc --version
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2020 NVIDIA Corporation
Built on Thu_Jun_11_22:26:38_PDT_2020
Cuda compilation tools, release 11.0, V11.0.194
Build cuda_11.0_bu.TC445_37.28540450_0

```

##### Do we also need -- - https://github.com/sshaoshuai/Pointnet2.PyTorch

##### RuntimeError - ERROR in BUILD 

RuntimeError: 
The detected CUDA version (11.0) mismatches the version that was used to compile
PyTorch (10.2). Please make sure to use the same CUDA versions.


- dont run the -- /original_PointRCNN/PointRCNN/build_and_install.sh
- RUN ALL 3 setup.py mentioned in he SHELL Script Separately 
- cd /home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/lib/utils/iou3d
- (env_lyft) dhankar@dhankar-1:~/.../iou3d$ python setup.py install
- Error as seen below -- CUDA and Pytorch Versions Mismatched 

```bash
(env_lyft) dhankar@dhankar-1:~/.../iou3d$ python setup.py install
running install
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/easy_install.py:144: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
running bdist_egg
running egg_info
writing iou3d.egg-info/PKG-INFO
writing dependency_links to iou3d.egg-info/dependency_links.txt
writing top-level names to iou3d.egg-info/top_level.txt
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:381: UserWarning: Attempted to use ninja as the BuildExtension backend but we could not find ninja.. Falling back to using the slow distutils backend.
  warnings.warn(msg.format('we could not find ninja.'))
reading manifest file 'iou3d.egg-info/SOURCES.txt'
writing manifest file 'iou3d.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_ext
Traceback (most recent call last):
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/lib/utils/iou3d/setup.py", line 4, in <module>
    setup(
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/__init__.py", line 87, in setup
    return distutils.core.setup(**attrs)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/core.py", line 185, in setup
    return run_commands(dist)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/core.py", line 201, in run_commands
    dist.run_commands()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/dist.py", line 968, in run_commands
    self.run_command(cmd)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/dist.py", line 1217, in run_command
    super().run_command(command)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/dist.py", line 987, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/install.py", line 74, in run
    self.do_egg_install()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/install.py", line 123, in do_egg_install
    self.run_command('bdist_egg')
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/cmd.py", line 319, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/dist.py", line 1217, in run_command
    super().run_command(command)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/dist.py", line 987, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/bdist_egg.py", line 165, in run
    cmd = self.call_command('install_lib', warn_dir=0)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/bdist_egg.py", line 151, in call_command
    self.run_command(cmdname)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/cmd.py", line 319, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/dist.py", line 1217, in run_command
    super().run_command(command)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/dist.py", line 987, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/install_lib.py", line 11, in run
    self.build()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/command/install_lib.py", line 112, in build
    self.run_command('build_ext')
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/cmd.py", line 319, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/dist.py", line 1217, in run_command
    super().run_command(command)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/dist.py", line 987, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/build_ext.py", line 84, in run
    _build_ext.run(self)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/command/build_ext.py", line 346, in run
    self.build_extensions()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py", line 404, in build_extensions
    self._check_cuda_version()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py", line 781, in _check_cuda_version
    raise RuntimeError(CUDA_MISMATCH_MESSAGE.format(cuda_str_version, torch.version.cuda))
RuntimeError: 
The detected CUDA version (11.0) mismatches the version that was used to compile
PyTorch (10.2). Please make sure to use the same CUDA versions.

(env_lyft) dhankar@dhankar-1:~/.../iou3d$ 
(env_lyft) dhankar@dhankar-1:~/.../iou3d$ 
```






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

#### -- Install Errors Probable Solution -- get Older Versions -- 
- https://pytorch.org/get-started/previous-versions/

##### CUDA 10.2
conda install pytorch==1.10.0 torchvision==0.11.0 torchaudio==0.10.0 cudatoolkit=10.2 -c pytorch


```bash
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ conda install pytorch==1.10.0 torchvision==0.11.0 torchaudio==0.10.0 cudatoolkit=10.2 -c pytorch

Collecting package metadata (current_repodata.json): done
Solving environment: failed with initial frozen solve. Retrying with flexible solve.
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/dhankar/anaconda3/envs/env_lyft

  added / updated specs:
    - cudatoolkit=10.2
    - pytorch==1.10.0
    - torchaudio==0.10.0
    - torchvision==0.11.0


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    libuv-1.40.0               |       h7b6447c_0         736 KB
    pytorch-1.10.0             |py3.9_cuda10.2_cudnn7.6.5_0       768.1 MB  pytorch
    torchaudio-0.10.0          |       py39_cu102         4.5 MB  pytorch
    torchvision-0.11.0         |       py39_cu102         8.7 MB  pytorch
    ------------------------------------------------------------
                                           Total:       782.0 MB

The following NEW packages will be INSTALLED:

  cudatoolkit        pkgs/main/linux-64::cudatoolkit-10.2.89-hfd86e86_1 None
  libuv              pkgs/main/linux-64::libuv-1.40.0-h7b6447c_0 None

The following packages will be DOWNGRADED:

  pytorch                1.13.0-py3.9_cuda11.7_cudnn8.5.0_0 --> 1.10.0-py3.9_cuda10.2_cudnn7.6.5_0 None
  torchaudio                              0.13.0-py39_cu117 --> 0.10.0-py39_cu102 None
  torchvision                             0.14.0-py39_cu117 --> 0.11.0-py39_cu102 None


Proceed ([y]/n)? 
Proceed ([y]/n)? y


Downloading and Extracting Packages
torchvision-0.11.0   | 8.7 MB    | ################################################################################################### | 100% 
torchaudio-0.10.0    | 4.5 MB    | ################################################################################################### | 100% 
libuv-1.40.0         | 736 KB    | ################################################################################################### | 100% 
pytorch-1.10.0       | 768.1 MB  | ################################################################################################### | 100% 
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
Retrieving notices: ...working... done
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ 


```

#
<br>

```bash
File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/dist.py", line 1217, in run_command
    super().run_command(command)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/dist.py", line 987, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/build_ext.py", line 84, in run
    _build_ext.run(self)
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/_distutils/command/build_ext.py", line 346, in run
    self.build_extensions()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py", line 404, in build_extensions
    self._check_cuda_version()
  File "/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py", line 781, in _check_cuda_version
    raise RuntimeError(CUDA_MISMATCH_MESSAGE.format(cuda_str_version, torch.version.cuda))
RuntimeError: 
The detected CUDA version (11.0) mismatches the version that was used to compile
PyTorch (10.2). Please make sure to use the same CUDA versions.

```


#
<br>

#

#### DATA SUMMARY -- KITTI 3D object detection
- https://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=3 
#

####  CALIB - CALIBRATION == data_object_calib.zip == 25.6 MB 
- https://s3.eu-central-1.amazonaws.com/avg-kitti/data_object_calib.zip

#### data >> KITTI >> object >> training_and_testing >> image_2 ==  data_object_image_2.zip 
- https://s3.eu-central-1.amazonaws.com/avg-kitti/data_object_image_2.zip

#### data >> KITTI >> object >> training_and_testing >> velodyne ==  data_object_image_2.zip 
- https://s3.eu-central-1.amazonaws.com/avg-kitti/data_object_image_2.zip


#
<br>





#
<br>




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
