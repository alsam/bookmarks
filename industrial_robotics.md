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

+ Forward and Inverse Kinematics
    + [Transformation Matrices Part 1](https://www.youtube.com/watch?v=I7Xvchh0L_4&list=PLB46C8B9857C32201)
    + [Transformation Matrices Part 2](https://www.youtube.com/watch?v=Vt_pSfVcrhI&index=2&list=PLB46C8B9857C32201)
    + [Transformation Matrices Part 3](https://www.youtube.com/watch?v=3zeMsf0vcs4&list=PLB46C8B9857C32201&index=3)
    + [Forward and Inverse Kinematics Part 1](https://www.youtube.com/watch?v=VjsuBT4Npvk)
    + [Forward and Inverse Kinematics Part 2](https://www.youtube.com/watch?v=3ZcYSKVDlOc)
    + [Forward and Inverse Kinematics Part 3](https://www.youtube.com/watch?v=llUBbpWVPQE&index=6&list=PLB46C8B9857C32201)
    + [Velocity, Force and the Jacobian Part 1](https://www.youtube.com/watch?v=g_Nl4iPd1jI&list=PLB46C8B9857C32201&index=7)
    + [Velocity, Force and the Jacobian Part 2](https://www.youtube.com/watch?v=5DJ10praEZ8&list=PLB46C8B9857C32201&index=8)
    + [Velocity, Force and the Jacobian Part 3](https://www.youtube.com/watch?v=nT3kms4pbKw&list=PLB46C8B9857C32201&index=9)
    + [Velocity, Force and the Jacobian Part 4](https://www.youtube.com/watch?v=3CbyOt32nrY&list=PLB46C8B9857C32201&index=10)
        + [milfordrobotics](https://www.youtube.com/channel/UCD2zDJK8c5Is7StyjWku6zw)
        + [ENB339 Introduction to Robotics](https://wiki.qut.edu.au/display/cyphy/ENB339+Introduction+to+Robotics)
        + [Introduction to Robotics (ENB339) Lecture Notes](https://www.studocu.com/en/document/queensland-university-of-technology/introduction-to-robotics/lecture-notes/lecture-notes-week-9-13/332743/view?auth=0&auth_prem=0&prem_doc=0&new_title=0&has_flashcards=0)

+ robot camera calibration
    + [High-Precision Calibration Approaches to Robot Vision Systems](https://tams.informatik.uni-hamburg.de/paper/2009/Fangwu_Shu_Dissertation_SUB.pdf)

    + [A Vision-Based Self-Calibration Method for Robotic Visual
Inspection Systems](http://www.mdpi.com/1424-8220/13/12/16565/pdf)

    + [Robot Calibration: Modeling Measurement and Applications ](http://cdn.intechopen.com/pdfs/258/InTech-Robot_calibration_modeling_measurement_and_applications.pdf)

    + [Accurate Robotic 3D Vision](http://universallogic.com/wp-content/uploads/2016/04/20110721-Acurate-Robotic-3D-Vision-Webinar.pdf)

+ ROS
    + [Introduction to the Robot Operating System (ROS) Middleware - Mike Anderson, The PTR Group, Inc.](https://www.youtube.com/watch?v=yWtGUk3PBms)
    + [The Robot Operating System (ROS)](http://www.ros.org/)
        + [ROS wiki](http://wiki.ros.org/)
        + [ROS intro](http://www.uio.no/studier/emner/matnat/ifi/INF3480/v17/timeplan/lecturenotes/inf3480---ros---spring-2017---simplified.pdf)
        + [Programming for Robotics (ROS) Course 1](https://www.youtube.com/watch?v=0BxVPCInS3M)
            + [Programming for Robotics - ROS](http://www.rsl.ethz.ch/education-students/lectures/ros.html)
                + [Programming for Robotics - ROS - lecture 1](https://www.ethz.ch/content/dam/ethz/special-interest/mavt/robotics-n-intelligent-systems/rsl-dam/ROS2017/lecture1.pdf)
            + [ROS Best Practices from ETHZ](https://github.com/ethz-asl/ros_best_practices/wiki)
                + [ROS Design Patterns](https://courses.cs.washington.edu/courses/cse466/11au/calendar/ros_cc_2_patterns.pdf)
                + [ROS Best Practices](http://robohow.eu/_media/meetings/first-integration-workshop/ros-best-practices.pdf)
                + How to set debug level: from rosconsole](http://wiki.ros.org/rosconsole)
                    + tl;dr
                    ```c++
                    #include <ros/console.h>
                    if( ros::console::set_logger_level(ROSCONSOLE_DEFAULT_NAME,
                        ros::console::levels::Debug) ) {
                       ros::console::notifyLoggerLevelsChanged();
                    }
                    ```
            + [A set of solutions to ETHZ ROS lectures](https://github.com/luym11/ros_practise)
        + [Messages and Topics: Communicating between nodes](https://github.com/fp-robotics/myp_ros/wiki/Messages-and-Topics:-Communicating-between-nodes)
            + [ROS simple_message](http://wiki.ros.org/simple_message)
                + [industrial::typed_message::TypedMessage Class Reference](http://docs.ros.org/jade/api/simple_message/html/classindustrial_1_1typed__message_1_1TypedMessage.html)
        + [ROS callbacks, threads and spinning](https://answers.ros.org/question/53055/ros-callbacks-threads-and-spinning/)
            + [roscppOverviewCallbacks and Spinning](http://wiki.ros.org/roscpp/Overview/Callbacks%20and%20Spinning)
                + [Significance of ros::spinOnce()](https://answers.ros.org/question/11887/significance-of-rosspinonce/)
                + [What is spinOnce() used for in ROS?](https://www.quora.com/What-is-spinOnce-used-for-in-ROS)
                    + [Difference between spin and rate.sleep in ROS](https://stackoverflow.com/questions/23227024/difference-between-spin-and-rate-sleep-in-ros)
                + [ROS Nodelet receive and processing in parallel](https://answers.ros.org/question/259725/ros-nodelet-receive-and-processing-in-parallel/)
                    + [ROS nodelet](http://wiki.ros.org/nodelet)
                    + [Nodelet Everything](http://www.clearpathrobotics.com/assets/guides/ros/Nodelet%20Everything.html)
                + [ROS device drivers](https://github.com/ros-drivers)
                    + [ROS fanuc driver](https://github.com/ros-industrial/fanuc/tree/indigo-devel/fanuc_driver)
                    + [ROS-Industrial Robot Driver Specification (Final)](http://wiki.ros.org/Industrial/Industrial_Robot_Driver_Spec)
            + [Threaded Applications with the roscpp API](https://vimeo.com/123502207)
                + [This is a simple controller built with ROS and Qt5 libraries](https://github.com/allenh1/ros-qt-controller)
                + [Tasks and Scheduling in the context of ROS](https://courses.cs.washington.edu/courses/cse466/11au/calendar/11-TasksAndScheduling.pdf)
            + [ROS industrial motoman meta package](https://github.com/ros-industrial/motoman)

    + Planning
        + [MoveIt! motion planning](http://moveit.ros.org/)
        + [The Open Motion Planning Library](http://ompl.kavrakilab.org/)
        + [The MoveIt! Motion Planning Framework](https://github.com/ros-planning/moveit)
            + [ROS Planning](https://github.com/ros-planning)

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


    + ROS transport level protocol
        + [convenient cross-reference](http://code.metager.de/source/xref/ros/comm/clients/cpp/roscpp/include/ros/transport/)
        + [github repository for transport level protocol](https://github.com/strawlab/ros_comm/tree/master/clients/cpp/roscpp/include/ros/transport)
        + [Robot Communication Protocol from JBC](http://www.jbctools.com/pdf/robot_communication_protocol.pdf)
        + TCP backup
            + [Chapter 2. The Transport Layer: TCP, UDP, and SCTP](https://notes.shichao.io/unp/ch2/)
                + [Chapter 4. Elementary TCP Sockets](https://notes.shichao.io/unp/ch4/)
            + [«Boost.Asio C++ Network Programming». Глава 4: Клиент и Сервер](https://habrahabr.ru/post/195794/)
            + [Boost.Asio C++ Network Programming examples](http://www.boost.org/doc/libs/1_65_1/doc/html/boost_asio/examples/cpp11_examples.html)
            + [SOCKETS - SERVER & CLIENT C++ - 2017](http://www.bogotobogo.com/cplusplus/sockets_server_client.php#block_vs_non_blocking)
            + [Error : “Transport endpoint is already connected”](https://stackoverflow.com/questions/7140438/error-transport-endpoint-is-already-connected)
                + [Socket program gives “Transport endpoint is already connected” error](https://stackoverflow.com/questions/9873650/socket-program-gives-transport-endpoint-is-already-connected-error)
                + [Reconnecting with connect() on restarted server returns -Transport endpoint is already connected](https://stackoverflow.com/questions/16910973/reconnecting-with-connect-on-restarted-server-returns-transport-endpoint-is-a)

    + ROS web
        + [Web based supervisory system for ROS](https://github.com/EESC-LabRoM/rosweb)
        + [Rosbridge provides a JSON API to ROS functionality for non-ROS programs. There are a variety of front ends that interface with rosbridge, including a WebSocket server for web browsers to interact with.](http://wiki.ros.org/rosbridge_suite)
        + [A web-based control center for ROS robots](https://github.com/pantor/ros-control-center)
            + [Settings](https://pantor.github.io/ros-control-center/#!/settings)
        + [Web Applications for Robots using rosbridge](https://cs.brown.edu/research/pubs/theses/masters/2012/lee.pdf)
        + [robot web tools is a collection of open-source modules and tools for building web-based robot apps](http://robotwebtools.org/)

    + [How to Roslaunch Nodes in Valgrind or GDB](http://wiki.ros.org/roslaunch/Tutorials/Roslaunch%20Nodes%20in%20Valgrind%20or%20GDB)
    tl;dr
    ```
    <node pkg="planning_servers" launch-prefix="xterm -e cgdb --args" name="mainserver" type="mainserver_node"
    ...
    ```

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

    + [Snapcraft builds for ROS](https://docs.snapcraft.io/build-snaps/ros)
        + [Install snapd on Arch Linux](https://docs.snapcraft.io/core/install-arch-linux)
        + [Install snapd on Ubuntu](https://docs.snapcraft.io/core/install-ubuntu)

    + [rosdep install fails on Archlinux](https://github.com/ros-infrastructure/rosdep/issues/395)
        + [ROS Kinetic Installing from source](http://wiki.ros.org/kinetic/Installation/Source)
            + [Catkin fails on osx 10.9, can't find '__main__' module in empy-3.1-py2.7.egg/em.pyc ; on arch linux fails as well](https://answers.ros.org/question/100741/catkin-fails-on-osx-109-cant-find-__main__-module-in-empy-31-py27eggempyc/)
            tl;dr a confusion between pyhon packages `em` and `empy`
            ```sh
            sudo pip uninstall em
            sudo pip install empy
            rosinstall_generator desktop --rosdistro kinetic --deps --wet-only --tar > kinetic-desktop-wet.rosinstall
            rosinstall_generator industrial_core --rosdistro kinetic --deps --wet-only --tar >> kinetic-desktop-wet.rosinstall
            wstool init -j8 src kinetic-desktop-full-wet.rosinstall
            wstool update -j 4 -t src
            #rosdep install --from-paths src --ignore-src --rosdistro kinetic -y
            ./src/catkin/bin/catkin_make_isolated --install -DCMAKE_BUILD_TYPE=Debug --make-args VERBOSE=1
            ...
              Could not find a package configuration file provided by "console_bridge"
            ...
            ```
                + [ROS `console_bridge`](http://wiki.ros.org/console_bridge)
            ```sh
            Poco was not found
            sudo apt-get install libpoco-dev
            sudo apt-get install libpocofoundation9v5-dbg
            with Arch Linux many annoying errors; quick-n-dirty fixes to link.txt add -lPocoNet -lPocoUtil
            ```
            + `opencv3` build: see above on `yaourt -S aur/ros-kinetic-opencv3` and in `opencv3/cmake/OpenCVPCHSupport.cmake`
            ```cmake
            SET(_PCH_include_prefix "-I")
            #SET(_PCH_isystem_prefix "-isystem")
            SET(_PCH_isystem_prefix "-I")
            ```
            as workaround for [Source compile of Kinetic on Fedora24](https://answers.ros.org/question/236227/source-compile-of-kinetic-on-fedora24/); symptoms:
            ```sh
            cstdlib:75:25: fatal error: stdlib.h: No such file or directory
             #include_next <stdlib.h>
            ```
            + [ROS package collada_parser: dae.h not found](https://answers.ros.org/question/136881/package-collada_parser-daeh-not-found/)
            + [get perception_pcl building on kinetic](https://github.com/ros-perception/perception_pcl/issues/119)
            + [kinetic-devel does not build on 16.04](https://github.com/ros-planning/navigation/issues/456)
            + [cmake error, poco was not found, Raspberry Pi, ROS Indigo](https://answers.ros.org/question/204532/cmake-error-poco-was-not-found-raspberry-pi-ros-indigo/)
            + sip: Unable to find file "QtCore/QtCoremod.sip"
                + [sip: Unable to find file "QtCore/QtCoremod.sip"](https://github.com/wbsoft/python-poppler-qt5/issues/17)
                + [Problem during compilation of ROS INDIGO on ARM/Ubuntu trusty from source](https://answers.ros.org/question/187851/problem-during-compilation-of-ros-indigo-on-armubuntu-trusty-from-source/)
                + [trying to install ROS from source on UBUNTU 13.10](https://answers.ros.org/question/98016/trying-to-install-ros-from-source-on-ubuntu-1310/)
            + [No module named defusedxml.xmlrpc](https://answers.ros.org/question/260377/no-module-named-defusedxmlxmlrpc/)
              + when executing command `roslaunch ...`
              ```sh
              sudo apt-get install python-defusedxml
              ```
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

+ [Point Cloud Library](https://github.com/PointCloudLibrary/pcl)

+ GA for robotics
    + [Geometric Algebra for Modeling in Robot Physics](http://www.beck-shop.de/fachbuch/leseprobe/9781848829282_Excerpt_002.pdf)

+ [Artificial Intelligence for Robotics by Georgia Institute of Technology Georgia Tech](https://www.udacity.com/course/artificial-intelligence-for-robotics--cs373)
    + [intro to Artificial Intelligence for Robotics](https://www.class-central.com/mooc/319/udacity-artificial-intelligence-for-robotics#)
    + [A python cheat sheet containing the basics needed for the course Artificial Intelligence for Robotics](https://github.com/ethz-asl/ai_for_robotics)
    + [Solution to the programming assignments in Artificial Intelligence For Robotics by Udacity](https://github.com/biodunalfet/Artificial-Intelligence-For-Robotics)

+ [RobOptim is a Modern, Open-Source, C++ Library for Numerical Optimization applied to Robotics](http://roboptim.net/index.html)
    + [RobOptim](https://github.com/roboptim)
    + [roboptim-tutorial](https://github.com/roboptim/roboptim-tutorial)

+ Protocols verification
    + [Design and Validation of Computer Protocols](http://spinroot.com/gerard/popd.html)
    + [Specifying Systems: The TLA+ Language and Tools for Hardware and Software Engineers](http://lamport.azurewebsites.net/tla/book.html#download)
    + [Yet another explicit state model checker](https://github.com/Smattr/rumur)
    + [SPIN An explicit state model checker](http://www.cs.cmu.edu/~emc/15-398/lectures/SPIN-LTL.pdf)


+ Misc
    + [Stanford Artificial Intelligence Laboratory](https://ai.stanford.edu/)
        + [Garrett Thomas papers on robotics and ML](https://ai.stanford.edu/~gwthomas/)
    + [JoelBurdick list for robotics](http://robotics.caltech.edu/wiki/index.php/JoelBurdick)
    + [Работа с SLAM в ROS на Raspberry Pi 3 на примере hector_slam](https://se7en.ws/rabota-s-slam-v-ros-na-raspberry-pi-3-na-primere-hector_slam/)
    + [OpenRAVE provides an environment for testing, developing, and deploying motion planning algorithms in real-world robotics application](http://openrave.org/)
    + [YARP stands for Yet Another Robot Platform](http://www.yarp.it/)
        + [CUDADeviceDriver.cpp](http://www.yarp.it/CUDADeviceDriver_8cpp.html)
        + [yarp-wholebodyinterface](https://github.com/robotology/yarp-wholebodyinterface/tree/master/app/robots)
        + [YARP: Port and connection protocols](http://www.yarp.it/yarp_protocol.html)
    + [Robotic Humanoid hand](https://discourse.ros.org/t/robotic-humanoid-hand/188)
    + [ROBOTIS-MANIPULATOR-H](http://wiki.ros.org/ROBOTIS-MANIPULATOR-H)
        + [robotis_controller](https://github.com/ROBOTIS-GIT/ROBOTIS-Documents/wiki/robotis_controller)
        + [ROBOTIS Official Github](https://github.com/ROBOTIS-GIT)
    + [Plucker Coordinates for Lines in the Space∗](http://web.cs.iastate.edu/~cs577/handouts/plucker-coordinates.pdf)


