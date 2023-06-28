PBR全称是Physicallly-Based Rendering，所以PBR材质就是指基于物理渲染的材质。

# Blender中的PBR材质
Blender中的PBR材质可以基于[[原理化BSDF]]进行对应图片的连接

![[PBR材质.png]]
![[PBR材质-3.png]]

![[PBR材质-1.png]]
![[PBR材质-各项异性.png]]

![[PBR材质-2.png]]

## 常见的图片后缀：
1.  基础色（漫射）diffuse/albedo/basecolor 缩写diff
2.  置换 displaceme 缩写disp
	需要连接置换节点
3.  法线 normal 缩写nor
4.  reflection/specular反射
	表现物体反射能力的强度
5.  粗糙度/光泽度 glossiness/rougness 缩写 rough
6.  金属 metalness/matallic
7.  不透明度 opacity
8.  高光 specular
9.  环境光遮蔽 AO/AmbienOcclusion
10.  法线贴图 Normal Maps （需要连接法线贴图节点）
11.  bump凹凸
	体现凹凸结构细节

## 置换贴图displaceme
需要连接置换节点，然后直接连接置换
![[PBR材质-4.png]]

## 环境光遮蔽 AO/AmbienOcclusion
与基础色相乘(正片叠底)，然后连接原理化的颜色
可以添加一个颜色渐变设置AO贴图的强度
![[PBR材质-5.png]]