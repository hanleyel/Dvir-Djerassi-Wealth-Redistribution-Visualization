# Wealth Redistribution Visualization
Asher Dvir-Djerassi, University of Michigan Center for Inequality Dynamics<br>
Liz Hanley, University of Michigan Institute for Social Research Population Studies Center

## Project Description
This interactive dashboard visualizes the effects of a proposed wealth redistribution program. The purpose of the dashboard is for end-users to see how modifying different parameters of the distribution program, such as grant size and interest rate, will impact wealth gaps over time. Visualizations include the share of wealth owned by the top 1% over time, median wealth by race, racial wealth gaps, and impacts of wealth redistribution programs on the share of wealth owned by the top 1%. Additional tables include descriptive statistics for U.S. population size and total endowment program cost over time. The dashboard is built using the D3.js library.

## Installation
Clone the project GitHub repository to your desired local directory: `git clone https://github.com/hanleyel/Dvir-Djerassi-Wealth-Redistribution-Visualization.git` <br>
Launch the index.html file in your browser by either double-clicking the file or dragging and dropping into a browser window

## If you want to…
### Modify Existing Data
Since data are pulled in directly from the GitHub repository, to modify existing data, you will simply need to replace a given .csv file with an updated version. As long as the file path, file name, column names, and data types remain the same, the program will automatically pull in the updated data.

### Add a New Data Set
If you wish to add a new data set, you will need to put the file in the `csv` directory within the GitHub repository. The URL any new file’s raw data on GitHub (i.e., click on the file within GitHub > click on the “Raw” tab > copy this URL) will need to be added to the `files` variable (an array of links to raw GitHub data) in the `index.html` file. You can then assign your dataset a variable name by adding the desired variable name to the array argument within :

`Promise.all(promises).then(function([..., share_taxable_wealth_3_15,
share_taxable_wealth_3_30, share_taxable_wealth_3_50, <NEW_DATASET_VARIABLE>]);`

You will need to be sure that the index of your data URL within the “files” array is the same index of your new variable name within the “Promise” function array.

### Update a Chart or  Table
To update and existing chart, you can simply change the arguments in its associated function call.

`drawLineChart(\
    data=<dataset variable name>,
   svg=<the ID of the SVG you want your chart bound to>,
   draw_line_only=<false (do you want to draw the whole chart or only the line portion)>,
   stroke_type="stroke-solid",
   stroke_color="#3da4ab",
   x_axis_var=<The variable you want to use to draw the x-axis>*,
   y_axis_var=<The variable you want to use to draw the y-axis>,
   x_axis_val=<The data you want to map onto the x-axis>,
   y_axis_val=<The data you want to map onto the y-axis>,
   filter_var=<The variable you want to use to filter data, or null>,
   filter_value=<The value you want to filter for, or null>,
   parse_time=false,
   area_chart=true);`

*May be different from “x_axis_val” if you want to use the same x-axis across different charts.

`drawTable(
   data=<dataset variable name>,
   svg=<the ID of the SVG you want the chart bound to>,
   table_id=<the ID of the table you want to draw>,
   columns=[<the column names you want to use (these need to be the exact column names from the CSV file)>],
   filter_var=<The variable you want to use to filter data, or null>,
   filter_value=<The value you want to filter for, or null>);`


### Change the Dashboard Styling
Dashboard styling can be changed via `static\style.css.`

### Rename a Table Column or Data Label
The easiest way to rename a table column or data label is to change the column name within the .csv file. You can then simply use this new column name within the `index.html` file.

## Contributing
Issue Tracking: https://github.com/hanleyel/Dvir-Djerassi-Wealth-Redistribution-Visualization/issues

## Licensing
This project was produced through the support of the University of Michigan Center for Inequality Dynamics and the Institute for Social Research Population Studies Center.

## Citation
Dvir-Djerassi, A.; Hanley, E. 2021. Wealth Redistribution Visualization. https://github.com/hanleyel/Dvir-Djerassi-Wealth-Redistribution-Visualization (\<date accessed\>).

## Contact
For research questions, contact Asher Dvir-Djerassi at asherd@umich.edu<br>
For code-related questions, contact Liz Hanley at hanleyel@umich.edu 

