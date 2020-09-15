# Depression Tweets Analysis 📊

> Depression is a common illness worldwide, with more than 264 million people affected. Depression is different from usual mood fluctuations and short-lived emotional 
responses to challenges in everyday life. Especially when long-lasting and with moderate or severe intensity, depression may become a serious health condition. 
It can cause the affected person to suffer greatly and function poorly at work, at school and in the family. At its worst, depression can lead to suicide. 
Close to 800 000 people die due to suicide every year. Suicide is the second leading cause of death in 15-29-year-olds. <br>
> <i> -- <a href="https://www.who.int/news-room/fact-sheets/detail/depression"> WHO </a> </i>

<p align="center">
          <img src="https://github.com/weronikazak/depression-tweets/blob/master/pictures/depr_img.PNG" width=700>
</p>

Sentiment analysis for depression based on Twitter posts. The aim of this project is to analyze linguistic markers
in social media posts and creating a model that can give an invidual insight into user's mental mealth.

Big shoutout to *twintproject* for their handy tweets scraping tool - <a href="https://github.com/twintproject/twint">Twint</a>.

## Models

### Tensorflow

To detect whether the post contains anxious linguistic markers, using the Tensorflow library I builded a CNN of a simple architecture with a summary shown below.

<p align="center">
          <img src="https://github.com/weronikazak/depression-tweets/blob/master/pictures/model.PNG" width=500>
</p>
          
In the end the model had accuracy of **96.98%** and the loss of **0.14%**.

<p align="center">
          <img src="https://github.com/weronikazak/depression-tweets/blob/master/pictures/acc.PNG" width=300>
          <img src="https://github.com/weronikazak/depression-tweets/blob/master/pictures/loss.PNG" width=300>
</p>

### Sklearn
          
An approach to try different classifiers available in *Sklearn* library, such as:
- KNeighborsRegressor(K-nn)
- Lasso
- Ridge
- ElasticNet
- GradientBoostingRegressor
- RandomForestRegressor
- ExtraTreesRegressor


<p align="center">
          <img src="https://github.com/weronikazak/depression-tweets/blob/master/pictures/errors.PNG" width=650>
  </br>
<i><small>From left to right: R^2 score, Mean Squared Error, Mean Absolute Error</small></i>
  
</p>



 The **RandomForestClassifier** turnt out to be the best among them with final score of **99.19%** accuracy, so even better than neural network.
 
 
<p align="center">
          <img src="https://github.com/weronikazak/depression-tweets/blob/master/pictures/classifiers.PNG" width=200>
</p>
