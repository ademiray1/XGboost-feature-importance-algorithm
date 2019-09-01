# XGboost-feature-importance-algorithm
XGboost feature importance algorithm

XGBoost implements a Gradient Boosting algorithm based on decision trees.


# The gradient boosting algorithm
If you are already familiar with Random Forests, the Gradient Boosting algorithm implemented in XGBoost is also an ensemble of decision trees. Those trees are poor models individually, but when they are grouped they can be really performant.

The difference between XGBoost and Random Forest lies in the way those trees are built and combined. Random Forest builds fully grown decision trees in parallel on subsamples of the data. Each tree is higly specialized to predict on its subsample and do not generalize well (high variance). By combining the predictions made by each individual tree, the Random Forest algorithm decreases variance and gives good performance.

XGBoost on the other hand, builds really short and simple decision trees iteratively. Each tree is called a "weak learner" for their high bias. XGBoost starts by creating a first simple tree which has poor performance by itself. It then builds another tree which is trained to predict what the first tree was not able to, and is itself a weak learner too. The algorithm goes on by sequentially building more weak learners, each one correcting the previous tree until a stopping condition is reached, such as the number of trees (estimators) to build.

# Why should we learn to use XGBoost?
XGBoost is widely used in Machine Learning and got particularly famous on Kaggle, the machine learning competition website. As Anthony Goldbloom CEO of Kaggle said back in 2016, when XGBoost was becoming big in competitive Machine Learning:

"It has almost always been ensembles of decision trees that have won competitions. It used to be random forest that was the big winner, but over the last six months a new algorithm called XGboost has cropped up, and it’s winning practically every competition in the structured data category."

XGBoost has shown a great track record of high performances on problems involving structured data and thus should be part of your data scientist toolbox, even more so if you are willing to compete on Kaggle. Apart from its performance, XGBoost is also recognized for its flexibility and speed. Whilst gradient boosting requires to build trees one by one sequentially, XGBoost implements a way to parallelize the training of each tree, making the training faster and the job of Data Scientists easier. XGBoost can be used with a simple SKlearn API (used in this tutorial) or a more flexible native API (used in the advanced tutorial). It is also available for other languages such as R, Java, Scala, C++, etc ... and can run on distributed environments such as Hadoop and Spark.

A word of warning before going further with the tutorial, as it is well known, there is no free lunch in Machine Learning, and XGBoost is no exception to this rule. It can sometimes be harder to tune or more propice to overfitting than a simpler model such as Random Forest and perform poorly with non structured data.
