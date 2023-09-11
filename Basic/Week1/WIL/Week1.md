# Week1

날짜: 2023년 9월 9일
상태: finish

## 목차

## Lec-01

### Supervised/Unsupervised learning

- **Supervised** : learning with labeld examples (traning set) ← 주로 이걸 볼거임
    - ex : image labeling, email spam filter, predicting exam score, AlphaGo …
    - training data set : x와 y의 관계를 학습하여 임의의 x가 들어왔을 때 y를 예측
    - Types
        - regression (predicting final exam score)
        - binary classification (pass/non-pass)
        - multi-label classification (letter grade)
- Unsupervised : un-labeld data

## Lec-02

### Regression

- Linear Regression
    - 데이터를 잘 대변하는 직선의 방정식(y = ax + b)을 찾는 것

### Hypothesis

- H(x) = Wx + b
    - W : weight
    - b : bias

### Cost function

- cost, loss, error : H(x) - y → 가설에 의한 값과 실제 값과의 차이
- 값의 차이가 음수일 때 총 합을 구하는 게 무의미 할 수 있음 → 에러 값을 제곱해서 사용
- 비용함수 : 가설 값과 실제 값의 차이의 제곱 후 평균을 낸 것 → 오차제곱의 평균

## Lab-02

### Hypothesis and Cost

![스크린샷 2023-09-09 오후 4.35.51.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-09_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_4.35.51.png)

### Code

- tf.reduce_mean() : 평균 구하는 함수
    - reduce : rank가 줄어들음
- Gradient descent
    - 경사하강을 이용하여 W, b를 조정해 비용을 최소화시키는 방법
    - tf.GradientTape → with 구문과 함께 쓰임.
- A.assign_sub(B) : A -= B
- Learning rate
    - gradient 값 반영 비율을 조정하는 변수, 기본적으로 굉장히 작게 함.

## Lec-03

### Intro

- how to minimize cost
    
    ![스크린샷 2023-09-09 오후 4.35.51.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-09_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_4.35.51.png)
    
    ![스크린샷 2023-09-11 오후 6.44.23.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-11_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_6.44.23.png)
    
    - 위 수식은 원래 수식에서 b를 제거하여 간략화 한 수식
    - 위 사진의 Cost 함수를 활용하여 W 값을 변화시켜 실제 값으로 대입 후 그래프에 표현

### Gradient descent algorithm

![스크린샷 2023-09-11 오후 6.53.24.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-11_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_6.53.24.png)

- 추정을 통해 초기 값을 넣고, W와 b값을 지속적으로 비용함수가 최소값을 가지는 지점까지 변경을 반복
- 비용함수의 기울기를 곱하여 기존 W에 빼주기 때문에 계속 최저점을 향해 가는 방법
- 위 사진에서 alpha : learning rate (반영 비율)을 의미함. 저 마지막 식이 Gradient descent.
- local minimum의 문제가 있을 수 있음. convex function이면 gradient descent 보장됨.

## Lec-04

### Recap

![스크린샷 2023-09-11 오후 7.34.24.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-11_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_7.34.24.png)

### Multi-variable (Multi-feature)

![스크린샷 2023-09-11 오후 8.29.08.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-11_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_8.29.08.png)

- multi variable일 때는 변수의 개수가 늘고 변수의 개수 만큼 가중치의 개수도 늘어남.
- 너무 많은 변수가 있을 때는 Matrix(행렬)를 활용하여 표현함.
    
    ![스크린샷 2023-09-11 오후 8.30.21.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-11_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_8.30.21.png)
    
    - matrix X 와 matrix W의 행렬곱(내적)으로 표현.
    - 앞의 행렬의 column과 뒤의 행렬의 row가 맞아야 행렬곱(내적)을 사용할 수 있음. 1xN Nx1 ⇒ 1x1.
- input 개수에 영향을 받지 않는 이점을 가짐.

## Lab-04

### data slicing

- 행렬 slicing 관련 코드
    - : 앞 뒤로 숫자가 어디서부터 어디까지를 의미,
        - 아무것도 없으면 전체, :-1은 처음부터 마지막
    - data[:, :-1]
        - 위 slicing은 row는 모든 row, column은 마지막을 제외한 나머지 모두
    - data[:, [-1]]
        - 위 slicing은 모든 row, 마지막 column만 을 의미

### efficiency

- matrix를 사용하면 변수를 줄일 수 있고, 그렇기에 사용되는 코드 양도 줄어들음.
- 표현 측면에서도 유용하고, 효용성 측면에서도 좋다.

## Lab-05

### What is Logistic Regression?

- Classification
    - Binary Classification : [0, 1]
- Logistic vs Linear
    - 데이터들이 불연속적 → Logistic, 데이터들이 연속적 → Linear
        - Logistic : 신발 사이즈, 회사 규모 등, Linear : 시간, 몸무게 등

### How to solve?

- Hypothesis Representation
    - Classification에는 새로운 수식이 필요 ⇒ Logistic function
    - Sigmoid function
        - 1/(1 + (e^-z))
    - Decision Boundary
        
        ![스크린샷 2023-09-11 오후 9.52.40.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-11_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_9.52.40.png)
        
        - 어떠한 값을 기준으로 1과 0 을 나누는 것.
- Linear function → Logistic function → decision boundary
- Cost function
    
    ![스크린샷 2023-09-11 오후 10.02.28.png](Week1%20e686ced3ecbe46f386ea21dd11451104/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-09-11_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_10.02.28.png)
    
    - 기존의 함수를 사용하면 꼬불꼬불한 함수가 나와 적합하지 않음
    - log 함수를 사용하여 Cost 함수를 표현
- Summary
    - 뉴럴 네트워크를 구성하는 하나의 Component
    - x in → linear → activation func → 1, 0 : 뒤에 나올 뉴럴 네트워크를 이해하기 위한 하나의 블록