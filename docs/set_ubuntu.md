
# set ubuntu

* 명령어 참고 `chmod`

## graphic driver

### 설치

```bash
## graphic driver

$ sudo apt-get update
$ sudo apt-get install -y build-essential curl gcc ssh git net-tools vim
$ wget https://us.download.nvidia.com/XFree86/Linux-x86_64/470.57.02/NVIDIA-Linux-x86_64-470.57.02.run
$ chmod +x NVIDIA-Linux-x86_64-470.57.02.run
$ sudo ./NVIDIA-Linux-x86_64-470.57.02.run
```

### 확인

```bash
$ nvidia-smi
```
![Screenshot from 2021-12-15 22-52-25](https://user-images.githubusercontent.com/8021479/146199238-d5295019-20fa-4b99-8ed8-ed0aad6e87f4.png)
들

여기서 이상 없어야 통과. 안되면 다시

## CUDA

* [CUDA 10.2](https://developer.nvidia.com/cuda-10.2-download-archive)
* [CUDA 11.1](https://developer.nvidia.com/cuda-11.1.0-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=2004&target_type=runfilelocal)

![Screenshot from 2021-12-15 22-57-20](https://user-images.githubusercontent.com/8021479/146199723-739b01c5-9aa0-4320-bbb5-d418e0100f35.png)
![Screenshot from 2021-12-15 22-57-46](https://user-images.githubusercontent.com/8021479/146199726-7a1cb40f-b614-4a78-a90f-18c36769c17e.png)


```bash
# cuda install
$ sudo apt-get update
$ wget https://developer.download.nvidia.com/compute/cuda/11.1.0/local_installers/cuda_11.1.0_455.23.05_linux.run
$ sudo sh ./cuda_11.1.0_455.23.05_linux.run

```

* CUDA 버전에 맞춰서 경로지정 `10.2`

```bash
# ~/.bashrc
export PATH=/usr/local/bin:$PATH
export PATH=/usr/local/cuda-10.2/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-10.2/lib64:${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
```

```bash
source ~/.bashrc
nvcc --version
```


완료된 모습

![Screenshot from 2021-12-15 22-54-35](https://user-images.githubusercontent.com/8021479/146199241-af22baaf-6e24-41d9-a42d-578d4e6f314b.png)



## PyTorch


```bash
# install torch
$ sudo apt-get update
$ pip3 install torch==1.8.0+cu111 torchvision==0.9.0+cu111 torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html
```




## (optional)

### dotnet

```bash
# dotnet
$ sudo apt-get update
$ sudo apt-get install -y apt-transport-https
$ sudo apt-get update
$ sudo apt-get install -y dotnet-sdk-6.0
$ sudo apt-get update
$ sudo apt-get install -y apt-transport-https
$ sudo apt-get update
$ sudo apt-get install -y aspnetcore-runtime-6.0
```


---

[다시 # Home main 으로](../README.md)
