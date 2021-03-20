[→ Open in Slid](https://slid.cc/vdocs/1892c51914264b23b9f7e3c02a84a884)


---

## 회귀 분석

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/db60f8b6-b09d-4611-a5a4-768a44f457fe.png "2강 image")


회귀 분석


 - 관찰된 연속형 변수들에 대해 두 변수 사이의 모형을 구한 뒤 적합도를 측정
 - 시간에 따라 변화하는 데이터, 어떤 영향, 가설적 실험, 인과 관계의 모델링 등
 - 입력 객체에 대한 속성을 백터 형태로 포함
 - 유추된 함수에서 연속적 값을 출력
 - 선형모델 : 입력 특성에 대한 선형함수를 만들어 예측을 시행한다.<br>입력(x, 독립변수) 출력(y, 종속 변수)
 - 단순 희귀 분석<br>1:1관계
 - 다중 희귀 분석<br>n:1관계(y,x1,x2,x3)




![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/20080cd7-e37a-4e49-88cb-29644678cce2.png "2강 image")




![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/ad7ff3c7-dd38-4091-82e7-6a6505f31b3c.png "2강 image")




![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/3e69a047-2efb-49f7-b9a5-6278104838a4.png "2강 image")


test값과 가장 가까운 데이터 k개를 선정하여 그 데이터와 가까운 훈련 데이터 값을 가져와서 예측을 함.


-&gt; 여러개 일 경우 평균값





g

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/6bf453c0-6561-4327-95fd-c1f57f61b952.png "2강 image")


test_size을 변경할 경우 (defult : 0.25)


R^2이 변경됨을 볼 수 있다.




## 결정계수 (R^2)

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/e47e0b37-f9a3-48fe-8b24-348b0991f5c8.png "2강 image")

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/a323fc09-080d-4ad5-bd96-2d0af6d4dfb3.png "2강 image")


 - 모든 예측값을 타겟의 평균이라고 가정
 - 매우 단순한 예측 모형과 만든 예측 모형을 비교함





0이 나올 경우


 - 0값이 나올 경우에는 평균값 예측 모델과 같다.





1이 나올 경우


 - 오차가 0인 상황, 완벽 예측
 - trainning error이 0이면 <b>과적합</b>





0이나 1둘다 문제가 됨


 - <b>평균보다 나쁘게 예측</b>하면 음수가 될 수 있음.




![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/ae09041f-9fb1-4866-bbbb-3305a7b9ee3e.png "2강 image")


결과를 볼때 k가 높을 수록 결정 경계가 부드럽게 형성됨.

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/0403c6c3-65f3-4c55-a18f-774ef71e2fea.png "2강 image")




![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/2aadf323-61de-4e22-a2fc-a9630636538c.png "2강 image")


중요 매개 변수


 1. 거리 측정 방법
 2. 이웃의 수





장점


 1. 이해하기 쉬움
 2. 조정없이 잘 작동 가능
 3. 처음 시도 모델 적합
 4. 비교적 빠름


단점


 1. 특정 개수나 샘플 개수가 크면 예측이 느리다.
 2. 정처리 중요
 3. 희소한 데이터 셋에 잘 작동 하지 않음




## 선형 회귀 모델

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/ca038c83-d9ba-4472-8fd2-27b4e602978e.png "2강 image")


y^는 예측값


 - 1차식으로 w[0]은 기울기, b는 절편
 - x가 여러개 일 경우 w도 많아진다.
 - x[n] = 데이터 특성
 - w,b 모델이 학습할 파라미터
 - y : 모델 생성 예측값




![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/a6954ced-6132-4746-b45d-6de6cb870e0b.png "2강 image")




## 선형회귀 : 최소 제곱법

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/3a4382db-99e8-4889-8b0c-65365f76fbce.png "2강 image")

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/58cdf90e-178a-41a4-86fe-b13fa849fded.png "2강 image")

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/7d8cec1f-dbdc-4b2d-871d-e31bd6fe13fb.png "2강 image")

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/ee24aa4c-e650-4502-a28e-912ac537718d.png "2강 image")


위의 그래프를 통해 각 기울기와 절편을 구할 수 있다.

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/b5a40684-851b-4c34-b0be-f1e00bf213f3.png "2강 image")


시간 평균 = 5


성적(y) 평균 = 90.5

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/2202539f-8b11-410b-ae82-ac523619976c.png "2강 image")




## 평균 제곱근 오차

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/7b78b28b-3686-48ca-9d40-52dd0685686f.png "2강 image")


그래프에서 각 변량과 그래프에서 오차가 발생 하는데 이 오차를 가장 적게 나오는(최소화)되는 그래프를 찾는 방법


 1. 임의의 선을 그림
 2. 이 선과 변량의 오차를 구해서 수정함

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/124b0435-1f45-4d31-8121-fb4c3926666b.png "2강 image")

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/f2fbe3bd-74d5-464c-86e4-0463aa7a130e.png "2강 image")

## 오차 수정하기 : 경사 하강법

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/c7d2d3d3-6f48-4175-8c81-427dec0b7f7f.png "2강 image")


소 제곱 문제의 근사해를 구해서 수치적으로 해결


 1. 임의의 선을 그림
 2. 기울기와 절편을 수정하며 가장 오차가 적은 선이 될 때 까지 선을 바꿈
 3. cost(평균제곱)의 최소값을 구함<br>-&gt; 2차 함수<br>w와, b에 대한 2차 함수가 그려진다<br>
 4. w, b가 가장 적은(기울기가 0인 곳 : 극소값)

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/407d9871-cd72-45fe-95bc-d96cdc088272.png "2강 image")


경사 하강법


 1. 임의의 점에서 시작
 2. 기울기가 0으로 가깝게 변하는 알고리즘을 구상함
 3. 0이 되면 멈춤





2번의 식

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/e1496d88-74c3-4076-ad55-2525deaf265c.png "2강 image")




## Cost Function/Optimizer

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/8013dc6f-90c0-49ae-9b3a-260217ea31d6.png "2강 image")


Cost Function


 - 손실함수(loss function)
 - 실제값과 예측값의 차이(y-y^)
 - 잔차, 잔차의 합, 잔차의 제곱합


Optimizer


 - 비용 함수의 최소값을 찾는 알고리즘
 - Gradient Descent(경사 하강법)<br>Optimizer중 하나<br>
 - Mean squared error function
 - 미분을 통해 cost가 최소(0)이 되는 곳을 찾는 지점





Gradient Descending

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/14e792f4-afb8-4bf9-bc76-af0f17c3fad9.png "2강 image")




![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/a99240de-15c6-413a-b35d-2abd0e6f07b5.png "2강 image")


학습률에 따라 다르게 됨


1번 그래프는 학습율이 작을 경우


2번 그래프는 학습율이 클 경우




## 선형 회귀 함수

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/d81fabae-da17-4a1e-97fc-45a97ebcac2f.png "2강 image")




## Linear_regression vs. KNN


Knn과 선형 회귀 모델을 해봄




## 선형 회귀 모델의 성능 측정

![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/d8e9ff7f-3c83-430b-b667-88a62fcf5f23.png "2강 image")


knn과 비교할 경우


(디폴트 = 5)


선형 모델이 조금 더 결과가 잘 나옴(위쪽)




![](https://slid-capture.s3.ap-northeast-2.amazonaws.com/public/capture_images/1892c51914264b23b9f7e3c02a84a884/471578b6-64c8-40f0-93fd-bc0a3ec828a9.png "2강 image")


특징을 104개로 확장 할경우 extended_boston을 이용해서 혹장 시킴


이 친구들을 다시 모델링 할 경우


훈련 세트 점수가 0.95가 나오는데 테스트 점수가 매우 낮아(0.61) 과대 적합이 되어서 좋지 않은 모델로 보인다.


KNN에 대해서도 0.9의 훈련 세트 점수가 나오나 테스트 세트 점수에서는 0.6이 나온다.
