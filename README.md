# manifest
The main repository to clone all the repositories.
To clone the repositories follow the commands bellow: 

```bash
mkdir jimmbot_ws
cd jimmbot_ws
repo init -u https://github.com/mh-Robotics/manifest.git
repo sync
catkin_init_workspace
catkin_make
```

Master branch contains work under process. Stable branches for ros disctros named: distro-devel