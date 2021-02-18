[toc]

## 面电流源

边界上设置面电流源（2D平面内其实是线电流源）：

+ 添加属性：Properties/Boundary/Add Properity/BC Type: Mixed
+ c0=0,  c1=-Js/2 (原因未知)
+ 右键选择线对象，空格，设置Segment Property

## 绕组激励

与材料一起设置

+ 添加属性：Properties/Circuits/Add Properity (串并联指同名绕组的电路连结关系)
+ 右键选择block对象，空格，Block type(选择材料)
+ In Circuit：选择绕组名
+ Number of Turns：匝数（负匝数，相当于与正向绕组构成回路，计算磁链、电感时有用）
