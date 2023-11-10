---
name: Homework 8 Charts
tools: [Python, HTML, vega-lite]
image: assets/pngs/Capture.png
description: These contain the plots for the project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework 8 Charts 
3 charts for assignment

Plot 1:

<vegachart schema-url="{{ site.baseurl }}/assets/json/Vis2.json" style="width: 100%"></vegachart>

Explanation for Plot 1:

Description of the Plot: 
The plot visualizes the distribution of building statuses in a dataset. Each bar represents a specific building status, providing a quick overview of the count of buildings associated with each status. The dataset is derived from building inventory data, and the focus is on understanding the distribution of building statuses.

Design Choices Encodings :
1) Mark: The choice of a vertical bar chart (mark="bar") is suitable for showing the count or frequency of different categories, in this case, building statuses. 
2) Width and Height: The dimensions of the chart (width=600, height=300) are chosen to balance clarity and space usage, providing a compact yet informative visualization. 
3) Encodings: The nominal encoding (x) is employed for the "Building Status," allowing distinct categories to be displayed along the x-axis. The count is aggregated and represented on the y-axis (y) as the height of the bars. 

Colormaps:
For the color encoding, a categorical color scheme ("category10") was deliberately chosen to represent different building statuses. This decision enhances visual clarity by providing distinct colors for each category, facilitating easy interpretation. The "category10" scheme's predefined set ensures clear differentiation, contributing both functionally and aesthetically to the chart.


Transformations: 
The plot includes a transformation (transform_filter) to filter the data, displaying only buildings acquired after the year 2000. This allows for a focused exploration of recent building statuses, contributing to a more relevant and up-to-date visualization. This design aims to offer a clear and concise representation of building statuses, emphasizing recent acquisitions through the applied transformation. The color choice helps draw attention to the bars, making the plot visually engaging and accessible.

Overlap with Homework 7 :
In the transition from Homework #7 to Homework #8, I redefined the initial bar chart by introducing a color map in Homework #8. For it to work with Altair a critical alteration involved removing the quotation marks around the numerical values specified for the "mark" and "width" parameters, which differed from the Homework #7 syntax. The chart now visualizes building status counts, with each status uniquely colored using a categorical color scheme. Additionally, a transformation filters out buildings acquired before 2000, refining the focus for a more relevant and insightful representation. This adaptation enhances the clarity and interpretability of the visualization.

Plot 2:

<vegachart schema-url="{{ site.baseurl }}/assets/json/Vis3.json" style="width: 100%"></vegachart>

Explanation for Plot 2:

Description of the plot:

The second visualization explores the relationship between counties and the mean square footage of buildings, focusing on those with square footage exceeding 20,000. The chart employs a bar mark to represent the mean square footage for each county, with the color intensity indicating the count of buildings meeting the specified square footage criterion.

Design Choices - Encodings :

Mark: The choice of a vertical bar chart (mark=”bar”) is suitable for showing the count or frequency of different categories, in this case, building statuses. Width and Height: The dimensions of the chart (width=600, height=300) are chosen to balance clarity and space usage, providing a compact yet informative visualization.
For the encoding choices, the X-axis represents the counties, offering a categorical view, while the Y-axis aggregates the mean square footage, providing a quantitative measure. This selection aims to highlight variations in square footage across different counties.

Design Choices - Color Map :

The color scheme utilizes a quantitative color map, where the intensity of color signifies the count of buildings. This choice aims to emphasize the distribution and density of buildings with square footage exceeding 20,000 in each county. The Viridis color map was chosen for its perceptual uniformity, ensuring accurate interpretation of building count variations.

Transformations :

A data transformation is applied to aggregate the average square footage for each county and subsequently filter out counties where the average square footage is below the threshold of 20,000. This transformation enhances the focus on counties with larger buildings, providing a clearer picture of the distribution.

Overlap with Homework 7:
In transitioning from Homework #7 to Homework #8, I modified the visualization approach while building upon the foundational aspects of Homework #7. In Homework #7, I employed a line chart with a continuous green color mark to represent the mean square footage across different counties. However, in Homework #8, I chose a bar chart for a more categorical representation of mean square footage, incorporating additional features for enhanced insights.

Changes Made:
For it to work with Altair a critical alteration involved removing the quotation marks around the numerical values specified for the "mark" and "width" parameters, which differed from the Homework #7 syntax. In Homework #8, the chart design was adapted to a bar mark, utilizing color as a quantitative representation of building count within each county. The color intensity indicates the count of buildings with square footage exceeding 20,000, offering a nuanced perspective on the distribution of larger buildings across counties. Additionally, a data transformation was introduced to filter out counties with mean square footage below the threshold of 20,000, focusing the visualization on relevant data points.

Interactivity Plot :

<vegachart schema-url="{{ site.baseurl }}/assets/json/Vis4.json" style="width: 100%"></vegachart>

Explanation for the interactivity plot :

In this visualization, I incorporated interactivity using a brush selection tool. The first chart, chart1_interactivity, is a heatmap with square footage on the x-axis, agency names on the y-axis, and color representing the count of buildings falling within each bin. The brush selection is applied to both the x and y axes, allowing users to interactively select a subset of the data. The second chart, chart2, is a bar graph displaying the count of buildings based on square footage. The bar chart dynamically updates based on the brush selection in the first chart. This interactivity enhances the exploration of building distribution across different agencies and square footage ranges. Users can visually identify patterns and relationships within the data by focusing on specific regions of interest, making the exploration process more intuitive and insightful.

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/deekshamanoharrao/deekshamanoharrao.github.io/tree/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

