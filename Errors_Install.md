

```bash

(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ 
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/dhankar/anaconda3/envs/env_lyft

  added / updated specs:
    - pytorch
    - pytorch-cuda=11.7
    - torchaudio
    - torchvision


The following NEW packages will be INSTALLED:

  blas               pkgs/main/linux-64::blas-1.0-mkl None
  brotlipy           pkgs/main/linux-64::brotlipy-0.7.0-py39h27cfd23_1003 None
  bzip2              pkgs/main/linux-64::bzip2-1.0.8-h7b6447c_0 None
  cffi               pkgs/main/linux-64::cffi-1.15.1-py39h74dc2b5_0 None
  charset-normalizer pkgs/main/noarch::charset-normalizer-2.0.4-pyhd3eb1b0_0 None
  cryptography       pkgs/main/linux-64::cryptography-38.0.1-py39h9ce1e76_0 None
  cuda               nvidia/linux-64::cuda-11.7.1-0 None
  cuda-cccl          nvidia/linux-64::cuda-cccl-11.7.91-0 None
  cuda-command-line~ nvidia/linux-64::cuda-command-line-tools-11.7.1-0 None
  cuda-compiler      nvidia/linux-64::cuda-compiler-11.7.1-0 None
  cuda-cudart        nvidia/linux-64::cuda-cudart-11.7.99-0 None
  cuda-cudart-dev    nvidia/linux-64::cuda-cudart-dev-11.7.99-0 None
  cuda-cuobjdump     nvidia/linux-64::cuda-cuobjdump-11.7.91-0 None
  cuda-cupti         nvidia/linux-64::cuda-cupti-11.7.101-0 None
  cuda-cuxxfilt      nvidia/linux-64::cuda-cuxxfilt-11.7.91-0 None
  cuda-demo-suite    nvidia/linux-64::cuda-demo-suite-11.8.86-0 None
  cuda-documentation nvidia/linux-64::cuda-documentation-11.8.86-0 None
  cuda-driver-dev    nvidia/linux-64::cuda-driver-dev-11.7.99-0 None
  cuda-gdb           nvidia/linux-64::cuda-gdb-11.8.86-0 None
  cuda-libraries     nvidia/linux-64::cuda-libraries-11.7.1-0 None
  cuda-libraries-dev nvidia/linux-64::cuda-libraries-dev-11.7.1-0 None
  cuda-memcheck      nvidia/linux-64::cuda-memcheck-11.8.86-0 None
  cuda-nsight        nvidia/linux-64::cuda-nsight-11.8.86-0 None
  cuda-nsight-compu~ nvidia/linux-64::cuda-nsight-compute-11.8.0-0 None
  cuda-nvcc          nvidia/linux-64::cuda-nvcc-11.7.99-0 None
  cuda-nvdisasm      nvidia/linux-64::cuda-nvdisasm-11.8.86-0 None
  cuda-nvml-dev      nvidia/linux-64::cuda-nvml-dev-11.7.91-0 None
  cuda-nvprof        nvidia/linux-64::cuda-nvprof-11.8.87-0 None
  cuda-nvprune       nvidia/linux-64::cuda-nvprune-11.7.91-0 None
  cuda-nvrtc         nvidia/linux-64::cuda-nvrtc-11.7.99-0 None
  cuda-nvrtc-dev     nvidia/linux-64::cuda-nvrtc-dev-11.7.99-0 None
  cuda-nvtx          nvidia/linux-64::cuda-nvtx-11.7.91-0 None
  cuda-nvvp          nvidia/linux-64::cuda-nvvp-11.8.87-0 None
  cuda-runtime       nvidia/linux-64::cuda-runtime-11.7.1-0 None
  cuda-sanitizer-api nvidia/linux-64::cuda-sanitizer-api-11.8.86-0 None
  cuda-toolkit       nvidia/linux-64::cuda-toolkit-11.7.1-0 None
  cuda-tools         nvidia/linux-64::cuda-tools-11.7.1-0 None
  cuda-visual-tools  nvidia/linux-64::cuda-visual-tools-11.7.1-0 None
  ffmpeg             pytorch/linux-64::ffmpeg-4.3-hf484d3e_0 None
  freetype           pkgs/main/linux-64::freetype-2.12.1-h4a9f257_0 None
  gds-tools          nvidia/linux-64::gds-tools-1.4.0.31-0 None
  giflib             pkgs/main/linux-64::giflib-5.2.1-h7b6447c_0 None
  gmp                pkgs/main/linux-64::gmp-6.2.1-h295c915_3 None
  gnutls             pkgs/main/linux-64::gnutls-3.6.15-he1e5248_0 None
  idna               pkgs/main/linux-64::idna-3.4-py39h06a4308_0 None
  intel-openmp       pkgs/main/linux-64::intel-openmp-2021.4.0-h06a4308_3561 None
  jpeg               pkgs/main/linux-64::jpeg-9e-h7f8727e_0 None
  lame               pkgs/main/linux-64::lame-3.100-h7b6447c_0 None
  lcms2              pkgs/main/linux-64::lcms2-2.12-h3be6417_0 None
  lerc               pkgs/main/linux-64::lerc-3.0-h295c915_0 None
  libcublas          nvidia/linux-64::libcublas-11.11.3.6-0 None
  libcublas-dev      nvidia/linux-64::libcublas-dev-11.11.3.6-0 None
  libcufft           nvidia/linux-64::libcufft-10.9.0.58-0 None
  libcufft-dev       nvidia/linux-64::libcufft-dev-10.9.0.58-0 None
  libcufile          nvidia/linux-64::libcufile-1.4.0.31-0 None
  libcufile-dev      nvidia/linux-64::libcufile-dev-1.4.0.31-0 None
  libcurand          nvidia/linux-64::libcurand-10.3.0.86-0 None
  libcurand-dev      nvidia/linux-64::libcurand-dev-10.3.0.86-0 None
  libcusolver        nvidia/linux-64::libcusolver-11.4.1.48-0 None
  libcusolver-dev    nvidia/linux-64::libcusolver-dev-11.4.1.48-0 None
  libcusparse        nvidia/linux-64::libcusparse-11.7.5.86-0 None
  libcusparse-dev    nvidia/linux-64::libcusparse-dev-11.7.5.86-0 None
  libdeflate         pkgs/main/linux-64::libdeflate-1.8-h7f8727e_5 None
  libiconv           pkgs/main/linux-64::libiconv-1.16-h7f8727e_2 None
  libidn2            pkgs/main/linux-64::libidn2-2.3.2-h7f8727e_0 None
  libnpp             nvidia/linux-64::libnpp-11.8.0.86-0 None
  libnpp-dev         nvidia/linux-64::libnpp-dev-11.8.0.86-0 None
  libnvjpeg          nvidia/linux-64::libnvjpeg-11.9.0.86-0 None
  libnvjpeg-dev      nvidia/linux-64::libnvjpeg-dev-11.9.0.86-0 None
  libpng             pkgs/main/linux-64::libpng-1.6.37-hbc83047_0 None
  libtasn1           pkgs/main/linux-64::libtasn1-4.16.0-h27cfd23_0 None
  libtiff            pkgs/main/linux-64::libtiff-4.4.0-hecacb30_1 None
  libunistring       pkgs/main/linux-64::libunistring-0.9.10-h27cfd23_0 None
  libwebp            pkgs/main/linux-64::libwebp-1.2.4-h11a3e52_0 None
  libwebp-base       pkgs/main/linux-64::libwebp-base-1.2.4-h5eee18b_0 None
  lz4-c              pkgs/main/linux-64::lz4-c-1.9.3-h295c915_1 None
  mkl                pkgs/main/linux-64::mkl-2021.4.0-h06a4308_640 None
  mkl-service        pkgs/main/linux-64::mkl-service-2.4.0-py39h7f8727e_0 None
  mkl_fft            pkgs/main/linux-64::mkl_fft-1.3.1-py39hd3c417c_0 None
  mkl_random         pkgs/main/linux-64::mkl_random-1.2.2-py39h51133e4_0 None
  nettle             pkgs/main/linux-64::nettle-3.7.3-hbbd107a_1 None
  nsight-compute     nvidia/linux-64::nsight-compute-2022.3.0.22-0 None
  numpy              pkgs/main/linux-64::numpy-1.23.3-py39h14f4228_1 None
  numpy-base         pkgs/main/linux-64::numpy-base-1.23.3-py39h31eccc5_1 None
  openh264           pkgs/main/linux-64::openh264-2.1.1-h4ff587b_0 None
  pillow             pkgs/main/linux-64::pillow-9.2.0-py39hace64e9_1 None
  pycparser          pkgs/main/noarch::pycparser-2.21-pyhd3eb1b0_0 None
  pyopenssl          pkgs/main/noarch::pyopenssl-22.0.0-pyhd3eb1b0_0 None
  pysocks            pkgs/main/linux-64::pysocks-1.7.1-py39h06a4308_0 None
  pytorch            pytorch/linux-64::pytorch-1.13.0-py3.9_cuda11.7_cudnn8.5.0_0 None
  pytorch-cuda       pytorch/noarch::pytorch-cuda-11.7-h67b0de4_0 None
  pytorch-mutex      pytorch/noarch::pytorch-mutex-1.0-cuda None
  requests           pkgs/main/linux-64::requests-2.28.1-py39h06a4308_0 None
  six                pkgs/main/noarch::six-1.16.0-pyhd3eb1b0_1 None
  torchaudio         pytorch/linux-64::torchaudio-0.13.0-py39_cu117 None
  torchvision        pytorch/linux-64::torchvision-0.14.0-py39_cu117 None
  typing_extensions  pkgs/main/linux-64::typing_extensions-4.3.0-py39h06a4308_0 None
  urllib3            pkgs/main/linux-64::urllib3-1.26.12-py39h06a4308_0 None
  zstd               pkgs/main/linux-64::zstd-1.5.2-ha4553b6_0 None


Proceed ([y]/n)? y

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
Retrieving notices: ...working... done
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ 
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ sh build_and_install.sh

running install
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/easy_install.py:144: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
running bdist_egg
running egg_info
creating pointnet2.egg-info
writing pointnet2.egg-info/PKG-INFO
writing dependency_links to pointnet2.egg-info/dependency_links.txt
writing top-level names to pointnet2.egg-info/top_level.txt
writing manifest file 'pointnet2.egg-info/SOURCES.txt'
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:476: UserWarning: Attempted to use ninja as the BuildExtension backend but we could not find ninja.. Falling back to using the slow distutils backend.
  warnings.warn(msg.format('we could not find ninja.'))
reading manifest file 'pointnet2.egg-info/SOURCES.txt'
writing manifest file 'pointnet2.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_ext
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:387: UserWarning: The detected CUDA version (11.0) has a minor version mismatch with the version that was used to compile PyTorch (11.7). Most likely this shouldn't be a problem.
  warnings.warn(CUDA_MISMATCH_WARN.format(cuda_str_version, torch.version.cuda))
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:397: UserWarning: There are no g++ version bounds defined for CUDA version 11.0
  warnings.warn(f'There are no {compiler_name} version bounds defined for CUDA version {cuda_str_version}')
building 'pointnet2_cuda' extension
creating build
creating build/temp.linux-x86_64-cpython-39
creating build/temp.linux-x86_64-cpython-39/src
gcc -pthread -B /home/dhankar/anaconda3/envs/env_lyft/compiler_compat -Wno-unused-result -Wsign-compare -DNDEBUG -O2 -Wall -fPIC -O2 -isystem /home/dhankar/anaconda3/envs/env_lyft/include -I/home/dhankar/anaconda3/envs/env_lyft/include -fPIC -O2 -isystem /home/dhankar/anaconda3/envs/env_lyft/include -fPIC -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/TH -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/THC -I/usr/local/cuda-11.0/include -I/home/dhankar/anaconda3/envs/env_lyft/include/python3.9 -c src/ball_query.cpp -o build/temp.linux-x86_64-cpython-39/src/ball_query.o -g -DTORCH_API_INCLUDE_EXTENSION_H -DPYBIND11_COMPILER_TYPE=\"_gcc\" -DPYBIND11_STDLIB=\"_libstdcpp\" -DPYBIND11_BUILD_ABI=\"_cxxabi1011\" -DTORCH_EXTENSION_NAME=pointnet2_cuda -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++14
src/ball_query.cpp:3:10: fatal error: THC/THC.h: No such file or directory
 #include <THC/THC.h>
          ^~~~~~~~~~~
compilation terminated.


error: command '/usr/lib/ccache/gcc' failed with exit code 1
running install


/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/easy_install.py:144: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
running bdist_egg
running egg_info
creating iou3d.egg-info
writing iou3d.egg-info/PKG-INFO
writing dependency_links to iou3d.egg-info/dependency_links.txt
writing top-level names to iou3d.egg-info/top_level.txt
writing manifest file 'iou3d.egg-info/SOURCES.txt'
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:476: UserWarning: Attempted to use ninja as the BuildExtension backend but we could not find ninja.. Falling back to using the slow distutils backend.
  warnings.warn(msg.format('we could not find ninja.'))
reading manifest file 'iou3d.egg-info/SOURCES.txt'
writing manifest file 'iou3d.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_ext
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:387: UserWarning: The detected CUDA version (11.0) has a minor version mismatch with the version that was used to compile PyTorch (11.7). Most likely this shouldn't be a problem.
  warnings.warn(CUDA_MISMATCH_WARN.format(cuda_str_version, torch.version.cuda))
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:397: UserWarning: There are no g++ version bounds defined for CUDA version 11.0
  warnings.warn(f'There are no {compiler_name} version bounds defined for CUDA version {cuda_str_version}')
building 'iou3d_cuda' extension
creating build
creating build/temp.linux-x86_64-cpython-39
creating build/temp.linux-x86_64-cpython-39/src
gcc -pthread -B /home/dhankar/anaconda3/envs/env_lyft/compiler_compat -Wno-unused-result -Wsign-compare -DNDEBUG -O2 -Wall -fPIC -O2 -isystem /home/dhankar/anaconda3/envs/env_lyft/include -I/home/dhankar/anaconda3/envs/env_lyft/include -fPIC -O2 -isystem /home/dhankar/anaconda3/envs/env_lyft/include -fPIC -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/TH -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/THC -I/usr/local/cuda-11.0/include -I/home/dhankar/anaconda3/envs/env_lyft/include/python3.9 -c src/iou3d.cpp -o build/temp.linux-x86_64-cpython-39/src/iou3d.o -g -DTORCH_API_INCLUDE_EXTENSION_H -DPYBIND11_COMPILER_TYPE=\"_gcc\" -DPYBIND11_STDLIB=\"_libstdcpp\" -DPYBIND11_BUILD_ABI=\"_cxxabi1011\" -DTORCH_EXTENSION_NAME=iou3d_cuda -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++14
src/iou3d.cpp: In function ‘int boxes_overlap_bev_gpu(at::Tensor, at::Tensor, at::Tensor)’:
src/iou3d.cpp:7:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/iou3d.cpp:9:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/iou3d.cpp:36:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes_a);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/iou3d.cpp:7:23: error: ‘AT_CHECK’ was not declared in this scope
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/iou3d.cpp:7:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/iou3d.cpp:36:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes_a);
     ^
src/iou3d.cpp:7:23: note: suggested alternative: ‘CHECK’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/iou3d.cpp:7:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/iou3d.cpp:36:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes_a);
     ^
src/iou3d.cpp:7:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/iou3d.cpp:9:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/iou3d.cpp:37:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes_b);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/iou3d.cpp:7:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/iou3d.cpp:9:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/iou3d.cpp:38:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(ans_overlap);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/iou3d.cpp:43:54: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * boxes_a_data = boxes_a.data<float>();
                                                      ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp:44:54: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * boxes_b_data = boxes_b.data<float>();
                                                      ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp:45:56: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * ans_overlap_data = ans_overlap.data<float>();
                                                        ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp: In function ‘int boxes_iou_bev_gpu(at::Tensor, at::Tensor, at::Tensor)’:
src/iou3d.cpp:7:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/iou3d.cpp:9:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/iou3d.cpp:57:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes_a);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/iou3d.cpp:7:23: error: ‘AT_CHECK’ was not declared in this scope
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/iou3d.cpp:7:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/iou3d.cpp:57:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes_a);
     ^
src/iou3d.cpp:7:23: note: suggested alternative: ‘CHECK’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/iou3d.cpp:7:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/iou3d.cpp:57:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes_a);
     ^
src/iou3d.cpp:7:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/iou3d.cpp:9:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/iou3d.cpp:58:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes_b);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/iou3d.cpp:7:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/iou3d.cpp:9:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/iou3d.cpp:59:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(ans_iou);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/iou3d.cpp:64:54: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * boxes_a_data = boxes_a.data<float>();
                                                      ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp:65:54: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * boxes_b_data = boxes_b.data<float>();
                                                      ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp:66:48: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * ans_iou_data = ans_iou.data<float>();
                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp: In function ‘int nms_gpu(at::Tensor, at::Tensor, float)’:
src/iou3d.cpp:7:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/iou3d.cpp:9:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/iou3d.cpp:77:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/iou3d.cpp:7:23: error: ‘AT_CHECK’ was not declared in this scope
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/iou3d.cpp:7:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/iou3d.cpp:77:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes);
     ^
src/iou3d.cpp:7:23: note: suggested alternative: ‘CHECK’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/iou3d.cpp:7:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/iou3d.cpp:77:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes);
     ^
src/iou3d.cpp:81:50: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * boxes_data = boxes.data<float>();
                                                  ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp:82:40: warning: ‘T* at::Tensor::data() const [with T = long int]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     long * keep_data = keep.data<long>();
                                        ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp: In function ‘int nms_normal_gpu(at::Tensor, at::Tensor, float)’:
src/iou3d.cpp:7:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/iou3d.cpp:9:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/iou3d.cpp:127:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/iou3d.cpp:7:23: error: ‘AT_CHECK’ was not declared in this scope
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/iou3d.cpp:7:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/iou3d.cpp:127:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes);
     ^
src/iou3d.cpp:7:23: note: suggested alternative: ‘CHECK’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/iou3d.cpp:7:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/iou3d.cpp:127:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes);
     ^
src/iou3d.cpp:131:50: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * boxes_data = boxes.data<float>();
                                                  ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/iou3d.cpp:132:40: warning: ‘T* at::Tensor::data() const [with T = long int]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     long * keep_data = keep.data<long>();
                                        ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/iou3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
error: command '/usr/lib/ccache/gcc' failed with exit code 1
running install
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/setuptools/command/easy_install.py:144: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
running bdist_egg
running egg_info
creating roipool3d.egg-info
writing roipool3d.egg-info/PKG-INFO
writing dependency_links to roipool3d.egg-info/dependency_links.txt
writing top-level names to roipool3d.egg-info/top_level.txt
writing manifest file 'roipool3d.egg-info/SOURCES.txt'
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:476: UserWarning: Attempted to use ninja as the BuildExtension backend but we could not find ninja.. Falling back to using the slow distutils backend.
  warnings.warn(msg.format('we could not find ninja.'))
reading manifest file 'roipool3d.egg-info/SOURCES.txt'
writing manifest file 'roipool3d.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_ext
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:387: UserWarning: The detected CUDA version (11.0) has a minor version mismatch with the version that was used to compile PyTorch (11.7). Most likely this shouldn't be a problem.
  warnings.warn(CUDA_MISMATCH_WARN.format(cuda_str_version, torch.version.cuda))
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/utils/cpp_extension.py:397: UserWarning: There are no g++ version bounds defined for CUDA version 11.0
  warnings.warn(f'There are no {compiler_name} version bounds defined for CUDA version {cuda_str_version}')
building 'roipool3d_cuda' extension
creating build
creating build/temp.linux-x86_64-cpython-39
creating build/temp.linux-x86_64-cpython-39/src
gcc -pthread -B /home/dhankar/anaconda3/envs/env_lyft/compiler_compat -Wno-unused-result -Wsign-compare -DNDEBUG -O2 -Wall -fPIC -O2 -isystem /home/dhankar/anaconda3/envs/env_lyft/include -I/home/dhankar/anaconda3/envs/env_lyft/include -fPIC -O2 -isystem /home/dhankar/anaconda3/envs/env_lyft/include -fPIC -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/TH -I/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/THC -I/usr/local/cuda-11.0/include -I/home/dhankar/anaconda3/envs/env_lyft/include/python3.9 -c src/roipool3d.cpp -o build/temp.linux-x86_64-cpython-39/src/roipool3d.o -g -DTORCH_API_INCLUDE_EXTENSION_H -DPYBIND11_COMPILER_TYPE=\"_gcc\" -DPYBIND11_STDLIB=\"_libstdcpp\" -DPYBIND11_BUILD_ABI=\"_cxxabi1011\" -DTORCH_EXTENSION_NAME=roipool3d_cuda -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++14
src/roipool3d.cpp: In function ‘int roipool3d_gpu_slow(at::Tensor, at::Tensor, at::Tensor, at::Tensor, at::Tensor)’:
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:21:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(xyz);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:5:23: error: ‘AT_CHECK’ was not declared in this scope
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/roipool3d.cpp:5:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/roipool3d.cpp:21:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(xyz);
     ^
src/roipool3d.cpp:5:23: note: suggested alternative: ‘CHECK’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/roipool3d.cpp:5:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/roipool3d.cpp:21:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(xyz);
     ^
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:22:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes3d);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:23:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(pts_feature);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:24:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(pooled_features);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:25:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(pooled_empty_flag);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:34:46: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * xyz_data = xyz.data<float>();
                                              ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:35:54: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * boxes3d_data = boxes3d.data<float>();
                                                      ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:36:62: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * pts_feature_data = pts_feature.data<float>();
                                                              ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:37:64: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * pooled_features_data = pooled_features.data<float>();
                                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:38:64: warning: ‘T* at::Tensor::data() const [with T = int]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     int * pooled_empty_flag_data = pooled_empty_flag.data<int>();
                                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp: In function ‘int roipool3d_gpu(at::Tensor, at::Tensor, at::Tensor, at::Tensor, at::Tensor)’:
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:54:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(xyz);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:5:23: error: ‘AT_CHECK’ was not declared in this scope
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/roipool3d.cpp:5:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/roipool3d.cpp:54:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(xyz);
     ^
src/roipool3d.cpp:5:23: note: suggested alternative: ‘CHECK’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^
src/roipool3d.cpp:5:23: note: in definition of macro ‘CHECK_CUDA’
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                       ^~~~~~~~
src/roipool3d.cpp:54:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(xyz);
     ^
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:55:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(boxes3d);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:56:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(pts_feature);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:57:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(pooled_features);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:5:39: warning: ‘at::DeprecatedTypeProperties& at::Tensor::type() const’ is deprecated: Tensor.type() is deprecated. Instead use Tensor.options(), which in many cases (e.g. in a constructor) is a drop-in replacement. If you were using data from type(), that is now available from Tensor itself, so instead of tensor.type().scalar_type(), use tensor.scalar_type() instead and instead of tensor.type().backend() use tensor.device(). [-Wdeprecated-declarations]
 #define CHECK_CUDA(x) AT_CHECK(x.type().is_cuda(), #x, " must be a CUDAtensor ")
                                       ^
src/roipool3d.cpp:7:24: note: in expansion of macro ‘CHECK_CUDA’
 #define CHECK_INPUT(x) CHECK_CUDA(x);CHECK_CONTIGUOUS(x)
                        ^~~~~~~~~~
src/roipool3d.cpp:58:5: note: in expansion of macro ‘CHECK_INPUT’
     CHECK_INPUT(pooled_empty_flag);
     ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:216:30: note: declared here
   DeprecatedTypeProperties & type() const {
                              ^~~~
src/roipool3d.cpp:67:46: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * xyz_data = xyz.data<float>();
                                              ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:68:54: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * boxes3d_data = boxes3d.data<float>();
                                                      ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:69:62: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     const float * pts_feature_data = pts_feature.data<float>();
                                                              ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:70:64: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * pooled_features_data = pooled_features.data<float>();
                                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:71:64: warning: ‘T* at::Tensor::data() const [with T = int]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     int * pooled_empty_flag_data = pooled_empty_flag.data<int>();
                                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp: In function ‘int pts_in_boxes3d_cpu(at::Tensor, at::Tensor, at::Tensor)’:
src/roipool3d.cpp:6:29: error: ‘AT_CHECK’ was not declared in this scope
 #define CHECK_CONTIGUOUS(x) AT_CHECK(x.is_contiguous(), #x, " must be contiguous ")
                             ^
src/roipool3d.cpp:6:29: note: in definition of macro ‘CHECK_CONTIGUOUS’
 #define CHECK_CONTIGUOUS(x) AT_CHECK(x.is_contiguous(), #x, " must be contiguous ")
                             ^~~~~~~~
src/roipool3d.cpp:6:29: note: suggested alternative: ‘CHECK’
 #define CHECK_CONTIGUOUS(x) AT_CHECK(x.is_contiguous(), #x, " must be contiguous ")
                             ^
src/roipool3d.cpp:6:29: note: in definition of macro ‘CHECK_CONTIGUOUS’
 #define CHECK_CONTIGUOUS(x) AT_CHECK(x.is_contiguous(), #x, " must be contiguous ")
                             ^~~~~~~~
src/roipool3d.cpp:109:48: warning: ‘T* at::Tensor::data() const [with T = long int]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     long * pts_flag_flat = pts_flag.data<long>();
                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:110:40: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * pts_flat = pts.data<float>();
                                        ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:111:48: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * boxes3d_flat = boxes3d.data<float>();
                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp: In function ‘int roipool3d_cpu(at::Tensor, at::Tensor, at::Tensor, at::Tensor, at::Tensor, at::Tensor)’:
src/roipool3d.cpp:6:29: error: ‘AT_CHECK’ was not declared in this scope
 #define CHECK_CONTIGUOUS(x) AT_CHECK(x.is_contiguous(), #x, " must be contiguous ")
                             ^
src/roipool3d.cpp:6:29: note: in definition of macro ‘CHECK_CONTIGUOUS’
 #define CHECK_CONTIGUOUS(x) AT_CHECK(x.is_contiguous(), #x, " must be contiguous ")
                             ^~~~~~~~
src/roipool3d.cpp:6:29: note: suggested alternative: ‘CHECK’
 #define CHECK_CONTIGUOUS(x) AT_CHECK(x.is_contiguous(), #x, " must be contiguous ")
                             ^
src/roipool3d.cpp:6:29: note: in definition of macro ‘CHECK_CONTIGUOUS’
 #define CHECK_CONTIGUOUS(x) AT_CHECK(x.is_contiguous(), #x, " must be contiguous ")
                             ^~~~~~~~
src/roipool3d.cpp:146:40: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * pts_flat = pts.data<float>();
                                        ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:147:48: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * boxes3d_flat = boxes3d.data<float>();
                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:148:56: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * pts_feature_flat = pts_feature.data<float>();
                                                        ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:149:54: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * pooled_pts_flat = pooled_pts.data<float>();
                                                      ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:150:64: warning: ‘T* at::Tensor::data() const [with T = float]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     float * pooled_features_flat = pooled_features.data<float>();
                                                                ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
src/roipool3d.cpp:151:66: warning: ‘T* at::Tensor::data() const [with T = long int]’ is deprecated: Tensor.data<T>() is deprecated. Please use Tensor.data_ptr<T>() instead. [-Wdeprecated-declarations]
     long * pooled_empty_flag_flat = pooled_empty_flag.data<long>();
                                                                  ^
In file included from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/Tensor.h:3:0,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/Tensor.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/function_hook.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/cpp_hook.h:2,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/autograd/variable.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/jit/api/module.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/input-archive.h:6,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/archive.h:3,
                 from /home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/torch/csrc/api/include/torch/serialize/tensor.h:3,
                 from src/roipool3d.cpp:1:
/home/dhankar/anaconda3/envs/env_lyft/lib/python3.9/site-packages/torch/include/ATen/core/TensorBody.h:238:7: note: declared here
   T * data() const {
       ^~~~
error: command '/usr/lib/ccache/gcc' failed with exit code 1
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ 
(env_lyft) dhankar@dhankar-1:~/.../PointRCNN$ 
```