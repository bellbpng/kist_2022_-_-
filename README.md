# kist_2022_summer_internship
2022 하계 kist 의료AI 연구실에서 인턴으로 근무하며 진행한 내용들을 정리보았습니다.


## 대장내시경 이미지
### 데이터셋
<img src="https://user-images.githubusercontent.com/59792046/187331096-d81c2f06-b8c1-4daf-a833-d7bb2ef4ba75.png" width="700" height="400"/>

<img src="https://user-images.githubusercontent.com/59792046/187331361-59c31145-7ce2-4b1a-9784-62aab669fc6d.png" width="200" height="200"/> <img src="https://user-images.githubusercontent.com/59792046/187331442-ef1c935e-42a6-42ae-99f3-865c17d4a9c1.png" width="300" height="200"/>

#### 용종의 단계는 4단계로 NOR, LGD, HGD, ADC로 구분합니다.
#### Cross Entropy Loss를 사용하여 네트워크 별 성능을 비교하였습니다.
--------------------------------------------------------------------------------------------------------------
### Classification Models - Simple CNN, Pre-trained VGG16, Pre-trained EfficientNet

### Segmentation Models - Custom U-net, Pre-trained FCN_resnet50
#### Segmentation on the ADC class
<img src="https://user-images.githubusercontent.com/59792046/187332675-310cefc5-cc6c-4ae3-a64f-45ade48f55e1.png" width="400" height="500"/>

## 바터팽대부 내시경 이미지
### 데이터셋 - 전처리 전
<img src="https://user-images.githubusercontent.com/59792046/187347879-0c69ffff-5dd4-49ec-8f9c-c4dd32058964.png" width="700" height="700"/>

#### 내시경 이미지만 잘라내는 데이터 전처리 작업을 진행했습니다.
#### 채널 픽셀값들을 모두 합하여 x축 summation, y축 summation을 진행하였습니다. 배경은 주로 검정색 픽셀로 이루어져있기 때문에 적절한 임계값을 정한 후 내시경 이미지 부분의 좌표값을 계산합니다.

### 데이터셋 - 전처리 후
<img src="https://user-images.githubusercontent.com/59792046/187348963-6fe5aaaf-2c97-42ff-87d4-2f72d2aa31f9.png" width="700" height="700"/>

#### 용종의 단계는 4단계로 Normal, LGD, HGD, Cancer로 구분합니다.
#### Pre-trained VGG16 vs Scratch training VGG16 훈련 결과를 비교하였습니다.
#### Focal Loss, Confusion Rate Loss를 활용하며 클래스 불균형 문제를 개선하고자 했습니다.
----------------------------------------------------------------------------------------------------------------
## 대장 내시경 데이터셋 마스크 이미지 활용
### 데이터셋 - 대장 내시경 이미지와 마스크 이미지를 합하여 4개의 채널로 구현

<img src="https://user-images.githubusercontent.com/59792046/187349536-e0baa6ec-5d98-4ea2-ba7f-4f8e78347501.png" width="1000" height="300"/>

#### Pre-trained VGG16 모델을 기준모델로 선정하고 내시경 이미지로만 훈련하였을 때, mask 이미지를 함께 훈련하였을 때 성능을 비교하였습니다.
#### Cross Entropy Loss, Focal Loss를 사용하여 성능을 비교하였습니다.

