# rye-sample-pkg
This is a sample ros package with [rye](https://rye-up.com/).  

# Environment

| Item | Version |
|:-: | :-:|
| Ubuntu | 22.04 |
| ROS2 | Humble |

# Dependencies
Rye
https://rye-up.com/

```
curl -sSf https://rye-up.com/get | bash
echo 'source "$HOME/.rye/env"' >> ~/.bashrc
```

# Usage
## Clone and sync for rye

```bash
cd ~/ros2_ws/src
git clone https://github.com/koichirokato/rye_sample_pkg
cd rye_sample_pkg
rye sync
```

## Build

```bash
cd ~/ros2_ws/
colcon build --packages-select rye_sample_pkg --symlink-install
source install/setup.bash
```

## Run

```bash
cd ~/ros2_ws/src/rye_sample_pkg
rye shell
ros2 run rye_sample_pkg talker.py
```

## Work on your rye environment!

```bash
ros2 run rye_sample_pkg talker.py
[INFO] [1700807070.570010760] [minimal_publisher]: python path: /home/$USER/ros2_ws/src/rye_sample_pkg/.venv/bin/python3
[INFO] [1700807071.071507709] [minimal_publisher]: Publishing: "Hello World: 0"
[INFO] [1700807071.573184340] [minimal_publisher]: Publishing: "Hello World: 1"
[INFO] [1700807072.072772997] [minimal_publisher]: Publishing: "Hello World: 2"
```

