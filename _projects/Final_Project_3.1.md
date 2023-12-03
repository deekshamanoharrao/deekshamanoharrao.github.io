---
name: Final Project 3.1
tools: [Python, HTML, vega-lite]
image: assets/pngs/Project.png
description: These contain the plots for the project that includes 2 datasets outlining income levels and investments for different countries around the world.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

Group Members : Deeksha Manohar Rao and Sachit Vasudev
# Final Project 3.1 

Plot 1:

<vegachart schema-url="{{ site.baseurl }}/assets/json/Interactive_Visualization.json" style="width: 100%"></vegachart>

 ##User Guide:

Navigating the IFC Investment Dashboard is user-friendly, even for those new to data visualization:

Exploring the Heatmap: Start by exploring the heatmap, which visually represents the distribution of IFC investments. Hover over each cell to view specific values. Use the brush tool to select specific industry sectors and countries of interest. This action will dynamically update the linked bar charts below.

Country and Sectoral Breakdown: The first linked bar chart focuses on the total IFC investment by country, while the second chart breaks down investments by industry sector. Click on specific bars in these charts to isolate and analyze individual data points. The visualizations respond dynamically to your selections, providing a tailored view of the data.

Comparative Analysis with MIGA: Switch to the contextual visualization section to compare IFC and MIGA investments. Explore the geographical and sectoral distribution of both institutions side by side. The time series chart for MIGA investments offers insights into the temporal dynamics of both organizations.

Saving and Sharing: The dashboard supports interactive exploration, but users can also save specific visualizations. Use the save option to export the charts in various formats, including JSON. This feature enables users to share specific insights or integrate visualizations into presentations or reports.

In summary, the IFC Investment Dashboard is designed to empower users with a visually rich and interactive tool for exploring the complexities of international financial investments. The thoughtful combination of heatmap, linked bar charts, and contextual visualizations offers a comprehensive and dynamic experience for users at all levels of expertise.

Plot 2:

<vegachart schema-url="{{ site.baseurl }}/assets/json/Contextual_Visulization.json" style="width: 100%"></vegachart>


Introduction to IFC Investment Dashboard:

The International Finance Corporation (IFC) Investment Dashboard provides a comprehensive exploration of IFC's financial activities, focusing on key dimensions such as geographical distribution, sectoral preferences, and temporal trends. This dashboard is a collaborative effort by Deeksha Manohar Rao and Sachit Vasudev, leveraging the Altair visualization library. The primary dataset, sourced from IFC, offers a detailed record of approved investments, including industry sectors, countries, and monetary values. The visualizations aim to empower users, especially those new to data analysis, to gain insights into the patterns and impact of IFC investments.

Understanding Geographical and Sectoral Distribution:

The first section of the dashboard revolves around the geographical distribution of IFC investments. The heatmap chart provides an immediate overview of the total IFC investment across different countries and industries. Viewers can interactively explore the data by selecting specific regions or industry sectors using the brush tool. Two linked bar charts dynamically update in response to the user's selection, offering a detailed breakdown of investments by country and industry. This approach allows users to discern patterns and understand which countries and sectors are prominent in IFC's investment portfolio.

Contextual Visualization with MIGA:

To provide a broader context and enhance the comparative analysis, the dashboard incorporates visualizations from the Multilateral Investment Guarantee Agency (MIGA). The MIGA contextual visualization complements the IFC dashboard by illustrating investment data from another multilateral institution. The integrated charts showcase the geographical distribution and sectoral preferences for both IFC and MIGA, facilitating a side-by-side comparison. Additionally, the time series chart for MIGA investments over fiscal years offers insights into the temporal dynamics of both institutions. This comparative approach enables users to draw nuanced conclusions about the unique strategies and impacts of IFC and MIGA in the global financial landscape.

## Primary datset

## Dataset Information
1) Name of the dataset: IFC Investment Services Projects

2) Obtained : i obtained the dataset form World Bank data , under finances sub-section 

3) URL : You can obatin this from : https://finances.worldbank.org/Projects/IFC-Investment-Services-Projects/efin-cagm

Relative Path : IFC_Investment_Services_Projects_20231110.csv (in the workspace)

4) License :The website do not explicitly state the specific license information for the dataset.
   
   Usage : The platform encourages users to explore, analyze, visualize, and share the data. Developers are invited to connect through APIs, and there is an emphasis on transparency and openness. While no explicit license is stated, the information suggests a user-friendly and open approach to accessing and using the data.
   
   The explicit licensing information is not available, the dataset is intended for public use.
   
5) The dataset is an Excel file with a size of 2.1 MB, consisting of 6064 rows and 24 columns. While this file size falls within GitHub's upload limits, it's important to consider potential future scenarios where datasets might exceed these limits. If hosting the data on GitHub, continuous monitoring of file sizes and potential growth is recommended. In the event that the dataset surpasses GitHub's limits, an alternative plan could involve leveraging other data hosting services such as Amazon S3, Google Cloud Storage, or a dedicated server. This ensures the dataset remains accessible and manageable, considering the scalability of the data over time.

## Contextual Dataset
## Dataset Information
1) Name of the dataset: MIGA Issued Services 

2) Obtained : I obtained the dataset form World Bank data , under finances sub-section 

3) URL : You can obatin this from : https://finances.worldbank.org/Projects/MIGA-Issued-Projects/cg7w-bf4s

Relative Path : MIGA Issued Projects.csv (in the workspace)

4) License :The website do not explicitly state the specific license information for the dataset.
   
   Usage : The platform is designed to motivate users to delve into and engage with the data by exploring, analyzing, visualizing, and disseminating it. It extends an invitation to developers to integrate via APIs, highlighting a commitment to transparency and openness. Although it lacks specific licensing details, the platform appears to adopt a user-centric and open stance towards data access and utilization. Despite the absence of clear licensing guidelines, the dataset seems to be intended for public use.
   
5) The dataset is an Excel file with a size of 80 KB, 559 rows and 15 columns.

The contextual dataset, comprising projects insured by MIGA, complements your primary IFC investment dataset by enabling comparative analysis across different international financial institutions. It offers insights into regional and sectoral investment trends, and highlights shifts in investment strategies and priorities over time. This combined analysis enriches the understanding of the roles and impacts of these institutions in global development finance.


## Dashboard Summary: Design Choices 

Design Choices:

The IFC Investment Dashboard is thoughtfully designed to provide an intuitive and informative exploration of IFC's financial landscape. Several design choices were made to enhance user experience and facilitate a comprehensive understanding of the data:

Interactive Heatmap: The heatmap chart serves as the centerpiece of the dashboard, offering an immediate visual summary of IFC investments. The use of color encoding allows users to quickly identify high and low investment areas, while interactivity is incorporated through a brush tool. Users can easily select specific industry sectors and countries of interest, triggering dynamic updates across linked charts.

Linked Bar Charts: To delve deeper into the selected data points, two linked bar charts are employed. The first bar chart displays the total IFC investment by country, providing a detailed breakdown. The second bar chart focuses on the sectoral distribution of investments, offering insights into the industries that attract significant funding. Both charts dynamically adjust based on user selections, facilitating a granular analysis.

Contextual Visualization with MIGA: To enrich the analysis and provide context, visualizations from the Multilateral Investment Guarantee Agency (MIGA) are seamlessly integrated. This comparative approach enables users to contrast IFC and MIGA investments, offering a holistic view of multilateral financial activities. The combined charts provide a comprehensive narrative of investment patterns, sectors, and temporal trends.

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/deekshamanoharrao/deekshamanoharrao.github.io/main/_data/IFC_Investment_Services_Projects.csv"
</div>

<div class="right">
{% include elements/button.html link="https://raw.githubusercontent.com/deekshamanoharrao/deekshamanoharrao.github.io/main/_data/MIGA_Issued_Projects.csv"
</div>

