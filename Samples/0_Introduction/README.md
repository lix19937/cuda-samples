# 0. 说明  


### [asyncAPI](./asyncAPI)

此示例说明了CUDA事件在GPU计时以及CPU和GPU执行重叠时的使用情况。事件被插入到CUDA调用流中。由于CUDA流调用是异步的，CPU可以在GPU执行时执行计算（包括主机和设备之间的DMA内存复制）。CPU可以查询CUDA事件以确定GPU是否已完成任务。

### [c++11_cuda](./c++11_cuda) 

此示例演示了CUDA中对C++11特性的支持。它扫描输入文本文件并打印x、y、z、w个字符的出现次数。  

### [clock](./clock)   

这个例子展示了如何使用时钟函数来准确地测量内核线程块的性能。


### [clock_nvrtc](./clock_nvrtc)  

这个例子展示了如何使用libNVRTC的时钟函数来准确地测量内核线程块的性能。  

### [concurrentKernels](./concurrentKernels)    

此示例演示了使用CUDA流在GPU设备上并发执行几个内核。它还说明了如何使用新的cudaStreamWaitEvent函数引入CUDA流之间的依赖关系。

### [cppIntegration](./cppIntegration)   

此示例演示了如何将CUDA集成到现有的C++应用程序中，即主机端的CUDA入口点只是从C++代码调用的函数，并且只有包含该函数的文件才使用nvcc编译。它还演示了可以从cpp使用向量类型。

### [cppOverload](./cppOverload)   

此示例演示如何在GPU上使用C++函数重载。


### [cudaOpenMP](./cudaOpenMP) 

此示例演示如何使用OpenMP API为多个GPU编写应用程序。可以研究。   

### [fp16ScalarProduct](./fp16ScalarProduct)  

计算FP16数字的两个矢量的标量乘积。注意一处。   


### [matrixMul](./matrixMul)
此示例实现矩阵乘法，与编程指南的第6章完全相同。它的编写是为了阐明各种CUDA编程原理，而不是为了为矩阵乘法提供最具性能的通用内核。为了说明GPU在矩阵乘法方面的性能，本示例还展示了如何使用CUBLAS的新CUDA 4.0接口来演示矩阵乘法的高性能。

### [matrixMul_nvrtc](./matrixMul_nvrtc)
此示例实现矩阵乘法，与编程指南的第6章完全相同。它的编写是为了阐明各种CUDA编程原理，而不是为了为矩阵乘法提供最具性能的通用内核。为了说明GPU在矩阵乘法方面的性能，本示例还展示了如何使用CUBLAS的新CUDA 4.0接口来演示矩阵乘法的高性能。 运行时编译。    

### [matrixMulDrv](./matrixMulDrv)  

此示例实现矩阵乘法，并使用新的CUDA4.0内核启动驱动程序API。它的编写是为了阐明各种CUDA编程原理，而不是为了为矩阵乘法提供最具性能的通用内核。CUBLAS提供高性能的矩阵乘法。    

### [matrixMulDynlinkJIT](./matrixMulDynlinkJIT)  

此示例使用CUDA驱动程序API重新访问矩阵乘法。它演示了如何在运行时链接到CUDA驱动程序，以及如何使用来自PTX代码的JIT（即时）编译。它的编写是为了阐明各种CUDA编程原理，而不是为了为矩阵乘法提供最具性能的通用内核。CUBLAS提供高性能的矩阵乘法。

### [mergeSort](./mergeSort)  
此示例实现了合并排序（也称为Batcher排序），属于排序网络类的算法。虽然与具有更好渐进算法复杂度的算法（即合并排序或基数排序）相比，在大序列上通常是次有效的，但可能是对中小型（键、值）数组对的批量排序的选择算法。http://www.iti.fh-flensburg.de/lang/algorithmen/sortieren/networks/indexen.htm

### [simpleAssert](./simpleAssert)  

这个CUDA Runtime API示例是一个非常基本的示例，它实现了如何在设备代码中使用断言函数。需要计算能力2.0。 

### [simpleAssert_nvrtc](./simpleAssert_nvrtc)

这个CUDA Runtime API示例是一个非常基本的示例，它实现了如何在设备代码中使用断言函数。需要计算能力2.0。

### [simpleAtomicIntrinsics](./simpleAtomicIntrinsics)

全局内存原子指令的简单演示。


### [simpleAtomicIntrinsics_nvrtc](./simpleAtomicIntrinsics_nvrtc)

全局内存原子指令的简单演示。此示例使用NVRTC进行运行时编译。


### [simpleAttributes](./simpleAttributes)   

这个CUDA Runtime API示例是一个非常基本的示例，它实现了如何使用影响L2位置的流属性。只有在计算能力8.0或更高版本上才能注意到由于使用二级访问策略窗口而导致的性能改进。

### [simpleAWBarrier](./simpleAWBarrier)

到达等待屏障的简单演示。   


### [simpleCallback](./simpleCallback)  

此示例使用CUDA5.0引入的CUDA流和事件的新CPU回调实现了多线程异构计算工作负载。  

### [simpleCooperativeGroups](./simpleCooperativeGroups)   

此示例是一个简单的代码，说明了线程块中协作组的基本用法。


### [simpleCubemapTexture](./simpleCubemapTexture)  

演示如何使用新的CUDA 4.1功能在CUDA C中支持立方体映射纹理的简单示例。 

### [simpleCUDA2GL](./simpleCUDA2GL)

此示例显示如何使用最有效的方法将CUDA图像复制回OpenGL。


### [simpleDrvRuntime](./simpleDrvRuntime)   

一个简单的例子演示了CUDA驱动程序和运行时API如何协同工作来加载向量添加内核的CUDA fatbinary并执行向量添加。

### [simpleHyperQ](./simpleHyperQ)  

此示例演示了在提供HyperQ（SM 3.5）的设备上使用CUDA流并行执行多个内核。没有HyperQ的设备（SM 2.0和SM 3.0）最多可同时运行两个内核。  

### [simpleIPC](./simpleIPC)
This CUDA Runtime API sample is a very basic sample that demonstrates Inter Process Communication with one process per GPU for computation.  Requires Compute Capability 3.0 or higher and a Linux Operating System, or a Windows Operating System with TCC enabled GPUs

### [simpleLayeredTexture](./simpleLayeredTexture)
Simple example that demonstrates how to use a new CUDA 4.0 feature to support layered Textures in CUDA C.

### [simpleMPI](./simpleMPI)
Simple example demonstrating how to use MPI in combination with CUDA.

### [simpleMultiCopy](./simpleMultiCopy)
Supported in GPUs with Compute Capability 1.1, overlapping compute with one memcopy is possible from the host system.  For Quadro and Tesla GPUs with Compute Capability 2.0, a second overlapped copy operation in either direction at full speed is possible (PCI-e is symmetric).  This sample illustrates the usage of CUDA streams to achieve overlapping of kernel execution with data copies to and from the device.

### [simpleMultiGPU](./simpleMultiGPU)
This application demonstrates how to use the new CUDA 4.0 API for CUDA context management and multi-threaded access to run CUDA kernels on multiple-GPUs.

### [simpleOccupancy](./simpleOccupancy)
This sample demonstrates the basic usage of the CUDA occupancy calculator and occupancy-based launch configurator APIs by launching a kernel with the launch configurator, and measures the utilization difference against a manually configured launch.

### [simpleP2P](./simpleP2P)
This application demonstrates CUDA APIs that support Peer-To-Peer (P2P) copies, Peer-To-Peer (P2P) addressing, and Unified Virtual Memory Addressing (UVA) between multiple GPUs. In general, P2P is supported between two same GPUs with some exceptions, such as some Tesla and Quadro GPUs.

### [simplePitchLinearTexture](./simplePitchLinearTexture)
Use of Pitch Linear Textures

### [simplePrintf](./simplePrintf)
This basic CUDA Runtime API sample demonstrates how to use the printf function in the device code.

### [simpleSeparateCompilation](./simpleSeparateCompilation)
This sample demonstrates a CUDA 5.0 feature, the ability to create a GPU device static library and use it within another CUDA kernel.  This example demonstrates how to pass in a GPU device function (from the GPU device static library) as a function pointer to be called.  This sample requires devices with compute capability 2.0 or higher.

### [simpleStreams](./simpleStreams)
This sample uses CUDA streams to overlap kernel executions with memory copies between the host and a GPU device.  This sample uses a new CUDA 4.0 feature that supports pinning of generic host memory.  Requires Compute Capability 2.0 or higher.

### [simpleSurfaceWrite](./simpleSurfaceWrite)
Simple example that demonstrates the use of 2D surface references (Write-to-Texture)

### [simpleTemplates](./simpleTemplates)
This sample is a templatized version of the template project. It also shows how to correctly templatize dynamically allocated shared memory arrays.

### [simpleTemplates_nvrtc](./simpleTemplates_nvrtc)
This sample is a templatized version of the template project. It also shows how to correctly templatize dynamically allocated shared memory arrays.

### [simpleTexture](./simpleTexture)
Simple example that demonstrates use of Textures in CUDA.

### [simpleTexture3D](./simpleTexture3D)
Simple example that demonstrates use of 3D Textures in CUDA.

### [simpleTextureDrv](./simpleTextureDrv)
Simple example that demonstrates use of Textures in CUDA.  This sample uses the new CUDA 4.0 kernel launch Driver API.

### [simpleVoteIntrinsics](./simpleVoteIntrinsics)
Simple program which demonstrates how to use the Vote (__any_sync, __all_sync) intrinsic instruction in a CUDA kernel.

### [simpleVoteIntrinsics_nvrtc](./simpleVoteIntrinsics_nvrtc)
Simple program which demonstrates how to use the Vote (any, all) intrinsic instruction in a CUDA kernel with runtime compilation using NVRTC APIs. Requires Compute Capability 2.0 or higher.

### [simpleZeroCopy](./simpleZeroCopy)
This sample illustrates how to use Zero MemCopy, kernels can read and write directly to pinned system memory.

### [systemWideAtomics](./systemWideAtomics)
A simple demonstration of system wide atomic instructions.

### [template](./template)
A trivial template project that can be used as a starting point to create new CUDA projects.

### [UnifiedMemoryStreams](./UnifiedMemoryStreams)
This sample demonstrates the use of OpenMP and streams with Unified Memory on a single GPU.

### [vectorAdd](./vectorAdd)
This CUDA Runtime API sample is a very basic sample that implements element by element vector addition. It is the same as the sample illustrating Chapter 3 of the programming guide with some additions like error checking.

### [vectorAdd_nvrtc](./vectorAdd_nvrtc)
This CUDA Driver API sample uses NVRTC for runtime compilation of vector addition kernel. Vector addition kernel demonstrated is the same as the sample illustrating Chapter 3 of the programming guide.

### [vectorAddDrv](./vectorAddDrv)
This Vector Addition sample is a basic sample that is implemented element by element.  It is the same as the sample illustrating Chapter 3 of the programming guide with some additions like error checking.   This sample also uses the new CUDA 4.0 kernel launch Driver API.

### [vectorAddMMAP](./vectorAddMMAP)
This sample replaces the device allocation in the vectorAddDrv sample with cuMemMap-ed allocations.  This sample demonstrates that the cuMemMap api allows the user to specify the physical properties of their memory while retaining the contiguous nature of their access, thus not requiring a change in their program structure.

