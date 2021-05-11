# manifest
The main repository to clone all the repositories neccesary for jimmBOT.

## Using repo tool 

Install repo tool
```bash
$ mkdir ~/bin
$ PATH=~/bin:$PATH
$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$ chmod a+x ~/bin/repo
```

Create a workspace
```bash
$ mkdir ~/jimmbot_ws
$ cd ~/jimmbot_ws
```

Populate workspace from manifest
```bash
$ repo init -u https://github.com/mh-Robotics/manifest.git
```

Additionally use a specific branch
```bash
$ repo init -u https://github.com/mh-Robotics/manifest.git -b noetic
```

Update the workspace
```bash
$ repo sync
```

**Available manifest branches:**
* master
* noetic

## Using vcstool

Install vcstool
```bash
$ sudo apt install python3-vcstool
```

Create a workspace
```bash
$ mkdir ~/jimmbot_ws
$ cd ~/jimmbot_ws
```

Populate workspace from .rosinstall file
```bash
$ vcs import src < PATH_TO_ROSINSTALL_FILE.rosinstall
```

Update the workspace
```bash
$ vcs pull src
```

**Notes:**
- Master branch contains work under process.
- Distro branches contain stable version for that ros-distro.

## Building sources

Change directory to workspace
```bash
cd ~/jimmbot_ws
```

Init the ROS workspace
```bash
catkin_init_workspace
```

Build
```
catkin_make
```