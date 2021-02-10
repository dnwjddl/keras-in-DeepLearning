# keras-in-DeepLearning

## 파이썬 라이브러리 ```KERAS```
- 엔진으로는 **Tensorflow**, **Theano**, **CNTK** 등이 있음
- 케라스는 인공지능 엔진 프로그램을 호출하여 인공지능 알고리즘을 수행한다
- 케라스는 특정 엔진에 국한되지 않는 공통 백엔드 함수도 제공해준다.

### CODE
- ```models```는 인공신경망의 각 게층을 연결하여 하나의 모델을 만든 후 컴파일, 학습, 예측을 담당
- ```layers```는 인공신경망의 각 계층을 만드는 클래스 제공

```python
# 케라스로 인공 신경망 모델 만듦. models.Sequential()을 사용하여 파이썬 프로세스에게 알림
## models.Sequential은 파이썬의 클래스
## model이라는 인스턴스 만듦

model = keras.models.Sequential()

# 모델 인스턴스가 생성되면 멤버 함수 add()를 이용하여 인공지능 계층 추가
model.add(keras.layers.Dense(1, input_shape =(1,))

# 학습에 사용되는 최적화 알고리즘 -> 확률적 경사하강법, 손실함수 -> 평균제곱 오차
model.compile('SGD', 'mse')

# 모델을 주어진 데이터로 학습
## verbose는 학습 진행사항 표시 여부
model.fit(x[:2], y[:2], epochs = 1000, verbose = 0)
```
