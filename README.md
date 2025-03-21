# ml-perceptron

# 퍼셉트론(Perceptron)
퍼셉트론(Perceptron)은 "퍼셉션(perception)"과 "트론(tron)"이라는 두 단어가 합쳐진 용어입니다.   
여기서 "퍼셉션"은 인식이나 지각을 의미하며, "트론"은 전자기기나 기계 장치를 나타내는 접미사로 사용됩니다.  
따라서 퍼셉트론은 인식 기능을 가진 기계적 장치라는 의미를 내포하고 있습니다.  
퍼셉트론은 1957년 프랭크 로젠블라트(Frank Rosenblatt)에 의해 개발된 인공 신경망의 가장 기본적인 형태로,  
주로 이진 분류 문제를 해결하는 데 사용됩니다. 
이 모델은 여러 입력을 받아 가중치를 곱한 후, 이들의 합을 활성화 함수에 통과시켜 최종 출력을 생성합니다.    

# 퍼셉트론의 구성 요소
- 입력값 (Inputs): 퍼셉트론은 여러 개의 입력값을 받습니다. 각 입력값은 특정 특성을 나타냅니다.

- 가중치 (Weights): 각 입력값에는 가중치가 부여되어, 입력값의 중요도를 조절합니다. 학습 과정에서 이 가중치는 조정됩니다.

- 바이어스 (Bias): 바이어스는 활성화 함수의 임계값을 조정하는 역할을 합니다. 이는 모델의 예측을 더 유연하게 만듭니다.

- 활성화 함수 (Activation Function): 입력값과 가중치의 가중합을 계산한 후, 이 값을 바탕으로 출력값을 결정합니다. 일반적으로 계단 함수(Step Function)가 사용됩니다.

- 출력 (Output): 최종적으로 퍼셉트론은 0 또는 1의 값을 출력하여 입력 데이터를 분류합니다.


![image](https://github.com/user-attachments/assets/ec0a6ef0-c07a-4b36-be93-11cfbacb5f18)


# Dot Product의 역할

### 가중합 계산:

z=np.dot(x,self.weights[1:])z=np.dot(x,self.weights[1:])는 입력 벡터와 가중치 벡터 간의 내적을 계산합니다. 내적은 각 입력 값과 해당 가중치 값을 곱한 후, 그 결과를 모두 더하는 연산입니다. 이는 다음과 같이 표현할 수 있습니다:  
z=x1⋅w1+x2⋅w2+...+xn⋅wnz=x1​⋅w1​+x2​⋅w2​+...+xn​⋅wn​  
여기서 xixi​는 입력 벡터의 각 요소, wiwi​는 가중치 벡터의 각 요소입니다. 이 계산은 입력의 가중합을 통해 각 입력의 중요도를 반영한 결과를 제공합니다.  

### 바이어스 추가:

이후에 바이어스 값을 추가하여 최종 가중합을 계산합니다. 이는 모델이 입력이 0일 때도 특정 출력을 생성할 수 있도록 합니다. 따라서 최종 식은 다음과 같습니다:  
z=(x1⋅w1+x2⋅w2+...+xn⋅wn)+bz=(x1​⋅w1​+x2​⋅w2​+...+xn​⋅wn​)+b  
