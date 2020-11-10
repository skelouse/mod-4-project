<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Model-Selection-for-Tweet-Sentiment-Analysis" data-toc-modified-id="Model-Selection-for-Tweet-Sentiment-Analysis-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Model Selection for Tweet Sentiment Analysis</a></span><ul class="toc-item"><li><span><a href="#This-Repository-Contains" data-toc-modified-id="This-Repository-Contains-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>This Repository Contains</a></span></li><li><span><a href="#Questions" data-toc-modified-id="Questions-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Questions</a></span></li><li><span><a href="#Using-the-OSEMN-Process" data-toc-modified-id="Using-the-OSEMN-Process-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Using the OSEMN Process</a></span></li><li><span><a href="#Results" data-toc-modified-id="Results-1.4"><span class="toc-item-num">1.4&nbsp;&nbsp;</span>Results</a></span><ul class="toc-item"><li><span><a href="#Gradient-Boosting-Classifier" data-toc-modified-id="Gradient-Boosting-Classifier-1.4.1"><span class="toc-item-num">1.4.1&nbsp;&nbsp;</span>Gradient Boosting Classifier</a></span></li><li><span><a href="#Stacking-Classifier" data-toc-modified-id="Stacking-Classifier-1.4.2"><span class="toc-item-num">1.4.2&nbsp;&nbsp;</span>Stacking Classifier</a></span></li></ul></li><li><span><a href="#Recommendations" data-toc-modified-id="Recommendations-1.5"><span class="toc-item-num">1.5&nbsp;&nbsp;</span>Recommendations</a></span></li><li><span><a href="#Next-Steps" data-toc-modified-id="Next-Steps-1.6"><span class="toc-item-num">1.6&nbsp;&nbsp;</span>Next Steps</a></span></li><li><span><a href="#Repository-Structure" data-toc-modified-id="Repository-Structure-1.7"><span class="toc-item-num">1.7&nbsp;&nbsp;</span>Repository Structure</a></span></li></ul></li></ul></div>

# Model Selection for Tweet Sentiment Analysis

![output_43_0.png](/md/output_43_0.png)

## This Repository Contains
 -  A Jupyter notebook <a href="https://github.com/skelouse/mod-4-project/blob/master/student.ipynb">`student.ipynb`</a> showing our tweet sentiment analysis
 - The dataset <a href="https://github.com/skelouse/mod-3-project/blob/master/data/tweet.csv">itself</a> Obtained from <a href="https://data.world/crowdflower/brands-and-product-emotions">brands-and-product-emotions</a>
 - A PowerPoint <a href="https://github.com/skelouse/mod-4-project/blob/master/presentation.pdf">presentation</a> of the data

## Questions
> * Which model will perform best?
> * How well will a model perform?
> * What can androids or iphones improve in their products to reduce negative feedback?

## Using the OSEMN Process
- Obtain the data
- Scrub the data
- Explore the data
- Model the data
- Interpret the data
- <a href="https://machinelearningmastery.com/how-to-work-through-a-problem-like-a-data-scientist/">Reference</a>

## Results


### Gradient Boosting Classifier

![output_75_1.png](/md/output_75_1.png)
<div class="shadow alert alert-info">
    <ul><b>From the model:</b>
<li>Slightly overfitting the training data</li>
<li>Odd that the True Label(1) doesn't add up to 100%</li>
<li>The best model overall at 79% accuracy</li>
<li>Successfully predicting 64% and 82% of Negatives and Positives respectively</li>
</ul>
</div>

### Stacking Classifier

![output_109_1.png](/md/output_109_1.png)

<div class="shadow alert alert-info">
    <ul><b>From the model:</b>
<li>Overfitting the training data at 98%</li>
<li>Predicting 56% and 91% of Negatives and Positives Respectively</li>
<li>86% accuracy on the Testing data</li>
<li>Still struggling to predict the negative emotion,  slightly better than flipping a coin in that aspect</li>
</ul>
</div>

## Recommendations

> * **Which model will perform best?**
>  * Gradient Boosting for balanced recall, and stacking for the highest overall accuracy

> * **How well will a model perform?**
>  * Overall Testing accuracy
>    * Gradient Boosting: 76%
>    * Stacking Classifier: 86%

> * **What can androids or iphones improve in their products to reduce negative feedback?**
>  * Android
>    * Contests
>    * Events
>  * Iphone
>    * Interface
>    * Ease of use

## Next Steps
> * Build an sklearn pipeline with and grid search with the tokenizer and vectorizer parameters along with the parameters for each of the classifiers.
> * Build neural networks for the data, using [Oscar](http://oscar.calldesk.ai/) for hyperparameter tuning
> * More tuning on the above models

## Repository Structure

```
|   data
\--- tweet.csv
|
|   images
\--- phone.jpg
|
|   presentation.pdf
|   README.md
|   student.ipynb
|   readme.ipynb
|       
\--- styles
|      custom.css

\--- md
|      student.md
|      .png files of all graphs

```


```python

```
