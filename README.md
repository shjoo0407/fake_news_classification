# fake_news_classification
- id :  unique id for a news article, Integer
- title : the title of a news article
- author : author of the news article
- text : the text of the article (could be incomplete)
- label : a label that marks the article as potentially unreliable, Integer
-  1 : Fake    0 : Non-fake
## EDA
- fake data 가 10413개, non-fake data가 10387개 있는 균형적인 데이터다.
- 비어 있는 곳은 (결측치) 들은 모두 빈칸으로 대체하였다.

## 전처리
- nltk에서 불용어를 다운받아 불용어를 제외하였다.
- 'content'라는 칼럼에 author 와 title 을 묶어 새로운 변수로 만들었다.
- TF-IDF를 적용하였다.
- 'content' 만을 사용하여 X 를 구성한다.

## 모델링
- Logistic regression, Multinomial naive bayes, passive aggressive classifier 를 사용하여 모데링을 진행하였다.
- (passive aggressive classifier 에 대한 공부 필요...)

## 결과
- passive aggressive model이 가장 잘 분류하고 있다.
- ![모델링결과](https://user-images.githubusercontent.com/69780999/216019456-aa50ac27-0515-4ff6-b129-abfc0fa40565.PNG)

