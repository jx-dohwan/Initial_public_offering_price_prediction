# Initial_public_offering_price_prediction

#### 일단 변수를 10~15개가 적절하다고 했다. 그렇기 때문에 무엇을 빼야할지에 집중하기 보다는 기존에 사용하였던 변수에 무엇을 추가할지를 생각하는게 더 효과적일 것이다.
#### 데이터를 살펴보니 기존 교수님이 제공해주셨던 데이터의 변수에 5가지를 추가적으로 넣어서 유의미한 출력을 뽑아낼 수 있을 것 같다. 
#### 그리고 6가지당 각각 하나의 변수를 더 사용할 것이다. 왜냐하면 각각 비슷한 변수가 많기는 하지만 특정 비율을 뽑아내기 위한 변수인것 같고 중요한것은 비율인 것 같다. 예를 들어 최근 "따" 비율등이다. 
#### 아니면 여섯개 다 사용하거나 조합을 했을 때 어떤 것이 더 좋은 성능이 나왔는지 파악하는것도 괜찮을 것 같다. 이거는 코드로 직접 파악하며 확인하기
#### 일단 여섯개 다 사용해서 상관관계를 시각화해보자 그리고 상관관계의 시각화가 높은 만큼 실제 값도 높았는지 확인해보자

- 꼭 사용해야할 칼럼
  - 기업명
  - 공모가
  - 기관경쟁률
  - 청약경쟁률
  - 총공모지식수
  - 매출액
  - 순이익
  - 자본금
  - 의무보유확약비율
  - 구주매출비율
  - 종속변수
- 여기에 더 추가할 변수는 카테고리로 나눠보자
  - 주간사가 미치는 영향파악
    - 주간사 순위만 추가로 사용하면 될 듯 
  - 최근 주식 동향이 미치는 영향(3개월->근데 왜 3개월로 정했는지도 이유가 들어가야함)
    - 최근 "따" 비율만 써도 될 것 같음
    - 최근 공모주 동향1과 공모주수를 비율로 나타낸거니까
    - 지금은 이진분류이기 때문에 양수 비율은 중요하지 않을 듯 
   - 밴드수익률
     - 공모주의 가격이 기대치와 얼마나 차이나는지 알수 있게 해주는 것인데 유의미한 정보를 가져다 줄 것으로 보인다. 
  - 업종이 미치는 영향
    - 업종코드와 업종대분류 카테고리를 매칭해서 사용하면 될듯 
  - 전문 투자자 비율
    - 일반청약자(비율)와 조금 겹치는 감이 있다. 하지만 전문 투자자의 의견이 더 중요하기 때문에 둘중에 하나를 선택한다면 전문 투자자 비율을 선택해야한다.
  - 유통 가능한 주식 합계(비율)도 중요해보이는데?흠



구주매출비율이란 기존 대주주가 소유한 주식을 기업공개할 때 내놓아 파는 방법이다. 따라서 청약에 나온 수량만큼 기존 대주주의 지분율은 떨어진다. 예를들어 총 주식수가 100주인데, 이 중에서 기존 50주를 공모한다면, 대주주의 지분율은 100%에서 50%로 떨어지게 된다. 구주매출은 보통 차익실현이 주된 목표이다.

https://solenedu.tistory.com/entry/IPO-%EA%B8%B0%EC%97%85%EA%B3%B5%EA%B0%9C-%EB%B0%A9%EC%8B%9D-%EA%B5%AC%EC%A3%BC%EB%A7%A4%EC%B6%9C-%EC%8B%A0%EC%A3%BC%EA%B3%B5%EB%AA%A8
