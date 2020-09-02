#### YOLO3D
这篇论文的重点在于，使用投影的方式将点云数据转换为二维的数据然后使用yolo进行CNN处理。分别使用高度图以及深度图作为输入，应该是将其concat在一起的只有两个通道。

在Loss的设计中增加了Z轴方向的损失、高度的损失以及偏角的损失

![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_1.png)
![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_2.png)
![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_3.png)
![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_4.png)
![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_5.png)
