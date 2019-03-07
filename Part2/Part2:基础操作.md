### 初始文档  
代码+注释：   
https://github.com/Elissa0723/JME-beginner-/blob/master/Part2/Part2-1:%E5%88%9D%E5%A7%8B%E7%A8%8B%E5%BA%8F    
  
### 改变位置 & 大小  
改变形状位置有两种方法：
+ geom.move(3.0f,-2.0f,1.0f);  
这里的f指的是float  
<b>相对位置</b>：把当前位置改变(3,-2,1)  
<b>主要适用于在loop中改变物体位置</b>  
+ geom.setLocalTranslation(3.0f,-2.0f,1.0f);   
<b>绝对位置</b>：定位到(3,-2,1)    

代码+注释：  
https://github.com/Elissa0723/JME-beginner-/blob/master/Part2/Part2-2:%E6%94%B9%E5%8F%98%E4%BD%8D%E7%BD%AE  

![Not found](https://github.com/Elissa0723/Image/blob/master/1-4.jpg)

当然改变大小也类似，函数如下：  
+ geom.scale(2.0f);  
<b>相对大小</b>  
+ geom.setLocalScale(0.5f);  
<b>绝对大小</b>  

### 旋转  
选择物体
