# threejs中的材质

材质就像是物体的皮肤，巨鼎几何体外表的样子。

#### 材质种类
+ MeshBasicMaterial(网格基础材质)：基础材质，可以赋予几何体一种简单的颜色，或者几何线条
+ MeshDepthMaterial(网格深度材质)：根据网格到相机的距离，这种材质决定如何给网格染色
+ MeshNormalMaterial(网格法向材质)：简单材质，根据物体表面的法向向量计算颜色
+ MeshLambertMaterial(玩个朗伯材质)：这种材质会考虑光照的影响，可以用来创建颜色暗淡的，不光亮的物体
+ MeshPhongMaterial(网格Phong材质)：会考虑光照的影响，用来创建光亮的物体
+ ShaderMaterial(着色器材质)：允许使用自定义的着色器程序，直接控制顶点的放置方式，以及像素的着色方式
+ LineBasicMaterial(直线基础材质)：可用于直线几何体，创建着色的直线
+ LineDashedMaterial(虚线材质)：同上，可以创建虚线效果

#### 基础属性
+ ID 标识符
+ name 名称
+ opacity 透明度，定义物体有多透明，与transparent仪器私用，取值0-1
+ transparent 是否透明，如果true，取值opacity，false不透明，着色明亮一些
+ overDraw 过度描绘 如果用THREE.CanvasRenderer对象，多边形会被渲染的稍微大一点，当用这个渲染器画出来物体有裂缝时，可以设置true
+ visible 是否可见
+ side 侧面：决定几何体哪一面用这个材质，默认THREE.FrontSide,可以设置为THREE.BackSide，或者THREE.DoubleSide
+ needsUpdate 对于材质的某些修改，要告诉three.js库材质已经改变了，为true的话three.js会使用新的材质属性刷新它的缓存。



