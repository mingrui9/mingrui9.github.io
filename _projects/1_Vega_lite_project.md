---
name: IS 445 HW10
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# HW10


## Plot 1

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1.json" style="width: 100%"></vegachart>


<b>(1) what features you are highlighting with your viz;<b>
    
Same as HW9, the 'base' plot here is the same in HW9. "I (mengyue) used the Square Footage as the horizontal axis and Senator Full Name as vertical axis for this first illustration of bar plot. I wanted to see the distribution of total building Square Footage for senators" (queto from HW9 plot1 write-up). However, different from HW9, we also put in the factors of 'building status' and 'County' to make the plot more informative.
    
<b>(2) the design choices you made (scales, encoding types, colors, etc.) to visualize your data appropriately;<b> 
    
We changed the code of “width”: “500”, “height”: “600” to rescale the plot in the originally JavaScript dictionary code to “.properties(width=500,height=600)” to fit in the “alt.Chart().mark_bar().encode()” instead of alt.Chart.from_dict() as a “pure” Altair plotting code. Besides, we choose our color scheme to be ‘set2’ from the vega color schemes since we want my colors for each building status group to be distinctive but also not too bright at the same time for aesthetic needs. We also used .configure_axis(labelFontSize=13,titleFontSize=20) to make the titles and labels in axis more readable.
    
<b>(3) Interactivity <b>

We add in the factor of 'building status' as color and dropdown for the audience to choose and five further into. We also add 'County' as a tooltip result to give more information about the building and its senator.


## Plot 2

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>

<b>(1) what features you are highlighting with your viz;<b>
    
For this visualization here, we are trying to plot a histogram between the ‘Year Constructed’ and ‘Total Floors’ variable for buildings to see if there exists an obvious pattern between these 2. We also add in the “Square Footage” of that building to help the audience read the plot more clearly.
    
<b>(2) the design choices you made (scales, encoding types, colors, etc.) to visualize your data appropriately;<b>
    
We also pay attention to the rescale of the plot size and text size in titles and scales. We use “.properties(width=700,height=400)” and “.configure_axis(labelFontSize=20,titleFontSize=20)” to take care of the readability of the plot.
    
<b>(3) Interactivity <b>
    
For this 2nd plot, we use tooltip to help the reader to read the tendency between “Year Constructed” and “Total Floors” more clearly with additional information about “Square Footage” as an extra visualizing figure.





<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/mingrui9/mingrui9.github.io/blob/main/python_notebooks/HW10.ipynb" text="The Analysis" %}
</div>

