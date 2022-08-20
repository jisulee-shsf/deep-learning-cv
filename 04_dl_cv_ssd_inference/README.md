####
## SSD inference
- one-stage detector의 대표 모델인 SSD 실습   
- TensorFlow에서 pretrained된 모델 파일을 OpenCV로 로드해 object detection 수행 실습 
####
#### ► [01_dl_cv_ssd_image_inference_220723]  
- cv_net = cv2.dnn.readNetFromTensorflow() : 가중치 모델 & 환경설정 파일로 inference network model 생성  
- cv_net.setInput(cv2.dnn.blobFromImage()) : image preprocessing 후, inference network model에 입력  
- cv_out = cv_net.forward() : inference한 object detection output을 변수(cv_out)에 저장  
- for detection in cv_out[0, 0, :, :] : detect된 object를 iteration하며 시각화 진행  
####
<img src="https://user-images.githubusercontent.com/109773795/180645517-0839caa9-7ac8-42a1-bed8-9cba8adc20d3.png" width="450" height="330"/><img src="https://user-images.githubusercontent.com/109773795/180645525-20880aa5-2045-411e-b314-9a31ab28c97f.png" width="500" height="330"/>

####
#### ► [02_dl_cv_ssd_video_inference_220723]    
- cap = cv2.VideoCapture() : 영상 각 frame capture 및 속성(frame count, frame size, FPS) 추출  
- video_writer = cv2.VideoWriter() : encoding 및 영상 write 설정  
- 각 frame마다 iteration하며 object detection을 수행하며, 이 과정은 image inference와 유사  
####