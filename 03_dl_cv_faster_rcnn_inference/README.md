####
## 📌 Faster R-CNN(Region-based Convolutional Neural Networks) inference  
- two-stage detector의 대표 모델인 Faster R-CNN 실습  
- TensorFlow에서 pretrained된 모델 파일을 OpenCV로 로드해 object detection 수행 실습 
####
#### ► [01_dl_cv_faster_rcnn_image_inference_220720]  
- cv_net = cv2.dnn.readNetFromTensorflow() : 가중치 모델 & 환경설정 파일로 inference network model 생성  
- cv_net.setInput(cv2.dnn.blobFromImage()) : image preprocessing 후, inference network model에 입력  
- cv_out = cv_net.forward() : inference한 object detection output을 변수(cv_out)에 저장  
- for detection in cv_out[0, 0, :, :] : detect된 object를 iteration하며 시각화 진행  
####
<img src="https://user-images.githubusercontent.com/108124534/180102570-59006ece-7c3b-4e79-aef3-f67c5a42e9cb.png" width="450" height="330"/><img src="https://user-images.githubusercontent.com/108124534/180102882-cb887229-a749-4ace-b156-6267223e7e13.png" width="500" height="330"/>

####
#### ► [02_dl_cv_faster_rcnn_video_inference_220720]  
- cap = cv2.VideoCapture() : 영상 각 frame capture 및 속성(frame count, frame size, FPS) 추출  
- video_writer = cv2.VideoWriter() : encoding 및 영상 write 설정  
- 각 frame마다 iteration하며 object detection을 수행하며, 이 과정은 image inference와 유사  
####
