# 1day-1monk
[Youtube - Mathematical Monk](https://www.youtube.com/playlist?list=PLD0F06AA0D2E8FFBA)을 공부하면서 덧붙일 내용과 질문을 정리하는 곳입니다. 수업 내용은 [cveai](https://github.com/cveai)님의 [블로그](https://cveai.github.io/notes/2018/03/08/mm-ml.html)를 참고해주세요. 
- collaborator께서는 해결되지 않은 질문들이나 좋은 자료들이 있으면 올려주시면 감사하겠습니다. 활동을 원하시는 분은 whikwon@gmail.com 으로 연락주세요. 

### 0. About the monk
- [Monk's blog](http://jwmi.github.io/background.html)
### 1.1 Machine learning - overview and applications
- ML과 Statistics의 차이점?
	- [ML vs Statistics - Blog](https://svds.com/machine-learning-vs-statistics/)
### 1.2 What is supervised learning?
- [ill-posed problem](https://en.m.wikipedia.org/wiki/Well-posed_problem)
- vector에 표기된 superscript, subscript의 작성 기준?
	- [Notation: subscript vs. superscript for coordinate vector fields](https://math.stackexchange.com/questions/552347/notation-subscript-vs-superscript-for-coordinate-vector-fields)
### 1.3 What is unsupervised learning?
- Dimensionality reduction의 개념? 
	- [Dimensinality reduction - Blog](http://sanghyukchun.github.io/72/)
### 1.4 Variations on supervised and unsupervised
- Semi-supervised Learning이란?
	- [Semi-supervised learning](https://mitpress.mit.edu/sites/default/files/titles/content/9780262033589_sch_0001.pdf)
	- [Deep Belief Network, Yoshua Bengio](http://www.iro.umontreal.ca/~lisa/pointeurs/dbn_supervised_tr1282.pdf)
	- [Meta-Learning for Semi-Supervised Few-Shot Classification, Mengye Ren](https://arxiv.org/abs/1803.00676)
	- [Semi-supervised learning - LG CNS Blog](http://blog.lgcns.com/1666)
- Decision theory란? 
	- [Decision Theory - Wikipedia](https://ko.m.wikipedia.org/wiki/결정이론)
### 1.5 Generative vs Discriminative models
- $f(x|y), f(x)$만 density function이라고 칭하는 이유?
	- x가 데이터 포인트고 y는 단순히 레이블이자나요 그래서 일반적으로 x에 대한 확률을 구하는게 상대적으로 엄청 어려울 듯 해요. 표본공간이 커서.
- Generative model 이란?
	- [What is a generative model? - Quora](https://www.quora.com/What-is-a-generative-model)
- Generative, discriminative model의 차이점? 
	- [Generative vs discriminative - Stackoverflow](https://stackoverflow.com/questions/879432/what-is-the-difference-between-a-generative-and-discriminative-algorithm)
### 1.6 k-Nearest Neighbor classification algorithm
### 2.1 Classification trees (CART)
### 2.2 Regression trees (CART)
- [Piecewise constant function - Wikipedia](https://en.m.wikipedia.org/wiki/Step_function)
- It will be piecewise constant in some regions that are defined by the binary splits and on some higher dimensional space. (강의 내용) 
	- 예로든건 정의구역이 실수의 집합이라 “구간”(interval) 별로 상수인거구요, 정의구역이 $R^n$ 으로 되면, 예를 들어 이차원이면 (n=2) 사각형(rectangle) 별로 상수함수가 되겠죠.
### 2.3 Growing a regression tree (CART)
### 2.4 Growing a classification tree (CART)
- [CART - Breiman et.al](https://rafalab.github.io/pages/649/section-11.pdf)
- [CART - blog](https://machinelearningmastery.com/classification-and-regression-trees-for-machine-learning/)
- $E_R = \min_y {\frac 1 {N_R}} \sum_{i: x_i \in R} I(y_i \neq y)$ 에서 min이 붙는 이유는?
	- majority vote를 했을 때 정답이 아닌 경우의 전체 vote에서의 비율을 최소한으로 해서 같은 class끼리 같은 공간에 split 되도록 학습하기 위함입니다. 
### 2.5 Generalizations for trees (CART)
- $p$ explanatory variables $X_1, ... X_p$, $n$ observations가 있다고 가정했을 때 $X_i$는 1) a  numeric value ($n - 1$), 2) an ordered factor ($k - 1$), 3) an unordered factor ($2^{k-1} - 1$) 개만큼 predictor space가 나뉠 수 있다고 합니다. 왜 그럴까요?
	- 언오더드 팩터의 가지수가 전 좀 이해가 잘안가네요. 일단 숫자형 변수같은 경우는 처음에 스플릿하면서 분기를 찾아나갈 때 수치형 변수를 오름차순 또는 내림차순으로 정렬한후, 정렬된 변수에 대하여 데이터 별 변수값의 관측치로 스플릿을 해봅니다. 정렬된 변수의 첫번째값과 두번째값의 평균 또는 중앙값으로 스플릿을 해보고, 그다음 두번째값과 세번째깂의 평균 또는 중앙값으로 스플릿해봅니다. 이 과정을 n개의 값 대해서 다 시행하므로 n-1번입니다. 오더드 팩터같은 경우는 마찬가지로 오더드 팩터의 개수가 k개라면 같은 방식으로 생각해서 k-1개라고 할 수 있을 것 같습니다.
### 2.6 Bootstrap aggregation (Bagging)
- [Bootstrapping - Blog](https://learningcarrot.wordpress.com/2015/11/12/%EB%B6%80%ED%8A%B8%EC%8A%A4%ED%8A%B8%EB%9E%A9%EC%97%90-%EB%8C%80%ED%95%98%EC%97%AC-bootstrapping/)
- [Why Does Bagging Work? A Bayesian Account and its Implications - Pedro Domingos](https://homes.cs.washington.edu/~pedrod/papers/kdd97.pdf)
### 2.7 Bagging for classification
- [Bagging Predictors - Breiman](https://www.stat.berkeley.edu/~breiman/bagging.pdf)

## Other resources
- Basic ML implementation: https://github.com/zotroneneis/machine_learning_basics
