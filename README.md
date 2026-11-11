# Sophus

This repository takes snapshots of the upstream [sophus](https://github.com/strasdat/Sophus) repository to create release branches for ROS.

There has been times in the past when these branches accomodated minor bug fixes to make them releasable whilst active development on Sophus had paused. Recent efforts aim to synchronise these with the upstream repository now that it is actively maintained again.

## ROS2 Releases

* Humble: [1.3.x](https://github.com/stonier/sophus/tree/release/1.3.x), sync'd with [sophus/tags/v22.04.1](https://github.com/strasdat/Sophus/tree/v22.04.1) (April 20, 2022)
* Foxy: [1.3.x](https://github.com/stonier/sophus/tree/release/1.3.x), sync'd with [sophus/tags/v22.04.1](https://github.com/strasdat/Sophus/tree/v22.04.1) (April 20, 2022)
* Foxy: [1.2.x](https://github.com/stonier/sophus/tree/release/1.2.x), sync'd with [sophus/master@593db475](https://github.com/strasdat/Sophus/commit/593db47500ea1a2de5f0e6579c86147991509c59) (July 15, 2020)
* Eloquent: [1.1.x](https://github.com/stonier/sophus/tree/release/1.1.x), sync'd with [sophus/master@ef9551ff](https://github.com/strasdat/Sophus/tree/ef9551ff429899b5adae66eabd5a23f165953199) (Oct 13, 2019).
* Dashing: [1.0.x](https://github.com/stonier/sophus/tree/release/1.0-dashing), sync'd with [sophus/master@00f3fd91](https://github.com/strasdat/Sophus/tree/00f3fd91c153ef04432ae26450080fd3357f421d) (Apr 02, 2018).

## ROS 1 Releases

* Noetic: [1.2.x](https://github.com/stonier/sophus/tree/release/1.2.x), sync'd with [sophus/master@593db475](https://github.com/strasdat/Sophus/commit/593db47500ea1a2de5f0e6579c86147991509c59) (July 15, 2020)
* Melodic: [1.1.x](https://github.com/stonier/sophus/tree/release/1.1.x), sync'd with [sophus/master@ef9551ff](https://github.com/strasdat/Sophus/tree/ef9551ff429899b5adae66eabd5a23f165953199) (Oct 13, 2019).

## About

This is a ros 3rd party package that provides Hauke Strasdat's
[sophus](https://github.com/stonier/sophus) library.

## Installation From Deb



```
$ sudo apt-get install ros-kinetic-sophus
```



To use it from your own catkin package you need to make sure you get the
dependency syntax right. The cmake commands in particular are subtly
different from depending on a catkin package. An example:

**CMakeLists.txt**



```highlight
find_package(catkin REQUIRED COMPONENTS                                   
                 ecl_linear_algebra
                 ecl_time 
                 dslam_common
                 )
find_package(sophus REQUIRED)

catkin_package(
    INCLUDE_DIRS include 
    LIBRARIES ${PROJECT_NAME}
    DEPENDS                
        sophus
    CATKIN_DEPENDS                
        ecl_linear_algebra
        ecl_time
        dslam_common
    )
```



**package.xml** 

```highlight
  <build_depend>ecl_linear_algebra</build_depend>
  <build_depend>ecl_time</build_depend>
  <build_depend>sophus</build_depend>
  <build_depend>dslam_common</build_depend>


  <run_depend>ecl_linear_algebra</run_depend>
  <run_depend>ecl_time</run_depend>
  <run_depend>sophus</run_depend>
  <run_depend>dslam_common</run_depend>
```



## Installation from Source

See the [README](https://github.com/stonier/sophus).
