### 建立监听器  
这里代码建立了2组监听器：  
+ C键，空格键变换cube颜色
+ 鼠标左键旋转cube

代码：  
https://github.com/Elissa0723/JME-beginner-/blob/master/Part3/Part3-1:%E7%9B%91%E5%90%AC%E5%99%A8  

### 建立有指向的监听器  
如果我们有多个object，我们如何选择只对其中的一个进行操作？  
首先，我们建立了一个瞄准点，通过计算这个瞄准点和cube之间的距离来判断选中了哪个cube
这样我们可以针对每个cube进行操作

代码+注释：  
https://github.com/Elissa0723/JME-beginner-/blob/master/Part3/Part3-2:%E6%9C%89%E6%8C%87%E5%90%91%E7%9A%84%E7%9B%91%E5%90%AC%E5%99%A8

### 鼠标&监控器  
上面做出了如何把物体对准瞄准器，然后让指定object移动，但是往往我们在实际情况中，并不是把object对准瞄准器，而是用鼠标去点击object操作
本节代码主要介绍如何把瞄准器改成鼠标，针对每个cube进行旋转  

我们的鼠标默认是不可见的，如何使鼠标可见：  
```
flyCam.setDragToRotate(true); 
inputManager.setCursorVisible(true);
```

距离算法部分代码+注释：  
https://github.com/Elissa0723/JME-beginner-/blob/master/Part3/Part3-3:%E9%BC%A0%E6%A0%87%26%E7%9B%91%E6%8E%A7%E5%99%A8 

### 方块追随者  
这部分介绍了一个神奇的算法，如何追随一个方块，当然，这里追随的意义是当相机举例10wu以上，立方体就会远离相机
这里我们指定了一个方块，并且随机创造了其他40个方块来凸显这个指定方块运动的轨迹  
![Not Found](https://github.com/Elissa0723/Image/blob/master/3-1.jpg?raw=true) 
为了达到目标，我们需要在simpleUpdate()中添加判断代码：  
```
if(cam.getLocation().distance(scaredCube.getLocalTranslation())	<10)	
                {scaredCube.move(cam.getDirection());} 
```
如果指定方块和相机的距离小于10wu，则把方块远离  
代码+注释：  
https://github.com/Elissa0723/JME-beginner-/blob/master/Part3/Part3-4:%20%E6%96%B9%E5%9D%97%E8%BF%BD%E9%9A%8F%E8%80%85
