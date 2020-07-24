# snapdragon and adreno tips

+ Qualcomm+Snapdragon
    + [Snapdragon 845 Mobile Platform](https://www.qualcomm.com/products/snapdragon-845-mobile-platform)
    + [FIRST Robotics](https://developer.qualcomm.com/hardware/first-robotics)
    + [Qualcomm Neural Processing SDK for AI](https://developer.qualcomm.com/software/qualcomm-neural-processing-sdk)
    + [Adreno GPU SDK](https://developer.qualcomm.com/software/adreno-gpu-sdk)
    + [FastCV Computer Vision SDK](https://developer.qualcomm.com/software/fastcv-sdk)
    + [Hexagon DSP SDK](https://developer.qualcomm.com/software/hexagon-dsp-sdk)
    + [Machine Vision SDK](https://developer.qualcomm.com/software/machine-vision-sdk)
        + [Snapdragon Flight VISLAM-ROS Sample Code](https://github.com/ATLFlight/ros-examples)
        + [Provides DFS ROS example for Snapdragon Flight](https://github.com/ATLFlight/dfs-ros-example)
    + [Qualcomm Math Library](https://developer.qualcomm.com/software/qualcomm-math-library)
    + [Snapdragon Profiler](https://developer.qualcomm.com/software/snapdragon-profiler)

+ Adreno
    + [OpenCL Optimization and Best Practices for Qualcomm Adreno GPUs](https://dl.acm.org/citation.cfm?id=3204935)
    + [Sub-optimal performance on Qualcomm Adreno GPUs](https://github.com/CNugteren/CLBlast/issues/228)
    + [Getting started with openCL on Adreno420 under linux](https://developer.qualcomm.com/forum/qdn-forums/software/adreno-gpu-sdk/34153)
    + [Qualcomm Adreno 630](https://www.notebookcheck.net/Qualcomm-Adreno-630-GPU.299832.0.html)
    + [How do I compute the GFLOPS of the Adreno 640 GPU?](https://www.quora.com/How-do-I-compute-the-GFLOPS-of-the-Adreno-640-GPU)
    + [open source driver project for adreno GPUs](https://github.com/freedreno/freedreno)
    + [Run OpenCL program on MOBILE GPU (Qualcomm & ARM)!](https://github.com/supernovaremnant/bazel-android-opencl)
        + [Compile OpenCL Program for Mobile GPU](https://sorrythenameistaken.blogspot.com/2018/06/compile-opencl-program-for-embedded-gpu.html)
            + [how to add `libOpenCL.so` to your project](https://github.com/googlesamples/android-ndk/blob/master/hello-libs/app/src/main/cpp/CMakeLists.txt)
    + [OpenCL Header/C++_Wrapper/Device Driver for SD820 Adreno 530, SD835 Adreno 540 on Android Phone](https://github.com/supernovaremnant/Android-OpenCL-Driver)
    + [How to Build & Use OpenCL on Android Studio](https://www.slideshare.net/noritsuna/how-to-build-use-opencl-on-android-studio)
    + [Setting Up OpenCL for OpenCV on Android, the full story](https://gist.github.com/iago-suarez/13c82b416ce6b07a93b5b6eee6bd29f3)
    + [Use OpenCL in Android camera preview based CV application](https://docs.opencv.org/trunk/d7/dbd/tutorial_android_ocl_intro.html)
        + [OpenCV-OpenCL-Android-Test-Drive](https://github.com/jingjieli/OpenCV-OpenCL-Android-Test-Drive)

    + [An experimental study of the Snapdragon 820 using an object detection algorithm](http://www.cs.man.ac.uk/~nobren/files/NunoNobre_TasterProjectReport.pdf)
    + [The State of OpenCL for Scientific Computing in 2018](https://mathema.tician.de/the-state-of-opencl-for-scientific-computing-in-2018/)

    + troubleshooting
        + [clGetDeviceInfo and clGetPlatformInfo fails in OpenCL with error code -30 (CL_INVALID_VALUE)](https://stackoverflow.com/questions/29290806/clgetdeviceinfo-and-clgetplatforminfo-fails-in-opencl-with-error-code-30-cl-in)

+ Profiling
    + [Capturing OpenCL applications in Snapdragon Profiler](https://www.youtube.com/watch?v=mevcqGF-jhc&feature=youtu.be)
    + [OpenCL Optimization 3 Profiling OpenCL](https://www.youtube.com/watch?v=S-alEZ7IZUQ&t=203s)
    + [A tool which profiles OpenCL devices to find their peak capacities](https://github.com/krrishnarraj/clpeak)

+ Computer Vision
    + [RSTensorFlow: GPU Enabled TensorFlow for Deep Learning on Commodity Android Devices](https://md2k.org/images/papers/methods/p7-alzantot.pdf)

+ [Arm NN Software Developer Kit (SDK)](developer.arm.com/ip-products/processors/machine-learning/arm-nn/)
    + [Arm NN ML software](https://github.com/arm-software/armnn)
    + [The ARM Computer Vision and Machine Learning library is a set of functions optimised for both ARM CPUs and GPUs using SIMD technologies.](https://github.com/arm-software/ComputeLibrary)
    + [Kirin980 tech specs](https://consumer.huawei.com/en/campaign/kirin980/)

+ **A**ndroid **O**pen **S**ource **P**roject
    + [Downloading the Android Source](https://source.android.com/setup/build/downloading)

+ Snapdragon Profiler troubleshooting
    + `brew cask install android-platform-tools`

+ Android Soong build system
    + [Soong Build System](https://source.android.com/setup/build/index)
    + [how Android soong/android.bp build works?](https://stackoverflow.com/questions/50264740/how-android-soong-android-bp-build-works)
        + [soong build system from AOSP tree](https://android.googlesource.com/platform/build/soong/)
        + [An experimental GNU make clone](https://github.com/google/kati)
        + [build_soong](https://github.com/derp-caf/build_soong)
        + [build_soong](https://github.com/UltraAOSP/build_soong)
        + [Blueprint Build System](https://github.com/google/blueprint)
            + [package blueprint](https://godoc.org/github.com/google/blueprint)
            + [blue print](https://android.googlesource.com/platform/build/blueprint)

+ Android Studio tips
    + [Build Your First Android App in Kotlin](https://codelabs.developers.google.com/codelabs/build-your-first-android-app-kotlin/index.html#0)
    + [Install and Create OpenCV project on Android Studio](https://www.youtube.com/watch?v=jN9Bv5LHXMk)
    + [OpenCV in Android Studio](https://stackoverflow.com/questions/27406303/opencv-in-android-studio)
        + [OpenCV on Android](https://opencv.org/platforms/android/)
        + [OpenCV4Android SDK](https://docs.opencv.org/2.4/doc/tutorials/introduction/android_binary_package/O4A_SDK.html)
            + [Добавление библиотеки OpenCV в проект Android Studio](https://habr.com/post/262089/)
        + [An Android Studio project which has a module that contains OpenCV SDK files ported and configured to use CMake](https://github.com/ahasbini/Android-OpenCV)
            + [Question: Native compilation failed](https://github.com/ahasbini/Android-OpenCV/issues/4)
        + [OpenCV For Android NDK](https://github.com/sjfricke/OpenCV-NDK)
            + [Error: package android.hardware.camera2 does not exist OpenCV](https://stackoverflow.com/questions/36204781/error-package-android-hardware-camera2-does-not-exist-opencv)
            + [Link STL library with Gradle CMake project](https://stackoverflow.com/questions/46106064/link-stl-library-with-gradle-cmake-project)    
            tl;dr
            for OpenCV for Android SDK use only deprecated `gnustl` that has only limited c++11 support, `c++` with c++17 support is incompatible    
            ```sh
            externalNativeBuild {
                cmake {
                    //arguments '-DANDROID_STL=c++_shared'
                    arguments '-DANDROID_STL=gnustl_static'
                    cppFlags "-fexceptions -frtti -std=c++11"
                }
            }
            ```
            + [C++ Runtime Libraries for Android](https://developer.android.com/ndk/guides/cpp-support)
            + [How to build executable ARM64-V8 program with OpenCL and fastcv for running on Android?](https://stackoverflow.com/questions/42313892/how-to-build-executable-arm64-v8-program-with-opencl-and-fastcv-for-running-on-a)
                + [https://stackoverflow.com/questions/43632700/clang-and-fuse-ld-gold-results-in-many-unused-option-warnings](https://stackoverflow.com/questions/43632700/clang-and-fuse-ld-gold-results-in-many-unused-option-warnings)
                tl;dr    
                ```cmake
                set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -fuse-ld=gold")

            + [undefined reference to `clCreateCommandQueueWithProperties'](https://github.com/fireice-uk/xmr-stak-amd/issues/40)
            tl;dr howto fix    
            ````c++
            #define CL_HPP_MINIMUM_OPENCL_VERSION 100
            #define CL_HPP_TARGET_OPENCL_VERSION  120
            
            #include <CL/cl2.hpp>
            ```

    + ARM64 Best Practices
        + [Best Practice Guide – ARM64, February 2019](http://www.prace-ri.eu/best-practice-guide-arm64/)
            + [Best Practice Guide - ARM64 . pdf](http://www.prace-ri.eu/IMG/pdf/Best-Practice-Guide-ARM64.pdf)

    + [Get device information (such as product, model) from adb command](https://stackoverflow.com/questions/22092118/get-device-information-such-as-product-model-from-adb-command)

    + [How to change clock frequency in Android?](https://stackoverflow.com/questions/4238959/how-to-change-clock-frequency-in-android)    
    ```sh    
    Set Governor:

    adb shell echo "userspace" > /sys/devices/system/cpu/cpu0/cpufreq/scaling_governor

    Set Frequency in KHz:

    adb shell su -c "echo "702000" > /sys/devices/system/cpu/cpu0/cpufreq/scaling_setspeed"
    //min frequency
    adb shell su -c "echo "384000" > /sys/devices/system/cpu/cpu0/cpufreq/scaling_min_freq"  
    //MAX frequency
    adb shell su -c "echo "384000" > /sys/devices/system/cpu/cpu0/cpufreq/scaling_max_freq" 

    Get current CPU Frequency:

    adb shell cat /sys/devices/system/cpu/cpu0/cpufreq/cpuinfo_cur_freq

    Show availables governors:

    adb shell su -c "cat /sys/devices/system/cpu/cpu0/cpufreq/scaling_available_governors"

    Disable service that overwrite cpu online file:

    adb shell su -c "stop mpdecision" 

    It's necessary to do this before enabling or disabling core. mp decision is restarted if the system is restarted.

    Disable core:

    adb shell su -c "echo "0" > /sys/devices/system/cpu/cpu3/online"

    If that doesn't work:

    & chmod 444 /sys/devices/system/cpu/cpu1/online
    ```

    + switch off SELinux    
    ```sh
    adb shell "setenforce 0"
    ```
        + [Understanding and resolving SELinux denials on Android](https://msfjarvis.dev/posts/understanding-and-resolving-selinux-denials-on-android/)


    + [What does 'adb remount' do? When is it useful?](https://stackoverflow.com/questions/28961572/what-does-adb-remount-do-when-is-it-useful/28961646#28961646)    
    ```sh
    adb remount
    ```


    + [How to read cpu frequency on android device](https://stackoverflow.com/questions/3021054/how-to-read-cpu-frequency-on-android-device)    
        tl;dr    
        ```sh
        cat /sys/devices/system/cpu/cpu0/cpufreq/stats/time_in_state
        ```

    + [ADB Install Fails With INSTALL_FAILED_TEST_ONLY](https://stackoverflow.com/questions/25274296/adb-install-fails-with-install-failed-test-only)    
        tl;dr    
        ```sh
        adb install -t hello.apk
        ```
    + [adb useful commands list](https://gist.github.com/Pulimet/5013acf2cd5b28e55036c82c91bd56d8)    
    tl;dr some useful commands
    ```sh
    == Screenshot
    adb shell screencap -p /sdcard/screenshot.png
    
    $ adb shell
    shell@ $ screencap /sdcard/screen.png
    shell@ $ exit
    $ adb pull /sdcard/screen.png
    
    ---
    adb shell screenrecord /sdcard/NotAbleToLogin.mp4
    
    $ adb shell
    shell@ $ screenrecord --verbose /sdcard/demo.mp4
    (press Control + C to stop)
    shell@ $ exit
    $ adb pull /sdcard/demo.mp4
    ```

    + [Установка android tools (ADB,fastboot, QTADB) на Debian/Ubuntu/Linux Mint](http://linux-notes.org/ustanovka-android-tools-adb-fastboot-qtadb-na-debian-ubuntu-linux-mint/)

    + [android-ndk archives](https://github.com/android-ndk/ndk/wiki)
    + [Insufficient permissions for device in Android Studio Workspace](https://stackoverflow.com/questions/28704636/insufficient-permissions-for-device-in-android-studio-workspace-running-in-opens)
    tl;dr    
    ```sh
    adb kill-server
    sudo adb start-server
    sudo adb devices
    ```

    + [ffplay has gone missing](https://discourse.brew.sh/t/ffplay-has-gone-missing/426)
    tl;dr    
    ```sh
    brew install ffmpeg --with-sdl2 to install ffplay
    ```

    + ARM Mali GPU
        + The Mali GPU: An Abstract Machine
            + [GPU Architecture Introduction](https://developer.samsung.com/game/gpu-architecture)
                + [Part 1 - Frame Pipelining](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/the-mali-gpu-an-abstract-machine-part-1---frame-pipelining)
                + [Part 2 - Tile-based Rendering](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/the-mali-gpu-an-abstract-machine-part-2---tile-based-rendering)
                + [Part 3 - The Midgard Shader Core](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/the-mali-gpu-an-abstract-machine-part-3---the-midgard-shader-core)
                + [Part 4 - The Bifrost Shader Core](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/the-mali-gpu-an-abstract-machine-part-4---the-bifrost-shader-core)
            + [Mali Performance 1: Checking the Pipeline](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/mali-performance-1-checking-the-pipeline)
            + [Mali Performance 2: How to Correctly Handle Framebuffers](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/mali-performance-2-how-to-correctly-handle-framebuffers)
            + [Mali Performance 3: Is EGL_BUFFER_PRESERVED a good thing?](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/mali-performance-3-is-egl_5f00_buffer_5f00_preserved-a-good-thing)
        + [ARM Mali GPU OpenGL ES Application Optimization Guide](https://developer.arm.com/docs/dui0555/b/introduction/about-optimization)
            + [ARM® Mali GPU Version: 3.0 OpenGL ES Application Optimization Guide](http://infocenter.arm.com/help/topic/com.arm.doc.dui0555c/DUI0555C_mali_optimization_guide.pdf)
            + [Accelerating Mali GPU analysis using Arm Mobile Studio](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/accelerating-mali-gpu-analysis-using-arm-mobile-studio)
            + [Touch/GPU profiling/Mali](https://wiki.ubuntu.com/Touch/GPU%20profiling/Mali)
                + [high res timer](https://github.com/ARM-software/gator/blob/master/hrtimer_module/hrtimer_module.c)
            + [events-Mali-TNOx_hw](https://github.com/ARM-software/gator/blob/master/daemon/events-Mali-TNOx_hw.xml)
                + [Mali Midgard Family Performance Counters](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/mali-midgard-family-performance-counters)
                + [Mali Bifrost Family Performance Counters](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/mali-bifrost-family-performance-counters)
                + [Understanding Mali GPU Hardware Counters](https://community.arm.com/developer/tools-software/graphics/f/discussions/8607/understanding-mali-gpu-hardware-counters)
                    + [GL_EXT_disjoint_timer_query for performance](https://community.arm.com/developer/tools-software/graphics/f/discussions/6869/gl_ext_disjoint_timer_query-for-performance)
                + [Hardware counters on Arm Graphics Analyzer tool](https://community.arm.com/developer/tools-software/graphics/f/discussions/13614/hardware-counters-on-arm-graphics-analyzer-tool)
                    + [Graphics and Gaming](https://community.arm.com/developer/tools-software/graphics)
        + [Panfrost](https://github.com/Panfrost)
        + [GDC 2014: Performance Analysis and Optimization (Lorenzo Dal Col, ARM)](https://www.youtube.com/watch?v=AAr-pt8S28M)
            + [Performance Analysis and Debug Tools for Mobile Games (Presented by ARM)](https://www.gdcvault.com/play/1020632/Performance-Analysis-and-Debug-Tools)
            + [GPU Compute Optimisation with Hardware Counters](https://www.youtube.com/watch?v=93cWfkyid7k)
        + [Arm Mali Graphics Debugger](https://developer.samsung.com/game/arm-mali)
            + [Arm Mobile Studio](https://developer.arm.com/tools-and-software/graphics-and-gaming/arm-mobile-studio)
                + [Using Mali Graphics Debugger on a Non-rooted device](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/using-mali-graphics-debugger-on-a-non-rooted-device)
                + [Improving data performance with Arm Streamline 7.1](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/improving-data-performance-with-streamline)

+ [Real Time For the Masses](https://rtfm.rs/0.5/book/en/)
    + [Real Time For the Masses: Organization for the RTFM scheduler and ecosystem](https://github.com/rtfm-rs)

+ [jsoncpp-android](https://github.com/leokwu/jsoncpp-android)

+ [Tools and information for the Broadcom VideoCore IV (RaspberryPi)](https://github.com/hermanhermitage/videocoreiv)
    + [Broadcom VideoCore-IV vs ARM Mali-T880 MP4](https://www.notebookcheck.net/VideoCore-IV-vs-Mali-T880-MP4_4017_7170.247598.0.html)
    + [Operating System development tutorials in Rust on the Raspberry Pi](https://github.com/rust-embedded/rust-raspberrypi-OS-tutorials)

