####
## 📌 Mask R-CNN(Region-based Convolutional Neural Networks) inference  
- Mask R-CNN 모델을 활용해 object detection & instance segmentation 수행을 통한 다양한 시각화 실습 진행  
####
#### ► [01_dl_cv_mask_rcnn_inference_practice_v1_220726]  
- class_mask_detected : network model에서 detect된 object의 class mask 정보 추출  
- class_mask_scaled : 15*15 class mask 사이즈를 image에 맞추어 scale out 진행  
- class_mask_scaled_bool : mask_threshold에 따른 boolean 형태의 mask 정보 생성  
- before_masking_roi : mask를 적용할 image 내의 bounding box 영역 추출  
- make_mask : 0 또는 255의 int로 변환된 mask 값 중, 0은 검은색 / 255는 흰색으로 시각화 진행  
- bitwise_masking_roi : 255의 object 영역만 시각화 진행  
- after_masking_roi_color : detect된 object의 mask에 랜덤 투명 색상 적용  
- after_masking_roi_contour : mask 정보를 이용해 외곽선 시각화 진행  
####
<img src="https://user-images.githubusercontent.com/109773795/184458888-92877b9e-7c83-4794-bf32-17e33f41a7f1.png" width="960" height="220"/>

####
#### ► [02_dl_cv_mask_rcnn_image_inference_v2_220726]  
- 상기 v1 practice 사항을 포함하여, Mask R-CNN을 활용한 inference 로직 함수화 진행  
- 함수화된 로직을 사용해 image 내 object detection & instance segmentation 시각화 진행  
####
<img src="https://user-images.githubusercontent.com/109773795/184459195-dd5f3a43-ba2f-4542-98ab-54db7f0f90ed.png" width="450" height="330"/><img src="https://user-images.githubusercontent.com/109773795/184459199-0aa754e2-4e52-41ca-bbae-a1f7e6dc6b54.png" width="500" height="330"/>

####
#### ► [03_dl_cv_mask_rcnn_video_inference_220726]  
- 상기 v2의 함수화된 로직을 사용해 video 각 frame에 object detection & instance segmentation 시각화 진행  
####
