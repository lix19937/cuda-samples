# 4. CUDA 相关库


### [batchCUBLAS](./batchCUBLAS)
CUDA示例，演示如何使用批处理CUBLAS API 调用来提高总体性能。 [v]    

### [batchedLabelMarkersAndLabelCompressionNPP](./batchedLabelMarkersAndLabelCompressionNPP)
An NPP CUDA Sample that demonstrates how to use the NPP label markers generation and label compression functions based on a Union Find (UF) algorithm including both single image and batched image versions.

### [boxFilterNPP](./boxFilterNPP)
A NPP CUDA Sample that demonstrates how to use NPP FilterBox function to perform a Box Filter.

### [cannyEdgeDetectorNPP](./cannyEdgeDetectorNPP)
An NPP CUDA Sample that demonstrates the recommended parameters to use with the nppiFilterCannyBorder_8u_C1R Canny Edge Detection image filter function. This function expects a single channel 8-bit grayscale input image. You can generate a grayscale image from a color image by first calling nppiColorToGray() or nppiRGBToGray(). The Canny Edge Detection function combines and improves on the techniques required to produce an edge detection image using multiple steps.

### [conjugateGradient](./conjugateGradient)
This sample implements a conjugate gradient solver on GPU using CUBLAS and CUSPARSE library.

### [conjugateGradientCudaGraphs](./conjugateGradientCudaGraphs)
此示例使用CUBLAS和CUSPARSE库调用在GPU上实现共轭梯度解算器，这些库调用是使用CUDA Graph API捕获和调用的。 [v]

### [conjugateGradientMultiBlockCG](./conjugateGradientMultiBlockCG)
This sample implements a conjugate gradient solver on GPU using Multi Block Cooperative Groups, also uses Unified Memory.

### [conjugateGradientMultiDeviceCG](./conjugateGradientMultiDeviceCG)
This sample implements a conjugate gradient solver on multiple GPUs using Multi Device Cooperative Groups, also uses Unified Memory optimized using prefetching and usage hints.

### [conjugateGradientPrecond](./conjugateGradientPrecond)
This sample implements a preconditioned conjugate gradient solver on GPU using CUBLAS and CUSPARSE library.

### [conjugateGradientUM](./conjugateGradientUM)

This sample implements a conjugate gradient solver on GPU using CUBLAS and CUSPARSE library, using Unified Memory

### [cudaNvSci](./cudaNvSci)

此示例演示CUDA NvSciBuf/NvSciSync互操作。两个CPU线程将NvSciBuf和NvSciSync导入CUDA，以对ppm图像执行两种图像处理算法-第一个线程中的图像旋转和第二个线程中旋转图像的rgba到灰度转换。目前仅在Ubuntu 18.04上支持   [v]    

### [cudaNvSciNvMedia](./cudaNvSciNvMedia)

此示例通过NvSciBuf/NvSciSync API演示CUDA NvMedia互操作。请注意，此示例仅支持从x86_64到aarch64的交叉构建，不支持aarch64本机构建。有关示例的详细工作流程，请查看示例目录中的cudaNvSciNvMedia_Readme.pdf。  

### [cuDLAErrorReporting](./cuDLAErrorReporting)

此示例演示了如何通过CUDA检测DLA错误。


### [cuDLAHybridMode](./cuDLAHybridMode)

该示例演示了cuDLA混合模式，其中DLA可以使用CUDA进行编程。


### [cuDLAStandaloneMode](./cuDLAStandaloneMode)

此示例演示了cuDLA独立模式，其中可以在不使用CUDA的情况下对DLA进行编程。

### [cuSolverDn_LinearSolver](./cuSolverDn_LinearSolver)

A CUDA Sample that demonstrates cuSolverDN's LU, QR and Cholesky factorization.

### [cuSolverRf](./cuSolverRf)
A CUDA Sample that demonstrates cuSolver's refactorization library - CUSOLVERRF.

### [cuSolverSp_LinearSolver](./cuSolverSp_LinearSolver)
A CUDA Sample that demonstrates cuSolverSP's LU, QR and Cholesky factorization.

### [cuSolverSp_LowlevelCholesky](./cuSolverSp_LowlevelCholesky)
A CUDA Sample that demonstrates Cholesky factorization using cuSolverSP's low level APIs.

### [cuSolverSp_LowlevelQR](./cuSolverSp_LowlevelQR)
A CUDA Sample that demonstrates QR factorization using cuSolverSP's low level APIs.

### [FilterBorderControlNPP](./FilterBorderControlNPP)
This sample demonstrates how any border version of an NPP filtering function can be used in the most common mode, with border control enabled. Mentioned functions can be used to duplicate the results of the equivalent non-border version of the NPP functions. They can be also used for enabling and disabling border control on various source image edges depending on what portion of the source image is being used as input.

### [freeImageInteropNPP](./freeImageInteropNPP)
A simple CUDA Sample demonstrate how to use FreeImage library with NPP.

### [histEqualizationNPP](./histEqualizationNPP)
This CUDA Sample demonstrates how to use NPP for histogram equalization for image data.

### [lineOfSight](./lineOfSight)
This sample is an implementation of a simple line-of-sight algorithm: Given a height map and a ray originating at some observation point, it computes all the points along the ray that are visible from the observation point. The implementation is based on the Thrust library.

### [matrixMulCUBLAS](./matrixMulCUBLAS)

此示例实现编程指南第3章中的矩阵乘法。为了说明GPU在矩阵乘法方面的性能，本示例还展示了如何使用CUBLAS的新CUDA 4.0接口来演示矩阵乘法的高性能。

### [MersenneTwisterGP11213](./MersenneTwisterGP11213)
This sample demonstrates the Mersenne Twister random number generator GP11213 in cuRAND.

### [nvJPEG](./nvJPEG)

CUDA示例，演示使用NVJPEG库对jpeg图像进行单次和批量解码。


### [nvJPEG_encoder](./nvJPEG_encoder)

CUDA示例，演示使用NVJPEG库对jpeg图像进行单一编码。


### [oceanFFT](./oceanFFT)
This sample simulates an Ocean height field using CUFFT Library and renders the result using OpenGL.

### [randomFog](./randomFog)
This sample illustrates pseudo- and quasi- random numbers produced by CURAND.

### [simpleCUBLAS](./simpleCUBLAS)
Example of using CUBLAS API interface to perform GEMM operations.

### [simpleCUBLAS_LU](./simpleCUBLAS_LU)
CUDA sample demonstrating cuBLAS API cublasDgetrfBatched() for lower-upper (LU) decomposition of a matrix.

### [simpleCUBLASXT](./simpleCUBLASXT)
Example of using CUBLAS-XT library which performs GEMM operations over Multiple GPUs.

### [simpleCUFFT](./simpleCUFFT)
Example of using CUFFT. In this example, CUFFT is used to compute the 1D-convolution of some signal with some filter by transforming both into frequency domain, multiplying them together, and transforming the signal back to time domain. cuFFT plans are created using simple and advanced API functions.

### [simpleCUFFT_2d_MGPU](./simpleCUFFT_2d_MGPU)
Example of using CUFFT. In this example, CUFFT is used to compute the 2D-convolution of some signal with some filter by transforming both into frequency domain, multiplying them together, and transforming the signal back to time domain on Multiple GPU.

### [simpleCUFFT_callback](./simpleCUFFT_callback)
Example of using CUFFT. In this example, CUFFT is used to compute the 1D-convolution of some signal with some filter by transforming both into frequency domain, multiplying them together, and transforming the signal back to time domain. The difference between this example and the Simple CUFFT example is that the multiplication step is done by the CUFFT kernel with a user-supplied CUFFT callback routine, rather than by a separate kernel call.

### [simpleCUFFT_MGPU](./simpleCUFFT_MGPU)
Example of using CUFFT. In this example, CUFFT is used to compute the 1D-convolution of some signal with some filter by transforming both into frequency domain, multiplying them together, and transforming the signal back to time domain on Multiple GPU.

### [watershedSegmentationNPP](./watershedSegmentationNPP)
An NPP CUDA Sample that demonstrates how to use the NPP watershed segmentation function.

----------------------------- 

本章节内容只选取 视觉网络中常用的技术。  @by lix19937    
