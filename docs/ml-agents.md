
# ML-Agents

[Unity ML-Agents Toolkit Documentation](https://github.com/Unity-Technologies/ml-agents/blob/release_18_docs/docs/Readme.md)

|||
|:---:|:---|
|설치|[Installation](https://github.com/Unity-Technologies/ml-agents/blob/release_18_docs/docs/Installation.md)|
|설정|[Getting Started Guide](https://github.com/Unity-Technologies/ml-agents/blob/release_18_docs/docs/Getting-Started.md)|
|설립|[Making a New Learning Environment](https://github.com/Unity-Technologies/ml-agents/blob/release_18_docs/docs/Learning-Environment-Create-New.md)|



---

## 참고


### Package Manager 

![](https://github.com/Unity-Technologies/URDF-Importer/blob/main/images~/Package_manager_add.png?raw=true)

>Input System

* 자체 내부에서 추가 가능
* ![](https://user-images.githubusercontent.com/8021479/145762158-0a2540a6-ba60-4cad-b455-895784871c22.png)



### optional

>Barracuda (Package Manager)

```bash
$ git clone https://github.com/Unity-Technologies/barracuda-release
```



#### ML Agents & ML Agents ExtentionConfigure your Development Environment

```bash
$ pip3 install mlagents==0.27.0

$ git clone --branch release_18 https://github.com/Unity-Technologies/ml-agents.git

$ cd ./ml-agents
$ pip3 install -e ./ml-agents-envs/
$ pip3 install -e ./ml-agents/
$ pip3 install -e ./gym-unity/

```

1. 그리고 유니티 Package Manager 에서 상단 플러스 버튼 누르고 `add package from disk` 선택
2. 다시 ml-agents 깃 받은 폴더에 들어가면 아래와 같이
   * ![Screenshot from 2021-12-15 23-34-04](https://user-images.githubusercontent.com/8021479/146205723-62ac2a57-cd0c-43e3-8941-550ec290fcfe.png)
   1. `com.unity.ml-agents`
      1. `package.json` 선택
   2. `com.unity.ml-agents.extensions`
      1. `package.json` 선택





### comment

처음에 계속 안되던 모습

![](https://user-images.githubusercontent.com/8021479/145679617-60b9bc24-e86d-4e96-a3b2-5b2dace4b78d.png)

이 부분 주석 처리

![](https://user-images.githubusercontent.com/8021479/145679624-adc38c99-3ef3-4506-8f3b-aff5dd9aacb4.png)
![](https://user-images.githubusercontent.com/8021479/145761529-dcf9f700-1d5f-47b4-972e-e3178f89dc9d.png)


* [이슈](https://github.com/NamWoo/My_ML_Agents/issues/1)



## final result


![](https://user-images.githubusercontent.com/8021479/145761527-a52be307-c210-4436-ab06-7e7cb37f64ba.png)



---

[다시 # Home main 으로](../README.md)
