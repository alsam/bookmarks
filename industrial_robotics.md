# Industrial Robotics

+ Intro
    + [Industrial robot](https://en.wikipedia.org/wiki/Industrial_robot)
      + abbrevs.
      + **TCP** - **T**ool **C**entral **P**oint
    + [Lectures on Robotic Planning and Kinematics](http://motion.me.ucsb.edu/book-lrpk/)

+ robot camera calibration
    + [High-Precision Calibration Approaches to Robot Vision Systems](https://tams.informatik.uni-hamburg.de/paper/2009/Fangwu_Shu_Dissertation_SUB.pdf)

    + [A Vision-Based Self-Calibration Method for Robotic Visual
Inspection Systems](http://www.mdpi.com/1424-8220/13/12/16565/pdf)

    + [Robot Calibration: Modeling Measurement and Applications ](http://cdn.intechopen.com/pdfs/258/InTech-Robot_calibration_modeling_measurement_and_applications.pdf)

    + [Accurate Robotic 3D Vision](http://universallogic.com/wp-content/uploads/2016/04/20110721-Acurate-Robotic-3D-Vision-Webinar.pdf)

+ ROS
    + [The Robot Operating System (ROS)](http://www.ros.org/)
        + [ROS wiki](http://wiki.ros.org/)
    + Planning
        + [MoveIt! motion planning](http://moveit.ros.org/)
        + [The Open Motion Planning Library](http://ompl.kavrakilab.org/)

          OMPL.app has the following required dependencies:

              * [Boost](http://www.boost.org) (version 1.54 or higher)
              * [CMake](http://www.cmake.org) (version 2.8.7 or higher)
              * [Assimp](http://assimp.org)
              * [FCL](https://github.com/flexible-collision-library/fcl)
              
              OMPL.app's build system will attempt to automatically download and build
              Assimp and FCL if not already installed.
              
              The following dependencies are optional:
              
              * [PyQt](http://www.riverbankcomputing.co.uk/software/pyqt/download5) (for GUI)
              * [PyOpenGL](http://pyopengl.sourceforge.net/) (for GUI)
              * [Py++](https://bitbucket.org/ompl/ompl/src/tip/doc/markdown/installPyPlusPlus.md) (needed to generate Python bindings)
              * [ODE](http://ode.org) (needed to compile support for planning using the Open Dynamics Engine)
              * [Doxygen](http://www.doxygen.org) (needed to create a local copy of the documentation at
                http://ompl.kavrakilab.org)
              * [Eigen](http://eigen.tuxfamily.org) (needed for an informed sampling technique to improve the optimization of path length and for the Vector Field RRT planner)

    + ROS web
        + [Web based supervisory system for ROS](https://github.com/EESC-LabRoM/rosweb)
        + [Rosbridge provides a JSON API to ROS functionality for non-ROS programs. There are a variety of front ends that interface with rosbridge, including a WebSocket server for web browsers to interact with.](http://wiki.ros.org/rosbridge_suite)
        + [A web-based control center for ROS robots](https://github.com/pantor/ros-control-center)
            + [Settings](https://pantor.github.io/ros-control-center/#!/settings)
        + [Web Applications for Robots using rosbridge](https://cs.brown.edu/research/pubs/theses/masters/2012/lee.pdf)
        + [robot web tools is a collection of open-source modules and tools for building web-based robot apps](http://robotwebtools.org/)

+ rust
    + https://tessel.io/
    + https://www.slideshare.net/AndyGrove1/rust-is-for-robots
    + https://users.rust-lang.org/t/rust-for-embedded-development-where-we-are-and-whats-missing/10861
    + https://github.com/robotrs/rust-wpilib
        https://kylestach1678.github.io/2017/01/03/rust-for-robotics-part-0-introduction.html
    + https://crates.io/crates/wpilib-hal

+ Point Cloud Library
    https://github.com/PointCloudLibrary/pcl