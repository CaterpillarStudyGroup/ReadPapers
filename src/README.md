# Template Implicit Warping 

NVIDIA   

## 核心问题是什么?

### 目的

.    
.    
.    
.    
.    

### 现有方法及局限性

.    
.    
.    
.    
.    

### 本文方法

.    
.    
.    
.    
.    

### 效果

.    
.    
.    
.    
.    

## 核心贡献是什么？

.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    

## 大致方法是什么？

![](./assets/51-手写公式1.png) 


1. 找出 source和driving 的 dense correspondence     
2. 基于 dense corresponence 的 warp，称其为 impicit warping 作者认为一个CA可以完成 1 和 2.     

![](./assets/IT图2.png) 

不需要显式地提取光流，Q 和 K 的相似度描述了隐式的光流。  

### 构造 Q. K .V    

**K**: Source keypoint feature     
**Q**: driving keypoint feature   
**V**: Source image feature   

Q 的构造：    

![](./assets/IT手写2.png) 

spafial keypoint 表示，[:,:,i] 为以第i个 keypoint 位置为中心，特定均值和方差的二维一通道高斯。        
   
Q 和 K 的区别：UNet 的输入 concat (加权利spafial keypoint 表示，source Image)     
优势：后面由模块与 keypoint 的个数无关。     

V 的构造：
![](./assets/IT手写3.png) 


Q、K、V 在空间上是对应的。     

CA存在的问题，所有的 key与 quey 都相们度不高时，也会可食见并不合适，或者从key中选择一个SCore最高的,但这个keu选择任何-个keu都不台适    
.    
解决方法:l 增如额外的V 2 使用 aret来鼓励使用额
外的长V[?了额外团KV从师P里来了因为GwCrbpo优议应用于attetm(aer,不能应用于Con.l是有位置关示的
crsss - modal attention，K.kxa，V:kxd'Q:qxa由于soure imane可能有为头，因此 9市p卡不一定相等K= k+PEQ工Q 十FE   
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.    
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

## 训练

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

### 数据集

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

### loss

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

### 训练策略

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

## 实验与结论

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

## 有效

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  


## 局限性

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

## 启发

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

## 遗留问题

.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  

## 参考材料