# EduWing AI Autonomous Robot Project
이 프로젝트는 ROS2와 YOLOv8 기반의 AI 자율주행 모바일 로봇 시스템 제어 코드 저장소입니다.

## 개발 환경 (Environment)
- **OS:** Ubuntu 24.04 LTS
- **Framework:** Jazzy
- **Hardware:** TurtleBot3 (Raspberry Pi 4)

## 필수 설치 요소 (Prerequisites)
로봇을 구동하기 전 아래 패키지들을 먼저 설치해 주세요.
```bash
sudo apt update
sudo apt install ros-$ROS_DISTRO-turtlebot3-navigation2

# 기타 필요한 의존성 패키지 기술
```

## 실행 방법 (Quick Start)
이 저장소를 복제(Clone)한 뒤, 아래 명령어를 순서대로 터미널에 입력하여
로봇 노드를 구동하세요.

```bash
# 1. 로봇 워크스페이스 폴더로 이동
cd ~/clone_test/git_ws

# 2. 로봇 소스코드 빌드 (ROS2 전용 빌드 명령어)
colcon build --symlink-install

# 3. 빌드된 실행 환경을 현재 터미널에 로드
source install/setup.bash

# 4. AI 자율주행 모바일 로봇 노드 실행!
ros2 run robot_drive drive_node
