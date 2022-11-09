




##### NOT SOLVED - same error as earlier 
> The following packages have unmet dependencies:
 cuda : Depends: cuda-11-8 (>= 11.8.0) but it is not going to be installed
E: Unable to correct problems, you have held broken packages.



#
<br>



/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/

- pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu116



- https://askubuntu.com/questions/1407632/key-is-stored-in-legacy-trusted-gpg-keyring-etc-apt-trusted-gpg

```bash

pub   rsa4096 2016-06-24 [SC]
      AE09 FE4B BD22 3A84 B2CC  FCE3 F60F 4B3D 7FA2 AF80
uid           [ unknown] cudatools <cudatools@nvidia.com>

(env_point_net) dhankar@dhankar-1:.../preferences.d$ sudo apt-key list | grep cuda
Warning: apt-key output should not be parsed (stdout is not a terminal)
uid           [ unknown] cudatools <cudatools@nvidia.com>
(env_point_net) dhankar@dhankar-1:.../preferences.d$ 

```

```bash
$ pwd
/home/dhankar
(base) dhankar@dhankar-1:~$ 
(base) dhankar@dhankar-1:~$ sudo apt-key del 7fa2af80
[sudo] password for dhankar: 
OK
(base) dhankar@dhankar-1:~$ 
(base) dhankar@dhankar-1:~$ sudo apt-key del 7fa2af80
OK
(base) dhankar@dhankar-1:~$ 
#
(base) dhankar@dhankar-1:~$ wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-keyring_1.0-1_all.deb
--2022-11-10 01:08:46--  https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-keyring_1.0-1_all.deb
Resolving developer.download.nvidia.com (developer.download.nvidia.com)... 152.199.39.144
Connecting to developer.download.nvidia.com (developer.download.nvidia.com)|152.199.39.144|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4332 (4.2K) [application/x-deb]
Saving to: ‘cuda-keyring_1.0-1_all.deb’

cuda-keyring_1.0-1_all.deb          100%[=================================================================>]   4.23K  --.-KB/s    in 0s      

2022-11-10 01:08:47 (97.7 MB/s) - ‘cuda-keyring_1.0-1_all.deb’ saved [4332/4332]

(base) dhankar@dhankar-1:~$ 
#
(base) dhankar@dhankar-1:~$ sudo dpkg -i cuda-keyring_1.0-1_all.deb
Selecting previously unselected package cuda-keyring.
(Reading database ... 973290 files and directories currently installed.)
Preparing to unpack cuda-keyring_1.0-1_all.deb ...
Unpacking cuda-keyring (1.0-1) ...
Setting up cuda-keyring (1.0-1) ...
(base) dhankar@dhankar-1:~$ 

#
(base) dhankar@dhankar-1:~$ wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin 
--2022-11-10 01:11:07--  https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin
Resolving developer.download.nvidia.com (developer.download.nvidia.com)... 152.199.39.144
Connecting to developer.download.nvidia.com (developer.download.nvidia.com)|152.199.39.144|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 190 [application/octet-stream]
Saving to: ‘cuda-ubuntu1804.pin’

cuda-ubuntu1804.pin                 100%[=================================================================>]     190  --.-KB/s    in 0s      

2022-11-10 01:11:07 (26.2 MB/s) - ‘cuda-ubuntu1804.pin’ saved [190/190]


#

(base) dhankar@dhankar-1:~$ sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600

(base) dhankar@dhankar-1:~$ cd /etc/apt/preferences.d/
(base) dhankar@dhankar-1:.../preferences.d$ 
(base) dhankar@dhankar-1:.../preferences.d$ ls -lahtr
total 12K
-rw-rw-r-- 1 dhankar dhankar  190 Jun 24  2020 cuda-repository-pin-600
drwxr-xr-x 7 root    root    4.0K Nov 10 01:07 ..
drwxr-xr-x 2 root    root    4.0K Nov 10 01:11 .
(base) dhankar@dhankar-1:.../preferences.d$ 

#
#

$ 
(base) dhankar@dhankar-1:.../preferences.d$ cd -
/home/dhankar
(base) dhankar@dhankar-1:~$ 
(base) dhankar@dhankar-1:~$ wget https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb
--2022-11-10 01:14:20--  https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb
Resolving developer.download.nvidia.com (developer.download.nvidia.com)... 152.199.39.144
Connecting to developer.download.nvidia.com (developer.download.nvidia.com)|152.199.39.144|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1896270068 (1.8G) [application/x-deb]
Saving to: ‘cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb’

cuda-repo-ubuntu1804-10-2-local-10. 100%[=================================================================>]   1.77G  24.0MB/s    in 82s     

2022-11-10 01:15:42 (22.1 MB/s) - ‘cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb’ saved [1896270068/1896270068]

(base) dhankar@dhankar-1:~$ 

#
(base) dhankar@dhankar-1:~$ sudo dpkg -i cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb
(Reading database ... 973295 files and directories currently installed.)
Preparing to unpack cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb ...
Unpacking cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01 (1.0-1) over (1.0-1) ...
Setting up cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01 (1.0-1) ...

The public CUDA GPG key does not appear to be installed.
To install the key, run this command:
sudo apt-key add /var/cuda-repo-10-2-local-10.2.89-440.33.01/7fa2af80.pub

(base) dhankar@dhankar-1:~$ 

#
#
(base) dhankar@dhankar-1:~$ sudo apt-key add /var/cuda-repo-10-2-local-10.2.89-440.33.01/7fa2af80.pub
OK
(base) dhankar@dhankar-1:~$ 

#
(base) dhankar@dhankar-1:~$ sudo apt-key add /var/cuda-repo-10-2-local-10.2.89-440.33.01/7fa2af80.pub
OK
(base) dhankar@dhankar-1:~$ 
(base) dhankar@dhankar-1:~$ sudo apt-get update
Get:1 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  InRelease
Ign:1 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  InRelease
Get:2 file:/var/cuda-repo-ubuntu1804-11-0-local  InRelease
Ign:2 file:/var/cuda-repo-ubuntu1804-11-0-local  InRelease
Get:3 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  Release [574 B]
Get:4 file:/var/cuda-repo-ubuntu1804-11-0-local  Release [564 B]
Get:3 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  Release [574 B]
Get:4 file:/var/cuda-repo-ubuntu1804-11-0-local  Release [564 B]
Hit:5 https://download.docker.com/linux/ubuntu bionic InRelease      
Hit:7 https://dl.winehq.org/wine-builds/ubuntu bionic InRelease                                                                              
Get:8 https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  InRelease [1,581 B]                                        
Get:9 http://dl.google.com/linux/chrome/deb stable InRelease [1,811 B]                                                                       
Ign:11 http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.4 InRelease                                                                   
Get:12 http://packages.microsoft.com/repos/code stable InRelease [10.4 kB]                                                                   
Ign:13 https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 InRelease                                                                  
Get:14 http://security.ubuntu.com/ubuntu bionic-security InRelease [88.7 kB]                                                                 
Ign:15 https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.4 InRelease                                                                  
Hit:16 http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.4 Release                                                                     
Hit:17 http://in.archive.ubuntu.com/ubuntu bionic InRelease                                                                                  
Hit:18 https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 Release                                                                    
Get:19 https://cloud.r-project.org/bin/linux/ubuntu bionic-cran40/ InRelease [3,626 B]                                                       
Hit:20 http://ppa.launchpad.net/alexlarsson/flatpak/ubuntu bionic InRelease                                                                  
Get:21 https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  Packages [992 kB]                                         
Get:22 http://in.archive.ubuntu.com/ubuntu bionic-updates InRelease [88.7 kB]                                                                
Hit:24 https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.4 Release                                                                    
Err:9 http://dl.google.com/linux/chrome/deb stable InRelease                                                                                 
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 4EB27DB2A3B88B8B
Hit:25 http://ppa.launchpad.net/apandada1/brightness-controller/ubuntu bionic InRelease                                                      
Get:27 http://packages.microsoft.com/repos/code stable/main armhf Packages [120 kB]                                                          
Ign:29 http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64  InRelease                                      
Hit:30 http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64  Release                                        
Hit:31 http://ppa.launchpad.net/cybermax-dexter/sdl2-backport/ubuntu bionic InRelease                                                        
Ign:33 https://kx.studio/repo stable InRelease                                                                                               
Get:35 http://packages.microsoft.com/repos/code stable/main arm64 Packages [120 kB]                                                          
Ign:36 https://kx.studio/repo gcc5 InRelease                                                                                                 
Hit:38 https://repo.fortinet.com/repo/ubuntu /bionic InRelease                                                                               
Hit:39 http://ppa.launchpad.net/kxstudio-debian/libs/ubuntu bionic InRelease                                                                 
Get:40 http://packages.microsoft.com/repos/code stable/main amd64 Packages [119 kB]                                                          
Hit:41 https://kx.studio/repo stable Release                                                                                                 
Hit:42 https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/bionic pgadmin4 InRelease                                                         
Hit:45 https://kx.studio/repo gcc5 Release                                                                                                   
Get:47 http://in.archive.ubuntu.com/ubuntu bionic-backports InRelease [83.3 kB]                                                              
Get:44 http://packages.ros.org/ros/ubuntu bionic InRelease [4,680 B]                                                                         
Get:48 https://repo.skype.com/deb stable InRelease [4,501 B]                                                                                 
Get:50 http://ppa.launchpad.net/kxstudio-debian/plugins/ubuntu bionic InRelease [15.4 kB]                                                    
Get:51 http://security.ubuntu.com/ubuntu bionic-security/main amd64 DEP-11 Metadata [55.2 kB]                                         
Get:52 http://security.ubuntu.com/ubuntu bionic-security/universe amd64 DEP-11 Metadata [61.1 kB]                                            
Get:53 http://security.ubuntu.com/ubuntu bionic-security/multiverse amd64 DEP-11 Metadata [2,468 B]                                          
Hit:54 http://ppa.launchpad.net/kxstudio-debian/apps/ubuntu bionic InRelease                                                                 
Hit:56 http://ppa.launchpad.net/kxstudio-debian/kxstudio/ubuntu bionic InRelease                                               
Hit:58 http://ppa.launchpad.net/mixxx/mixxx/ubuntu bionic InRelease                                    
Hit:59 http://ppa.launchpad.net/ubuntugis/ubuntugis-unstable/ubuntu bionic InRelease                                                  
Get:61 http://in.archive.ubuntu.com/ubuntu bionic-updates/main i386 Packages [1,562 kB]                                                      
Hit:62 https://packages.microsoft.com/repos/ms-teams stable InRelease                                                                        
Err:44 http://packages.ros.org/ros/ubuntu bionic InRelease                                                                                   
  The following signatures were invalid: EXPKEYSIG F42ED6FBAB17C654 Open Robotics <info@osrfoundation.org>
Get:46 http://ppa.launchpad.net/kxstudio-debian/music/ubuntu bionic InRelease [15.4 kB]                            
Err:48 https://repo.skype.com/deb stable InRelease                                                                                   
  The following signatures were invalid: EXPKEYSIG 1F3045A5DF7587C3 Skype Linux Client Repository <se-um@microsoft.com>
Get:63 http://in.archive.ubuntu.com/ubuntu bionic-updates/main amd64 Packages [2,790 kB]                          
Get:64 http://in.archive.ubuntu.com/ubuntu bionic-updates/main amd64 DEP-11 Metadata [297 kB]                    
Get:65 http://in.archive.ubuntu.com/ubuntu bionic-updates/universe amd64 DEP-11 Metadata [302 kB]
Get:66 http://in.archive.ubuntu.com/ubuntu bionic-updates/multiverse amd64 DEP-11 Metadata [2,468 B]
Get:67 http://in.archive.ubuntu.com/ubuntu bionic-backports/main amd64 DEP-11 Metadata [8,088 B]
Get:68 http://in.archive.ubuntu.com/ubuntu bionic-backports/universe amd64 DEP-11 Metadata [10.0 kB]
Hit:32 https://scala.jfrog.io/artifactory/debian all InRelease                                                                               
Ign:37 https://scala.jfrog.io/artifactory/debian  InRelease                                                                                  
Hit:57 https://packagecloud.io/slacktechnologies/slack/debian jessie InRelease                                                               
Get:23 https://ubuntugis.qgis.org/ubuntugis bionic InRelease [3,673 B]                                                                       
Err:23 https://ubuntugis.qgis.org/ubuntugis bionic InRelease                                                                                 
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D155B8E6A419C5BE
Get:28 https://ubuntu.qgis.org/ubuntu bionic InRelease [3,673 B]                                                                             
Err:28 https://ubuntu.qgis.org/ubuntu bionic InRelease                                                                                       
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D155B8E6A419C5BE
Get:69 https://deb.torproject.org/torproject.org bionic InRelease [3,524 B]                                                                  
Err:69 https://deb.torproject.org/torproject.org bionic InRelease                                                                            
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 74A941BA219EC810
Hit:70 https://scala.jfrog.io/artifactory/debian  Release                                                                                    
Reading package lists... Done
W: Target Packages (stable/binary-amd64/Packages) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Packages (stable/binary-all/Packages) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Translations (stable/i18n/Translation-en_IN) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Translations (stable/i18n/Translation-en) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11 (stable/dep11/Components-amd64.yml) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11 (stable/dep11/Components-all.yml) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11-icons-small (stable/dep11/icons-48x48.tar) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11-icons (stable/dep11/icons-64x64.tar) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target CNF (stable/cnf/Commands-amd64) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target CNF (stable/cnf/Commands-all) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Packages (Packages) is configured multiple times in /etc/apt/sources.list:78 and /etc/apt/sources.list.d/cuda-ubuntu1804-x86_64.list:1
W: Target Translations (en_IN) is configured multiple times in /etc/apt/sources.list:78 and /etc/apt/sources.list.d/cuda-ubuntu1804-x86_64.list:1
W: Target Translations (en) is configured multiple times in /etc/apt/sources.list:78 and /etc/apt/sources.list.d/cuda-ubuntu1804-x86_64.list:1
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: http://dl.google.com/linux/chrome/deb stable InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 4EB27DB2A3B88B8B
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: http://packages.ros.org/ros/ubuntu bionic InRelease: The following signatures were invalid: EXPKEYSIG F42ED6FBAB17C654 Open Robotics <info@osrfoundation.org>
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: https://repo.skype.com/deb stable InRelease: The following signatures were invalid: EXPKEYSIG 1F3045A5DF7587C3 Skype Linux Client Repository <se-um@microsoft.com>
E: Repository 'http://ppa.launchpad.net/kxstudio-debian/music/ubuntu bionic InRelease' changed its 'Label' value from 'Music' to 'Deprecated'
N: This must be accepted explicitly before updates for this repository can be applied. See apt-secure(8) manpage for details.
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: https://ubuntugis.qgis.org/ubuntugis bionic InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D155B8E6A419C5BE
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: https://ubuntu.qgis.org/ubuntu bionic InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D155B8E6A419C5BE
W: GPG error: https://deb.torproject.org/torproject.org bionic InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 74A941BA219EC810
E: The repository 'https://deb.torproject.org/torproject.org bionic InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
W: Target Packages (stable/binary-amd64/Packages) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Packages (stable/binary-all/Packages) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Translations (stable/i18n/Translation-en_IN) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Translations (stable/i18n/Translation-en) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11 (stable/dep11/Components-amd64.yml) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11 (stable/dep11/Components-all.yml) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11-icons-small (stable/dep11/icons-48x48.tar) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11-icons (stable/dep11/icons-64x64.tar) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target CNF (stable/cnf/Commands-amd64) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target CNF (stable/cnf/Commands-all) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Packages (Packages) is configured multiple times in /etc/apt/sources.list:78 and /etc/apt/sources.list.d/cuda-ubuntu1804-x86_64.list:1
W: Target Translations (en_IN) is configured multiple times in /etc/apt/sources.list:78 and /etc/apt/sources.list.d/cuda-ubuntu1804-x86_64.list:1
W: Target Translations (en) is configured multiple times in /etc/apt/sources.list:78 and /etc/apt/sources.list.d/cuda-ubuntu1804-x86_64.list:1
(base) dhankar@dhankar-1:~$ 
#
$ 
(base) dhankar@dhankar-1:~$ sudo apt-get -y install cuda
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Some packages could not be installed. This may mean that you have
requested an impossible situation or if you are using the unstable
distribution that some required packages have not yet been created
or been moved out of Incoming.
The following information may help to resolve the situation:

The following packages have unmet dependencies:
 cuda : Depends: cuda-11-8 (>= 11.8.0) but it is not going to be installed
E: Unable to correct problems, you have held broken packages.
(base) dhankar@dhankar-1:~$ 
(base) dhankar@dhankar-1:~$ 
```


```bash
wget https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb

sudo dpkg -i cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb

sudo apt-key add /var/cuda-repo-10-2-local-10.2.89-440.33.01/7fa2af80.pub

sudo apt-get update

sudo apt-get -y install cuda

```


#
<br>


##### Key Rotate -- Official NVIDIA -- 
- https://forums.developer.nvidia.com/t/notice-cuda-linux-repository-key-rotation/212772

```bash

sudo apt-key del 7fa2af80
#ubuntu1804/x86_64

wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-keyring_1.0-1_all.deb
sudo dpkg -i cuda-keyring_1.0-1_all.deb

```



#
<br>


```bash
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin 

sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600

wget https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb

sudo dpkg -i cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb

sudo apt-key add /var/cuda-repo-10-2-local-10.2.89-440.33.01/7fa2af80.pub

sudo apt-get update

sudo apt-get -y install cuda

```
#
<br>


##### Same ERROR / Issue as mine -- CUDA FORUMS -- public key is not available: NO_PUBKEY A4B469963BF863CC
- https://forums.developer.nvidia.com/t/invalid-public-key-for-cuda-apt-repository/212901/16

##### Same ERROR / Issue as mine -- CUDA DOCKER GIT REPO -- public key is not available: NO_PUBKEY A4B469963BF863CC

- https://github.com/NVIDIA/nvidia-docker/issues/1632

```bash

$ sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/3bf863cc.pub
$ sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64/7fa2af80.pub


```
#
<br>

###### the public key is not available: NO_PUBKEY A4B469963BF863CC


```bash

W: GPG error: https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY A4B469963BF863CC
E: The repository 'https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  InRelease' is no longer signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.

```
#
<br>

##### is the PIN Not Updated ? -- cuda-repository-pin-600

```bash

env_point_net) dhankar@dhankar-1:~/.../iou3d$ cd /etc/apt/preferences.d/
(env_point_net) dhankar@dhankar-1:.../preferences.d$ 
(env_point_net) dhankar@dhankar-1:.../preferences.d$ ls -lahtr
total 12K
-rw-rw-r-- 1 dhankar dhankar  190 Jun 24  2020 cuda-repository-pin-600
drwxr-xr-x 2 root    root    4.0K Nov  8 23:22 .
drwxr-xr-x 7 root    root    4.0K Nov  9 00:11 ..
(env_point_net) dhankar@dhankar-1:.../preferences.d$ 
(env_point_net) dhankar@dhankar-1:.../preferences.d$ pwd
/etc/apt/preferences.d
(env_point_net) dhankar@dhankar-1:.../preferences.d$ 
```




#
<br>


#### Get the -- CUDA toolkit from NVIDIA
- Per this SO Answer -- Get the -- CUDA toolkit from NVIDIA
- https://stackoverflow.com/a/71730556/4928635

```bash

wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin

sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600

wget https://developer.download.nvidia.com/compute/cuda/11.8.0/local_installers/cuda-repo-ubuntu1804-11-8-local_11.8.0-520.61.05-1_amd64.deb

sudo dpkg -i cuda-repo-ubuntu1804-11-8-local_11.8.0-520.61.05-1_amd64.deb
sudo cp /var/cuda-repo-ubuntu1804-11-8-local/cuda-*-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt-get -y install cuda
```

#
<br>


- packages in environment at /home/dhankar/anaconda3/envs/env_point_net

```bash

(env_point_net) dhankar@dhankar-1:~/.../iou3d$  conda list|grep cuda
cudatoolkit               10.2.89              hfd86e86_1  
pytorch                   1.10.1          py3.6_cuda10.2_cudnn7.6.5_0    pytorch
pytorch-mutex             1.0                        cuda    pytorch
(env_point_net) dhankar@dhankar-1:~/.../iou3d$  conda list
# packages in environment at /home/dhankar/anaconda3/envs/env_point_net:
#
# Name                    Version                   Build  Channel
_libgcc_mutex             0.1                        main  
_openmp_mutex             5.1                       1_gnu  
blas                      1.0                         mkl  
bzip2                     1.0.8                h7b6447c_0  
ca-certificates           2022.10.11           h06a4308_0  
certifi                   2021.5.30        py36h06a4308_0  
cudatoolkit               10.2.89              hfd86e86_1  
dataclasses               0.8                pyh4f3eec9_6  
ffmpeg                    4.3                  hf484d3e_0    pytorch
freetype                  2.12.1               h4a9f257_0  
gmp                       6.2.1                h295c915_3  
gnutls                    3.6.15               he1e5248_0  
intel-openmp              2022.1.0          h9e868ea_3769  
jpeg                      9e                   h7f8727e_0  
lame                      3.100                h7b6447c_0  
lcms2                     2.12                 h3be6417_0  
ld_impl_linux-64          2.38                 h1181459_1  
lerc                      3.0                  h295c915_0  
libdeflate                1.8                  h7f8727e_5  
libffi                    3.3                  he6710b0_2  
libgcc-ng                 11.2.0               h1234567_1  
libgomp                   11.2.0               h1234567_1  
libiconv                  1.16                 h7f8727e_2  
libidn2                   2.3.2                h7f8727e_0  
libpng                    1.6.37               hbc83047_0  
libstdcxx-ng              11.2.0               h1234567_1  
libtasn1                  4.16.0               h27cfd23_0  
libtiff                   4.4.0                hecacb30_1  
libunistring              0.9.10               h27cfd23_0  
libuv                     1.40.0               h7b6447c_0  
libwebp-base              1.2.4                h5eee18b_0  
lz4-c                     1.9.3                h295c915_1  
mkl                       2020.2                      256  
mkl-service               2.3.0            py36he8ac12f_0  
mkl_fft                   1.3.0            py36h54f3939_0  
mkl_random                1.1.1            py36h0573a6f_0  
ncurses                   6.3                  h5eee18b_3  
nettle                    3.7.3                hbbd107a_1  
numpy                     1.19.2           py36h54aff64_0  
numpy-base                1.19.2           py36hfa32c7d_0  
olefile                   0.46                     py36_0  
openh264                  2.1.1                h4ff587b_0  
openjpeg                  2.4.0                h3ad879b_0  
openssl                   1.1.1s               h7f8727e_0  
pillow                    8.3.1            py36h2c7a002_0  
pip                       21.2.2           py36h06a4308_0  
python                    3.6.13               h12debd9_1  
pytorch                   1.10.1          py3.6_cuda10.2_cudnn7.6.5_0    pytorch
pytorch-mutex             1.0                        cuda    pytorch
readline                  8.2                  h5eee18b_0  
setuptools                58.0.4           py36h06a4308_0  
six                       1.16.0             pyhd3eb1b0_1  
sqlite                    3.39.3               h5082296_0  
tk                        8.6.12               h1ccaba5_0  
torch                     1.10.0+cu102             pypi_0    pypi
torchaudio                0.10.1               py36_cu102    pytorch
torchvision               0.11.2               py36_cu102    pytorch
typing_extensions         4.1.1              pyh06a4308_0  
wheel                     0.37.1             pyhd3eb1b0_0  
xz                        5.2.6                h5eee18b_0  
zlib                      1.2.13               h5eee18b_0  
zstd                      1.5.2                ha4553b6_0  
(env_point_net) dhankar@dhankar-1:~/.../iou3d$ 

```

#
<br>


- Suggestions from - detectron2 -issues -- https://github.com/facebookresearch/detectron2/issues/4343 - https://download.pytorch.org/whl/cu116


#
<br>


```bash

(env_point_net) dhankar@dhankar-1:~/.../iou3d$ 
(env_point_net) dhankar@dhankar-1:~/.../iou3d$ python setup.py install
--torch.cuda.is_available()-----
 True
running install
running bdist_egg
running egg_info
writing iou3d.egg-info/PKG-INFO
writing dependency_links to iou3d.egg-info/dependency_links.txt
writing top-level names to iou3d.egg-info/top_level.txt
/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/torch/utils/cpp_extension.py:381: UserWarning: Attempted to use ninja as the BuildExtension backend but we could not find ninja.. Falling back to using the slow distutils backend.
  warnings.warn(msg.format('we could not find ninja.'))
reading manifest file 'iou3d.egg-info/SOURCES.txt'
writing manifest file 'iou3d.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_ext
Traceback (most recent call last):
  File "setup.py", line 20, in <module>
    cmdclass={'build_ext': BuildExtension})
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/__init__.py", line 153, in setup
    return distutils.core.setup(**attrs)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/core.py", line 148, in setup
    dist.run_commands()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 955, in run_commands
    self.run_command(cmd)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/install.py", line 67, in run
    self.do_egg_install()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/install.py", line 109, in do_egg_install
    self.run_command('bdist_egg')
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/bdist_egg.py", line 164, in run
    cmd = self.call_command('install_lib', warn_dir=0)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/bdist_egg.py", line 150, in call_command
    self.run_command(cmdname)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/install_lib.py", line 11, in run
    self.build()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/command/install_lib.py", line 107, in build
    self.run_command('build_ext')
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/build_ext.py", line 79, in run
    _build_ext.run(self)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/command/build_ext.py", line 339, in run
    self.build_extensions()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/torch/utils/cpp_extension.py", line 404, in build_extensions
    self._check_cuda_version()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/torch/utils/cpp_extension.py", line 781, in _check_cuda_version
    raise RuntimeError(CUDA_MISMATCH_MESSAGE.format(cuda_str_version, torch.version.cuda))
RuntimeError: 
The detected CUDA version (11.0) mismatches the version that was used to compile
PyTorch (10.2). Please make sure to use the same CUDA versions.

(env_point_net) dhankar@dhankar-1:~/.../iou3d$ 
```


#
<br>




```bash

(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ conda remove pytorch torchvision cudatoolkit
Collecting package metadata (repodata.json): done
Solving environment: failed

PackagesNotFoundError: The following packages are missing from the target environment:
  - cudatoolkit
  - pytorch
  - torchvision


(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ 
(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ conda install pytorch==1.10.1 torchvision==0.11.2 torchaudio==0.10.1 cudatoolkit=10.2 -c pytorch
Collecting package metadata (current_repodata.json): done
Solving environment: failed with initial frozen solve. Retrying with flexible solve.
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/dhankar/anaconda3/envs/env_point_net

  added / updated specs:
    - cudatoolkit=10.2
    - pytorch==1.10.1
    - torchaudio==0.10.1
    - torchvision==0.11.2


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    pytorch-1.10.1             |py3.6_cuda10.2_cudnn7.6.5_0       768.8 MB  pytorch
    torchaudio-0.10.1          |       py36_cu102         4.5 MB  pytorch
    torchvision-0.11.2         |       py36_cu102        30.0 MB  pytorch
    ------------------------------------------------------------
                                           Total:       803.3 MB

The following NEW packages will be INSTALLED:

  blas               pkgs/main/linux-64::blas-1.0-mkl None
  bzip2              pkgs/main/linux-64::bzip2-1.0.8-h7b6447c_0 None
  cudatoolkit        pkgs/main/linux-64::cudatoolkit-10.2.89-hfd86e86_1 None
  dataclasses        pkgs/main/noarch::dataclasses-0.8-pyh4f3eec9_6 None
  ffmpeg             pytorch/linux-64::ffmpeg-4.3-hf484d3e_0 None
  freetype           pkgs/main/linux-64::freetype-2.12.1-h4a9f257_0 None
  gmp                pkgs/main/linux-64::gmp-6.2.1-h295c915_3 None
  gnutls             pkgs/main/linux-64::gnutls-3.6.15-he1e5248_0 None
  intel-openmp       pkgs/main/linux-64::intel-openmp-2022.1.0-h9e868ea_3769 None
  jpeg               pkgs/main/linux-64::jpeg-9e-h7f8727e_0 None
  lame               pkgs/main/linux-64::lame-3.100-h7b6447c_0 None
  lcms2              pkgs/main/linux-64::lcms2-2.12-h3be6417_0 None
  lerc               pkgs/main/linux-64::lerc-3.0-h295c915_0 None
  libdeflate         pkgs/main/linux-64::libdeflate-1.8-h7f8727e_5 None
  libiconv           pkgs/main/linux-64::libiconv-1.16-h7f8727e_2 None
  libidn2            pkgs/main/linux-64::libidn2-2.3.2-h7f8727e_0 None
  libpng             pkgs/main/linux-64::libpng-1.6.37-hbc83047_0 None
  libtasn1           pkgs/main/linux-64::libtasn1-4.16.0-h27cfd23_0 None
  libtiff            pkgs/main/linux-64::libtiff-4.4.0-hecacb30_1 None
  libunistring       pkgs/main/linux-64::libunistring-0.9.10-h27cfd23_0 None
  libuv              pkgs/main/linux-64::libuv-1.40.0-h7b6447c_0 None
  libwebp-base       pkgs/main/linux-64::libwebp-base-1.2.4-h5eee18b_0 None
  lz4-c              pkgs/main/linux-64::lz4-c-1.9.3-h295c915_1 None
  mkl                pkgs/main/linux-64::mkl-2020.2-256 None
  mkl-service        pkgs/main/linux-64::mkl-service-2.3.0-py36he8ac12f_0 None
  mkl_fft            pkgs/main/linux-64::mkl_fft-1.3.0-py36h54f3939_0 None
  mkl_random         pkgs/main/linux-64::mkl_random-1.1.1-py36h0573a6f_0 None
  nettle             pkgs/main/linux-64::nettle-3.7.3-hbbd107a_1 None
  numpy              pkgs/main/linux-64::numpy-1.19.2-py36h54aff64_0 None
  numpy-base         pkgs/main/linux-64::numpy-base-1.19.2-py36hfa32c7d_0 None
  olefile            pkgs/main/linux-64::olefile-0.46-py36_0 None
  openh264           pkgs/main/linux-64::openh264-2.1.1-h4ff587b_0 None
  openjpeg           pkgs/main/linux-64::openjpeg-2.4.0-h3ad879b_0 None
  pillow             pkgs/main/linux-64::pillow-8.3.1-py36h2c7a002_0 None
  pytorch            pytorch/linux-64::pytorch-1.10.1-py3.6_cuda10.2_cudnn7.6.5_0 None
  pytorch-mutex      pytorch/noarch::pytorch-mutex-1.0-cuda None
  six                pkgs/main/noarch::six-1.16.0-pyhd3eb1b0_1 None
  torchaudio         pytorch/linux-64::torchaudio-0.10.1-py36_cu102 None
  torchvision        pytorch/linux-64::torchvision-0.11.2-py36_cu102 None
  typing_extensions  pkgs/main/noarch::typing_extensions-4.1.1-pyh06a4308_0 None
  zstd               pkgs/main/linux-64::zstd-1.5.2-ha4553b6_0 None


Proceed ([y]/n)? y


Downloading and Extracting Packages
pytorch-1.10.1       | 768.8 MB  | ################################################################################################### | 100% 
torchaudio-0.10.1    | 4.5 MB    | ################################################################################################### | 100% 
torchvision-0.11.2   | 30.0 MB   | ################################################################################################### | 100% 
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
Retrieving notices: ...working... done
(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ 
(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ 
```




#
<br>


```bash
(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ conda install pytorch==1.10.0 torchvision==0.10.0 torchaudio==0.10.0 cudatoolkit=10.2 -c pytorch
Collecting package metadata (current_repodata.json): done
Solving environment: failed with initial frozen solve. Retrying with flexible solve.
Collecting package metadata (repodata.json): done
Solving environment: failed with initial frozen solve. Retrying with flexible solve.
Solving environment: / 
Found conflicts! Looking for incompatible packages.
This can take several minutes.  Press CTRL-C to abort.
failed                                                                                                                                        

UnsatisfiableError: The following specifications were found
to be incompatible with the existing python installation in your environment:

Specifications:

  - torchaudio==0.10.0 -> python[version='>=2.7,<2.8.0a0|>=3.10,<3.11.0a0|>=3.5,<3.6.0a0']
  - torchvision==0.10.0 -> python[version='>=2.7,<2.8.0a0|>=3.10,<3.11.0a0']

Your python: python=3.6

If python is on the left-most side of the chain, that's the version you've asked for.
When python appears to the right, that indicates that the thing on the left is somehow
not available for the python version you are constrained to. Note that conda will not
change your python version to a different minor version unless you explicitly specify
that.

The following specifications were found to be incompatible with each other:

Output in format: Requested package -> Available versions

Package _libgcc_mutex conflicts for:
python=3.6 -> libgcc-ng[version='>=7.5.0'] -> _libgcc_mutex[version='*|0.1',build=main]
cudatoolkit=10.2 -> libgcc-ng[version='>=7.3.0'] -> _libgcc_mutex[version='*|0.1',build=main]

Package libgcc-ng conflicts for:
python=3.6 -> libgcc-ng[version='>=7.2.0|>=7.3.0|>=7.5.0']
torchaudio==0.10.0 -> numpy[version='>=1.11'] -> libgcc-ng[version='>=11.2.0|>=7.5.0|>=7.3.0|>=7.2.0|>=9.3.0']
pytorch==1.10.0 -> cudatoolkit[version='>=11.3,<11.4'] -> libgcc-ng[version='>=11.2.0|>=7.3.0|>=9.3.0|>=7.5.0|>=7.2.0']
torchvision==0.10.0 -> ffmpeg[version='>=4.2'] -> libgcc-ng[version='>=11.2.0|>=7.2.0|>=7.3.0|>=7.5.0|>=8.4.0']
cudatoolkit=10.2 -> libgcc-ng[version='>=7.3.0']
python=3.6 -> ncurses[version='>=6.2,<7.0a0'] -> libgcc-ng[version='>=11.2.0']

Package pytorch conflicts for:
torchaudio==0.10.0 -> pytorch==1.10.0
torchvision==0.10.0 -> pytorch==1.9.0

Package cudatoolkit conflicts for:
torchvision==0.10.0 -> cudatoolkit[version='>=10.2,<10.3|>=11.1,<11.2']
torchaudio==0.10.0 -> cudatoolkit[version='>=10.2,<10.3|>=11.1,<11.2|>=11.3,<11.4']

Package pytorch-mutex conflicts for:
pytorch==1.10.0 -> pytorch-mutex==1.0[build='cuda|cpu']
torchaudio==0.10.0 -> pytorch==1.10.0 -> pytorch-mutex==1.0[build='cuda|cpu']The following specifications were found to be incompatible with your system:

  - feature:/linux-64::__glibc==2.27=0
  - feature:|@/linux-64::__glibc==2.27=0
  - cudatoolkit=10.2 -> libgcc-ng[version='>=7.3.0'] -> __glibc[version='>=2.17']
  - python=3.6 -> libgcc-ng[version='>=7.5.0'] -> __glibc[version='>=2.17']

Your installed version is: 2.27


(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ 

```


#
<br>



#### Removed the - using conda remove --- Now to install using PIP and not CONDA , but within thw CONDA ENV 

- https://www.anaconda.com/blog/using-pip-in-a-conda-environment


#
<br>

- conda remove pytorch torchvision cudatoolkit

```bash

(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ conda remove pytorch torchvision cudatoolkit
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/dhankar/anaconda3/envs/env_point_net

  removed specs:
    - cudatoolkit
    - pytorch
    - torchvision


The following packages will be REMOVED:

  blas-1.0-mkl
  bzip2-1.0.8-h7b6447c_0
  cudatoolkit-10.2.89-hfd86e86_1
  dataclasses-0.8-pyh4f3eec9_6
  ffmpeg-4.3-hf484d3e_0
  freetype-2.12.1-h4a9f257_0
  gmp-6.2.1-h295c915_3
  gnutls-3.6.15-he1e5248_0
  intel-openmp-2022.1.0-h9e868ea_3769
  jpeg-9e-h7f8727e_0
  lame-3.100-h7b6447c_0
  lcms2-2.12-h3be6417_0
  lerc-3.0-h295c915_0
  libdeflate-1.8-h7f8727e_5
  libiconv-1.16-h7f8727e_2
  libidn2-2.3.2-h7f8727e_0
  libpng-1.6.37-hbc83047_0
  libtasn1-4.16.0-h27cfd23_0
  libtiff-4.4.0-hecacb30_1
  libunistring-0.9.10-h27cfd23_0
  libuv-1.40.0-h7b6447c_0
  libwebp-base-1.2.4-h5eee18b_0
  lz4-c-1.9.3-h295c915_1
  mkl-2020.2-256
  mkl-service-2.3.0-py36he8ac12f_0
  mkl_fft-1.3.0-py36h54f3939_0
  mkl_random-1.1.1-py36h0573a6f_0
  nettle-3.7.3-hbbd107a_1
  numpy-1.19.2-py36h54aff64_0
  numpy-base-1.19.2-py36hfa32c7d_0
  olefile-0.46-py36_0
  openh264-2.1.1-h4ff587b_0
  openjpeg-2.4.0-h3ad879b_0
  pillow-8.3.1-py36h2c7a002_0
  pytorch-1.10.2-py3.6_cuda10.2_cudnn7.6.5_0
  pytorch-mutex-1.0-cuda
  six-1.16.0-pyhd3eb1b0_1
  torchaudio-0.10.2-py36_cu102
  torchvision-0.11.3-py36_cu102
  typing_extensions-4.1.1-pyh06a4308_0
  zstd-1.5.2-ha4553b6_0


Proceed ([y]/n)? y

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
(env_point_net) dhankar@dhankar-1:~/.../PointRCNN$ 
```

#
<br>


#### dpkg --help -- for Later Refrence 

```bash
$ dpkg --help
Usage: dpkg [<option> ...] <command>

Commands:
  -i|--install       <.deb file name> ... | -R|--recursive <directory> ...
  --unpack           <.deb file name> ... | -R|--recursive <directory> ...
  -A|--record-avail  <.deb file name> ... | -R|--recursive <directory> ...
  --configure        <package> ... | -a|--pending
  --triggers-only    <package> ... | -a|--pending
  -r|--remove        <package> ... | -a|--pending
  -P|--purge         <package> ... | -a|--pending
  -V|--verify <package> ...        Verify the integrity of package(s).
  --get-selections [<pattern> ...] Get list of selections to stdout.
  --set-selections                 Set package selections from stdin.
  --clear-selections               Deselect every non-essential package.
  --update-avail [<Packages-file>] Replace available packages info.
  --merge-avail [<Packages-file>]  Merge with info from file.
  --clear-avail                    Erase existing available info.
  --forget-old-unavail             Forget uninstalled unavailable pkgs.
  -s|--status <package> ...        Display package status details.
  -p|--print-avail <package> ...   Display available version details.
  -L|--listfiles <package> ...     List files 'owned' by package(s).
  -l|--list [<pattern> ...]        List packages concisely.
  -S|--search <pattern> ...        Find package(s) owning file(s).
  -C|--audit [<package> ...]       Check for broken package(s).
  --yet-to-unpack                  Print packages selected for installation.
  --predep-package                 Print pre-dependencies to unpack.
  --add-architecture <arch>        Add <arch> to the list of architectures.
  --remove-architecture <arch>     Remove <arch> from the list of architectures.
  --print-architecture             Print dpkg architecture.
  --print-foreign-architectures    Print allowed foreign architectures.
  --assert-<feature>               Assert support for the specified feature.
  --validate-<thing> <string>      Validate a <thing>'s <string>.
  --compare-versions <a> <op> <b>  Compare version numbers - see below.
  --force-help                     Show help on forcing.
  -Dh|--debug=help                 Show help on debugging.

  -?, --help                       Show this help message.
      --version                    Show the version.

Assertable features: support-predepends, working-epoch, long-filenames,
  multi-conrep, multi-arch, versioned-provides.

Validatable things: pkgname, archname, trigname, version.

Use dpkg with -b, --build, -c, --contents, -e, --control, -I, --info,
  -f, --field, -x, --extract, -X, --vextract, --ctrl-tarfile, --fsys-tarfile
on archives (type dpkg-deb --help).

Options:
  --admindir=<directory>     Use <directory> instead of /var/lib/dpkg.
  --root=<directory>         Install on a different root directory.
  --instdir=<directory>      Change installation dir without changing admin dir.
  --path-exclude=<pattern>   Do not install paths which match a shell pattern.
  --path-include=<pattern>   Re-include a pattern after a previous exclusion.
  -O|--selected-only         Skip packages not selected for install/upgrade.
  -E|--skip-same-version     Skip packages whose same version is installed.
  -G|--refuse-downgrade      Skip packages with earlier version than installed.
  -B|--auto-deconfigure      Install even if it would break some other package.
  --[no-]triggers            Skip or force consequential trigger processing.
  --verify-format=<format>   Verify output format (supported: 'rpm').
  --no-debsig                Do not try to verify package signatures.
  --no-act|--dry-run|--simulate
                             Just say what we would do - don't do it.
  -D|--debug=<octal>         Enable debugging (see -Dhelp or --debug=help).
  --status-fd <n>            Send status change updates to file descriptor <n>.
  --status-logger=<command>  Send status change updates to <command>'s stdin.
  --log=<filename>           Log status changes and actions to <filename>.
  --ignore-depends=<package>,...
                             Ignore dependencies involving <package>.
  --force-...                Override problems (see --force-help).
  --no-force-...|--refuse-...
                             Stop when problems encountered.
  --abort-after <n>          Abort after encountering <n> errors.

Comparison operators for --compare-versions are:
  lt le eq ne ge gt       (treat empty version as earlier than any version);
  lt-nl le-nl ge-nl gt-nl (treat empty version as later than any version);
  < << <= = >= >> >       (only for compatibility with control file syntax).

Use 'apt' or 'aptitude' for user-friendly package management.
(base) dhankar@dhankar-1:.../local$ 

```


#### Install of the deb(local) gives errors -- thus trying the RUNFILE - runfile(local)

- Basis this ANSWER -- https://forums.developer.nvidia.com/t/cannot-install-cuda-11-x-on-amd64-ubuntu-18-04-depends-cuda-11-3-11-3-1-but-it-is-not-going-to-be-installed/181108

- https://developer.nvidia.com/cuda-10.2-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1804&target_type=runfilelocal

- sudo sh cuda_10.2.89_440.33.01_linux.run

```bash

$ wget https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda_10.2.89_440.33.01_linux.run
--2022-11-09 20:00:09--  https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda_10.2.89_440.33.01_linux.run
Resolving developer.download.nvidia.com (developer.download.nvidia.com)... 152.199.39.144
Connecting to developer.download.nvidia.com (developer.download.nvidia.com)|152.199.39.144|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2645419389 (2.5G) [application/octet-stream]
Saving to: ‘cuda_10.2.89_440.33.01_linux.run’

cuda_10.2.89_440.33.01_linux.run    100%[=================================================================>]   2.46G  27.7MB/s    in 92s     

2022-11-09 20:01:41 (27.3 MB/s) - ‘cuda_10.2.89_440.33.01_linux.run’ saved [2645419389/2645419389]

```


#### ERRORS --- FAILS --->> CUDA Toolkit 10.2 Download

```bash

Err:8 https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  InRelease                                                  
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY A4B469963BF863CC


```


#### CUDA Toolkit 10.2 Download

- https://developer.nvidia.com/cuda-10.2-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1804&target_type=deblocal

> Base installer is available for download below.
There are 2 patches available. These patches require the base installer to be installed first.

Base Installer 	
Installation Instructions:

#
<br>


```bash
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin 

sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600

wget https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb

sudo dpkg -i cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb

sudo apt-key add /var/cuda-repo-10-2-local-10.2.89-440.33.01/7fa2af80.pub

sudo apt-get update

sudo apt-get -y install cuda

```
#
<br>

```bash

$ wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin
--2022-11-08 23:21:51--  https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin
Resolving developer.download.nvidia.com (developer.download.nvidia.com)... 152.199.39.144
Connecting to developer.download.nvidia.com (developer.download.nvidia.com)|152.199.39.144|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 190 [application/octet-stream]
Saving to: ‘cuda-ubuntu1804.pin’

cuda-ubuntu1804.pin                 100%[=================================================================>]     190  --.-KB/s    in 0s      

2022-11-08 23:21:51 (5.71 MB/s) - ‘cuda-ubuntu1804.pin’ saved [190/190]

#
$ wget https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb
--2022-11-08 23:22:57--  https://developer.download.nvidia.com/compute/cuda/10.2/Prod/local_installers/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb
Resolving developer.download.nvidia.com (developer.download.nvidia.com)... 152.199.39.144
Connecting to developer.download.nvidia.com (developer.download.nvidia.com)|152.199.39.144|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1896270068 (1.8G) [application/x-deb]
Saving to: ‘cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb’

cuda-repo-ubuntu1804-10-2-local-10. 100%[=================================================================>]   1.77G  27.9MB/s    in 65s     

2022-11-08 23:24:02 (27.9 MB/s) - ‘cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb’ saved [1896270068/1896270068]

#

mv /home/dhankar/temp/11_22/own_fork_PointRCNN/PointRCNN/cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb /home/dhankar/temp/11_22/

#

$ sudo dpkg -i cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb
Selecting previously unselected package cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01.
(Reading database ... 973202 files and directories currently installed.)
Preparing to unpack cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01_1.0-1_amd64.deb ...
Unpacking cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01 (1.0-1) ...
Setting up cuda-repo-ubuntu1804-10-2-local-10.2.89-440.33.01 (1.0-1) ...


#

$ sudo apt-get -y install cuda
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Some packages could not be installed. This may mean that you have
requested an impossible situation or if you are using the unstable
distribution that some required packages have not yet been created
or been moved out of Incoming.
The following information may help to resolve the situation:

The following packages have unmet dependencies:
 cuda : Depends: cuda-11-6 (>= 11.6.2) but it is not going to be installed
E: Unable to correct problems, you have held broken packages.


```

##### Need to install with RUNFILE -- as the deb(local) - fails with - unmet dependencies ? 
- https://forums.developer.nvidia.com/t/cannot-install-cuda-11-x-on-amd64-ubuntu-18-04-depends-cuda-11-3-11-3-1-but-it-is-not-going-to-be-installed/181108


```bash

(base) dhankar@dhankar-1:~/.../11_22$ 
(base) dhankar@dhankar-1:~/.../11_22$ sudo apt-key add /var/cuda-repo-10-2-local-10.2.89-440.33.01/7fa2af80.pub
OK
(base) dhankar@dhankar-1:~/.../11_22$ 
(base) dhankar@dhankar-1:~/.../11_22$ sudo apt-get update
Get:1 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  InRelease
Ign:1 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  InRelease
Get:2 file:/var/cuda-repo-ubuntu1804-11-0-local  InRelease
Ign:2 file:/var/cuda-repo-ubuntu1804-11-0-local  InRelease
Get:3 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  Release [574 B]
Get:4 file:/var/cuda-repo-ubuntu1804-11-0-local  Release [564 B]
Get:3 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  Release [574 B]
Get:4 file:/var/cuda-repo-ubuntu1804-11-0-local  Release [564 B] 
Get:5 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  Release.gpg [833 B]
Get:5 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  Release.gpg [833 B]
Hit:7 https://dl.winehq.org/wine-builds/ubuntu bionic InRelease                                                                              
Get:8 https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  InRelease [1,581 B]                                        
Get:9 file:/var/cuda-repo-10-2-local-10.2.89-440.33.01  Packages [23.8 kB]                                                                   
Get:10 http://dl.google.com/linux/chrome/deb stable InRelease [1,811 B]                                                                      
Ign:11 http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.4 InRelease                                                                   
Ign:12 https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 InRelease                 

Err:8 https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  InRelease                                                  
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY A4B469963BF863CC


Ign:14 https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.4 InRelease                                                                  
Hit:15 http://ppa.launchpad.net/alexlarsson/flatpak/ubuntu bionic InRelease                                                                  
Hit:16 https://download.docker.com/linux/ubuntu bionic InRelease                                                                             
Ign:17 http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64  InRelease                                      
Hit:18 http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64  Release                                        
Err:10 http://dl.google.com/linux/chrome/deb stable InRelease                                                                                
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 4EB27DB2A3B88B8B
Hit:19 http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.4 Release                                                                     
Hit:21 http://ppa.launchpad.net/apandada1/brightness-controller/ubuntu bionic InRelease                                                      
Hit:22 http://packages.microsoft.com/repos/code stable InRelease                                                                             
Hit:23 https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 Release                                                                    
Ign:24 https://kx.studio/repo stable InRelease                                                                                               
Hit:25 https://cloud.r-project.org/bin/linux/ubuntu bionic-cran40/ InRelease                                                                 
Hit:26 http://in.archive.ubuntu.com/ubuntu bionic InRelease                                                                                  
Hit:27 http://ppa.launchpad.net/cybermax-dexter/sdl2-backport/ubuntu bionic InRelease                                                        
Hit:28 https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.4 Release                                                                    
Ign:30 https://kx.studio/repo gcc5 InRelease                                                                                                 
Get:31 http://security.ubuntu.com/ubuntu bionic-security InRelease [88.7 kB]                                                                 
Get:33 http://in.archive.ubuntu.com/ubuntu bionic-updates InRelease [88.7 kB]                                                                
Hit:35 https://kx.studio/repo stable Release                                                                                                 
Hit:36 http://ppa.launchpad.net/kxstudio-debian/libs/ubuntu bionic InRelease                                                                 
Hit:37 https://kx.studio/repo gcc5 Release                                                                                                   
Get:41 http://ppa.launchpad.net/kxstudio-debian/plugins/ubuntu bionic InRelease [15.4 kB]                                                    
Hit:42 https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/bionic pgadmin4 InRelease                                                         
Get:43 https://repo.skype.com/deb stable InRelease [4,502 B]                                                                                 
Get:40 http://packages.ros.org/ros/ubuntu bionic InRelease [4,680 B]                                                                         
Get:45 http://in.archive.ubuntu.com/ubuntu bionic-backports InRelease [83.3 kB]                                                              
Hit:46 http://ppa.launchpad.net/kxstudio-debian/apps/ubuntu bionic InRelease                                                                 
Hit:47 http://ppa.launchpad.net/kxstudio-debian/kxstudio/ubuntu bionic InRelease                                                             
Hit:49 http://ppa.launchpad.net/mixxx/mixxx/ubuntu bionic InRelease                                                                          
Hit:51 https://repo.fortinet.com/repo/ubuntu /bionic InRelease                                                                               
Hit:52 http://ppa.launchpad.net/ubuntugis/ubuntugis-unstable/ubuntu bionic InRelease                                                         
Get:39 http://ppa.launchpad.net/kxstudio-debian/music/ubuntu bionic InRelease [15.4 kB]                
Hit:55 https://packages.microsoft.com/repos/ms-teams stable InRelease                                                 
Get:56 http://security.ubuntu.com/ubuntu bionic-security/main amd64 Packages [2,449 kB]
Err:43 https://repo.skype.com/deb stable InRelease                                                                 
  The following signatures were invalid: EXPKEYSIG 1F3045A5DF7587C3 Skype Linux Client Repository <se-um@microsoft.com>
Err:40 http://packages.ros.org/ros/ubuntu bionic InRelease                                                         
  The following signatures were invalid: EXPKEYSIG F42ED6FBAB17C654 Open Robotics <info@osrfoundation.org>
Get:57 http://security.ubuntu.com/ubuntu bionic-security/main i386 Packages [1,264 kB]                                                       
Get:58 http://security.ubuntu.com/ubuntu bionic-security/main Translation-en [424 kB]                                                        
Get:59 http://security.ubuntu.com/ubuntu bionic-security/main amd64 DEP-11 Metadata [55.3 kB]                                                
Get:60 http://security.ubuntu.com/ubuntu bionic-security/universe i386 Packages [1,039 kB]                                                   
Get:61 http://in.archive.ubuntu.com/ubuntu bionic-updates/main i386 Packages [1,562 kB]                                                      
Get:62 http://security.ubuntu.com/ubuntu bionic-security/universe amd64 Packages [1,238 kB]                                                  
Get:63 http://security.ubuntu.com/ubuntu bionic-security/universe amd64 DEP-11 Metadata [61.1 kB]                                            
Get:64 http://security.ubuntu.com/ubuntu bionic-security/multiverse amd64 DEP-11 Metadata [2,464 B]                                          
Get:65 http://in.archive.ubuntu.com/ubuntu bionic-updates/main amd64 Packages [2,790 kB]                                                     
Get:66 http://in.archive.ubuntu.com/ubuntu bionic-updates/main Translation-en [513 kB]                                                       
Get:67 http://in.archive.ubuntu.com/ubuntu bionic-updates/main amd64 DEP-11 Metadata [297 kB]                                                
Get:68 http://in.archive.ubuntu.com/ubuntu bionic-updates/universe i386 Packages [1,630 kB]                                                  
Get:69 http://in.archive.ubuntu.com/ubuntu bionic-updates/universe amd64 Packages [1,853 kB]                                                 
Get:70 http://in.archive.ubuntu.com/ubuntu bionic-updates/universe amd64 DEP-11 Metadata [302 kB]                                            
Get:71 http://in.archive.ubuntu.com/ubuntu bionic-updates/multiverse amd64 DEP-11 Metadata [2,468 B]                                         
Get:72 http://in.archive.ubuntu.com/ubuntu bionic-backports/main amd64 DEP-11 Metadata [8,136 B]                                             
Get:73 http://in.archive.ubuntu.com/ubuntu bionic-backports/universe amd64 DEP-11 Metadata [10.0 kB]                                         
Hit:32 https://scala.jfrog.io/artifactory/debian all InRelease                                                                               
Ign:38 https://scala.jfrog.io/artifactory/debian  InRelease                                                                                  
Get:74 https://deb.torproject.org/torproject.org bionic InRelease [3,524 B]                                                                  
Err:74 https://deb.torproject.org/torproject.org bionic InRelease                                                                            
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 74A941BA219EC810
Hit:53 https://packagecloud.io/slacktechnologies/slack/debian jessie InRelease                                                               
Get:13 https://ubuntugis.qgis.org/ubuntugis bionic InRelease [3,673 B]                                                                       
Err:13 https://ubuntugis.qgis.org/ubuntugis bionic InRelease                                                                                 
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D155B8E6A419C5BE
Get:20 https://ubuntu.qgis.org/ubuntu bionic InRelease [3,673 B]                                                                             
Err:20 https://ubuntu.qgis.org/ubuntu bionic InRelease                                                                                       
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D155B8E6A419C5BE
Hit:75 https://scala.jfrog.io/artifactory/debian  Release                                                                                    
Reading package lists... Done                                         


W: GPG error: https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY A4B469963BF863CC
E: The repository 'https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64  InRelease' is no longer signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.


W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: http://dl.google.com/linux/chrome/deb stable InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 4EB27DB2A3B88B8B


W: Target Packages (stable/binary-amd64/Packages) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Packages (stable/binary-all/Packages) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Translations (stable/i18n/Translation-en_IN) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Translations (stable/i18n/Translation-en) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11 (stable/dep11/Components-amd64.yml) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11 (stable/dep11/Components-all.yml) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11-icons-small (stable/dep11/icons-48x48.tar) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11-icons (stable/dep11/icons-64x64.tar) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target CNF (stable/cnf/Commands-amd64) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target CNF (stable/cnf/Commands-all) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: https://repo.skype.com/deb stable InRelease: The following signatures were invalid: EXPKEYSIG 1F3045A5DF7587C3 Skype Linux Client Repository <se-um@microsoft.com>
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: http://packages.ros.org/ros/ubuntu bionic InRelease: The following signatures were invalid: EXPKEYSIG F42ED6FBAB17C654 Open Robotics <info@osrfoundation.org>
E: Repository 'http://ppa.launchpad.net/kxstudio-debian/music/ubuntu bionic InRelease' changed its 'Label' value from 'Music' to 'Deprecated'
N: This must be accepted explicitly before updates for this repository can be applied. See apt-secure(8) manpage for details.
W: GPG error: https://deb.torproject.org/torproject.org bionic InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 74A941BA219EC810
E: The repository 'https://deb.torproject.org/torproject.org bionic InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: https://ubuntugis.qgis.org/ubuntugis bionic InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D155B8E6A419C5BE
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: https://ubuntu.qgis.org/ubuntu bionic InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY D155B8E6A419C5BE
W: Target Packages (stable/binary-amd64/Packages) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Packages (stable/binary-all/Packages) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Translations (stable/i18n/Translation-en_IN) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target Translations (stable/i18n/Translation-en) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11 (stable/dep11/Components-amd64.yml) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11 (stable/dep11/Components-all.yml) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11-icons-small (stable/dep11/icons-48x48.tar) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target DEP-11-icons (stable/dep11/icons-64x64.tar) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target CNF (stable/cnf/Commands-amd64) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
W: Target CNF (stable/cnf/Commands-all) is configured multiple times in /etc/apt/sources.list:61 and /etc/apt/sources.list.d/docker.list:1
(base) dhankar@dhankar-1:~/.../11_22$ 
(base) dhankar@dhankar-1:~/.../11_22$ sudo apt-get -y install cuda
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Some packages could not be installed. This may mean that you have
requested an impossible situation or if you are using the unstable
distribution that some required packages have not yet been created
or been moved out of Incoming.
The following information may help to resolve the situation:

The following packages have unmet dependencies:
 cuda : Depends: cuda-11-6 (>= 11.6.2) but it is not going to be installed
E: Unable to correct problems, you have held broken packages.
(base) dhankar@dhankar-1:~/.../11_22$ 
(base) dhankar@dhankar-1:~/.../11_22$ 


```

> Patch 1 (Released Aug 26, 2020) 	This patch fixes an issue in the cuBLAS library bundled in CUDA 10.2 which caused silent corruption of data in uncommon e


#
<br>



```bash
lspci | grep -i nvidia
(env_point_net) dhankar@dhankar-1:.../local$ lspci | grep -i nvidia
01:00.0 VGA compatible controller: NVIDIA Corporation Device 1f82 (rev a1)
01:00.1 Audio device: NVIDIA Corporation Device 10fa (rev a1)
(env_point_net) dhankar@dhankar-1:.../local$ 

#
(env_point_net) dhankar@dhankar-1:.../local$ uname -m && cat /etc/*release
x86_64
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=18.04
DISTRIB_CODENAME=bionic
DISTRIB_DESCRIPTION="Ubuntu 18.04.5 LTS"
NAME="Ubuntu"
VERSION="18.04.5 LTS (Bionic Beaver)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 18.04.5 LTS"
VERSION_ID="18.04"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=bionic
UBUNTU_CODENAME=bionic
(env_point_net) dhankar@dhankar-1:.../local$ 
#
gcc --version
gcc (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.0
Copyright (C) 2017 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
#
uname -r
5.4.0-131-generic
#

```

##### Not done any UN-INSTALL 


```python
Use the following command to uninstall a Toolkit runfile installation:

sudo /usr/local/cuda-X.Y/bin/cuda-uninstaller

Use the following command to uninstall a Driver runfile installation:

sudo /usr/bin/nvidia-uninstall
```


- lrwxrwxrwx  1 root    root       9 Jul 25  2020 cuda -> cuda-11.0

```bash
(env_point_net) dhankar@dhankar-1:~/.../iou3d$ cd /usr/local/
(env_point_net) dhankar@dhankar-1:.../local$ 
(env_point_net) dhankar@dhankar-1:.../local$ ls -lahtr
total 355M
drwxr-xr-x  2 root    root    4.0K Aug  6  2019 src
drwxr-xr-x  2 root    root    4.0K Aug  6  2019 sbin
drwxr-xr-x  2 root    root    4.0K Aug  6  2019 games
drwxr-xr-x  4 root    root    4.0K Apr 17  2020 etc
drwxr-xr-x  3 root    root    4.0K Jul  4  2020 aws-cli
drwxr-xr-x 15 root    root    4.0K Jul 25  2020 cuda-11.0
lrwxrwxrwx  1 root    root       9 Jul 25  2020 cuda -> cuda-11.0
drwxr-xr-x  4 root    root    4.0K Jul 30  2020 man
drwxr-xr-x  4 root    root    4.0K Jul 30  2020 doc
drwxr-xr-x 19 root    root    4.0K Jul 30  2020 share
drwxr-xr-x  3 root    root    4.0K Jul 30  2020 include
drwxr-xr-x  7 root    root     12K Aug  4  2020 lib
drwxr-xr-x 10 root    root    4.0K Dec  3  2020 go
-rw-rw-r--  1 dhankar dhankar 355M Jan 12  2021 go1.15.6.linux-amd64.tar
drwxr-xr-x 15 root    root    4.0K Jan 12  2021 .
drwxr-xr-x 13 root    root    4.0K Feb 14  2021 ..
drwxr-xr-x  2 root    root    4.0K Mar 12  2022 bin
(env_point_net) dhankar@dhankar-1:.../local$ 
(env_point_net) dhankar@dhankar-1:.../local$ 

```


conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch


ettle             pkgs/main/linux-64::nettle-3.7.3-hbbd107a_1 None
  numpy              pkgs/main/linux-64::numpy-1.19.2-py36h54aff64_0 None
  numpy-base         pkgs/main/linux-64::numpy-base-1.19.2-py36hfa32c7d_0 None
  olefile            pkgs/main/linux-64::olefile-0.46-py36_0 None
  openh264           pkgs/main/linux-64::openh264-2.1.1-h4ff587b_0 None
  openjpeg           pkgs/main/linux-64::openjpeg-2.4.0-h3ad879b_0 None
  pillow             pkgs/main/linux-64::pillow-8.3.1-py36h2c7a002_0 None
  pytorch            pytorch/linux-64::pytorch-1.10.2-py3.6_cuda10.2_cudnn7.6.5_0 None
  pytorch-mutex      pytorch/noarch::pytorch-mutex-1.0-cuda None
  six                pkgs/main/noarch::six-1.16.0-pyhd3eb1b0_1 None
  torchaudio         pytorch/linux-64::torchaudio-0.10.2-py36_cu102 None
  torchvision        pytorch/linux-64::torchvision-0.11.3-py36_cu102 None
  typing_extensions  pkgs/main/noarch::typing_extensions-4.1.1-pyh06a4308_0 None
  zstd               pkgs/main/linux-64::zstd-1.5.2-ha4553b6_0 None


Proceed ([y]/n)? y




```bash

RuntimeError: 
The detected CUDA version (11.0) mismatches the version that was used to compile
PyTorch (10.2). Please make sure to use the same CUDA versions.

(env_point_net) dhankar@dhankar-1:~/.../iou3d$ 
(env_point_net) dhankar@dhankar-1:~/.../iou3d$ python3 setup.py install
/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/torch/package/_directory_reader.py:17: UserWarning: Failed to initialize NumPy: numpy.core.multiarray failed to import (Triggered internally at  ../torch/csrc/utils/tensor_numpy.cpp:68.)
  _dtype_to_storage = {data_type(0).dtype: data_type for data_type in _storages}

--torch.cuda.is_available()-----
 True


running install
running bdist_egg
running egg_info
writing iou3d.egg-info/PKG-INFO
writing dependency_links to iou3d.egg-info/dependency_links.txt
writing top-level names to iou3d.egg-info/top_level.txt

/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/torch/utils/cpp_extension.py:381: UserWarning: Attempted to use ninja as the BuildExtension backend but we could not find ninja.. Falling back to using the slow distutils backend.
  warnings.warn(msg.format('we could not find ninja.'))


reading manifest file 'iou3d.egg-info/SOURCES.txt'
writing manifest file 'iou3d.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_ext
Traceback (most recent call last):
  File "setup.py", line 20, in <module>
    cmdclass={'build_ext': BuildExtension})
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/__init__.py", line 153, in setup
    return distutils.core.setup(**attrs)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/core.py", line 148, in setup
    dist.run_commands()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 955, in run_commands
    self.run_command(cmd)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/install.py", line 67, in run
    self.do_egg_install()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/install.py", line 109, in do_egg_install
    self.run_command('bdist_egg')
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/bdist_egg.py", line 164, in run
    cmd = self.call_command('install_lib', warn_dir=0)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/bdist_egg.py", line 150, in call_command
    self.run_command(cmdname)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/install_lib.py", line 11, in run
    self.build()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/command/install_lib.py", line 107, in build
    self.run_command('build_ext')
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/setuptools/command/build_ext.py", line 79, in run
    _build_ext.run(self)
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/distutils/command/build_ext.py", line 339, in run
    self.build_extensions()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/torch/utils/cpp_extension.py", line 404, in build_extensions
    self._check_cuda_version()
  File "/home/dhankar/anaconda3/envs/env_point_net/lib/python3.6/site-packages/torch/utils/cpp_extension.py", line 781, in _check_cuda_version
    raise RuntimeError(CUDA_MISMATCH_MESSAGE.format(cuda_str_version, torch.version.cuda))
RuntimeError: 
The detected CUDA version (11.0) mismatches the version that was used to compile
PyTorch (10.2). Please make sure to use the same CUDA versions.
```

#
<br>




```bash

(env_point_net) dhankar@dhankar-1:~/.../iou3d$ 
(env_point_net) dhankar@dhankar-1:~/.../iou3d$ sudo python3 setup.py install
[sudo] password for dhankar: 
--torch.cuda.is_available()-----
 True
running install
running bdist_egg
running egg_info
writing iou3d.egg-info/PKG-INFO
writing dependency_links to iou3d.egg-info/dependency_links.txt
writing top-level names to iou3d.egg-info/top_level.txt
/usr/local/lib/python3.6/dist-packages/torch/utils/cpp_extension.py:381: UserWarning: Attempted to use ninja as the BuildExtension backend but we could not find ninja.. Falling back to using the slow distutils backend.
  warnings.warn(msg.format('we could not find ninja.'))
reading manifest file 'iou3d.egg-info/SOURCES.txt'
writing manifest file 'iou3d.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_ext
Traceback (most recent call last):
  File "setup.py", line 20, in <module>
    cmdclass={'build_ext': BuildExtension})
  File "/usr/lib/python3/dist-packages/setuptools/__init__.py", line 129, in setup
    return distutils.core.setup(**attrs)
  File "/usr/lib/python3.6/distutils/core.py", line 148, in setup
    dist.run_commands()
  File "/usr/lib/python3.6/distutils/dist.py", line 955, in run_commands
    self.run_command(cmd)
  File "/usr/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/usr/lib/python3/dist-packages/setuptools/command/install.py", line 67, in run
    self.do_egg_install()
  File "/usr/lib/python3/dist-packages/setuptools/command/install.py", line 109, in do_egg_install
    self.run_command('bdist_egg')
  File "/usr/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/usr/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/usr/lib/python3/dist-packages/setuptools/command/bdist_egg.py", line 172, in run
    cmd = self.call_command('install_lib', warn_dir=0)
  File "/usr/lib/python3/dist-packages/setuptools/command/bdist_egg.py", line 158, in call_command
    self.run_command(cmdname)
  File "/usr/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/usr/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/usr/lib/python3/dist-packages/setuptools/command/install_lib.py", line 24, in run
    self.build()
  File "/usr/lib/python3.6/distutils/command/install_lib.py", line 109, in build
    self.run_command('build_ext')
  File "/usr/lib/python3.6/distutils/cmd.py", line 313, in run_command
    self.distribution.run_command(command)
  File "/usr/lib/python3.6/distutils/dist.py", line 974, in run_command
    cmd_obj.run()
  File "/usr/lib/python3/dist-packages/setuptools/command/build_ext.py", line 78, in run
    _build_ext.run(self)
  File "/usr/lib/python3.6/distutils/command/build_ext.py", line 339, in run
    self.build_extensions()
  File "/usr/local/lib/python3.6/dist-packages/torch/utils/cpp_extension.py", line 404, in build_extensions
    self._check_cuda_version()
  File "/usr/local/lib/python3.6/dist-packages/torch/utils/cpp_extension.py", line 781, in _check_cuda_version
    raise RuntimeError(CUDA_MISMATCH_MESSAGE.format(cuda_str_version, torch.version.cuda))
RuntimeError: 
The detected CUDA version (9.1) mismatches the version that was used to compile
PyTorch (10.2). Please make sure to use the same CUDA versions.

(env_point_net) dhankar@dhankar-1:~/.../iou3d$ 


```




#
<br>



```bash

(base) dhankar@dhankar-1:~/.../original_PointRCNN$ conda create -n env_point_net python=3.6
Collecting package metadata (current_repodata.json): done
Solving environment: failed with repodata from current_repodata.json, will retry with next repodata source.
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/dhankar/anaconda3/envs/env_point_net

  added / updated specs:
    - python=3.6


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    certifi-2021.5.30          |   py36h06a4308_0         139 KB
    pip-21.2.2                 |   py36h06a4308_0         1.8 MB
    python-3.6.13              |       h12debd9_1        32.5 MB
    setuptools-58.0.4          |   py36h06a4308_0         788 KB
    ------------------------------------------------------------
                                           Total:        35.2 MB

The following NEW packages will be INSTALLED:

  _libgcc_mutex      pkgs/main/linux-64::_libgcc_mutex-0.1-main None
  _openmp_mutex      pkgs/main/linux-64::_openmp_mutex-5.1-1_gnu None
  ca-certificates    pkgs/main/linux-64::ca-certificates-2022.10.11-h06a4308_0 None
  certifi            pkgs/main/linux-64::certifi-2021.5.30-py36h06a4308_0 None
  ld_impl_linux-64   pkgs/main/linux-64::ld_impl_linux-64-2.38-h1181459_1 None
  libffi             pkgs/main/linux-64::libffi-3.3-he6710b0_2 None
  libgcc-ng          pkgs/main/linux-64::libgcc-ng-11.2.0-h1234567_1 None
  libgomp            pkgs/main/linux-64::libgomp-11.2.0-h1234567_1 None
  libstdcxx-ng       pkgs/main/linux-64::libstdcxx-ng-11.2.0-h1234567_1 None
  ncurses            pkgs/main/linux-64::ncurses-6.3-h5eee18b_3 None
  openssl            pkgs/main/linux-64::openssl-1.1.1s-h7f8727e_0 None
  pip                pkgs/main/linux-64::pip-21.2.2-py36h06a4308_0 None
  python             pkgs/main/linux-64::python-3.6.13-h12debd9_1 None
  readline           pkgs/main/linux-64::readline-8.2-h5eee18b_0 None
  setuptools         pkgs/main/linux-64::setuptools-58.0.4-py36h06a4308_0 None
  sqlite             pkgs/main/linux-64::sqlite-3.39.3-h5082296_0 None
  tk                 pkgs/main/linux-64::tk-8.6.12-h1ccaba5_0 None
  wheel              pkgs/main/noarch::wheel-0.37.1-pyhd3eb1b0_0 None
  xz                 pkgs/main/linux-64::xz-5.2.6-h5eee18b_0 None
  zlib               pkgs/main/linux-64::zlib-1.2.13-h5eee18b_0 None


Proceed ([y]/n)? y


Downloading and Extracting Packages
certifi-2021.5.30    | 139 KB    | ################################################################################################### | 100% 
python-3.6.13        | 32.5 MB   | ################################################################################################### | 100% 
setuptools-58.0.4    | 788 KB    | ################################################################################################### | 100% 
pip-21.2.2           | 1.8 MB    | ################################################################################################### | 100% 
Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate env_point_net
#
# To deactivate an active environment, use
#
#     $ conda deactivate

Retrieving notices: ...working... done
(base) dhankar@dhankar-1:~/.../original_PointRCNN$ 
(base) dhankar@dhankar-1:~/.../original_PointRCNN$ conda activate env_point_net
(env_point_net) dhankar@dhankar-1:~/.../original_PointRCNN$ 
(env_point_net) dhankar@dhankar-1:~/.../original_PointRCNN$ 
(env_point_net) dhankar@dhankar-1:~/.../original_PointRCNN$ nvidia-smi
Tue Nov  8 18:06:14 2022       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 450.51.05    Driver Version: 450.51.05    CUDA Version: 11.0     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  GeForce GTX 1650    On   | 00000000:01:00.0  On |                  N/A |
|  0%   44C    P8     4W /  75W |    299MiB /  3910MiB |      1%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A      2455      G   /usr/lib/xorg/Xorg                 14MiB |
|    0   N/A  N/A      2865      G   /usr/bin/gnome-shell               48MiB |
|    0   N/A  N/A      4000      G   /usr/lib/xorg/Xorg                104MiB |
|    0   N/A  N/A      4929      G   /usr/bin/gnome-shell               94MiB |
|    0   N/A  N/A      9693      G   /usr/lib/firefox/firefox            2MiB |
|    0   N/A  N/A     17927      G   ...RendererForSitePerProcess       30MiB |
+-----------------------------------------------------------------------------+
(env_point_net) dhankar@dhankar-1:~/.../original_PointRCNN$ 
(env_point_net) dhankar@dhankar-1:~/.../original_PointRCNN$ nvcc --version
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2020 NVIDIA Corporation
Built on Thu_Jun_11_22:26:38_PDT_2020
Cuda compilation tools, release 11.0, V11.0.194
Build cuda_11.0_bu.TC445_37.28540450_0
(env_point_net) dhankar@dhankar-1:~/.../original_PointRCNN$ 

```


```bash

(base) dhankar@dhankar-1:~/.../11_22$ nvidia-smi
Tue Nov  8 23:46:37 2022       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 450.51.05    Driver Version: 450.51.05    CUDA Version: 11.0     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  GeForce GTX 1650    On   | 00000000:01:00.0  On |                  N/A |
|  0%   45C    P8     4W /  75W |    301MiB /  3910MiB |      1%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A      2455      G   /usr/lib/xorg/Xorg                 14MiB |
|    0   N/A  N/A      2865      G   /usr/bin/gnome-shell               48MiB |
|    0   N/A  N/A      4000      G   /usr/lib/xorg/Xorg                102MiB |
|    0   N/A  N/A      4929      G   /usr/bin/gnome-shell               94MiB |
|    0   N/A  N/A      9693      G   /usr/lib/firefox/firefox            2MiB |
|    0   N/A  N/A     17927      G   ...RendererForSitePerProcess       33MiB |
+-----------------------------------------------------------------------------+
(base) dhankar@dhankar-1:~/.../11_22$ 

(base) dhankar@dhankar-1:~/.../11_22$ nvcc --version
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2020 NVIDIA Corporation
Built on Thu_Jun_11_22:26:38_PDT_2020
Cuda compilation tools, release 11.0, V11.0.194
Build cuda_11.0_bu.TC445_37.28540450_0
(base) dhankar@dhankar-1:~/.../11_22$ 

```

```bash
(env_lyft) dhankar@dhankar-1:~/.../tools$ python eval_rcnn.py --cfg_file cfgs/default.yaml --ckpt PointRCNN.pth --batch_size 1 --eval_mode rcnn --set RPN.LOC_XZ_FINE False
Traceback (most recent call last):
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/tools/eval_rcnn.py", line 8, in <module>
    from lib.net.point_rcnn import PointRCNN ## MISSING-- iou3d_cuda
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/tools/../lib/net/point_rcnn.py", line 3, in <module>
    from lib.net.rpn import RPN
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/tools/../lib/net/rpn.py", line 4, in <module>
    from lib.rpn.proposal_layer import ProposalLayer
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/tools/../lib/rpn/proposal_layer.py", line 6, in <module>
    import lib.utils.iou3d.iou3d_utils as iou3d_utils
  File "/home/dhankar/temp/11_22/original_PointRCNN/PointRCNN/tools/../lib/utils/iou3d/iou3d_utils.py", line 2, in <module>
    import iou3d_cuda
ModuleNotFoundError: No module named 'iou3d_cuda'

```







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

- https://mmdetection3d.readthedocs.io/en/v0.17.3/datasets/kitti_det.html#prepare-dataset


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