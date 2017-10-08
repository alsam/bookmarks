# Industrial Robotics

+ Intro
    + [Industrial robot](https://en.wikipedia.org/wiki/Industrial_robot)
      + abbrevs.
      + **TCP** - **T**ool **C**entral **P**oint
    + [Lectures on Robotic Planning and Kinematics](http://motion.me.ucsb.edu/book-lrpk/)
    + MIT Introduction to Robotics
        + [Lecture Notes](https://ocw.mit.edu/courses/mechanical-engineering/2-12-introduction-to-robotics-fall-2005/lecture-notes/)
        + [Download](https://ocw.mit.edu/courses/mechanical-engineering/2-12-introduction-to-robotics-fall-2005/download-course-materials/)
        + [Chapter 4: Planar Kinematics](https://ocw.mit.edu/courses/mechanical-engineering/2-12-introduction-to-robotics-fall-2005/lecture-notes/chapter4.pdf)
    + [A Mathematical Introduction to Robotic Manipulation](http://www.cds.caltech.edu/~murray/books/MLS/pdf/mls94-complete.pdf)
    + [DISTANCE-BASED FORMULATIONS FOR THE POSITION ANALYSIS OF KINEMATIC CHAINS](http://www.tdx.cat/bitstream/handle/10803/83516/TNRL1de1.pdf)
    + [robotics-315](http://thydzik.com/academic/robotics-315/index.php)
        + [UWA course robotics-315](http://thydzik.com/academic/robotics-315/portfolio/)

+ robot camera calibration
    + [High-Precision Calibration Approaches to Robot Vision Systems](https://tams.informatik.uni-hamburg.de/paper/2009/Fangwu_Shu_Dissertation_SUB.pdf)

    + [A Vision-Based Self-Calibration Method for Robotic Visual
Inspection Systems](http://www.mdpi.com/1424-8220/13/12/16565/pdf)

    + [Robot Calibration: Modeling Measurement and Applications ](http://cdn.intechopen.com/pdfs/258/InTech-Robot_calibration_modeling_measurement_and_applications.pdf)

    + [Accurate Robotic 3D Vision](http://universallogic.com/wp-content/uploads/2016/04/20110721-Acurate-Robotic-3D-Vision-Webinar.pdf)

+ ROS
    + [The Robot Operating System (ROS)](http://www.ros.org/)
        + [ROS wiki](http://wiki.ros.org/)
        + [ROS intro](http://www.uio.no/studier/emner/matnat/ifi/INF3480/v17/timeplan/lecturenotes/inf3480---ros---spring-2017---simplified.pdf
        + [Messages and Topics: Communicating between nodes](https://github.com/fp-robotics/myp_ros/wiki/Messages-and-Topics:-Communicating-between-nodes)
            + [ROS simple_message](http://wiki.ros.org/simple_message)
                + [industrial::typed_message::TypedMessage Class Reference](http://docs.ros.org/jade/api/simple_message/html/classindustrial_1_1typed__message_1_1TypedMessage.html)
        + [ROS callbacks, threads and spinning](https://answers.ros.org/question/53055/ros-callbacks-threads-and-spinning/)
            + [roscppOverviewCallbacks and Spinning](http://wiki.ros.org/roscpp/Overview/Callbacks%20and%20Spinning)
                + [Significance of ros::spinOnce()](https://answers.ros.org/question/11887/significance-of-rosspinonce/)
                + [What is spinOnce() used for in ROS?](https://www.quora.com/What-is-spinOnce-used-for-in-ROS)
                + [ROS Nodelet receive and processing in parallel](https://answers.ros.org/question/259725/ros-nodelet-receive-and-processing-in-parallel/)
                    + [ROS nodelet](http://wiki.ros.org/nodelet)
                    + [Nodelet Everything](http://www.clearpathrobotics.com/assets/guides/ros/Nodelet%20Everything.html)
                + [ROS device drivers](https://github.com/ros-drivers)
                    + [ROS fanuc driver](https://github.com/ros-industrial/fanuc/tree/indigo-devel/fanuc_driver)
            + [Threaded Applications with the roscpp API](https://vimeo.com/123502207)
                + [This is a simple controller built with ROS and Qt5 libraries](https://github.com/allenh1/ros-qt-controller)
                + [Tasks and Scheduling in the context of ROS](https://courses.cs.washington.edu/courses/cse466/11au/calendar/11-TasksAndScheduling.pdf)
            + [ROS industrial motoman meta package](https://github.com/ros-industrial/motoman)

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

+ building ROS with moveIt on arch linux
    + install octomap
    ```
    yaourt -S aur/octomap
    in PKGBUILD change pkgversion from 1.7.0 to 1.8.1
    fix sha256
    ```
    + install fcl with octomap support
    ```sh
    yaourt -S aur/fcl
    in PKGBUILD change pkgversion from 0.4.0 to 0.5.0
    fix sha256
    check less /usr/include/fcl/config.h has octomap support with octomap version > 1.8.0
    ```
        + [C++11 error on ROS buildfarm for kinetic](https://github.com/ros-planning/geometric_shapes/issues/49)
        + [issue: Dependencies on fcl->octomap](https://github.com/ros-planning/moveit_core/issues/299)
        + [fcl 0.5 release with octomap 1.8 support](https://github.com/flexible-collision-library/fcl/issues/137)
    + install `yaourt -S aur/ros-kinetic-opencv3`
    ```sh
    export CC=/usr/bin/gcc-5
    export CXX=/usr/bin/g++-5

    diff -u /etc/makepkg.conf.ORIG /etc/makepkg.conf 
    --- /etc/makepkg.conf.ORIG	2017-07-04 12:29:42.000000000 +0300
    +++ /etc/makepkg.conf	2017-10-06 01:19:20.550612564 +0300
    @@ -37,8 +37,8 @@
     # -march (or -mcpu) builds exclusively for an architecture
     # -mtune optimizes for an architecture, but builds for whole processor family
     CPPFLAGS="-D_FORTIFY_SOURCE=2"
    -CFLAGS="-march=x86-64 -mtune=generic -O2 -pipe -fstack-protector-strong -fno-plt"
    -CXXFLAGS="-march=x86-64 -mtune=generic -O2 -pipe -fstack-protector-strong -fno-plt"
    +CFLAGS="-march=x86-64 -mtune=generic -O2 -pipe -fstack-protector-strong"
    +CXXFLAGS="-march=x86-64 -mtune=generic -O2 -pipe -fstack-protector-strong"
    ```
        + i.e. remove `-fno-plt` for `CFLAGS`, `CXXFLAGS` in `/etc/makepkg.conf` temporary
        + [ AUR Issues, Discussion & PKGBUILD Requests» gcc: error: unrecognized command line option ‘-fno-plt’](https://bbs.archlinux.org/viewtopic.php?id=228332)
        + [Build error: GCC-5 fail on "-fno-plt" flag](https://www.reddit.com/r/archlinux/comments/6nxxre/build_error_gcc5_fail_on_fnoplt_flag/)

    ```sh
    yaourt -S aur/ros-kinetic-core --noconfirm
    yaourt -S aur/ros-kinetic-desktop --noconfirm
    yaourt -S aur/ros-kinetic-desktop-full --noconfirm
    yaourt -S aur/ros-kinetic-moveit-core --noconfirm
    yaourt -S aur/ros-kinetic-moveit --noconfirm
    ```

    + [rosdep install fails on Archlinux](https://github.com/ros-infrastructure/rosdep/issues/395)
        + [ROS Kinetic Installing from source](http://wiki.ros.org/kinetic/Installation/Source)
            + [Catkin fails on osx 10.9, can't find '__main__' module in empy-3.1-py2.7.egg/em.pyc ; on arch linux fails as well](https://answers.ros.org/question/100741/catkin-fails-on-osx-109-cant-find-__main__-module-in-empy-31-py27eggempyc/)
        + [Ros Build System code gists](https://codegists.com/code/ros-build-system/)

+ rust
    + ROS
        + [Awesome Rust for Robotics](http://robotics.rs/)
        + [Urdf-viz: URDF file viewer](http://ros-users.122217.n3.nabble.com/Discourse-ros-org-ROS-Projects-Urdf-viz-URDF-file-viewer-td4025049.html)
            tl;dr links to
                + [kinematics](https://github.com/OTL/k)
                + [urdf loader](https://github.com/OTL/urdf-rs)
                + [visualizer](https://github.com/OTL/urdf-viz)
                + [rrt](https://github.com/OTL/rrt)
                + [OTL repositories](https://github.com/OTL?tab=repositories)
            in Rust
        + [adnanademovic repositories](https://github.com/adnanademovic?tab=repositories)
            + [Pure Rust implementation of a ROS client library](https://github.com/adnanademovic/rosrust)
            + [A pure Rust implementation of xml-rpc](https://github.com/adnanademovic/xml-rpc-rs)
            + [Serde ROSMSG](https://github.com/adnanademovic/serde_rosmsg)
    + Haptics
        + [Haptics Group Research: Surface Texture Perception](https://alexburka.com/penn/proton.php)
            + [video explaining haptic prototype](https://alexburka.com/penn/proton/icra_video.mp4)
            + [durka repositories](https://github.com/durka?tab=repositories)
                + [A rust **cool** library for indicating progress in command line applications to users](https://github.com/mitsuhiko/indicatif)
    + Backup
        + https://tessel.io/
        + https://www.slideshare.net/AndyGrove1/rust-is-for-robots
        + https://users.rust-lang.org/t/rust-for-embedded-development-where-we-are-and-whats-missing/10861
        + https://github.com/robotrs/rust-wpilib
            https://kylestach1678.github.io/2017/01/03/rust-for-robotics-part-0-introduction.html
        + https://crates.io/crates/wpilib-hal

+ Point Cloud Library
    https://github.com/PointCloudLibrary/pcl

+ GA for robotics
    + [Geometric Algebra for Modeling in Robot Physics](http://www.beck-shop.de/fachbuch/leseprobe/9781848829282_Excerpt_002.pdf)

+ Misc
    + [JoelBurdick list for robotics](http://robotics.caltech.edu/wiki/index.php/JoelBurdick)
    + [Работа с SLAM в ROS на Raspberry Pi 3 на примере hector_slam](https://se7en.ws/rabota-s-slam-v-ros-na-raspberry-pi-3-na-primere-hector_slam/)
