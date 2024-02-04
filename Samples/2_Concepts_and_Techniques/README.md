# 2. 概念和技术


### [boxFilter](./boxFilter)  

使用CUDA和OpenGL渲染的快速图像框滤波器。

### [convolutionSeparable](./convolutionSeparable)

该样本实现了具有高斯核的2D信号的可分离卷积滤波器。 

### [convolutionTexture](./convolutionTexture)

基于纹理的具有高斯核的可分离2D卷积的实现。用于与卷积Separable进行性能比较。

### [cuHook](./cuHook)

此示例演示如何使用CUDA构建和使用拦截库. 通过 **LD_PRELOAD**, e.g. LD_PRELOAD=<full_path>/libcuhook.so.1 ./cuHook    [v]     

### [dct8x8](./dct8x8)

此示例演示了如何使用CUDA对8乘8像素的块执行离散余弦变换（DCT）：根据定义，这是一种简单的实现方式，也是许多库中使用的一种更传统的方法。与在片段着色器中实现DCT相反，CUDA允许更简单、更高效的实现。

### [EGLStream_CUDA_CrossGPU](./EGLStream_CUDA_CrossGPU)

演示CUDA和EGL Streams互操作，其中使用者的EGL Stream在一个GPU上，生产者在另一个GPU，并且使用者和生产者都是不同的进程。  

### [EGLStream_CUDA_Interop](./EGLStream_CUDA_Interop)

演示CUDA和EGL Streams之间的数据交换。

### [EGLSync_CUDAEvent_Interop](./EGLSync_CUDAEvent_Interop) 

演示CUDA Event和EGL Sync/EGL Image之间的互操作性，使用该互操作性可以在GPU本身上实现GL-EGL-CUDA操作的同步，而不是阻止CPU进行同步。

### [eigenvalues](./eigenvalues)  

所有特征值的全部或子集的计算是线性代数、统计学、物理学和许多其他领域的一个重要问题。该示例演示了使用CUDA计算任意大小的三对角对称矩阵的所有特征值的平分算法的并行实现。

### [FunctionPointers](./FunctionPointers)

此示例说明了如何使用函数指针并实现8位单色图像的Sobel边缘检测滤波器。  [v]   

### [histogram](./histogram)

此示例演示了64位和256位直方图的有效实现。 [v]    

### [imageDenoising](./imageDenoising)

该示例演示了两种自适应图像去噪技术：KNN和NLM，基于纹理元素之间的几何距离和颜色距离的计算。虽然这两种技术都是在DirectX SDK中使用着色器实现的，但除了DirectX对应技术之外，还利用共享内存实现了后一种技术的大幅加速变体。

### [inlinePTX](./inlinePTX)

一个简单的测试应用程序，展示了CUDA 4.0在CUDA内核中嵌入PTX的新功能。 [v]   

### [inlinePTX_nvrtc](./inlinePTX_nvrtc)

一个简单的测试应用程序，展示了CUDA 4.0在CUDA内核中嵌入PTX的新功能。 [v]   

### [interval](./interval)

区间算术运算符示例。使用各种C++功能（模板和递归）。递归模式需要Compute SM 2.0功能。

### [MC_EstimatePiInlineP](./MC_EstimatePiInlineP)

此示例使用蒙特卡罗模拟来估计Pi（使用内联PRNG）。此示例还使用NVIDIA CURAND库。

### [MC_EstimatePiInlineQ](./MC_EstimatePiInlineQ)

此示例使用蒙特卡罗模拟来估计Pi（使用内联QRNG）。此示例还使用NVIDIA CURAND库。

### [MC_EstimatePiP](./MC_EstimatePiP)

此示例使用蒙特卡罗模拟来估计Pi（使用批处理PRNG）。此示例还使用NVIDIA CURAND库。

### [MC_EstimatePiQ](./MC_EstimatePiQ)

此示例使用蒙特卡罗模拟来估计Pi（使用批QRNG）。此示例还使用NVIDIA CURAND库。

### [MC_SingleAsianOptionP](./MC_SingleAsianOptionP)

此示例使用蒙特卡罗模拟使用NVIDIA CURAND库的Single Asian Options。

### [particles](./particles) 

此示例使用CUDA来模拟和可视化一大组粒子及其物理相互作用。在命令行中添加“-particles=<N>”将允许用户设置模拟的粒子数。此示例使用原子运算或Thrust库中的快速基数排序来实现统一的网格数据结构

### [radixSortThrust](./radixSortThrust)

此示例演示了使用Thrust库的一种非常快速高效的并行基数排序。包含的RadixSort类可以对键值对（使用浮点或无符号整数键）或仅对键进行排序。  [v]    

### [reduction](./reduction)

一种并行求和约简，用于计算大型值数组的和。此示例演示了数据并行算法的几个重要优化策略，如使用共享内存减少、__shfl_down_sync、__reduce_add_sync和cooperative_groups-reduce。  [v]   

### [reductionMultiBlockCG](./reductionMultiBlockCG) 

此示例演示了使用多块协作组的单程规约。此示例要求具有6.0或更高计算能力的设备具有计算抢占权。  [v]    

### [scalarProd](./scalarProd)

此示例计算给定一组输入向量对的标量乘积。   [v]    

### [scan](./scan)

此示例演示了并行前缀和的高效CUDA实现，也称为“扫描”。给定一个数字数组，scan计算一个新数组，其中每个元素都是输入数组中它之前的所有元素的总和。   [v]    

### [segmentationTreeThrust](./segmentationTreeThrust)

此示例演示了一种构建图像分割树的方法。该方法基于Boruvka的MST算法。 [v]    

### [shfl_scan](./shfl_scan)

此示例演示如何使用shuffle内在__shfl_up_sync在线程块上执行扫描操作。 [v]   

### [sortingNetworks](./sortingNetworks)

此示例实现了属于排序网络类别的双调排序和奇偶合并排序（也称为Batcher排序）。虽然通常效率较低，但与具有更好渐进算法复杂性的算法（即合并排序或基数排序）相比，对于大序列，这可能是排序从短到中（键、值）数组对的批量的首选算法。 http://www.iti.fh-flensburg.de/lang/algorithmen/sortieren/networks/indexen.htm    [v]    

### [streamOrderedAllocation](./streamOrderedAllocation)

此示例演示了使用cudaMallocAsync和cudaMemPool系列API在GPU上进行流顺序内存分配。 [v]   

### [streamOrderedAllocationIPC](./streamOrderedAllocationIPC)

此示例演示了使用cudaMallocAsync和cudaMemPool系列API分配的流序内存的IPC池。 [v]    

### [streamOrderedAllocationP2P](./streamOrderedAllocationP2P)

此示例演示了使用cudaMallocAsync和cudaMemPool系列API分配的流序内存的p2p访问。 [v]    

### [threadFenceReduction](./threadFenceReduction)

此示例显示如何使用线程Fence内在函数对值数组执行归约操作，以在单个内核中生成单个值（而不是“归约”CUDA示例中所示的两个或多个内核调用）。单程还原需要全局原子指令（Compute Capability 2.0或更高版本）和_threadfence（）内在指令（CUDA 2.2或更高级别）。 [v]    

### [threadMigration](./threadMigration)  

简单的程序说明如何使用CUDA上下文管理API并使用新的CUDA 4.0参数传递和CUDA启动API。CUDA上下文可以单独创建，并独立附加到不同的线程。 [v]    

