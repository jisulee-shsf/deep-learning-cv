####
## 📌 YOLO(You Only Look Once) inference
- YOLOv3 & YOLOv3-tiny 모델의 image inference 속도 및 성능 비교 실습
- Darknet 사이트에서 pretrained된 모델을 다운로드한 뒤, OpenCV로 inference 모델을 생성해 object detection 수행 실습  
- 3개의 scale output layer에서 detect된 정보를 추출해 NMS(Non-Maximum Suppression)로 최종 결과 filtering 진행  
####
#### ► [01_dl_cv_yolov3_image_inference_220724]  
- performance는 우수하나, CPU 기준 image 1장을 inference하기 위해 약 1.62초의 detection time이 소요됨
- inference 속도가 매우 느려 real-time object detection 진행이 부적절함을 실습을 통해 확인
####
#### ► [02_dl_cv_yolov3_tiny_image_inference_220724]  
- YOLOv3의 단점인 느린 inference 속도를 보완하기 위해 network 모델이 간소화된 YOLOv3-tiny 모델 실습 진행
- 약 0.28초의 비교적 짧은 detection time이 소요되나, YOLOv3에 비해 performance가 상당히 떨어짐을 실습을 통해 확인
####
<img src="https://user-images.githubusercontent.com/109773795/184443685-be509a8c-033e-4dcc-89d6-e6c038d62f64.png" width="450" height="350"/><img src="https://user-images.githubusercontent.com/109773795/184443704-d68882ff-f4a1-4c41-8645-7d3c1d96ced9.png" width="450" height="350"/>

####
