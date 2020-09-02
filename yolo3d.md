#### YOLO3D
这篇论文的重点在于，使用投影的方式将点云数据转换为二维的数据然后使用yolo进行CNN处理。分别使用高度图以及深度图作为输入，应该是将其concat在一起的只有两个通道。

在Loss的设计中增加了Z轴方向的损失、高度的损失以及偏角的损失

![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_1.png)
![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_2.png)
![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_3.png)
![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_4.png)
![image](https://github.com/fanbinqi/paper/blob/master/pic/yolo3d_5.png)




|  模型		       | size		   | mIoU	 	 | params	 	 | FLOPs		  | BackBone	  | Decoder	  | Head	 	 | CRF		| inference   
|  ---- 		     | ----		   |  ---- 	 |  ---- 		 |  ---- 		  |  ---- 		  |  ---- 	  |  ---- 	 |  ---- 	| ----
|  SqueezeSeg	   | 64*2048	 | 33.3	 	 | 915.0K	 	 | 13.33G		  | 7.5ms		  | 3.0ms		  | 0.2ms	 	 | none		| 100fps
|  MobileNet	   | 64*2048 	 | 34.6	 	 | 2.33M	 	 | 33.81G		  | 5.3ms		  | 2.5ms		  | 0.2ms	 	 | none		| 125fps
|  HRNet    	   | 64*2048 	 | 16.6	 	 | ~    	 	 | ~    		  | ~   		  | ~   		  | ~   	 	 | none		| ~ 
|  MobileNet_1	 | 64*2048 	 | 33.0	 	 | 1.62M	 	 | 29.84G		  | 2.9ms		  | 1.7ms		  | 0.2ms	 	 | 16.7ms	| 46fps
|  ShuffleNet	   | 64*2048 	 | 33.9	 	 | 959.9K	 	 | 14.09G		  | 12.0ms	  | 2.1ms		  | 0.2ms	 	 | none		| 70fps
|  ShuffleNet_2	 | 64*2048 	 | 32.3	 	 | 823.7K	 	 | 12.88G		  | 7.1ms		  | 1.7ms		  | 0.2ms	 	 | none		| 111fps
|  SqueezeSeg_xyz| 64*2048 	 | 12.9	 	 | ~	    	 | ~		     | ~		      | ~		      | ~	 	    | ~		    | ~
