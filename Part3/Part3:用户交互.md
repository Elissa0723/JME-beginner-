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

代码+注释：  
https://github.com/Elissa0723/JME-beginner-/blob/master/Part3/Part3-3:%E9%BC%A0%E6%A0%87%26%E7%9B%91%E6%8E%A7%E5%99%A8 
