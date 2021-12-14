# Installation

ref : https://github.com/Unity-Technologies/ml-agents/blob/main/docs/Installation.md

INDEX
1. Set My ENV
2. Set In Unity


---

## My ENV
* OS
  * Ubuntu 18.04 - good
  * Ubuntu 20.04 - good
* Graphic Driver
  * Nvidia 470.57.02 (NVIDIA-Linux-x86_64-470.57.02.run)
* CUDA
  * CUDA 11.1
    * `wget https://developer.download.nvidia.com/compute/cuda/11.1.0/local_installers/cuda_11.1.0_455.23.05_linux.run`
  * CUDA 11.3 - failed
  * CUDA 11.5 - failed
* Python
  * 3.6.9 - good
  * 3.8.10 - good
  * 3.9. - failed
  * 3.11. - failed


### dependency
```

sudo apt-get update
sudo apt install build-essential -y
wget https://us.download.nvidia.com/XFree86/Linux-x86_64/470.57.02/NVIDIA-Linux-x86_64-470.57.02.run
chmod +x NVIDIA-Linux-x86_64-470.57.02.run
sudo ./NVIDIA-Linux-x86_64-470.57.02.run

sudo apt-get install -y build-essential curl gcc ssh git net-tools vim
pip3 install torch==1.8.0+cu111 torchvision==0.9.0+cu111 torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html

   
git clone https://github.com/Unity-Technologies/barracuda-release

pip3 install mlagents==0.27.0

git clone --branch release_18 https://github.com/Unity-Technologies/ml-agents.git
cd ./ml-agents
pip3 install -e ./ml-agents-envs/
pip3 install -e ./ml-agents/
pip3 install -e ./gym-unity/

```

### optional

dotnet
```
sudo apt-get update;   sudo apt-get install -y apt-transport-https &&   sudo apt-get update &&   sudo apt-get install -y dotnet-sdk-6.0
sudo apt-get update;   sudo apt-get install -y apt-transport-https &&   sudo apt-get update &&   sudo apt-get install -y aspnetcore-runtime-6.0
```



## In Unity

### External Tools

External Scripts Editor Visual Studio Code Insiders

![](https://user-images.githubusercontent.com/8021479/145763001-67d72e9f-9fdf-4432-83b8-32ecafac7afd.png)


### Project Settings

Player - Other Settings Configuration
![](https://user-images.githubusercontent.com/8021479/145762239-0a8e4fe6-da82-4bca-a0e0-295a84106066.png)

1. Api Compatibility Level .NET 4.X
2. Active Input Handling - Input Manager(OLD)

### Package Manager 

#### required
1. Input System
2. ML Agents
3. ML Agents Extenstions

#### optional
1. Barracuda
2. Visual Studio Code Editor

![](https://user-images.githubusercontent.com/8021479/145762158-0a2540a6-ba60-4cad-b455-895784871c22.png)



### comment
![](https://user-images.githubusercontent.com/8021479/145761529-dcf9f700-1d5f-47b4-972e-e3178f89dc9d.png)



## final result


![](https://user-images.githubusercontent.com/8021479/145761527-a52be307-c210-4436-ab06-7e7cb37f64ba.png)
