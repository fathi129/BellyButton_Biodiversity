# BellyButton_Biodiversity
A dynamic BellyButton Biodiversity Dashboard is built using JavaScript, which displays bar chart, bubble chart, gauge chart, and demographic information according to the selected ID by the user.

## Overview of the Analysis
Data Professionals not only need to analyze the data and draw conclusions. They need to visualize data to communicate the findings to the audience. Using JavaScript, we create data visualizations that are attractive, accessible, and interactive. We will use Plotly, a JavaScript data visualization library. It offers interactivity that increases audience comprehension. We will be using JavaScript's interactive features like buttons and drop-down menu and retrieving the data from .json, and .csv files. We will deploy the polished visualization to the web.

## Purpose of the Analysis
Roza is a biological researcher whose role is to discover and document the bacteria. She is interested in bacterial species that can synthesize proteins that taste like beef. She hypothesizes that these bacteria are found on the human body. The human body is a source of thousand of types of bacteria, different parts of the body harbor different species. She hypothesizes that the ideal bacterial species to make the synthetic beef may be found in the belly button. To help her, we test it. We have samples of the navel of the people across the country to identify the bacterial species. Each person is identified with an id number. Now we need to extract the sample values and bacteria IDs to plot the charts. The dashboard is built to see each person's different types of bacteria. The dashboard is deployed on the Github pages so everyone can access the site to see what bacteria live on the belly button.

## Resources Used
*DataSources*: [samples.json](https://github.com/fathi129/BellyButton_Biodiversity/blob/master/samples.json)<br>
*Software used*: HTML, CSS, Bootstrap 3.3.7,D3.js Library.<br>
*Language*: JavaScript. <br>
The Belly Button Biodiversity is deployed on the Github page: https://fathi129.github.io/BellyButton_Biodiversity/<br>

## Deliverable 1: Create a Horizontal Bar Chart 
Using the knowledge of JavaScript, Plotly, and D3.js, a horizontal bar chart is created which displays the top 10 bacterial species (OTUs) when an individual's ID is selected from the drop-down menu on the webpage. The horizontal bar chart displays the sample_values as the values, the otu_ids as the labels, and the otu_labels as the hover text for the bars on the chart. The Horizontal bar chart looks like the following image:<br>
<img src = "https://github.com/fathi129/BellyButton_Biodiversity/blob/master/Screenshots_plotly/Bar_Chart.png" width = 600><br>

The buildCharts() function contains the argument sample, which is the sample selected from the drop-down menu.The code has been developed to retrieve the contents from the samples.json file using the d3.json().then() method.A variable has been created that has the array for all the samples. We have created a variable that will hold an array containing all the data from the new sample chosen from the drop-down menu. To retrieve the data from the new sample, filter the variable for the sample id that matches the new sample id chosen from the drop-down menu and passed into the buildCharts() function as the argument.We have created variables that have arrays for otu_ids, otu_labels, and sample_values,yticks for the bar chart. Using the Plotly method, the bar chart is created.

## Deliverable 2: Create a Bubble Chart 
A bubble chart is created by taking otu_ids as the x-axis values,sample_values as the y-axis, and assigning otu_labels as text properties. For the mode and marker properties, the mode is "markers" and the marker property is a dictionary that defines the size, color, and color scale of the markers. using the hover mode property, the text is made to display when the cursor hovers over the graph.Finally, the chart is created using the Plotly.newplot() function.The bubble chart looks like the following image:<br><br>
<img src = "https://github.com/fathi129/BellyButton_Biodiversity/blob/master/Screenshots_plotly/BubbleChart.png" width = 900><br>

## Deliverable 3: Create a Gauge Chart 
A gauge chart is created which displays the weekly washing frequency's value, and displays the value as a measure from 0-10 on the progress bar in the gauge chart when an individual ID is selected from the drop-down menu.created a variable that filters the metadata array for an object in the array whose id property matches the ID number passed into buildCharts() function as the argument.A variable is used to hold the washing frequency. The trace object for the gauge chart is created by taking washing frequency as value, and choosing the type of chart as indicator. Finally the gauge chart looks like the image below:<br>
<img src = "https://github.com/fathi129/BellyButton_Biodiversity/blob/master/Screenshots_plotly/Gauge_chart.png" width = 500><br>

## Deliverable 4: Customize the Dashboard 
Using HTML and Bootstrap, the dashboard is customized
- Added an image to the jumbotron class.<br>
 <img src = "https://github.com/fathi129/BellyButton_Biodiversity/blob/master/Screenshots_plotly/jumbotron.png" width = 700><br>
- Added background image and a variety of compatible colors to the webpage, Added color to the font and, customized the fonts, Added information about what each graph visualizes.<br>
- Made the webpage mobile-responsive.<br>
<img src = "https://github.com/fathi129/BellyButton_Biodiversity/blob/master/Screenshots_plotly/Mobile_responsive.png" width = 500><br>
- When the dashboard is first opened in a browser, ID 940's data is displayed in the dashboard, and the three charts are working according to their requirements.When a sample is selected, the dashboard displays the data in the panel and all three charts according to their requirements. The final dashboard looks like this below: bar chart,bubble chart and gauge chart.<br>

<img src = "https://github.com/fathi129/BellyButton_Biodiversity/blob/master/Screenshots_plotly/entiredashboard.png" width = 900><br>




