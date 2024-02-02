# CUDA Samples

CUDA开发人员示例，演示CUDA Toolkit中的功能. 当前版本支持 [CUDA Toolkit 12.3](https://developer.nvidia.com/cuda-downloads).

## 发布说明  

本仓仅介绍GitHub上CUDA示例的发布说明。

### CUDA 12.3

### [历史版本...](./CHANGELOG.md)

### 前提  

基于你相应的平台，下载和安装 [CUDA Toolkit 12.3](https://developer.nvidia.com/cuda-downloads).
关于cuda工具包的系统要求和安装说明, 请参考 [Linux Installation Guide](http://docs.nvidia.com/cuda/cuda-installation-guide-linux/), and the [Windows Installation Guide](http://docs.nvidia.com/cuda/cuda-installation-guide-microsoft-windows/index.html).

### 获取示例  

使用如下命令    
```
git clone https://github.com/NVIDIA/cuda-samples.git
```

在不使用git的情况下，使用这些示例的最简单方法是通过单击repo页面上的“下载zip”按钮下载包含当前版本的zip文件。然后，您可以解压缩整个归档文件并使用示例。

## 编译示例    

### Windows

略

### Linux   
Linux示例是使用makefile构建的。要使用makefiles，请将当前目录更改为要构建的示例目录，然后运行make：   
```
$ cd <sample_dir>
$ make
```
The samples makefiles can take advantage of certain options:
*  **TARGET_ARCH=<arch>** - cross-compile targeting a specific architecture. Allowed architectures are x86_64, ppc64le, armv7l, aarch64.
    By default, TARGET_ARCH is set to HOST_ARCH. On a x86_64 machine, not setting TARGET_ARCH is the equivalent of setting TARGET_ARCH=x86_64.<br/>
`$ make TARGET_ARCH=x86_64` <br/> `$ make TARGET_ARCH=ppc64le` <br/> `$ make TARGET_ARCH=armv7l` <br/> `$ make TARGET_ARCH=aarch64` <br/>
    See [here](http://docs.nvidia.com/cuda/cuda-samples/index.html#cross-samples) for more details on cross platform compilation of cuda samples.
*   **dbg=1** - build with debug symbols
    ```
    $ make dbg=1
    ```
*   **SMS="A B ..."** - override the SM architectures for which the sample will be built, where `"A B ..."` is a space-delimited list of SM architectures. For example, to generate SASS for SM 50 and SM 60, use `SMS="50 60"`.
    ```
    $ make SMS="50 60"
    ```

*  **HOST_COMPILER=<host_compiler>** - override the default g++ host compiler. See the [Linux Installation Guide](http://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html#system-requirements) for a list of supported host compilers.
    ```
    $ make HOST_COMPILER=g++
    ```

## Samples list

### [0. Introduction](./Samples/0_Introduction/README.md)
Basic CUDA samples for beginners that illustrate key concepts with using CUDA and CUDA runtime APIs.

### [1. Utilities](./Samples/1_Utilities/README.md)
Utility samples that demonstrate how to query device capabilities and measure GPU/CPU bandwidth.

### [2. Concepts and Techniques](./Samples/2_Concepts_and_Techniques/README.md)
Samples that demonstrate CUDA related concepts and common problem solving techniques.

### [3. CUDA Features](./Samples/3_CUDA_Features/README.md)
Samples that demonstrate CUDA Features (Cooperative Groups, CUDA Dynamic Parallelism, CUDA Graphs etc).

### [4. CUDA Libraries](./Samples/4_CUDA_Libraries/README.md)
Samples that demonstrate how to use CUDA platform libraries (NPP, NVJPEG, NVGRAPH cuBLAS, cuFFT, cuSPARSE, cuSOLVER and cuRAND).

### [5. Domain Specific](./Samples/5_Domain_Specific/README.md)
Samples that are specific to domain (Graphics, Finance, Image Processing).

### [6. Performance](./Samples/6_Performance/README.md)
Samples that demonstrate performance optimization.

### [7. libNVVM](./Samples/7_libNVVM/README.md)
Samples that demonstrate the use of libNVVVM and NVVM IR.

## 依赖  

一些CUDA示例依赖于第三方应用程序和/或库，或CUDA Toolkit和Driver提供的功能来构建或执行。下面列出了这些依赖关系。

如果某个示例具有系统上可用但未安装的第三方依赖项，则该示例将在构建时放弃自己。

每个样本的依赖项都列在其自述文件的依赖项部分中。   

### 第三方依赖  

某些CUDA示例需要这些第三方依赖项。如果可用，这些依赖项将自动安装在您的系统上，或者可以通过系统的软件包管理器（Linux）或第三方网站进行安装。

#### FreeImage

FreeImage是一个开源的图像库。FreeImage通常可以使用发行版的软件包管理器系统安装在Linux上。FreeImage也可以从FreeImage网站下载。

要在Windows系统上设置FreeImage，请将FreeImage DLL分发提取到文件夹`../..//Common/FreeImage/Dist/x64`，使其包含.h和.lib文件。将.dll文件复制到根级别“bin/win64/Debug”和“bin/winn64/Release”文件夹。  

#### Message Passing Interface

MPI（消息传递接口）是一种用于在分布式进程之间进行数据通信的API。MPI编译器可以使用Linux发行版的包管理器系统进行安装。它也可以在一些在线资源中获得, [Open MPI](http://www.open-mpi.org/). Windows下, [MS-MPI SDK](https://msdn.microsoft.com/en-us/library/bb524831(v=vs.85).aspx).

#### Only 64-Bit

某些示例只能在64位操作系统上运行。


#### DirectX

DirectX是一组API，旨在允许在Microsoft平台上开发多媒体应用程序。对于Microsoft平台，NVIDIA的CUDA驱动程序支持DirectX。Windows的几个CUDA示例演示了CUDA DirectX互操作性，要构建此类示例，需要安装Microsoft Visual Studio 2012或更高版本，该版本提供适用于Windows 8的Microsoft Windows SDK。  

#### DirectX12

DirectX 12是一个高级低级编程API的集合，可以减少驱动程序开销，旨在允许从Windows 10操作系统开始在Microsoft平台上开发多媒体应用程序。对于Microsoft平台，NVIDIA的CUDA驱动程序支持DirectX。用于Windows的少数CUDA示例演示了CUDA-DirectX12互操作性, [Windows 10 SDK or higher](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk), with VS 2015 or VS 2017.

#### OpenGL

OpenGL是一个用于二维和三维渲染的图形库。在支持OpenGL的系统上，NVIDIA的OpenGL实现提供了CUDA驱动程序。  

#### OpenGL ES

OpenGL ES是一个用于2D和3D渲染的嵌入式系统图形库。在支持OpenGL ES的系统上，NVIDIA的OpenGL ES实现提供了CUDA驱动程序。

#### Vulkan

Vulkan是一款低开销、跨平台的三维图形和计算API。Vulkan的目标是高性能实时3D图形应用程序，如所有平台上的视频游戏和交互式媒体。在支持Vulkan的系统上，NVIDIA的Vulkan实现提供了CUDA驱动程序。[Vulkan SDK](https://www.lunarg.com/vulkan-sdk/).

#### OpenMP

OpenMP是一种用于多处理编程的API。OpenMP可以使用Linux发行版的软件包管理器系统进行安装。它通常预装GCC。 [OpenMP website](http://openmp.org/).

#### Screen

Screen是QNX操作系统上的一个窗口系统。屏幕通常是根文件系统的一部分。

#### X11

X11是一个窗口系统，常见于*-nix风格的操作系统。X11可以使用Linux发行版的软件包管理器安装，并且预装在Mac OS X系统上。

#### EGL

EGL是Khronos渲染API（如OpenGL、OpenGL ES或OpenVG）与底层原生平台窗口系统之间的接口。

#### EGLOutput

EGLOutput是一组EGL扩展，允许EGL直接呈现到显示器上。


#### EGLSync

EGLSync是一组EGL扩展，它提供作为同步原语的同步对象，表示可以测试或等待其完成的事件。

#### NVSCI

NvSci是一组通信接口库，CUDA从中与NvSciBuf和NvSciSync进行互操作。NvSciBuf允许应用程序在内存中分配和交换缓冲区。NvSciSync允许应用程序管理同步对象，这些对象在操作序列开始和结束时进行协调。

#### NvMedia

NvMedia为NVIDIA **Tegra**设备提供强大的多媒体数据处理功能，实现真正的硬件加速。应用程序利用NvMedia应用程序编程接口（API）来处理图像和视频数据。  

### CUDA Features

一些CUDA特性需要这些CUDA功能。它们由CUDA工具包或CUDA驱动程序提供。某些功能可能在您的系统上不可用。

#### CUFFT Callback Routines

CUFFT回调例程是用户提供的内核例程，CUFFT将在加载或存储数据时调用这些例程。这些回调例程仅在Linux x86_64和ppc64le系统上可用。  

#### CUDA Dynamic Parallellism

CDP（CUDA动态并行）允许从GPU上运行的线程启动内核。CDP仅在SM体系结构为3.5或更高版本的GPU上可用。

#### Multi-block Cooperative Groups   

多块协作组（MBCG）扩展了协作组和CUDA编程模型来表示线程间块同步。MBCG可在具有Pascal和更高架构的GPU上使用。

#### Multi-Device Cooperative Groups    
多设备协作组扩展了协作组和CUDA编程模型，使在多个GPU上执行的线程块能够在执行时进行协作和同步。此功能在具有Pascal和更高体系结构的GPU上可用。

#### CUBLAS

CUBLAS (CUDA Basic Linear Algebra Subroutines) CUDA基本线性代数子程序.

#### CUDA Interprocess Communication

IPC (Interprocess Communication) 进程间通信，允许进程共享设备指针.

#### CUFFT

CUFFT cuda 快速傅里叶变换.

#### CURAND

CURAND cuda 随机数生成.

#### CUSPARSE

CUSPARSE cuda 稀疏矩阵，提供用于稀疏矩阵计算的线性代数子程序.

#### CUSOLVER
CUSOLVER库是一个基于CUBLAS和CUSPARSE库的高级包。它将三个独立的库组合在一个保护伞下，每个库都可以独立使用，也可以与其他工具包库协同使用。CUSOLVER的目的是提供有用的类似LAPACK的功能，例如常见的矩阵分解和密集矩阵的三角形求解例程、稀疏最小二乘解算器和特征值解算器。此外，cuSolver提供了一个新的重构库，可用于求解具有共享稀疏性模式的矩阵序列。

#### NPP

性能元件，提供gpu加速的图像, 视频, 信号处理函数.

#### NVGRAPH

一个GPU加速的图形分析库。

#### NVJPEG

为深度学习和超大规模多媒体应用程序中常用的图像格式提供了高性能、GPU加速的JPEG解码功能。

#### NVRTC

NVRTC (CUDA RunTime Compilation) 针对CUDA C++的实时编译库 

#### 流优先级

流优先级允许创建具有指定优先级的流。流优先级仅在SM体系结构为3.5或以上的GPU上可用。   

#### 统一虚拟内存

UVM (Unified Virtual Memory) 使CPU和GPU都可以访问的存储器，而无需在两者之间进行显式复制。UVM仅在Linux和Windows系统上可用。  

#### 16-bit 浮点  

FP16是一种16位浮点格式。1位用于符号，5位用于指数，10位用于尾数。  

#### C++11 CUDA

NVCC support of [C++11 features](https://en.wikipedia.org/wiki/C++11).

## FAQs   

http://developer.nvidia.com/cuda-faq 
http://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html   

## 参考  

*   [CUDA Programming Guide](http://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html)
*   [Accelerated Computing Blog](https://developer.nvidia.com/blog/?tags=accelerated-computing)

@updated by lix19937


