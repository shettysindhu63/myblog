<!-- 
.. title: Lessons learned along the data-driven journey
.. slug: lessons-learned
.. date: 2017-09-30 00:57:35 UTC+08:00
.. tags: draft, data science, machine learning
.. category: 
.. link: 
.. description: 
.. type: text
-->

There are many tutorials and courses on both fundamental concepts and the tools required for data science. However, it is often difficult to find simple, useful and practical guidelines on the workflow of the data analysis process and what you will actually be doing on a daily basis and what you can do in order to keep improving. 


Occasionally, I would find a blog post or video that tries to talk about the process of data analysis and what to do when you hit a roadblock. I also learned a lot from talking to data scientists in local meetups. I have collated some points below from my own experience as well as from listening to others. 

<br>
**Clean data delivers results more often than sophisticated algorithms**

Expect the most benefits from clean data and standard bread and butter approaches [1]. A simple and parsimonious model that explains a lot of data is often better than a complicated algorithm that is difficult to interpret,  when both deliver results not significantly different. Instead of diving into the state-of-the-art algorithm, first make sure there are no data defects and data leakage. Also, check if there is any easy solution and simple preprocessing that could lead to drastically better results. If you are deploying your model or machine learning algorithm, it is crucial that your training, testing and holdout data are representative of the data that will be generated during deployment and the results will hold despite the assumptions you have made of the real world. In this regard, extra caution is required while dealing with time series data where treating all data points as independent and randomly selecting subsets for training and test data may create problems [2]. 

<br>
**Visualization matters, only looking at numbers can be deceiving** 

Visualization is essential not only at the end of the analysis while communicating your results but at every step of the data analysis. Datasets can generate similar summary statistics, yet be clearly different when plotted [3]. During exploratory analysis, looking at the distribution of the data and drawing lots of graphs to analyze the different properties are extremely important. Many statistical methods only hold for normally distributed data. Interactive data analysis during the exploration stage can reveal hidden problems and save you tons of time if you are faced with unexpected results [8]. You may even realize there's a simpler solution then you initially assumed. While communicating your results, take extra care in ensuring that the visualization reflects the data and the results accurately and you don't end up unintentionally misleading or confusing the audience. 

<br>
**Decide on the metrics before diving into the data**

Define the metrics before you can actually go ahead and start tackling the problem. It is near impossible to achieve 100% accuracy, in fact you need to be extra cautious if you get over 90% accuracy, closely check for defects or leakage. Metrics must be decided on the end goals - you may not need very high accuracy, you may need human-level accuracy for some tasks. Go through literature and make sure you are not trying to do the infeasible or something that does not make sense for the particular problem you are trying to solve. Looking back at the metrics you have set at every stage of your analysis is also immensely helpful when you hit a roadblock and get things done without getting overwhelmed.

Deciding your metrics upfront based on your end goals and the problem you are trying to solve will save you a lot of time and effort throughout the data analysis process. You can always look back at these when you hit a roadblock and realign your analysis without feeling overwhelmed. 

<br>
**Don't reinvent the wheel, use libraries**

Use standard packages - this will simplify your workflow, improve readability and enhance your productivity while writing code. In the beginning, I used to write everything in base R, then switched to packages my favorites being dplyr, ggplot2, data.table. Even though the former is great for understanding what's happening under the hood but using packages just makes things so much easier to write and to read. In addition, you have the guarantee that many people have optimized and debugged so the code you write is likely to have less bugs. 
Reference : https://www.quora.com/Should-I-write-my-own-code-or-use-libraries

<br>
**Define your workflow, update it regularly**

In the book [5], the authors give some useful guideline on how to go about the data analysis process itself and the importance of matching the data to your expectations at each stage of the analysis. The 5 core activities outlined are :  stating and refining the question, exploring the data, building formal models, interpreting the results and communicating the results. Asking the right questions is often the most difficult part of the whole process. Also, having a standard data analysis workflow or pipeline also helps in deciding on what to do next and helps in preventing too much time spent in something that does not return any value. Use jupyter notebook to document the workflow. It need not be perfect, there is no well-defined workflow for data scientists because each problem is different and may require a different approach. But having a general guideline will save you tons of time. 

<br>
**References and useful links** 

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
11. [DeepRLHacks](https://github.com/williamFalcon/DeepRLHacks)

<br>
**Related Meetups in Singapore (not exhaustive)**

- [DataScienceSG](https://www.meetup.com/DataScience-SG-Singapore/)
- [#IoTSG](https://www.meetup.com/IoT_SG/)
- [R Users Group Singapore (RUGS)](https://www.meetup.com/R-User-Group-SG/)
- [Singapore Python User Group](https://www.meetup.com/Singapore-Python-User-Group/)
- [PyData Singapore](https://www.meetup.com/PyData-SG/)
- [Tensorflow and Deep Learning Singapore](https://www.meetup.com/TensorFlow-and-Deep-Learning-Singapore/)
 






