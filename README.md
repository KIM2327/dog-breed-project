# dog-breed-project

trained_weights_final.h5
yolov3.weights

위 두 파일은 용량 문제(>100MB)로 올리지 못하였음.

# 프로젝트 요약

Created: 2022년 3월 25일 오후 2:44
Last Edited Time: 2022년 3월 25일 오후 4:50
Participants: 익명, 익명, 익명, 익명, 익명

# 제목 : 영상 객체탐지 기술을 기반한 견종 분류 및 실종견 탐색 서비스

## 선정배경

> 반려동물의 양육 가구수가 2018~2020 최근 3년 간 꾸준히 증가하고 있다.  유기,유실견수도 함께 증가 중이다. 유기견 관련 기존 웹서비스 탐색 후 기존 서비스가 유기견 분양에 집중되어 있고 실종신고 리스트가 여러 곳에 업로드 되어 있어 한 눈에 보기 불편하다는 것을 발견하였다. 실종견을 소유주에게 단기간에 인도하기 위한 방법으로  이 웹서비스를 기획하였다.
> 

![개요1.png](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3%20%2035087/%EA%B0%9C%EC%9A%941.png)

![개요2.png](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3%20%2035087/%EA%B0%9C%EC%9A%942.png)

## 데이터 수집 및 전처리

- 데이터 종류 :  10종 이미지, 견종 정보, 실종신고데이터

<aside>
💡 10종 : 비글, 웰시코기, 불독, 포메라니안, 진돗개, 시추, 말티즈, 치와와, 푸들, 골든 리트리버

</aside>

- 데이터 수집 및 저장 : Requests, Beautifulsoup, sqlite3
- 데이터 전처리 : Labelimg, tensorflow hub object detection API, Pandas, Numpy, Imgaug

## 모델 학습

- 모델 :  YOLOv3
- 사전훈련에 사용된 Dataset : COCO dataset
- 학습방법 : 전이학습, 배치학습
- 학습결과
    - 데이터 수 : 4580장
    - learning rate: 0.00001
    - epoch : 76
    - 한 epoch당 860초
    - loss : 12.6
    - Accuracy : 77.8%
    
    ![Untitled](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3%20%2035087/Untitled.png)
    

## 웹 서비스

- 사용 언어 : HTML5, CSS, Javascript
- 웹 프레임워크 : Bootstrap,Flask
- 웹페이지
    
    ![Untitled](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3%20%2035087/Untitled%201.png)
    
    ![Untitled](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3%20%2035087/Untitled%202.png)