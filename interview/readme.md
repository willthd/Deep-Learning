# Interview

> 머신러닝 Interview 준비

### 손실 함수 종류

* MSE(Mean Squared Error)

* RMSE

* MAE

* CEE(Cross Entropy Error)



정확도를 놔두고 '손실 함수'라는 우회적인 방법을 택하는 이유는 딥러닝은 **오차역전파법**(역전파, back propagation) 방식을 활용해 오차를 줄여 나가는데 이 때 미분을 사용한다. 하지만 정확도 or AUC 등은 미분 불가능하기 때문에 매개변수의 미소 변화가 있어도 반응이 없거나 불연속적으로 변화한다. 따라서 '손실 함수'라는 우회적인 방법을 이용하는 것이며, 궁극적으로 손실 함수가 최소가 되는 최적의 매개 변수 값을 찾는다.(계단 함수를 활성화 함수로 사용하지 않는 이유와도 동일하다.)

기울기 산출 시, 오차역전파법 방식은 중복 계산을 피하면서 수치 미분법보다 훨씬 계산이 빠르다.(수치 미분법은 구현하기 더 쉬우며, 오차역전파법으로 구한 기울기를 확인하는 데 사용한다.)

</br>

### 확률적 경사 하강법 (SGD)

무작위로 골라낸 데이터(미니 배치)를 이용해 손실 함수를 기울기가 감소 하는 방향으로 최소화 시켜 최적의 매개변수를 찾는 방법

![sgd](/Users/bagjongsu/Desktop/github/Machine-Learning/interview/sgd.png)

</br>

### batch_size, epoch, iterations

train data의 개수가 20,000개. batch_size가 500이라고 가정하면 1epoch을 돌기 위해 40회 학습 필요하다. 그리고 30 epoch을 돌기 원한다면 30 * 40회 학습을 해야한다.

</br>
