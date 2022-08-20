####
## Instance segmentation  
- COCO(Common Objects in Context) dataset과 API를 활용한 instance segmentation 시각화 수행 실습
- polygon & mask annotation 정보를 활용해 instance segmentation 시각화 수행 실습
####
#### ► [01_dl_cv_coco_api_220725]  
- coco = COCO(annotation_file) : annotation 파일을 객체로 로드해 COCO API인 pycocotools 활용
- coco.getAnnIds() : imgIds & catIds를 입력해 image의 annotation id 반환
- coco.loadAnns() : 반환된 annotation id를 입력해 각 object의 annotation 정보 반환
- coco.showAnns() : 반환된 annotation 정보를 입력해 시각화 진행
####
<img src="https://user-images.githubusercontent.com/109773795/184450892-c0e09504-0f71-45c1-9946-58c35cc5a8a2.png" width="450" height="310"/><img src="https://user-images.githubusercontent.com/109773795/184450899-bb76c9bc-0888-4570-b1c8-cc72d6174b4e.png" width="450" height="310"/>

####
#### ► [02_dl_cv_polygons_n_masks_220725]  
- cv2.polylines() : polygon 좌표 정보를 활용해 instance segmentation 외곽선 시각화 진행
- cv2.fillPoly() : polygon 좌표 정보를 활용해 instance segmentation 내부 시각화 진행
- coco.annToMask() : polygon 좌표 정보에 따라 mask 형태로 변환
- cv2.bitwise_and() : 0 또는 255의 int로 변환된 mask 값 중, 255의 object 영역만 시각화 진행 
- cv2.findContours() & cv2.drawContours() : mask의 외곽선을 찾은 후, 외곽선 시각화 진행 
- draw_instance_segmentation : 상기 실습 내용을 바탕으로, 최종 instance segmentation 시각화 진행
####
<img src="https://user-images.githubusercontent.com/109773795/184449990-4f63b03b-7cce-4fa9-bfba-74aab72eda5e.png" width="300" height="220"/><img src="https://user-images.githubusercontent.com/109773795/184450083-9db6412e-ef88-4f48-b9c4-7287533dfa31.png" width="300" height="220"/><img src="https://user-images.githubusercontent.com/109773795/184450133-485249d7-60e5-4672-baae-c20b3599de06.png" width="300" height="220"/>
<img src="https://user-images.githubusercontent.com/109773795/184450106-8adfc59b-658b-4d8f-8c8b-25100831a2af.png" width="300" height="220"/><img src="https://user-images.githubusercontent.com/109773795/184450108-ec0d1b7b-528b-4747-847c-1dd12a353565.png" width="300" height="220"/><img src="https://user-images.githubusercontent.com/109773795/184450118-aecffbd3-2a8d-4d5f-9544-ca481a6b53f9.png" width="300" height="220"/>

####