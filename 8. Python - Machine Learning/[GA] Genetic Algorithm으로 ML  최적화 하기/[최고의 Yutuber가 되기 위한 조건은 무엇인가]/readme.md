 # 분석내용 소개
---
##### 전반적으로 다량의 앙상블과 유전 알고리즘을 사용해 스크롤의 양이 매우 많음


- 유튜브에서 인기 영상에 오른 영상들에 대한 데이터를 기반으로 어떤 feature가 Views에 영향을 미치는지를 파악하고자 회귀 분석
- 기본적으로 앙상블 최적화를 위해 총 6개의 모델(ElasticNet, RF, MLP, XGB, SVM, KNN)에 각각 Grid / Randomized search 를 사용했다.
- 이후 이 모델들을 Voting 앙상블 하였고, 해당 모델과 Genetic Algorithm을 활용해 일반적인 or 인기있는 영상이 되기 위한 각 feature별 조건을 세부적으로 확인 했다.
- 이때, Genetic Algorithm 을 적용해 모든 feature는 동일한 상황에서 특정 feature 가 변했을때, Views가 어떻게 변동되는지를 확인할 수 있었다. 
- 다만 데이터 자체가 Views를 예측하기에는 적합하지 않은 feature들이 많아서 정확한 모델링이 어려웠다는 한계점이 존재한다.
