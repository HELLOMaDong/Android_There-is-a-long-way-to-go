## 日常速记 -> 关于减少APK体积

重点：APP结构要先清楚一下   
1. AS双击编译好的apk 
2. apk本就是一个zip

### 代码阶段
1. 避免使用枚举    
1. 减少不必要的生成的代码
### 减少无用资源 
1. so文件，三方Library 网上也是各种软解决 只是提供各种思路     
1. 
1. 能用<shape> in XML 尽量减少png  
1.  减少无用文件例如 xml;png;string;color;等
##### 减少资源分多种  ： 
1.Analyze -> Run Inspection by Name... -> Unused res 可根据条件筛选 

2.右键 -> Refactor -> Remove Unused res (这个是有个坑的一般代码引用的资源文件是不会筛选删除的但Kotlin类代码的资源引用会被删除 有Kotlin慎用)
 
3. minifyEnabled true   
proguardFiles 'proguard.cfg'    
shrinkResources true（引用的资源可以剔除 但要注意有的资源文件是根据代码动态匹配添加这种情况是有问题的）

### 压缩项目中引用的png图

1.可通过在Mac上安装Guetzli 具体细节google   
2.TinyPNG for Mac 这种压缩计算方式暂时算是最优

### 微信混淆
### 插件化了解一下 



