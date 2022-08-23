<img width="1266" alt="title" src="https://user-images.githubusercontent.com/105242871/186199337-6770c199-f1ff-4c5a-b6d6-1b8664cf861c.png">

# 🤖 𝐂𝐥𝐚𝐬𝐬 𝐃𝐞𝐦𝐨 & 𝐑𝐞𝐬𝐨𝐮𝐫𝐜𝐞𝐬

## What are Anomalies?
### 🔹 Anomaly:

Anomalies are unusual, unexpected, surprising patterns in the observed world. An anomalous data point is a deviation from a rule or from what is regarded as normal; an outlier. An anomaly is any event or measurement that is out of the ordinary regardless of whether it is exceptional or not.

### 🔹 Outliers:
An outlier is an observation that lies an abnormal distance from other values in a random sample from a population. In a sense, this definition leaves it up to the analyst (or a consensus process) to decide what will be considered abnormal. Before abnormal observations can be singled out, it is necessary to characterize normal observations.

[e-Handbook of Statistical Methods](https://www.itl.nist.gov/div898/handbook/prc/section1/prc16.htm)

- The terms "outlier" and "anomaly" are frequently used interchangeably.

- In some cases, statisticians sometimes use the term 'outlier' to mean "something I should remove from the dataset so that it doesn't skew my model I'm building".

- In other cases, we may reserve the word 'anomaly' for data points we want to keep because they are valuable if caught or costly if missed. It's also possible to have an anomaly that is an inlier, meaning that the data is anomalous in nature but is close (in distance) to the mean, mode, or expected grouping(s).

### 🔹 Examples of Anomaly Detection in Data Science
- Fraud detection for financial companies

- Medical scans like XRays, ultrasounds, and MRIs seeking abnormalities in location, density, growth, etc..

- Detecting and preventing cyber-crime

- Malware detection

- Intelligence and Defense applications

- Analytical Marketing looking for new trends in business or household purchases

### 🔹 The BEST Way to Detect Anomaliesi s to *know your domain*
- For example, knowing that there is nothing colder than absolute zero degrees Kelvin informs how we approach an observation below 0 degrees Kelvin. It may mean that there is something wrong with the measuring tool or a clerical error like a typo (more likely).

- What determines if a data point is an outlier is a function of who determines if that data point is anomalous and why.

- One person's noise is another person's signal, depending on their goals and the costs and benefits to be gained/avoided from identifying that data point.
   
    - To one analyst aiming for a clean model of 50/50 chance, observing a flipped coin that lands exactly on its side is an anomaly may be noise that they should ignore from their model.

    - To another practitioner, the anomaly may be an observation of very high value that they want to catch, like early detection of a rare disease.

- In [e-Handbook of Statistical Methods](https://www.itl.nist.gov/div898/handbook/prc/section1/prc16.htm), **definition of an outlier**:  "an observation that lies an abnormal distance from other values in a random sample from a population. In a sense, this definition leaves it up to the analyst (or a consensus process) to decide what will be considered abnormal".

- It's important to define the criteria, the decision rule, for what makes an observation an inlier or an outlier.

- Usually, the deciding factor is cost/benefit analysis:
    - Is our goal to hunt for anomalies at all costs because lives are on the line?
    
    - Or do we do more good for people by producing a model that treats outliers as noise?
    
    - What is the cost of a false positive or a false negative?
    
    - What is the benefit of a true positive or a true negative?

### 🔹 Types of Anomalies
- **Use Cases**: Response times (longer than usual), error rates (more than usual), network load, cyber intrusions, fraud.

- **Point Anomalies**: A *single* instance of data is anomalous if it's too far off from the rest. For example, detecting data exfiltration based on gigabytes leaving the network, detecting credit card fraud based on "amount spent", etc.

- **Contextual Anomalies**: The abnormality is *context specific*. This type of anomaly is common in time-series data. For example, accessing confidential files during work hours is normal, but in the middle of the night is odd.

- **Collective Anomalies**: A set of data instances collectively helps in detecting anomalies. For example, someone is trying to copy data form a remote machine to a local host unexpectedly, an anomaly that would be flagged as a *potential cyber attack*. The combination of the event from the remote machine and the event from the local host combine to detect the anomaly.

- **Anomalies vs. Noise Removal vs. Novelty Detection**: Novelty detection is concerned with identifying an unobserved pattern in new observations not included in training data — for instance, a sudden interest in a new channel on YouTube during Christmas. Noise Removal (NR) is the process of immunizing analysis from the occurrence of unwanted observations; in other words, removing noise from an otherwise meaningful signal.

***
## Specific Techniques for Identifying/Detecting Anomalies
### 🔹 Statistical Methods
- Flag the data points that deviate from the expected, based on the statistical properties, such as mean, median, mode, and quantiles.

- You could define an anomalous data point as one that deviates by a certain standard deviation from the mean.

- You could use a simple or exponential moving average to smooth short-term fluctuations and highlight long-term ones.

- This method is challenging with really noisy data.

### 🔹 Clustering-Based Anomaly Detection
- **Assumption**: Data points that are similar tend to belong to similar groups or clusters, as determined by their distance from local centroids.

- **K-means**: it creates 'k' similar clusters of data points. Data instances that fall into abnormally small clusters could potentially be marked as anomalies.

- With density based clustering, like `DBSCAN`, we can design the model such that the data points that do not fall into a cluster are the anomalies. Assumption: Normal data points occur around a dense neighborhood and abnormalities are far away.

***
## Continuous Variable Probabilistic Methods for Identifying Outliers
> “Observation which deviates so much from other observations as to arouse suspicion it was generated by a different mechanism” — Hawkins(1980)

### 🔹 Visualize the data to see distribution, trend, shape
Visualizing our data is a key step to wrapping our mind around the shape, distribution, and skew in the data.

- Box plots
    - See [Boxplot Demo](https://matplotlib.org/3.1.1/gallery/pyplots/boxplot_demo_pyplot.html#sphx-glr-gallery-pyplots-boxplot-demo-pyplot-py)
    - [Creating Boxplots with Matplotlib] http://blog.bharatbhole.com/creating-boxplots-with-matplotlib/

- Scatter plots

- Plot a histogram
    - [pandas.DataFrame.hist](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.hist.html)

### 🔹 Anscombe's Quartet
![Anscombe's_quartet](https://user-images.githubusercontent.com/105242871/186199435-6266f865-0887-4b0c-b285-89c81873dc44.png)

- The measures of central tendancy as well as min/max don't identify the shape our any outliers

- The linear model for each quartet dataset has almost the exact same slope and intercept

- The visualization makes the general trends of the data, as well as the presence of outliers, crystal clear

## 



***
# 🤖 𝐄𝐱𝐞𝐫𝐜𝐢𝐬𝐞𝐬
