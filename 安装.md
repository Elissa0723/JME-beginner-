### 安装JMonkeyEngineer
理论上JME可以装在其他java IDE里面，但是对于初学者而言，建议直接下载JME3的SDK  
下载地址：http://jmonkeyengine.org/downloads/   
### 运行第一个JME程序
File--->New project,得到以下界面
![Not found](https://github.com/Elissa0723/Image/blob/master/1-1.jpg?raw=true)  
选择JME3--->basic game   
这样就建立好了第一个JME程序  

点击左侧 Source Packages-->mygame-->Main.java,得到如下代码  
```
package mygame;

import com.jme3.app.SimpleApplication;
import com.jme3.material.Material;
import com.jme3.math.ColorRGBA;
import com.jme3.renderer.RenderManager;
import com.jme3.scene.Geometry;
import com.jme3.scene.shape.Box;

/**
 * This is the Main Class of your Game. You should only do initialization here.
 * Move your Logic into AppStates or Controls
 * @author normenhansen
 */
public class Main extends SimpleApplication {

    public static void main(String[] args) {
        Main app = new Main();
        app.start();
    }

    @Override
    public void simpleInitApp() {
        Box b = new Box(1, 1, 1);
        Geometry geom = new Geometry("Box", b);

        Material mat = new Material(assetManager, "Common/MatDefs/Misc/Unshaded.j3md");
        mat.setColor("Color", ColorRGBA.Blue);
        geom.setMaterial(mat);

        rootNode.attachChild(geom);
    }

    @Override
    public void simpleUpdate(float tpf) {
        //TODO: add update code
    }

    @Override
    public void simpleRender(RenderManager rm) {
        //TODO: add render code
    }
}
```
右键运行，跳出如下窗口  
![Not found](https://github.com/Elissa0723/Image/blob/master/1-2.jpg?raw=true)  
确认！  
第一个程序完成~~  
![Not found](https://github.com/Elissa0723/Image/blob/master/1-3.jpg?raw=true)
