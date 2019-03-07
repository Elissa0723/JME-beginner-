# first program  
```
import	com.jme3.app.SimpleApplication; 
import	com.jme3.material.Material; 
import	com.jme3.math.ColorRGBA; 
import	com.jme3.math.Vector3f; 
import	com.jme3.renderer.RenderManager; 
import	com.jme3.scene.Geometry; 
import	com.jme3.scene.shape.Box;
/**	Basic	jMonkeyEngine	game	template.	*/ 
public	class	Main	extends	SimpleApplication	{
				@Override				
        /**	initialize	the	scene	here	*/				
        public	void	simpleInitApp()	{							
        //	create	a	cube-shaped	mesh							
        Box b	=	new	Box(Vector3f.ZERO,	1,	1,	1);											
        //	create	an	object	from	the	mesh							
        Geometry	geom	=	new	Geometry("Box",	b);					
							
        //	create	a	simple	blue	material							
        Material	mat	=	new	Material(assetManager,"Common/MatDefs/Misc/Unshaded.j3md");							
        mat.setColor("Color",	ColorRGBA.Blue);													
        //	give	the	object	the	blue	material							
        geom.setMaterial(mat);							
        //	make	the	object	appear	in	the	scene							
        rootNode.attachChild(geom);				}
        
        @Override				
        /**	(optional)	Interact	with	update	loop	here	*/				
        public	void	simpleUpdate(float	tpf)	{}
				@Override				
        /**	(optional)	Advanced	renderer/frameBuffer	modifications	*/				
        public	void	simpleRender(RenderManager	rm)	{}
				/**	Start	the	jMonkeyEngine	application	*/				
        public	static	void	main(String[]	args)	{							
        Main	app	=	new	Main();							
        app.start();				
        } 
    }
```
