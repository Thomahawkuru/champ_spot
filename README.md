## zoo

This repository contains configuration package of Boston Dynamics Spot robot generated by CHAMP's [setup assistant](https://github.com/chvmp/champ_setup_assistant).

## Installation

You need to have [CHAMP](https://github.com/chvmp/champ) installed in your machine to make these robots walk.

Navigate to `src` directory in your workspace, then:

```bash
  git clone https://github.com/Thomahawkuru/champ_spot.git
  cd champ_spot
  git submodule init
  git submodule update
```

[spot_ros submodule](https://github.com/Thomahawkuru/spot_ros)

### Gazebo Worlds
Add `models` directory to the GAZEBO_MODEL_PATH environment variable. You can add the following line to the end of your ~/.bashrc:

```bash
  export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:<path to>/models
```
Examples: https://github.com/leonhartyao/gazebo_models_worlds_collection

### Quick Start Guide

Run the Gazebo environment:

```
roslaunch spot_config spawn_world.launch
```

Spawn the robot:
```
roslaunch spot_config spawn_robot.launch
```

In the simulation, only the robot's front cameras are available. Note that the cameras are mounted sideways, so they have a narrower horizontal FoV, but a larger vertical one. The camera data is rotated anticlockwise by 90 degrees.

You can find the pre-configured robot in [config](https://github.com/Thomahawkuru/champ_spot/tree/master/spot_config) folder. There's an auto-generated README in the configuration package that contains instructions on how to run the demos.

Please take note that although the README may contain instructions how to run in Gazebo, only the following pre-configured robots work in Gazebo:

- Boston Dynamic's Spot

## Credits

The URDFs found in this repository have been forked/modified/linked from the following projects:

- [Boston Dynamic's Spot](https://github.com/clearpathrobotics/spot_ros)
