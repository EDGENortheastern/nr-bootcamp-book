---
sidebar_position: 3
---

# D3S3. Summative Statistics

Data exploration is one of the key tasks a data analyst performs.

## Statistics

Statistics is the study of organizing, summarizing, and describing quantifiable data and methods of interpreting this data.

There are two main types of Statistics:

1. Descriptive statistics
2. Inferential statistics

The word statistics has two common meanings. Firstly, it often means a collection of quantitative information about a data set. Secondly, it may refer to drawing inferences about large groups (populations) based on observations made on smaller ones (samples).

## Populations, parameters, samples, and statistics

In statistics, **a population** is the pool of individuals, creatures, or objects grouped by a common feature.

A population does not have to be very large, although statistical procedures assume extremely large or infinite populations.

> In stats, a population is defined as "an **entire** distribution of similar observations or events." ([from Data Camp](https://campus.datacamp.com/courses/introduction-to-statistics-in-spreadsheets))

**Parameters** measures and describe population characteristics.

A sample is a subset of a population.

## Descriptive and inferential statistics

**Inferential or inductive statistics** infer or predict population parameters from sample measures. We will cover them later in the course.

**Descriptive statistics** organize, summarize, and describe measures of a sample.

The first step to analyzing a data set is to obtain descriptive statistics such as:

1. exploratory data visualizations, e.g., histograms
2. summary or **summative statistics**, e.g., averages

Some of he most common summary statistics inlcude:

- [Mean](#mean)
- [Mode](#mode)
- [Median](#median)
- [Percentiles](#percentiles)
- [Standard Deviation](#standard-deviation)
- [Variance](#variance)
- [Inter Quartile Range](#inter-quartile-range)

## Mean

One of the most common summative statistical measures for numeric data is the mean. In Google Sheets, it is called `AVERAGE(),` which is a terrible name, as it is only one of the averages. Mean is calculated by adding the values and dividing the total by the number of values.

Python Standard library does not have a mean function.

```python
# The error you'll see if you try to use mean() without importing
>>> mean(my_list)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'mean' is not defined
```

`NumPy` and `statistics` modules have mean methods.

Pandas data frame also has a mean method.

```python
dogs["height_cm"].mean()
```

## Mode

Mode is the value, which appears most often in the set. To find the mode, you need to count how many times each value appears.

To calculate mode in Google Sheets use:

```vb
=MODE.SNGL(A1:A10)
```

The easiest way to calculate mode of a Python list is to use `statistics.`

```python
>>> import statistics
>>> my_data_set = [1,2,3,5,5,5,6]
>>> statistics.mode(my_data_set)
5
```

## Median

You find median by putting the numeric values in order from the smallest to largest and figuring out the middle value.

## Variance

The variance measures data's dispersion from the mean.

It is computed by finding the difference between every data point and the mean, squaring them, summing them up, and then averaging.

## Standard Deviation

The standard deviation is just the square root of the variance.

## Inter Quartile Range

The interquartile range tells you the spread of the middle half of your distribution.

Just like median divides the data into two parts, the quartile divides the data into four parts.

So in median, if we divide the data into two parts, we are left with one point.

And that point is called as the median whereas when we divide data into four parts, then we will get three points of split.

And these points are called as quartile.

## Deepnote

Duplicate the Deepnote below, run or re-run the cells and try the tasks (signposted 🏋️).

[<img
    src="/img/icons/deepnote-logo.svg"
    alt="Deepnote link"
/>](https://deepnote.com/project/summative-stats-DoRNGkLaSoOOrvcogWo29Q/%2Fsumstats.ipynb)
