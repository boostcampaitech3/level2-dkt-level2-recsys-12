# DKT-EDA 실전

작성일시: 2022년 4월 18일 오후 6:01

## DKT Basic

---

 기본적인 Feature에 대해서 알아보자

| userID | 누가 풀었는지 | 6698개 |
| --- | --- | --- |
| assessmentItemID | 어떤 문제를 | 9454개 |
| testID  | 어떤 시험지에서 풀었고 | 1537개 |
| answerCode  | 정답이 맞았는지 | 2개 |
| Timestamp | 언제 풀었고 | No Need |
| KnowledgeTag | 문제 테그 | 912개 |

전체 데이터 개수

2266586 개

### AssessmentItemID

---

### A060001001

1: 무조건 A

2~6 = 시험지 번호

나머지 = 문제 번호

### TestID

---

### A060000001

1: 무조건 A

2~4, 8~ = AssessmentItemId의 시험지 번호와 일치

5~7 = 무조건 000

### AnswerCode

---

 1 = 맞은것 0 = 틀린것

전체의 62%가 1, 나머지 0

### 1인당 문제를 푼 개수

---

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/79d1b25c-2000-41b4-b785-f1381ad8ade3/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220421%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220421T073845Z&X-Amz-Expires=86400&X-Amz-Signature=615dc152b2dc7c79edae2f092b1f66b1f03a2538d8731d287d32e4499fd67d0b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

평균은 321.3314 문제

가장 적게 푼 사람: 43명

가장 많이 푼 사람: 454명

### 1인당 정답률

---

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/da3ccf46-2e35-4b98-b212-4bac7af9110f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220421%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220421T073900Z&X-Amz-Expires=86400&X-Amz-Signature=521ac59982b440f7de0f96efa8fb91eba2e7b4e0f35ffa1da4f67ceab5a5671e&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

얼마나 맞았는가? 전체는 62%가 맞았다. 

<aside>
💡 모두 맞는다에 걸기만 해도 62점은 나온다는 말이다.

</aside>

사람의 정답률을 따로 구한 다음 일정 기준 보다 낮은 사람은 다 틀린것으로 예측해 버려도 좋을 듯 하다.

### 어려운 문제들

---

 

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/718c2f84-d893-4fa7-89fa-742996e55e5e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220421%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220421T073917Z&X-Amz-Expires=86400&X-Amz-Signature=21cd7af39fc98f347d86156f47c5cd1ef745566f2e7dff32d81afa08b26b3c22&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

문항의 정답률 평균은 65% 

그렇다면 일정 기준 보다 낮은 정답률을 가진 문제는 다 틀렸다고 예측 해 버려도 좋을 듯 하다. 

### 문제를 많이 풀수록 문제를 더 맞추는가?

---

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/69946129-6d5c-4e9c-96ff-155135b1e8bb/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220421%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220421T073928Z&X-Amz-Expires=86400&X-Amz-Signature=768529a892082acd17eee3b0526c93357d3bdffa33d8d6a56290b5b8c675f7da&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

큰 차이 없다. 문제를 오히려 적게 풀면 정답률이 올라갈수도 있기때문이다. 쉬운 문제만 골라풀면 못할 것도 없다.

 예) 16/16 100% 정답률

### 더 많이 노출될수록 정답률이 더 높은가?

---

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/b61d8825-59f8-4537-8b3c-22c301d54e1e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220421%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220421T073942Z&X-Amz-Expires=86400&X-Amz-Signature=51f007c47bced4beeb6065ff85121f0d6188cd917ea145b525ab04fd6178c08e&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)
아까보다는 차이가 나지만 전부다 맞았다고 할경우 62%에 비해서 크게 유의미 한것 같지 않다.

### 문제를 많이 풀수록 정답률이 더 높은가?

---

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4d2419cb-12fd-4dd9-ab2a-7b729282212d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220421%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220421T074014Z&X-Amz-Expires=86400&X-Amz-Signature=7658429c636e20c62415deebdf1d342c602eade0e55424898a5392fd885168f6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

아니다 오히려 초반에 정답률이 급격히 올랐다가 시간이 지날수록 떨어지고 조금씩 오르지만 초반의 정답률에는 따라갈 수 없다.  

마지막을 예측해야 하는 문제 특성과, 해당 사람이 어느 위치에 있는가를 모르는 이상 유의미한 지표가 될수 없다.

### 문제 푸는 시간 과 정답률

---

 같은 시험지라면 문제를 푸는데 얼마나 걸렸는지 알수 있다. 

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/1e10a18f-deb4-4139-9d43-ead2e54a560b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220421%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220421T074049Z&X-Amz-Expires=86400&X-Amz-Signature=75460c9c7092cdefe4be80bba45525895e271487f817eb56308209e78a2a0e30&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

문제를 푸는데 걸리는 시간이 너무 짧으면 틀렸다고 보는것이 맞겠다.

### 생각해볼 아이디어

---

 테그가 무언가를 나타낼수 있다고 본다. 

테그는 문제의 유형을 포함할수도 있을 것이고 사람마다 강한 유형이 있고 못하는 유형이 있을 수 있다. 

 data augmentation 을 해보면 어떨까 시험지 기준으로 추가한다. 

아니면 모두 일정한 크기로 자르고 나누면?
