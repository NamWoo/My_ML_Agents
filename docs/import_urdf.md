# Add URDF

* ref : https://github.com/Unity-Technologies/URDF-Importer
* URDF 개념 참고 https://pinkwink.kr/1007
* Tutorial: Using a URDF in Gazebo http://gazebosim.org/tutorials/?tut=ros_urdf

|Name|Type|Description|
|:---|:---|:---|
|material|value|Material of visual element|
|gravity|bool|Use gravity|
|dampingFactor|	double | Exponential velocity decay of the link velocity - takes the value and multiplies the previous link velocity by (1-dampingFactor).|
|maxVel|	double|	maximum contact correction velocity truncation term.|
|minDepth|	double|	minimum allowable depth before contact correction impulse is applied|
|mu1 / mu2|	double|	Friction coefficients μ for the principal contact directions along the contact surface as defined by the Open Dynamics Engine (ODE) (see parameter descriptions in ODE's user guide)|
|fdir1|string|	3-tuple specifying direction of mu1 in the collision local reference frame.|
|kp / kd|	double|	Contact stiffness k_p and damping k_d for rigid body contacts as defined by ODE (ODE uses erp and cfm but there is a mapping between erp/cfm and stiffness/damping)|
|selfCollide|	bool|	If true, the link can collide with other links in the model.|
|maxContacts|	int|	Maximum number of contacts allowed between two entities. This value overrides the max_contacts element defined in physics.|
|laserRetro|	double|	intensity value returned by laser sensor.|




## Add Package from Git URL


1. 패키지 추가
   * ![](https://github.com/Unity-Technologies/URDF-Importer/blob/main/images~/Package_manager_add.png?raw=true)
   * `https://github.com/Unity-Technologies/URDF-Importer.git?path=/com.unity.robotics.urdf-importer#v0.5.0`





## Import Robot from Selected URDF file

* ref : https://github.com/ROBOTIS-GIT/turtlebot3/tree/master/turtlebot3_description/urdf

Asset 에 미리 작성한 URDF 파일 드레그엔드롭

급히 만든 mybot urdf

|URDF|Images|
|:---:|:---:|
|[nw_mybot](../urdf/nw_mybot_00.urdf)|![Screenshot from 2021-12-16 01-00-22](https://user-images.githubusercontent.com/8021479/146221062-f06f0ffd-76d8-4704-a7d8-2b9dcc6468f6.png)|
|[turtlebot3_burger](../urdf/turtlebot3_burger.urdf)|![Screenshot from 2021-12-16 01-01-26](https://user-images.githubusercontent.com/8021479/146221065-d7e4e3eb-a4b0-473b-9a66-fbd7e6a03e63.png)|
|[turtlebot3_waffle_pi](../urdf/turtlebot3_waffle_pi.urdf)|![Screenshot from 2021-12-16 01-01-34](https://user-images.githubusercontent.com/8021479/146221069-c836b55f-e3e3-4edc-aed3-0ccfe95a4f9b.png)|


오른쪽 클릭해서 불러오기


![](https://github.com/Unity-Technologies/URDF-Importer/blob/main/images~/URDF%20Menu.png?raw=true)

![](https://user-images.githubusercontent.com/8021479/145799381-a5359dc6-be07-4db6-ac70-87503c839d0a.png?raw=true)

일단 모르니까 기본 불러오기 


급히 만든 mybot
* wheel 2개
* caster 1개
* 상단 라이다 모형 1개


![](https://user-images.githubusercontent.com/8021479/145799385-1bf22c95-bcd3-4921-bc4a-79819083d9c4.png)


### done

잘 불러와진 모습
![](https://user-images.githubusercontent.com/8021479/145799404-a4df7972-9c47-4067-a5f5-7f75fa2858be.png)



### 참고


```bash
# urdf check
$ check_urdf ./turtlebot3_waffle_pi.urdf
robot name is: turtlebot3_waffle_pi
---------- Successfully Parsed XML ---------------
root Link: base_footprint has 1 child(ren)
    child(1):  base_link
        child(1):  camera_link
            child(1):  camera_rgb_frame
                child(1):  camera_rgb_optical_frame
        child(2):  caster_back_left_link
        child(3):  caster_back_right_link
        child(4):  imu_link
        child(5):  base_scan
        child(6):  wheel_left_link
        child(7):  wheel_right_link

```

## 비교

1. visual - 검은 색, 3D 모델링 프로그램으로 그린 부분
2. collider - 초록 색, 충돌 가능한 부분


![Screenshot from 2021-12-15 12-12-56](https://user-images.githubusercontent.com/8021479/146123690-08740ae6-408b-4867-8bb5-6e6258c5bf11.png)
![Screenshot from 2021-12-15 12-10-27](https://user-images.githubusercontent.com/8021479/146123687-3184d3fa-5769-4071-9029-b114cca4eb2e.png)
![Screenshot from 2021-12-15 12-09-45](https://user-images.githubusercontent.com/8021479/146123681-27de7cfb-72a3-4e62-8a9d-3f0c5ed36b39.png)


추가해야할 부분
* ros component
* ArticulationBody https://docs.unity3d.com/Manual/class-ArticulationBody.html





https://user-images.githubusercontent.com/8021479/146311174-cd3efe74-cbc5-4cc7-b187-6b5af9b2e00b.mp4


---

[다시 # Home main 으로](../README.md)


