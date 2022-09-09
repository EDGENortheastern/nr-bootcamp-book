---
sidebar_position: 1
---

# D5S1. Filtering and Visualizing with Google Sheets

You can access the data used [here](https://docs.google.com/spreadsheets/d/1bsy6bM7p-69rjkkaiKfjlW2LtuuqOUoTAlmox09ymIM/edit?usp=sharing). Note you will need to *make a copy* using File->Make a Copy to be able to work with the data!

## UI Filters

There are a number of different types of filters. We can use the built in filter function in the Google Sheets interface. 
*On the athlete_events sheet, select all of the data -> CTRL-A -> then select Data at the top, then Create a Filter*
<img
    src="/img/sheets/create_filter.png"
    alt="Create Filter"
/>

We can filter each column by selecting the three lines in a triangle next to each column.
When a filter has been applied, it will turn into a funnel.

<img
    src="/img/sheets/column_filter.png"
    alt="Column Filter"
/>


*Sort allows us to sort items alphabetically or numerically, A-Z (ascending) or Z-A (descending)*
*Filter by values allows us to select certain values to show or not show. We can also search for certain values, hide or show all.*
<img
    src="/img/sheets/filter1.png"
    alt="Filter By Values"
/>

*Filter by condition allows us to set certain criteria for what a text should contain or what a date or value should be.*

<img
    src="/img/sheets/filter2.png"
    alt="Filter By Conditions"
/>

We can also use filter views. Unlike filters, filter views are only visible if they are selected; you can apply a filter view and access the information you need without disrupting the view of another user.

## Formula Filters

The formula `FILTER(range, filter_range=condition)` can be used to FILTER data.

For example, the filter `FILTER(athlete_events!A2:O,athlete_events!O2:O="Gold")` will filter the entire table - part 1 of the formula - `athlete_events!A2:O` - to show only the records meeting the condition in part 2 of the formula `athlete_events!O2:O="Gold"`. Generally it is better to do this on a different sheet to avoid interfering with existing data.

<img
    src="/img/sheets/filter2.png"
    alt="Filter By Conditions"
/>

## Pivot Tables

Before creating a Pivot table, it is helpful to select a range. To select all of the data on a table, choose CTRL-A (CMD-A on a Mac).

To create a Pivot, select 'Insert' and then choose Pivot Table. A pivot table allows you to 'shape' data, visualising it a different way. Use the selected range, and then create the pivot on a new sheet.

<img
    src="/img/sheets/insert_pivot.png"
    alt="Insert a Pivot"
/>

The section on the right allows us to select from the columns, determining what will be on the rows (horizontal), the columns (vertical) and in the values themselves. The values are some kind of *aggregation*, counting specific values, or calculating totals.

<img
    src="/img/sheets/pivot1.png"
    alt="Pivot"
/>

Here, we add the 'year' to rows, and the medal to columns and value. By default, the `COUNTA()` function is selected, counting the amount of rows that meet the criteria of having that year and that medal.

<img
    src="/img/sheets/pivot2.png"
    alt="Pivot"
/>

Note that this shows the athletes who did not win a medal - shown as NA - also as part of the total. In order to get a better grasp of the information, sometimes we need to combine pivots and filters!


<img
    src="/img/sheets/pivot3.png"
    alt="Pivot"
/>

## Charts

Charts are another powerful way of getting to understand our data. In order to create a chart choose Insert -> Chart. It generally makes sense to move charts to their own page - you can do this by selecting the three dots on the top right, and select 'move to own page'

<img
    src="/img/sheets/move_chart.png"
    alt="Move chart"
/>

## Pie Charts

A pie chart is a popular way to visualise the proportion of values within a particular column. To get this, select 'Edit Chart'. Under chart type, choose *Pie Chart*. Select a column as the data range, for example `athlete_events!C2:C`. You will also select *aggregate* as here we aren't showing individual records, but a fact about the data in the column as a whole.

<img
    src="/img/sheets/pie_chart_setup.png"
    alt="Pie chart"
/>

A scatter chart is a way to visualise the relationship between values in two columns. In order to do this, we need to look at two numeric columns - for example, to compare athlete's height and weight, we can choose `athlete_events!E2:F`. We want to see individual rows *scattered*, so we unselect *aggregate*

<img
    src="/img/sheets/scatter_chart_setup.png"
    alt="Scatter chart"
/>

Note that in this particular visualization, athletes competing in multiple years or events will be plotted multiple times. Again, we can use filters to improve the quality of our visualizations.
