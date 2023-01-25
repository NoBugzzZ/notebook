- ## 环境配置
	- ### mac m1
	  collapsed:: true
		- ### 环境
			- OS and Verison: mac m1 12.4
			- vscode version: 1.73.1
			- c/c++ extension pack version: v1.3.0
		- ### 问题描述
			- ![问题.png](../assets/问题_1670477052948_0.png)
		- ### 解决方案
			- 在源代码中插入
			- ```code
			  #if __INTELLISENSE__
			  #undef __ARM_NEON
			  #undef __ARM_NEON__
			  #endif
			  ```
			-
			- [参考issue](https://github.com/microsoft/vscode-cpptools/issues/7413)
	- ### win11 + wsl2 +vscode
		- 下载wsl插件，然后连接，[参考文档](https://code.visualstudio.com/blogs/2019/09/03/wsl2)
		- ### wsl ubuntu 20.04 镜像
			- 使用对应版本的[清华镜像](https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/)
- ## Lecture 1
	- ### 向量
		- #### dot product
		- #### cross product
		  collapsed:: true
			- 作用： 判断一个向量在另一个向量的左/右，点在三角形内/外。参考：【GAMES101-现代计算机图形学入门-闫令琪】 【精准空降到 37:07】 https://www.bilibili.com/video/BV1X7411F744/?p=2&share_source=copy_web&vd_source=e68dbcdc0f762c484d3e86710ff04abe&t=2227
- ## Lecture 4
	- ### 视图变换
		- 注意：旋转矩阵为正交矩阵，正交矩阵的逆为正交矩阵的转置
	- ### 透视投影
		- 透视->正交的矩阵的推导
- ## lecture 9
	- 纹理太大，远处的texture出现摩尔纹
	- ### mipmap
		- 最大存储极限
		- 判断mipmap层级
		- 三线性插值
		- 问题：overblur，部分解决：各向异性过滤
	- ### 各向异性过滤
		- 从正方形查询->矩形查询
		- 2x为竖直水平方向压缩一次，4x竖直水平方向压缩两次，...
## lecture 10
	- 凹凸贴图改变法线公式
- ## lecture 11
	- ### 贝塞尔曲线
		- 随t变化的线性插值的点
		- Bernstein polynomial，以及其形式的贝塞尔曲线
		- 三次贝塞尔曲线的一些性质
		- 凸包性质
		- 连续性
- ## lecture 12
	- ### Loop 细分 只用于三角形面
		- 在三角形上生成新的顶点
		- 更新新顶点与旧顶点位置
	- ### Catmull-Clark 细分 用于任意面
		- 添加face point，edge point
		- 更新旧的点
		- 连接对应的点
	- ### 网格简化：边坍缩
		- 二次度量误差
		- 边坍缩算法
	- ### shadow map
- ## lecture 13
	- ### 光线与三角形求交点