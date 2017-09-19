<!-- 
.. title: Lessons learned along the data-driven journey
.. slug: lessons-learned
.. date: 2017-09-19 08:00:35 UTC+08:00
.. tags: data science, machine learning
.. category: 
.. link: 
.. description: 
.. type: text
-->

There are many tutorials and courses on both fundamental concepts and the tools required for data science. However, it is often difficult to find simple, useful and practical guidelines on the workflow of the data analysis process and what you will actually be doing on a daily basis and what you can do in order to keep improving. 
Occasionally, I would find a blog post or video that tries to talk about the process of data analysis and what to do when you hit a roadblock. I also learned a lot from talking to data scientists in local meetups. I have collated some points below from my own experience as well as from listening to others. 
<!-- TEASER_END -->

<br>
**Clean data delivers results more often than sophisticated algorithms**

<br>
Expect the most benefits from clean data and standard bread and butter approaches [1]. A simple and parsimonious model that explains a lot of data is often better than a complicated algorithm that is difficult to interpret,  when both deliver results not significantly different. Instead of diving into the state-of-the-art algorithm, first make sure there are no data defects and data leakage. Also, check if there is any easy solution and simple preprocessing that could lead to drastically better results. If you are deploying your model or machine learning algorithm, it is crucial that your training, testing and holdout data are representative of the data that will be generated during deployment and the results will hold despite the assumptions you have made of the real world. In this regard, extra caution is required while dealing with time series data where treating all data points as independent and randomly selecting subsets for training and test data may create problems [2]. 

<br>
**Visualization matters, only looking at numbers can be deceiving** 

<br>
Visualization is essential not only at the end of the analysis while communicating your results but at every step of the data analysis. Datasets can generate similar summary statistics, yet be clearly different when plotted [3]. During exploratory analysis, looking at the distribution of the data and drawing lots of plots to analyze the different properties are extremely important. Many statistical methods only hold for normally distributed data. Interactive data analysis during the exploration stage can reveal hidden problems and save you tons of time if you are faced with unexpected results [8]. You may even realize there's a simpler solution then you initially assumed. While communicating your results, take extra care in ensuring that the visualization reflects the data and the results accurately and you don't end up unintentionally misleading or confusing the audience. 

<br>
**Decide on the metrics before diving into the data**

<br>
Deciding your metrics upfront based on your end goals and the problem you are trying to solve will save you a lot of time and effort throughout the data analysis process. You can always look back at these when you hit a roadblock and realign your analysis without feeling overwhelmed. Metrics must be based on the end-goals and the time and effort that will be allotted to the project. Depending on the application, you may not always need a very high accuracy and looking at other metrics beyond accuracy and bias-variance like coverage, precision, recall could be helpful [1]. In some industries, models are retrained and rescored regularly, maybe even on a daily basis and this needs suitable metrics. For example, temporal consistency is used to evaluate the models for predicting home value [9].
 
<br>
**Don't reinvent the wheel, use packages**

<br>
Using packages will simplify your workflow, improve readability of your code and enhance your productivity. In addition, you have the guarantee that these packages are optimized and debugged regularly, hence your code is likely to have less bugs and you are more likely to find help if something goes wrong. [Tidyverse](https://www.tidyverse.org/packages/) is a good place to start for R users whereas matplotlib, pandas, numpy, scikit-learn are the common packages for Python users. 

<br>
**Define your workflow, update it regularly**

<br>
In the book [The Art of Data Science](https://leanpub.com/artofdatascience), the authors give some useful guidelines on how to go about the data analysis process itself and the importance of matching the data to your expectations at each stage of the analysis. The 5 core activities outlined are: stating and refining the question, exploring the data, building formal models, interpreting the results and communicating the results. Asking the right questions is often the most difficult part of the whole process. Tools like [Jupyter](http://jupyter.org/) are helpful in documenting the data analysis process. Even though there may not be a well-defined workflow as each problem is different and much of data analysis is the data exploration stage, having a general guideline is incredibly helpful.   

<br>
**References and useful links** 

<br>

1.  [Ian Goodfellow, Practical Methodology for Deploying Machine Learning](https://www.youtube.com/watch?v=NKiwFF_zBu4)
2.  [Alex Smolyanskaya, What's wrong with my time series](http://multithreaded.stitchfix.com/blog/2017/02/28/whats-wrong-with-my-time-series/)
3.  [Autodesk Research, Same Stats Different Graphs](https://www.autodeskresearch.com/publications/samestats)
4.  [Martin Zinkevich, Best Practices for ML Engineering](http://martin.zinkevich.org/rules_of_ml/rules_of_ml.pdf)
5.  [Roger D. Peng and Elizabeth Matsui, The Art of Data Science](https://leanpub.com/artofdatascience)
6.  [Foster Provost and Tom Fawcett, Data Science for Business](https://www.amazon.com/Data-Science-Business-Data-Analytic-Thinking/dp/1449361323)
7. [Kirill Eremenko, Super Data Science Podcast](https://www.superdatascience.com/podcast/)
8. [The Importance of Interactive Data Analysis for Data-Driven Discovery](https://simplystatistics.org/2017/04/03/interactive-data-analysis/)
9. [Train, Score, Repeat, Watch Out!](http://blog.kaggle.com/2017/08/30/train-score-repeat-watch-out-zillows-andrew-martin-on-modeling-pitfalls-in-a-dynamic-world/)
10. [My Neural Network isn't working! What should I do?](http://theorangeduck.com/page/neural-network-not-working)
11. [DeepRLHacks, Hacks for training RL systems from John Schulman's lecture](https://github.com/williamFalcon/DeepRLHacks)

<br>
**Related Meetups in Singapore (not exhaustive)**

<br>

- [DataScienceSG](https://www.meetup.com/DataScience-SG-Singapore/)
- [#IoTSG](https://www.meetup.com/IoT_SG/)
- [R Users Group Singapore (RUGS)](https://www.meetup.com/R-User-Group-SG/)
- [Singapore Python User Group](https://www.meetup.com/Singapore-Python-User-Group/)
- [PyData Singapore](https://www.meetup.com/PyData-SG/)
- [Tensorflow and Deep Learning Singapore](https://www.meetup.com/TensorFlow-and-Deep-Learning-Singapore/)
 






