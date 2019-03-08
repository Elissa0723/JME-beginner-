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

### 旋转物体  
如何将物体旋转到指定的角度？  
这里用到了函数 FastMath.DEG_TO_RAD, 可以将度数转成弧度（因为程序默认计算的是弧度）  
旋转物体45度：  
float r = FastMath.DEG_TO_RAD*45f;  
geom.rotate(0,r,0);  

![Not found](https://github.com/Elissa0723/Image/blob/master/1-5.jpg?raw=true)

沿x，y，z轴分别的旋转图像：  
![Not found](https://github.com/Elissa0723/Image/blob/master/1-6.jpg?raw=true)

代码+注释：  
https://github.com/Elissa0723/JME-beginner-/blob/master/Part2/Part2-3:%E6%97%8B%E8%BD%AC%E7%89%A9%E4%BD%93    

### 让一些物体一起动起来！  
有的时候我们给物体一个一个加效果太过复杂，则可以用到分级node的方法  
之前的总结有介绍过，将rootNode.attachChild(geom);这句话替换为：  
```
Node pivot = new Node("pivot node"); 
pivot.attachChild(geom); 
pivot.attachChild(geom2); 
pivot.rotate(00, 0, FastMath.DEG_TO_RAD * 45); 
rootNode.attachChild(pivot); 
```
这样直接对pivot节点进行操作，可以使geom和geom2同时移动  


