
# set ubuntu

* 명령어 참고 `chmod`


## ubuntu





![photo_2021-12-16_16-22-11](https://user-images.githubusercontent.com/8021479/146326097-086edb34-7682-442f-b8ba-0f7aa889ee1c.jpg)
![photo_2021-12-16_16-22-12](https://user-images.githubusercontent.com/8021479/146326101-c1d719ba-2e75-4f97-9f74-cfb2aaf0cae2.jpg)
![photo_2021-12-16_16-22-13](https://user-images.githubusercontent.com/8021479/146326103-cd39622b-7320-4453-9ada-ae74a61f4562.jpg)
![photo_2021-12-16_16-22-13 (2)](https://user-images.githubusercontent.com/8021479/146326104-8588c163-df47-48e5-acbd-803dc628949b.jpg)
![photo_2021-12-16_16-22-14](https://user-images.githubusercontent.com/8021479/146326106-5f07f5b5-d260-464b-9182-99681bf6f928.jpg)

지울 부분 !! ubuntu 20.04로 바뀔 부분

![photo_2021-12-16_16-22-15](https://user-images.githubusercontent.com/8021479/146326109-c1a56c85-679b-4019-b087-d8af13984547.jpg)



### after boot

![photo_2021-12-16_16-36-46](https://user-images.githubusercontent.com/8021479/146328412-8c25e510-e952-4942-960a-aca48ef683b6.jpg)
![photo_2021-12-16_16-36-48](https://user-images.githubusercontent.com/8021479/146328413-86adcbdd-2465-46ca-b033-545e4f385ed5.jpg)
![photo_2021-12-16_16-36-49](https://user-images.githubusercontent.com/8021479/146328414-7eb95bb2-6073-4e55-b1ea-50750558a458.jpg)





## graphic driver

### 준비

```bash
## graphic driver

$ sudo apt-get update
$ sudo apt-get install -y build-essential curl gcc ssh git net-tools vim
$ sudo bash -c "echo blacklist nouveau >> /etc/modprobe.d/blacklist.conf"
$ sudo bash -c "echo options nouveau modeset=0 >> /etc/modprobe.d/blacklist.conf"
# cat /etc/modprobe.d/blacklist-nvidia-nouveau.conf
# sudo bash -c "echo blacklist nouveau > /etc/modprobe.d/blacklist-nvidia-nouveau.conf"
# sudo bash -c "echo options nouveau modeset=0 >> /etc/modprobe.d/blacklist-nvidia-nouveau.conf"
$ sudo update-initramfs -u
```

![photo_2021-12-16_16-36-50](https://user-images.githubusercontent.com/8021479/146328416-9a77e513-9b82-4413-ac7a-95dc8f341c8a.jpg)
![photo_2021-12-16_16-36-51](https://user-images.githubusercontent.com/8021479/146328417-59b4f971-8ee3-4670-9864-b3b2d5d7cbf6.jpg)

이렇게 나오면 오류! 

`cat /etc/modprobe.d/blacklist.conf` 에서 맨 마지막에 

![photo_2021-12-16_16-36-52](https://user-images.githubusercontent.com/8021479/146328420-44912d8b-2f63-4c8a-86cd-619fa9994aa8.jpg)

```bash
# /etc/modprobe.d/blacklist.conf
blacklist nouveau
options nouveau modeset=0
```
이 내용이 들어가고 `sudo update-initramfs -u` 재시작 끝나고 나면 이상없이 설치 가능


![photo_2021-12-16_16-36-53](https://user-images.githubusercontent.com/8021479/146328423-4da8633f-b40a-43f8-ab40-11030f67849d.jpg)

다 되면 재시작

`sudo reboot`


![photo_2021-12-16_16-36-54](https://user-images.githubusercontent.com/8021479/146328426-6a088a76-1a82-4c7c-96ea-e071b1f5b77f.jpg)

처음 해서 그래픽 좋게 보일때 보다 다시 안좋게 보이면 잘 되고 있는것.


### 설치

```bash
$ wget https://us.download.nvidia.com/XFree86/Linux-x86_64/470.57.02/NVIDIA-Linux-x86_64-470.57.02.run
$ chmod +x NVIDIA-Linux-x86_64-470.57.02.run
$ sudo ./NVIDIA-Linux-x86_64-470.57.02.run
```

![photo_2021-12-16_16-36-54 (2)](https://user-images.githubusercontent.com/8021479/146328427-9b20f734-c9d5-431d-a8ed-3fc793549adc.jpg)


![photo_2021-12-16_16-53-56](https://user-images.githubusercontent.com/8021479/146330606-03d8e44d-dee4-462b-af8f-e170a07f127a.jpg)



### 확인

```bash
$ nvidia-smi
```
![Screenshot from 2021-12-15 22-52-25](https://user-images.githubusercontent.com/8021479/146199238-d5295019-20fa-4b99-8ed8-ed0aad6e87f4.png)

![photo_2021-12-16_16-53-57](https://user-images.githubusercontent.com/8021479/146330611-2e445f0c-8327-4d0a-9476-2e4a5bef1338.jpg)

여기서 이상 없어야 통과. 안되면 다시

## CUDA


Ubuntu 18.04 일땐
* [CUDA 10.2](https://developer.nvidia.com/cuda-10.2-download-archive)

ubuntu 20.04 일땐
* [CUDA 11.1](https://developer.nvidia.com/cuda-11.1.0-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=2004&target_type=runfilelocal)



![Screenshot from 2021-12-15 22-57-20](https://user-images.githubusercontent.com/8021479/146199723-739b01c5-9aa0-4320-bbb5-d418e0100f35.png)
![Screenshot from 2021-12-15 22-57-46](https://user-images.githubusercontent.com/8021479/146199726-7a1cb40f-b614-4a78-a90f-18c36769c17e.png)


```bash
# cuda install
$ sudo apt-get update
$ wget https://developer.download.nvidia.com/compute/cuda/11.1.0/local_installers/cuda_11.1.0_455.23.05_linux.run
$ sudo sh ./cuda_11.1.0_455.23.05_linux.run
```


![photo_2021-12-16_16-54-01](https://user-images.githubusercontent.com/8021479/146330614-3514a0da-a6fd-4e0f-904c-333142a12259.jpg)

* CUDA 버전에 맞춰서 경로지정 `11.1`
* CUDA 버전에 맞춰서 경로지정 `10.2`



```bash
# ~/.bashrc
$ sudo bash -c "echo export PATH=/usr/local/bin:$PATH >> ~/.bashrc"
$ sudo bash -c "echo export PATH=/usr/local/cuda-11.1/bin${PATH:+:${PATH}} >> ~/.bashrc"
$ sudo bash -c "echo LD_LIBRARY_PATH=/usr/local/cuda-11.1/lib64:${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}} >> ~/.bashrc"
$ source ~/.bashrc
```

<!--->
```bash
# ~/.bashrc
export PATH=/usr/local/bin:$PATH
export PATH=/usr/local/cuda-11.1/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-11.1/lib64:${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
```
-->

여기까지 설정 완료 시



```bash
nvcc --version
```


완료된 모습

![Screenshot from 2021-12-15 22-54-35](https://user-images.githubusercontent.com/8021479/146199241-af22baaf-6e24-41d9-a42d-578d4e6f314b.png)



## PyTorch


```bash
# install torch
$ sudo apt-get update
$ sudo apt-get install python3-pip -y
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


