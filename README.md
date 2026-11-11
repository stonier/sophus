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
