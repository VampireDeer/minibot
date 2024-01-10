# Mobile Robots Maneuver
## 1. 프로젝트 요약
### 1-1. 설명
자율 이동 로봇(AMR, Autonomous Mobile Robots)의 자율 이동을 위한 ROS2 Gazebo와 Rviz2를 사용해보기
### 1-2. 개발환경
- Ubuntu 22.04 Desktop
- ROS2 Humble
## 2. 프로젝트 
---
### 2-1. 가제보만 실행하기
- 터미널 3개에서 순서데로 각각 실행

1

    ros2 launch my_robot_description upload.launch.py use_sim_time:=true

2

    ros2 launch gazebo_ros gazebo.launch.py

3

    ros2 run gazebo_ros spawn_entity.py -topic robot_description -entity my_robot

---
### 2-2. 가제보와 rviz2에 minibot과 map 띄우기

Gazebo -> minibot and map
  
    ros2 launch my_robot_description launch_sim.launch.py 

rviz2 

    rviz2

- rviz2 Displays 설정\
Fixed Frame -> base_link\
RobotModel\
TF\
LaserScan\
Map\
Camera

### 2-3. Gazebo 와 rviz2로 map building하기

Gazebo

    ros2 launch my_robot_description launch_sim.launch.py

rviz2

   rviz2

teleopkeyboard

    ros2 run teleop_twist_keyboard teleop_twist_keyboard



   


