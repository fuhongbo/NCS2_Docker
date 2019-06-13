# NCS2 Docker File

This repository is used to build the docker image of NCS2.

###### 1.Raspbian (for ARM)

This docker file use for build docker image for "Raspberry Pi".

Follow Steps:

```
1. download this repository.

2. cd raspbian

3. wget https://download.01.org/opencv/2019/openvinotoolkit/l_openvino_toolkit_raspbi_p_2019.1.094.tgz

4. mkdir openvino && tar -xf l_openvino_toolkit_raspbi_p_2019.1.094.tgz -C openvino 

#you can add --build-arg HTTP_PROXY & HTTPS_PROXY in your build command.
5. docker build . -t <imagename>

6. docker run -it --privileged --net=host -v /dev:/dev <imagename> /bin/bash

```

###### 1.Ubuntu

This docker file use for build docker image for "Ubuntu".

Follow Steps:

```
1. download this repository.

2. cd ubuntu

3. wget http://registrationcenter-download.intel.com/akdlm/irc_nas/15512/l_openvino_toolkit_p_2019.1.144.tgz

4. tar -zxvf l_openvino_toolkit_raspbi_p_2019.1.094.tgz 

#you can add --build-arg HTTP_PROXY & HTTPS_PROXY in your build command.
5. docker build . -t <imagename>

6. docker run -it --privileged --net=host -v /dev:/dev <imagename> /bin/bash

```
