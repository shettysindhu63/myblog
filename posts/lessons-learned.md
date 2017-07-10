<!-- 
.. title: Lessons learned along the data-driven journey
.. slug: lessons-learned
.. date: 2017-07-20 00:57:35 UTC+08:00
.. tags: draft, data science, machine learning
.. category: 
.. link: 
.. description: 
.. type: text
-->

There are many tutorials and courses on both fundamental concepts and the tools required for data science. However, it is often difficult to find simple, useful and practical guidelines on the workflow of the data analysis process and what you will actually be doing on a daily basis and what you can do in order to keep improving. 


Occasionally, I would find a blog post or video that tries to talk about the process of data analysis and what to do when you hit a roadblock. I also learned a lot from talking to data scientists in local meetups. I have collated some points below both from experience with my own failings and from listening to others works.

<br>
**Clean data delivers results more often than sophisticated algorithms**

Expect the most benefits from clean data and standard bread and butter approaches [1]. A simple and parsimonious model is in most cases better than a sophisticated algorithm that is uninterpretable. Instead of diving into the state-of-the-art algorithm, first make sure there are no data defects and data leakage. Also, check if there is any easy solution and simple preprocessing helps a lot in some cases. These become doubly important if you need to deploy your model or machine learning algorithm. You need to double check your training, testing and holdout data and brainstorm on whether they are representative of the data that will be generated during deployment and your results will still hold. Take extra care of time series data [2]. 

<br>
**Visualization matters, statistics can be deceiving** 

Visualization is crucial. Generate lots of exploratory plots and then some more. Only looking at numbers can be deceptive [3]. You need to look at how the data is distributed. Most statistical methods only hold for normally distributed data. Outliers become obvious and you may realise that there is a n easy or simple solution. Even at the end of the analysis or at different stages when you need to communicate, take extra care that the visualization reflects the data and the results accurately and does not mislead the audience. 

<br>
**Fix the metrics before diving into the data**

Define the metrics before you can actually go ahead and start tackling the problem. It is near impossible to get 100% accuracy, in fact you need to be extra cautious if you get over 90% accuracy, closely check for defects or leakage. Metrics must be decided on the end goals - you may not need very high accuracy, you may need human-level accuracy for some tasks. Go through literature and make sure you are not trying to do the infeasible or something that does not make sense for the particular problem you are trying to solve. Looking back at the metrics you have set at every stage of your analysis is also immensely helpful when you hit a roadblock and get things done without getting overwhelmed.

<br>
**Don't reinvent the wheel, use libraries**

Use standard packages - this will simplify your workflow, improve readability and enhance your productivity while writing code. In the beginning, I used to write everything in base R, then switched to packages my favorites being dplyr, ggplot2, data.table. Even though the former is great for understanding what's happening under the hood but using packages just makes things so much easier to write and to read. In addition, you have the guarantee that many people have optimized and debugged so the code you write is likely to have less bugs. 
Reference : https://www.quora.com/Should-I-write-my-own-code-or-use-libraries

<br>
**Define your workflow, update it regularly**

In the book [5], the authors give some useful guideline on how to go about the data analysis process itself and the importance of matching the data to your expectations at each stage of the analysis. The 5 core activities outlined are :  stating and refining the question, exploring the data, building formal models, interpreting the results and communicating the results. Asking the right questions is often the most difficult part of the whole process. Also, having a standard data analysis workflow or pipeline also helps in deciding on what to do next and helps in preventing too much time spent in something that does not return any value. Use jupyter notebook to document the workflow. It need not be perfect, there is no well-defined workflow for data scientists because each problem is different and may require a different approach. But having a general guideline will save you tons of time. 

<br>
References 

1.  [Ian Goodfellow, Practical Methodology for Deploying Machine Learning](https://www.youtube.com/watch?v=NKiwFF_zBu4)
2.  [Alex Smolyanskaya, What's wrong with my time series](http://multithreaded.stitchfix.com/blog/2017/02/28/whats-wrong-with-my-time-series/)
3.  [Autodesk Research, Same Stats Different Graphs](https://www.autodeskresearch.com/publications/samestats)
4.  [Martin Zinkevich, Best Practices for ML Engineering](http://martin.zinkevich.org/rules_of_ml/rules_of_ml.pdf)
5.  [Roger D. Peng and Elizabeth Matsui, The Art of Data Science](https://leanpub.com/artofdatascience)
6.  [Foster Provost and Tom Fawcett, Data Science for Business](https://www.amazon.com/Data-Science-Business-Data-Analytic-Thinking/dp/1449361323)
7. [Kirill Eremenko, Super Data Science Podcast](https://www.superdatascience.com/podcast/)
 






