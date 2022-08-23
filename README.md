# Anomaly Detection Exercises

![title.png](title.png)


# 🤖 𝐂𝐥𝐚𝐬𝐬 𝐃𝐞𝐦𝐨 & 𝐑𝐞𝐬𝐨𝐮𝐫𝐜𝐞𝐬

## ◽ Data Acquisition
### ▫️ REST API
- **REST**, referring to *Representational State Transfer*, is a set of guidelines for structuring urls. Often times you will encounter the phrase RESTful to describe web sites or web services that follow **REST** guidelines.

    [REST](https://en.wikipedia.org/wiki/Representational_state_transfer)
    
- **API** stands for *Application Programming Interface*. It is a way that either developers interact with a program, or one program interacts with another.

- **JSON** stands for *JavaScript Object Notation*. All JSON is technically valid JavaScript code; JSON is very commonly used as a data representation format, and is commonly used as a data interchange format. In fact, if you were to open up a jupyter notebook in a plain text editor, you would see a big JSON object. JSON data structures consist of arrays (analogous to lists in python), objects (dictionaries), strings, booleans, and numbers.

    [Acquire Lesson](acquire_lesson.ipynb)

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
