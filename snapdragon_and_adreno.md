# snapdragon and adreno tips

+ Snapdragon
    + [Snapdragon 845 Mobile Platform](https://www.qualcomm.com/products/snapdragon-845-mobile-platform)

+ Adreno
    + [OpenCL Optimization and Best Practices for Qualcomm Adreno GPUs](https://dl.acm.org/citation.cfm?id=3204935)
    + [Sub-optimal performance on Qualcomm Adreno GPUs](https://github.com/CNugteren/CLBlast/issues/228)
    + [Getting started with openCL on Adreno420 under linux](https://developer.qualcomm.com/forum/qdn-forums/software/adreno-gpu-sdk/34153)
    + [Qualcomm Adreno 630](https://www.notebookcheck.net/Qualcomm-Adreno-630-GPU.299832.0.html)
    + [open source driver project for adreno GPUs](https://github.com/freedreno/freedreno)a
    + [Run OpenCL program on MOBILE GPU (Qualcomm & ARM)!](https://github.com/supernovaremnant/bazel-android-opencl)
        + [Compile OpenCL Program for Mobile GPU](https://sorrythenameistaken.blogspot.com/2018/06/compile-opencl-program-for-embedded-gpu.html)
            + [how to add `libOpenCL.so` to your project](https://github.com/googlesamples/android-ndk/blob/master/hello-libs/app/src/main/cpp/CMakeLists.txt)
    + [OpenCL Header/C++_Wrapper/Device Driver for SD820 Adreno 530, SD835 Adreno 540 on Android Phone](https://github.com/supernovaremnant/Android-OpenCL-Driver)
    + [How to Build & Use OpenCL on Android Studio](https://www.slideshare.net/noritsuna/how-to-build-use-opencl-on-android-studio)

    + troubleshooting
        + [clGetDeviceInfo and clGetPlatformInfo fails in OpenCL with error code -30 (CL_INVALID_VALUE)](https://stackoverflow.com/questions/29290806/clgetdeviceinfo-and-clgetplatforminfo-fails-in-opencl-with-error-code-30-cl-in)

+ Profiling
    + [Capturing OpenCL applications in Snapdragon Profiler](https://www.youtube.com/watch?v=mevcqGF-jhc&feature=youtu.be)
    + [OpenCL Optimization 3 Profiling OpenCL](https://www.youtube.com/watch?v=S-alEZ7IZUQ&t=203s)
    + [A tool which profiles OpenCL devices to find their peak capacities](https://github.com/krrishnarraj/clpeak)

+ Computer Vision
    + [RSTensorFlow: GPU Enabled TensorFlow for Deep Learning on Commodity Android Devices](https://md2k.org/images/papers/methods/p7-alzantot.pdf)

+ **A**ndroid **O**pen **S**ource **P**roject
    + [Downloading the Android Source](https://source.android.com/setup/build/downloading)

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
    + [Установка android tools (ADB,fastboot, QTADB) на Debian/Ubuntu/Linux Mint](http://linux-notes.org/ustanovka-android-tools-adb-fastboot-qtadb-na-debian-ubuntu-linux-mint/)
