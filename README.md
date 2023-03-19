## 第一天： 环境配置

### CUDA(Compute Unified Device Architecture)

1. 为什么要使用CUDA

   - CPU的架构中需要大量的空间去放置存储单元和控制单元，相比之下计算单元只占据了很小的一部分，所以它在大规模并行计算能力上极受限制，而更擅长于逻辑控制。

   - GPU包括更多的运算核心，其特别适合数据并行的计算密集型任务，如大型矩阵运算，而CPU的运算核心较少，但是其可以实现复杂的逻辑运算，因此其适合控制密集型任务。另外，CPU上的线程是重量级的，上下文切换开销大，但是GPU由于存在很多核心，其线程是轻量级的。
2. CUDA

   - CUDA提供了GPU编程的简易接口，基于CUDA编程可以构建基于GPU计算的应用程序，利用GPUs的并行计算引擎来更加高效地解决比较复杂的计算难题。
3. 安装
   - [Windows 下安装 CUDA 和 Pytorch 跑深度学习 - 动手学深度学习v2_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV18K411w7Vs/?spm_id_from=333.1007.top_right_bar_window_history.content.click&vd_source=9fd044cd772b8c20f289dea00586e50c)

### miniconda（已安装）

1. 创建虚拟环境(一定要根据书籍的环境推荐安装，不要安装其他版本的python)

   > conda create --name d2l python=3.9 -y
   >
   > conda activate d2l

 2. 下载对应的包(这里用conda install 没有找到对应的包，因为我更换了清华源。所以换成了没换源的pip install)

    > pip install torch==1.12.0
    >
    > pip install torchvision==0.13.0
    >
    > pip install d2l==0.17.6

3. 然后可以下载所有的notebook文件https://zh-v2.d2l.ai/d2l-zh.zip