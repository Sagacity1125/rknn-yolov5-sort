# rknn-yolov5-sort
传送带上单只出药计数，采用了yolov5+sort的方法
具体流程如下：
1. 训练出pytorch版本的yolov5目标检测模型 yolo_1class.pt；
2. 将yolo_1class.pt转为yolo_1class.onnx，转换过程中进行了算子优化；
3. 将yolo_1class.onnx转为yolo_1class.rknn；
4. 在rknn-toolkit-1.7.1中调用yolo_1class.rknn。
