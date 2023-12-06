# snapdragon and adreno tips

+ ARM 64 Assembly series
    + [ARM 64 Assembly Series — Basic definitions and registers](https://valsamaras.medium.com/arm-64-assembly-series-basic-definitions-and-registers-ec8cc1334e40)
    + [ARM 64 Assembly Series — Offset and Addressing modes](https://valsamaras.medium.com/arm-64-assembly-series-offset-and-addressing-modes-aa48b65b4c99)
    + [ARM 64 Assembly Series — Load and Store](https://valsamaras.medium.com/arm-64-assembly-series-load-and-store-6bfe9c1d1896)
    + [ARM 64 Assembly Series — Branch](https://valsamaras.medium.com/arm-64-assembly-series-branch-9ce820987fc6)
    + [ARM 64 Assembly Series — Data Processing (Part 1)](https://valsamaras.medium.com/arm-64-assembly-series-data-processing-part-1-b6f6f877c56b)
    + [ARM 64 Assembly Series — Data Processing (Part 2)](https://valsamaras.medium.com/arm-64-assembly-series-data-processing-part-2-3d0526dc07b6)
    + [Practical ARM64 (selections and loops)](https://valsamaras.medium.com/practical-arm64-selections-and-loops-89f9a0e7e395)
    + [Practical ARM64 (Subroutines)](https://valsamaras.medium.com/practical-arm64-subroutines-1b5ea3935ff5)
    + [A Gentle Introduction to Assembly Language Programming](https://github.com/pkivolowitz/asm_book)
    + [What does the exclamation mark mean in the end of an A64 instruction?](https://stackoverflow.com/questions/39780289/what-does-the-exclamation-mark-mean-in-the-end-of-an-a64-instruction#:~:text=on%20this%20post.-,The%20!,the%20transfer%2C%20and%20is%20updated.)
    + [ARM Synchronization Primitives Development Article](https://developer.arm.com/documentation/dht0008/a/arm-synchronization-primitives/exclusive-accesses/exclusive-monitors)
    + [Exclusive Monitors](https://dynamorio.org/page_ldstex.html)
    + [Modelling the ARMv8 Architecture, Operationally: Concurrency and ISA](https://www.cl.cam.ac.uk/~pes20/popl16-armv8/top.pdf)
        + [rmem: Executable concurrency models for ARMv8, RISC-V, Power, and x86](https://github.com/rems-project/rmem)

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
    + [Using multicursor in Android Studio](http://kevinpelgrims.com/blog/2017/12/29/using-multicursor-in-android-studio/)
    + [Build Your First Android App in Kotlin](https://codelabs.developers.google.com/codelabs/build-your-first-android-app-kotlin/index.html#0)
        + [Introduction to Android Activities with Kotlin](https://www.raywenderlich.com/2705552-introduction-to-android-activities-with-kotlin)
        + [How to invoke external command from within Kotlin code?](https://stackoverflow.com/questions/35421699/how-to-invoke-external-command-from-within-kotlin-code)
        + [**How do I programmatically launch a specific application?**](https://stackoverflow.com/questions/3343432/how-do-i-programmatically-launch-a-specific-application)
    + [Suggestion: add 'tools:replace="android:icon"' to element](https://programmersought.com/article/7933423433/)    
    tl;dr    
    ```xml
    <application  
            android:name="com.anthony.test.CustomApplication"  
            android:allowBackup="true"  
            android:icon="@mipmap/ic_launcher"  
            android:label="@string/app_name"  
            android:theme="@style/AppTheme"  
            tools:replace="android:icon, android:theme" >
    ```
    + [A dependent feature was defined but no package ID was set. You are probably missing a feature dependency in the base feature](https://stackoverflow.com/questions/45891659/a-dependent-feature-was-defined-but-no-package-id-was-set-you-are-probably-miss)    
    tl;dr    
    ```groovy
    apply plugin: 'com.android.library'
    ```
    + [android:extractNativeLibs="true" for Dynamic Feature Module](https://github.com/google/bundletool/issues/155)
    + [Android: Declaring Dependencies between Subprojects](https://docs.gradle.org/current/userguide/declaring_dependencies_between_subprojects.html#sec:project_jar_dependencies)
    + [Structuring and Building a Software Component with Gradle](https://docs.gradle.org/current/userguide/multi_project_builds.html#:~:text=A%20multi%2Dproject%20build%20in,and%20one%20or%20more%20subprojects.&text=This%20is%20the%20recommended%20project,project%20with%20a%20single%20subproject.)
    + [Android ListView in Kotlin](https://www.geeksforgeeks.org/android-listview-in-kotlin/)
    + [Kotlin Android ListView Example](https://www.tutorialkart.com/kotlin-android/kotlin-android-listview-example/)
    + [A simple socket-server written in Kotlin](https://gist.github.com/Silverbaq/a14fe6b3ec57703e8cc1a63b59605876)
        + [A simple socket client in Kotlin](https://gist.github.com/Silverbaq/1fdaf8aee72b86b8c9e2bd47fd1976f4)
    + [Android IPC Mechanisms](https://proandroiddev.com/ipc-techniques-for-android-45d815ac59be)
        + [Android IPC Mechanisms #1 — AIDL](https://proandroiddev.com/ipc-techniques-for-android-aidl-bb03ed62adaa)
        + [Android IPC Mechanisms #2 — Messenger](https://proandroiddev.com/ipc-techniques-for-android-messenger-3e8555a32167)
        + [Android IPC Mechanisms #3 — Broadcast](https://proandroiddev.com/ipc-techniques-for-android-broadcast-ee4ed1f56261)
        + [IPC-Examples](https://github.com/perihanmirkelam/IPC-Examples)
        + [Why Connection refused got when connecting to LocalServerSocket from native program in Android](https://stackoverflow.com/questions/65432874/why-connection-refused-got-when-connecting-to-localserversocket-from-native-prog)
            + [UNIX domain sockets : for UNIX but not for Android](https://troydhanson.github.io/network/Unix_domain_sockets.html)
            + [Operation now in progress error on connect( function) error](https://stackoverflow.com/questions/6202454/operation-now-in-progress-error-on-connect-function-error)
        + [How to create named pipe (mkfifo) in Android?](https://stackoverflow.com/questions/2740321/how-to-create-named-pipe-mkfifo-in-android/2758038#2758038)
        + [requestLegacyExternalStorage is not working in Android 11 - API 30](https://stackoverflow.com/questions/63364476/requestlegacyexternalstorage-is-not-working-in-android-11-api-30)
    + [list all installed packages in android adb shell](https://gist.github.com/davidnunez/1404789)
    + [Android Media Samples Repository](https://github.com/android/media-samples)
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
            ```c++
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

    + [ADB Hack - Granting extra capabilities via the ADB tool](https://www.macrodroidforum.com/index.php?threads/adb-hack-granting-extra-capabilities-via-the-adb-tool.48/)    
        tl;dr, e.g.    
        ```sh
        adb shell pm grant com.arlosoft.macrodroid android.permission.READ_LOGS
        adb shell pm grant com.arlosoft.macrodroid android.permission.DUMP
        adb shell pm grant com.arlosoft.macrodroid android.permission.PACKAGE_USAGE_STATS
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
            + [Mali Performance 5: An Application's Performance Responsibilities](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/mali-performance-5-an-application-s-performance-responsibilities)
        + [ARM Mali GPU OpenGL ES Application Optimization Guide](https://developer.arm.com/docs/dui0555/b/introduction/about-optimization)
            + [ARM® Mali GPU Version: 3.0 OpenGL ES Application Optimization Guide](http://infocenter.arm.com/help/topic/com.arm.doc.dui0555c/DUI0555C_mali_optimization_guide.pdf)
            + [Accelerating Mali GPU analysis using Arm Mobile Studio](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/accelerating-mali-gpu-analysis-using-arm-mobile-studio)
            + [Touch/GPU profiling/Mali](https://wiki.ubuntu.com/Touch/GPU%20profiling/Mali)
                + [~high res timer 404~](https://github.com/ARM-software/gator/blob/master/hrtimer_module/hrtimer_module.c)
                + [high res timer](https://github.com/alexvonduar/gator/tree/master/hrtimer_module)
            + [events-Mali-TNOx_hw](https://github.com/ARM-software/gator/blob/master/daemon/events-Mali-TNOx_hw.xml)
                + [events-Mali-G76_hw](https://github.com/ARM-software/gator/blob/master/daemon/events-Mali-G76_hw.xml)
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

+ [ARM Neon](https://developer.arm.com/architectures/instruction-sets/simd-isas/neon)
    + [Neon guide](https://github.com/thenifty/neon-guide/)
    + [Neon Intrinsics](https://developer.arm.com/architectures/instruction-sets/simd-isas/neon/intrinsics?search=vfmaq_laneq_f32)
    + [Arm® A64 Instruction Set Architecture: Armv8, for Armv8-A architecture profile FMLA (vector)](https://developer.arm.com/docs/ddi0596/h/simd-and-floating-point-instructions-alphabetic-order/fmla-vector-floating-point-fused-multiply-add-to-accumulator-vector)
    + [Arm Neon Intrinsics Add Functions (Explained With C)](https://medium.com/@luc.trudeau/arm-neon-intrinsics-add-functions-explained-with-c-90346d912796)

+ [Launch Activity from Native code](https://stackoverflow.com/questions/19945984/launch-activity-from-native-code)
    + [How to launch a new Activity using NativeActivity?](https://groups.google.com/g/android-ndk/c/SHCXgUCE7t4)
    + [call android activity from jni directly from c++ process without java side](https://stackoverflow.com/questions/22326302/call-android-activity-from-jni-directly-from-c-process-without-java-side)
        + [How to launch an Activity from another Application in Android](https://stackoverflow.com/questions/3872063/how-to-launch-an-activity-from-another-application-in-android?noredirect=1&lq=1)
    + [Java Runtime.getRuntime(): getting output from executing a command line program](https://stackoverflow.com/questions/5711084/java-runtime-getruntime-getting-output-from-executing-a-command-line-program)
    + [Getting started with C++ and Android Native Activities](https://medium.com/androiddevelopers/getting-started-with-c-and-android-native-activities-2213b402ffff)
        + [Understand Tasks and Back Stack](https://developer.android.com/guide/components/activities/tasks-and-back-stack)
            + [Android NativeActivity + other activity](https://stackoverflow.com/questions/13268372/android-nativeactivity-other-activity/13269422)
    + [Cross-process locking with Android NDK?](https://stackoverflow.com/questions/18603267/cross-process-locking-with-android-ndk/18606519#18606519)
    + [Product-consumer with semaphores and forks](https://stackoverflow.com/questions/23485100/product-consumer-with-semaphores-and-forks)
    + [test-flock.c](https://github.com/Chainfire/android-ndk-compression-tools/blob/master/gnulib/tests/test-flock.c)
    + [Android Native Semaphore Not implemented](https://stackoverflow.com/questions/48083883/android-native-semaphore-not-implemented)

+ [CNTPCT_EL0, Counter-timer Physical Count register](https://developer.arm.com/documentation/ddi0595/2021-06/AArch64-Registers/CNTPCT-EL0--Counter-timer-Physical-Count-register)
+ [MRS](https://developer.arm.com/documentation/dui0802/a/A64-General-Instructions/MRS)
