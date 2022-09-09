---
sidebar_position: 2
---

# D3S2. Introduction to Pandas

## 🐼🐼🐼

[Pandas](https://pandas.pydata.org/docs/) stands for Python Data Analysis Library, sorry to disappoint.

Pandas is really good at processing tabular datasets, the ones with columns and rows. Tabular data is important because it often comes from:

- Spreadsheets
- Databases

The Data Science convention is to import Pandas as `pd`:

```python
import pandas as pd # imports pandas package, aliases as pd
```

## `.csv` files

CSV stands for comma separated values.

It is a plain text format with commas used to separate table columns.
CSV files are very small in size and easy to import into most spreadsheet software packages. They can be previewed in the simplest text editor.
Reading and understanding the contents of a CSV file, however, is not that easy in a text editor - there are no table borders, column headers and values inside columns are not aligned. Multiple worksheets cannot be exported directly
into a single CSV file.

Click on a CSV icon below to download a `.csv` file of the richest people data set from day one. Whatever system you have, the `.csv` file should open in a text editor.

[<img
    src="/img/icons/csv-logo.svg"
    alt="SVG download link"
/>](/img/csvs/richest.csv)

An CSV file in a text editor:

```text
1,Elon Musk,$271.5 B,▶ $1.4 B | 0.54%,50,"Tesla, SpaceX",United States
2,Bernard Arnault & family,$193.0 B,▶ $1.2 B | 0.64%,72,LVMH,France
3,Jeff Bezos,$188.8 B,▶ $1.4 B | 0.76%,58,Amazon,United States
4,Bill Gates,$134.8 B,▶ $638 M | -0.47%,66,Microsoft,United States
5,Larry Ellison,$120.7 B,▶ $1.2 B | -1.02%,77,software,United States
```

CSV files allow data analysts to perform data exploration on data sets that come from a range of sources, e.g., databases, financial spreadsheets.

<img
    src="/img/tabular-data-to-pandas.png"
    alt="SVG role"
/>

## Data frames

A data frame is a pandas-specific data type:

1. is 2-dimensional (aka tabular, rectangular)
2. has columns, columns have names
3. has rows and rows might also have names
4. can be a pandas or an R data frame
5. has special methods for fast and easy data analytics
6. normally has data of the same data type in a single column
7. has observations in rows, features in columns

## Exploratory methods and attributes

This `df.info()` prints information about a DataFrame including the index dtype and columns, non-null values and memory usage.

```python
df.info()
```

The `.shape` gets the number of rows and columns

```python
df.shape
```

The `.describe()` gets escriptive statistics include those that summarize the central tendency, dispersion and shape of a dataset’s distribution.

## Deepnote

[<img
    src="/img/icons/deepnote-logo.svg"
    alt="Deepnote link"
/>](https://deepnote.com/project/Intro-2-Pandas-FOcID7jESuK5QP-Rn1pc8Q/%2FIntro2pandas-movies.ipynb)

[Link](https://deepnote.com/project/Intro-2-Pandas-FOcID7jESuK5QP-Rn1pc8Q/%2FIntro2pandas-movies.ipynb)
