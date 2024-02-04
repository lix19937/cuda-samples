# 0. 说明  


### [asyncAPI](./asyncAPI)

此示例说明了CUDA事件在GPU计时以及CPU和GPU执行重叠时的使用情况。事件被插入到CUDA调用流中。由于CUDA流调用是异步的，**CPU可以在GPU执行时执行计算（包括主机和设备之间的DMA内存复制）**。CPU可以查询CUDA事件以确定GPU是否已完成任务。  [v]    

### [c++11_cuda](./c++11_cuda) 

此示例演示了CUDA中对C++11特性的支持。它扫描输入文本文件并打印x、y、z、w个字符的出现次数。    [v]    

### [clock](./clock)   

这个例子展示了如何**使用时钟函数来准确地测量内核线程块的性能**。     [v]    

### [clock_nvrtc](./clock_nvrtc)  

这个例子展示了如何使用libNVRTC的时钟函数来准确地测量内核线程块的性能。    [v]    

### [concurrentKernels](./concurrentKernels)    

此示例演示了**使用CUDA流在GPU设备上并发执行几个kernel**。它还说明了如何使用新的cudaStreamWaitEvent函数引入CUDA流之间的依赖关系。  [v]    

### [cppIntegration](./cppIntegration)   

此示例演示了如何将CUDA集成到现有的C++应用程序中，即主机端的CUDA入口点只是从C++代码调用的函数，并且只有包含该函数的文件才使用nvcc编译。它还演示了可以从cpp使用向量类型。

### [cppOverload](./cppOverload)   

此示例演示如何在GPU上使用C++函数重载。  [v]      

### [cudaOpenMP](./cudaOpenMP) 

此示例演示如何使用OpenMP API为多个GPU编写应用程序。可以研究。   [v]      

### [fp16ScalarProduct](./fp16ScalarProduct)  

计算FP16数字的两个矢量的标量乘积。注意计算溢出。     [v]     

### [matrixMul](./matrixMul)
此示例实现矩阵乘法，与编程指南的第6章完全相同。它的编写是为了阐明各种CUDA编程原理，而不是为了为矩阵乘法提供最具性能的通用内核。为了说明GPU在矩阵乘法方面的性能，本示例还展示了如何使用CUBLAS的新CUDA 4.0接口来演示矩阵乘法的高性能。   [v]    

### [matrixMul_nvrtc](./matrixMul_nvrtc)
此示例实现矩阵乘法，与编程指南的第6章完全相同。它的编写是为了阐明各种CUDA编程原理，而不是为了为矩阵乘法提供最具性能的通用内核。为了说明GPU在矩阵乘法方面的性能，本示例还展示了如何使用CUBLAS的新CUDA 4.0接口来演示矩阵乘法的高性能。 **运行时编译**。      

### [matrixMulDrv](./matrixMulDrv)  

此示例实现矩阵乘法，并使用新的CUDA4.0内核启动驱动程序API。它的编写是为了阐明各种CUDA编程原理，而不是为了为矩阵乘法提供最具性能的通用内核。CUBLAS提供高性能的矩阵乘法。    

### [matrixMulDynlinkJIT](./matrixMulDynlinkJIT)  

此示例使用CUDA驱动程序API重新访问矩阵乘法。它演示了如何在运行时链接到CUDA驱动程序，以及如何使用来自PTX代码的JIT（即时）编译。它的编写是为了阐明各种CUDA编程原理，而不是为了为矩阵乘法提供最具性能的通用内核。CUBLAS提供高性能的矩阵乘法。

### [mergeSort](./mergeSort)  
此示例实现了合并排序（也称为Batcher排序），属于排序网络类的算法。虽然与具有更好渐进算法复杂度的算法（即合并排序或基数排序）相比，在大序列上通常是次有效的，但可能是对中小型（键、值）数组对的批量排序的选择算法。http://www.iti.fh-flensburg.de/lang/algorithmen/sortieren/networks/indexen.htm 

### [simpleAssert](./simpleAssert)  

这个CUDA Runtime API示例是一个非常基本的示例，它实现了如何在设备代码中使用断言函数。需要计算能力2.0。   [v]    

### [simpleAssert_nvrtc](./simpleAssert_nvrtc)

这个CUDA Runtime API示例是一个非常基本的示例，它实现了如何在设备代码中使用断言函数。需要计算能力2.0。

### [simpleAtomicIntrinsics](./simpleAtomicIntrinsics)

全局内存原子指令的简单演示。   [v]     

### [simpleAtomicIntrinsics_nvrtc](./simpleAtomicIntrinsics_nvrtc)

全局内存原子指令的简单演示。此示例使用NVRTC进行运行时编译。  

### [simpleAttributes](./simpleAttributes)   

这个CUDA Runtime API示例是一个非常基本的示例，它实现了**如何使用影响L2位置的流属性**。只有在计算能力8.0或更高版本上才能注意到由于使用二级访问策略窗口而导致的性能改进。  [v]    

### [simpleAWBarrier](./simpleAWBarrier)

到达等待屏障的简单演示。     [v]    

### [simpleCallback](./simpleCallback)  

此示例使用CUDA5.0引入的CUDA流和事件的新CPU回调实现了多线程异构计算工作负载。    [v]    

### [simpleCooperativeGroups](./simpleCooperativeGroups)   

此示例是一个简单的代码，说明了线程块中协作组的基本用法。    [v]    

### [simpleCubemapTexture](./simpleCubemapTexture)  

演示如何使用新的CUDA 4.1功能在CUDA C中支持立方体映射纹理的简单示例。 

### [simpleCUDA2GL](./simpleCUDA2GL)

此示例显示如何使用最有效的方法将CUDA图像复制回OpenGL。  

### [simpleDrvRuntime](./simpleDrvRuntime)   

一个简单的例子演示了CUDA驱动程序和运行时API如何协同工作来加载向量添加内核的CUDA fatbinary并执行向量添加。  [v]    

### [simpleHyperQ](./simpleHyperQ)  

此示例演示了在提供HyperQ（SM 3.5）的设备上使用CUDA流并行执行多个内核。没有HyperQ的设备（SM 2.0和SM 3.0）最多可同时运行两个内核。  

### [simpleIPC](./simpleIPC)

这个CUDA Runtime API示例是一个非常基本的示例，它演示了每个GPU有一个进程用于计算的进程间通信。需要计算能力3.0或更高版本和Linux操作系统，或具有启用TCC的GPU的Windows操作系统。  [v]    

### [simpleLayeredTexture](./simpleLayeredTexture)

演示如何使用新的CUDA 4.0功能在CUDA C中支持分层纹理的简单示例。  

### [simpleMPI](./simpleMPI)  

演示如何将MPI与CUDA结合使用的简单示例。  [v]    

### [simpleMultiCopy](./simpleMultiCopy)

在具有计算能力1.1的GPU中支持，主机系统可以使用一个memcopy进行重叠计算。对于具有Compute Capability 2.0的Quadro和Tesla GPU，可以全速在任一方向进行第二次重叠复制操作（PCI-e是对称的）。此示例说明了使用CUDA流来实现内核执行与设备之间的数据副本的重叠。  [v]    

### [simpleMultiGPU](./simpleMultiGPU)

此应用程序演示如何使用新的CUDA 4.0 API进行CUDA上下文管理和多线程访问，以便在多个GPU上运行CUDA内核。    [v]    

### [simpleOccupancy](./simpleOccupancy)

此示例通过使用启动配置器启动内核来演示CUDA占用率计算器和基于占用率的启动配置器API的基本用法，并测量与手动配置的启动的利用率差异。    [v]    

### [simpleP2P](./simpleP2P)

此应用程序演示了CUDA API，这些API支持多个GPU之间的对等（P2P）拷贝、对等（对等）寻址和统一虚拟内存寻址（UVA）。一般来说，P2P在两个相同的GPU之间得到支持，但也有一些例外，例如一些特斯拉和Quadro GPU。  [v]    

### [simplePitchLinearTexture](./simplePitchLinearTexture)

间距线性纹理的使用

### [simplePrintf](./simplePrintf)

这个基本的CUDARuntime API示例演示了如何在设备代码中使用printf函数。  [v]    

### [simpleSeparateCompilation](./simpleSeparateCompilation)

此示例演示了CUDA 5.0功能，即创建GPU设备静态库并在另一个CUDA内核中使用它的能力。此示例演示如何传入GPU设备函数（来自GPU设备静态库）作为要调用的函数指针。此示例需要具有2.0或更高计算能力的设备。  [v]    

### [simpleStreams](./simpleStreams)

此示例使用CUDA流将内核执行与主机和GPU设备之间的内存副本重叠。此示例使用了一个新的CUDA 4.0功能，该功能支持锁定通用主机内存。  [v]    

### [simpleSurfaceWrite](./simpleSurfaceWrite)

演示2D曲面引用使用的简单示例（写入纹理）

### [simpleTemplates](./simpleTemplates)

此示例是模板项目的模板化版本。它还展示了如何正确地将动态分配的共享内数组模板化。  [v]    

### [simpleTemplates_nvrtc](./simpleTemplates_nvrtc)

此示例是模板项目的模板化版本。它还展示了如何正确地将动态分配的共享内存数组模板化。  

### [simpleTexture](./simpleTexture)

演示在CUDA中使用纹理的简单示例。

### [simpleTexture3D](./simpleTexture3D)

演示在CUDA中使用3D纹理的简单示例。

### [simpleTextureDrv](./simpleTextureDrv)

演示在CUDA中使用纹理的简单示例。此示例使用新的CUDA4.0内核启动驱动程序API。

### [simpleVoteIntrinsics](./simpleVoteIntrinsics)

演示如何在CUDA内核中使用Vote（__any_sync，__all_sync）内在指令的简单程序。  [v]    

### [simpleVoteIntrinsics_nvrtc](./simpleVoteIntrinsics_nvrtc)  

一个简单的程序，演示如何在CUDA内核中使用Vote（任意，全部）内在指令，并使用NVRTC API进行运行时编译。需要计算能力2.0或更高版本。  [v]    

### [simpleZeroCopy](./simpleZeroCopy) 

这个示例演示了如何使用Zero-MemCopy，内核可以直接读取和写入锁页内存。    [v]    

### [systemWideAtomics](./systemWideAtomics)

系统范围原子指令的简单演示。  [v]    

### [template](./template)

一个琐碎的模板项目，可以作为创建新CUDA项目的起点。  [v]    

### [UnifiedMemoryStreams](./UnifiedMemoryStreams)

此示例演示了在单个GPU上使用OpenMP和带有统一内存的流。  [v]    

### [vectorAdd](./vectorAdd)

这个CUDA运行时API示例是一个非常基本的示例，它实现逐元素的向量相加。它与编程指南第3章的示例相同，添加了一些内容，如错误检查。  [v]    

### [vectorAdd_nvrtc](./vectorAdd_nvrtc)

此CUDA驱动程序API示例使用NVRTC进行向量加法内核的运行时编译。演示的矢量加法内核与编程指南第3章的示例相同。  

### [vectorAddDrv](./vectorAddDrv)

此矢量相加样本是逐元素实现的基本样本。它与编程指南第3章的示例相同，添加了一些内容，如错误检查。此示例还使用新的CUDA4.0内核启动驱动程序API。    [v]    

### [vectorAddMMAP](./vectorAddMMAP) 

此示例将vectorAddDrv示例中的设备分配替换为cuMemMap-ed分配。此示例演示了cuMemMap api允许用户指定其内存的物理属性，同时保留其访问的连续性，因此不需要更改其程序结构。
