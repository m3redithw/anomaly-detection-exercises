![title.png](title.png)


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

- **Point Anomalies**: A single instance of data is anomalous if it's too far off from the rest. For example, detecting data exfiltration based on gigabytes leaving the network, detecting credit card fraud based on "amount spent", etc.

- **Contextual Anomalies**: The abnormality is context specific. This type of anomaly is common in time-series data. For example, accessing confidential files during work hours is normal, but in the middle of the night is odd.

- **Collective Anomalies**: A set of data instances collectively helps in detecting anomalies. For example, someone is trying to copy data form a remote machine to a local host unexpectedly, an anomaly that would be flagged as a potential cyber attack. The combination of the event from the remote machine and the event from the local host combine to detect the anomaly.

- **Anomalies vs. Noise Removal vs. Novelty Detection**: Novelty detection is concerned with identifying an unobserved pattern in new observations not included in training data — for instance, a sudden interest in a new channel on YouTube during Christmas. Noise Removal (NR) is the process of immunizing analysis from the occurrence of unwanted observations; in other words, removing noise from an otherwise meaningful signal.

**Other Resources**: 
## ◽ Working with Time Series Data
### ▫️ `dt`
The `.dt` accessor can be used to access various properties of a date. Some of the more common ones are listed here, and you can reference the pandas documentation for a full list.

| **Property**   | **Description**   | 
|:--------|:------------|
| year | The year of the datetime |
| month | The month of the datetime |
| day | The days of the datetime | 
| hour | The hour of the datetime | 
| week | The week ordinal of the year |
| weekday | The number of the day of the week with Monday=0, Sunday=6 |
| weekday_name | The name of the day in a week (ex: Friday) |
| quarter | Quarter of the date: Jan-Mar = 1, Apr-Jun = 2, etc.

###  ▫️ `strfrtime`
`strftime` method and give date string to format the date in a custom way.

#### `strfrtime` Format Cheat Sheet
| **Units**   | **Specifier**   | **Description**                                                    |
|:--------|:------------|:---------------------------------------------------------------|
| seconds | %S          | Second of the minute (00..60)                                  |
| minutes | %M          | Minute of the hour (00..59)                                    |
| hours   | %H          | Hour of the day, 24-hour clock (00..23)                        |
|         | %I          | Hour of the day, 12-hour clock (01..12)                        |
| days    | %d          | Day of the month                                               |
|         | %a          | The abbreviated weekday name ("Sun")                           |
|         | %A          | The full weekday name ("Sunday")                               |
|         | %j          | Day of the year (001..366)                                     |
|         | %w          | Day of the week, Sunday is 0 (0..6)                            |
| weeks   | %U          | Week of the year, Sunday is the first day of the week (00..53) |
|         | %W          | Week of the year, Monday is the first day of the week (00..53) |
| months  | %b          | The abbreviated month name ("Jan")                             |
|         | %B          | The full month name ("January")                                |
|         | %d          | Day of the month (01..31)                                      |
|         | %m          | Month of the year (01..12)                                     |
| years   | %y          | Year without a century (00..99)                                |
|         | %Y          | Year with century (1999)                                       |
| misc    | %z          | Time zone offset (-0500)                                       |
|         | %Z          | Time zone name ("CDT")                                         |
|         | %p          | Meridian indicator ("AM" or "PM")                              |
|         | %c          | The preferred local date and time representation               |
|         | %x          | Preferred representation for the date alone, no time           |
|         | %X          | Preferred representation for the time alone, no date           |
**Reference**: [datetime — Basic date and time types](https://docs.python.org/3/library/datetime.html#strftime-and-strptime-behavior)

[Working with Time Series Data in Pandas](working_with_time_series_in_pandas.ipynb)

## ◽ Data Preparation
### ▫️ Prepare
- The most common activity in preparing time series data is setting dates to datetime types using `pd.to_datetime`.

- Another common activity is looking at the frequency of the data and gaps in time or null values.

### ▫️ Data Splitting
Splitting time series data into train, test, and validate sets is a little trickier than with previous data we have looked at. Because the data points have an order to them, we **cannot** simply assign each point randomly to train, validate, or test.

Ideally all splits should contain one season's worth of data. There are several methods we can use to split our time series data:

- **Human-based**: use, for example, the last year in the dataset as test split

- **Percentage based**: use the last 20% as test

- **Cross Validate**: break data up into slices and use successive slices as train and test repeatedly (`sklearn.model_selection.TimeSeriesSplit`)

## ◽ Exploratory Analysis
The primary use case for Time Series EDA techniques is when we have a single continuous variable sampled over time and we want to identify **trend** and **seasonality**.



## ◽ Forecasting
- **Last bbserved value**
- **Simple average**
- **Moving average**
- **Holt's Linear Trend**
- **Previous Cycle**




***
# 🤖 𝐄𝐱𝐞𝐫𝐜𝐢𝐬𝐞𝐬

## ◽ Data Acquisition

## ◽ Working with Time Series Data


## ◽ Data Preparation


## ◽ Exploratory Analysis

## ◽ Forecasting
