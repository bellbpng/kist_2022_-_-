# kist_2022_summer_internship
2022 하계 kist 의료AI 연구실에서 인턴으로 근무하며 진행한 내용들을 정리보았습니다.


## 대장내시경 이미지
### 데이터셋
![image](https://user-images.githubusercontent.com/59792046/187331096-d81c2f06-b8c1-4daf-a833-d7bb2ef4ba75.png)

![image](https://user-images.githubusercontent.com/59792046/187331361-59c31145-7ce2-4b1a-9784-62aab669fc6d.png) ![image](https://user-images.githubusercontent.com/59792046/187331442-ef1c935e-42a6-42ae-99f3-865c17d4a9c1.png)

#### 용종의 단계는 4단계로 NOR, LGD, HGD, ADC로 구분합니다.

### Classification Models - Simple CNN, Pre-trained VGG16, Pre-trained EfficientNet

### Segmentation Models - Custom U-net, Pre-trained FCN_resnet50
#### Segmentation on the ADC class
![image](https://user-images.githubusercontent.com/59792046/187332675-310cefc5-cc6c-4ae3-a64f-45ade48f55e1.png)
