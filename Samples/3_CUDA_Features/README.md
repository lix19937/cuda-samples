# 3. CUDA 特性  

### [bf16TensorCoreGemm](./bf16TensorCoreGemm)
演示了__nv_bfloat16（e8m7）GEMM计算，该计算使用了Ampere芯片系列张量核中CUDA 11引入的Warp Matrix Multiply and Accumulate（WMMA）API，以实现更快的矩阵运算。此示例还使用了cuda管道接口为gmem到shmem异步加载提供的异步副本，这提高了内核性能并减少了寄存器压力。  [v]   

### [binaryPartitionCG](./binaryPartitionCG)

此示例是一个简单的代码，用于说明线程块内的二进制分区协作组和reduce。  [v]   

### [bindlessTexture](./bindlessTexture)

此示例演示了CUDA中cudaSurfaceObject、cudaTextureObject和MipMap支持的使用。需要具有计算能力SM 3.0的GPU来运行示例。

### [cdpAdvancedQuicksort](./cdpAdvancedQuicksort)

此示例演示了使用CUDA动态并行性实现的高级快速排序。此示例需要具有3.5或更高计算能力的设备。  [v]    

### [cdpBezierTessellation](./cdpBezierTessellation)

此示例演示了使用CUDA动态并行度实现的线的贝塞尔镶嵌(bezier tessellation of lines)。此示例需要具有3.5或更高计算能力的设备。

### [cdpQuadtree](./cdpQuadtree)   

此示例演示了使用CUDA动态并行性实现的四叉树。此示例需要具有3.5或更高计算能力的设备。

### [cdpSimplePrint](./cdpSimplePrint)

此示例演示了使用CUDA动态并行性实现的简单printf。此示例需要具有3.5或更高计算能力的设备。  [v]   

### [cdpSimpleQuicksort](./cdpSimpleQuicksort)

此示例演示了使用CUDA动态并行性实现的简单快速排序。此示例需要具有3.5或更高计算能力的设备。 [v]   

### [cudaCompressibleMemory](./cudaCompressibleMemory)

此示例演示了使用cuMemMap API的可压缩内存分配。 [v]   

### [cudaTensorCoreGemm](./cudaTensorCoreGemm)

CUDA示例演示了使用CUDA 9中引入的Warp Matrix Multiply and Accumulate（WMMA）API进行GEMM计算。

此示例演示了新CUDA WMMA API的使用，该API采用Volta芯片系列中引入的Tensor核心，以实现更快的矩阵运算。

除此之外，它还演示了新的CUDA函数属性cudaFuncAttributeMaxDynamicSharedMemorySize的使用，该属性允许应用程序保留比默认情况下更多的共享内存。 [v]   

### [dmmaTensorCoreGemm](./dmmaTensorCoreGemm)

演示了双精度GEMM计算，该计算使用双精度Warp Matrix Multiply and Accumulate（WMMA）API在Ampere芯片族张量核中与CUDA 11一起引入，以实现更快的矩阵运算。此示例还使用了cuda pipeline 接口为gmem到shmem异步加载提供的异步副本，这提高了内核性能并减少了寄存器压力。此外，此示例还演示了如何在组上使用协作组异步复制接口来执行gmem到shmem异步加载。 [v]   

### [globalToShmemAsyncCopy](./globalToShmemAsyncCopy) 

此示例实现矩阵乘法，当使用8.0或更高的计算能力时，该矩阵乘法使用数据从全局到共享内存的异步副本。还演示了同步的到达等待屏障。   [v]   
### [graphMemoryFootprint](./graphMemoryFootprint)

此示例演示了图内存节点如何重用虚拟地址和物理内存。  [v]   

### [graphMemoryNodes](./graphMemoryNodes)

使用Graph API和Stream Capture API演示CUDA图中的内存分配和释放。  [v]   

### [immaTensorCoreGemm](./immaTensorCoreGemm)

CUDA示例演示了使用CUDA 10中引入的用于整数的Warp Matrix Multiply and Accumulate（WMMA）API进行整数GEMM计算。此示例演示了CUDA WMMA API的使用，该API采用Volta芯片系列中引入的Tensor核心来实现更快的矩阵运算。除此之外，它还演示了新的CUDA函数属性cudaFuncAttributeMaxDynamicSharedMemorySize的使用，该属性允许应用程序保留比默认情况下更多的共享内存。 [v]   

### [jacobiCudaGraphs](./jacobiCudaGraphs)

使用cudaGraphExecKernelNodeSetParams 和 cudaGraphiExecUpdate 方法演示使用Jacobi迭代方法的实例化CUDA图更新。  

### [memMapIPCDrv](./memMapIPCDrv)

这个CUDA驱动程序API示例是一个非常基本的示例，它演示了使用cuMemMap API的进程间通信，每个GPU有一个进程用于计算。需要计算能力3.0或更高版本以及Linux操作系统或Windows操作系统  [v]    

### [newdelete](./newdelete)

此示例演示了通过CUDA 4.0提供的设备C++new和delete运算符以及虚拟函数声明进行的动态全局内存分配。  [v]   

### [ptxjit](./ptxjit)

此示例使用驱动程序API从PTX代码中实时编译（JIT）内核。此外，此示例演示了CUDA运行时和CUDA驱动程序API调用的无缝互操作能力。对于CUDA 5.5，此示例显示如何在运行时使用cuLink*函数使用CUDA驱动程序链接PTX程序集。

### [simpleCudaGraphs](./simpleCudaGraphs)

使用Graphs API和Stream Capture API演示CUDA Graphs的创建、实例化和启动。 [v]   

### [StreamPriorities](./StreamPriorities)

此示例演示**流优先级** 的基本用法。 [v]   

### [tf32TensorCoreGemm](./tf32TensorCoreGemm)

CUDA样本演示了tf32（e8m10）GEMM 计算，该计算使用了Ampere芯片系列张量核中CUDA11引入的 Warp Matrix Multiply and Accumulate（WMMA）API，以实现更快的矩阵运算。此示例还使用了cuda pipeline 接口为gmem到shmem异步加载提供的异步副本，这提高了内核性能并减少了寄存器压力。 [v]   

### [warpAggregatedAtomicsCG](./warpAggregatedAtomicsCG)   

此示例演示了如何使用协作组（CG）对单个和多个计数器执行 warp aggregated 原子，这是一种在多个线程原子添加到单个或多个计数器时提高性能的有用技术。
