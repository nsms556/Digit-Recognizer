# Digit Recognizer
  - https://www.kaggle.com/competitions/digit-recognizer
  - PyTorch

## 모델
---
### LinearModel
  - nn.Linear 레이어
  - Linear 레이어 사이에 ReLU 활성화
  - 784 -> 128 -> 32 -> 10
  - val_dataset 정확도 : 95.24 %
  - Kaggle 점수 : 0.95210
    
### CNNModel
  - LeNet 구조를 바탕으로 커스텀
  - Conv 레이어 = nn.Conv2d + nn.MaxPool2d
  - Classifier = 2개의 nn.Linear
  - 2번의 Conv 레이어를 거친 후 Classifier 레이어를 거쳐서 출력
  - val_dataset 정확도 : 97.54 %
  - Kaggle 점수 : 0.97339

### AlexNet_28
  - AlexNet 구조를 바탕으로 커스텀
  - Conv1 (Conv2d + ReLU + LRN + Pool) 2층
  - Conv2 (Conv2d + ReLU) 3층 + Pool 1층
  - Classifier = (Dropout + Linear + ReLU) 2층 + Linear 1층
  - val_dataset 정확도 : 98.8 %
  - Kaggle 점수 : 0.98792

## 성적
---
![Score](https://raw.githubusercontent.com/nsms556/Digit-Recognizer/master/Final_Score.png)