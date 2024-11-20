# Building inventory Dataset Visualisations
*Submitted By Tanvi Lakhani(tjl8@illinois.edu)*


## Visualization 1: Bar Chart of Total Square Footage by County

<!-- Embed the JSON chart for Total Square Footage by County -->
<div id="vis1"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
  // Load the JSON specification for Visualization 1
  vegaEmbed('#vis1', 'county_data_plot.json').catch(console.error);
</script>

**Writeup:**

### **1. Description**  
This bar chart shows the total square footage of buildings across different counties, grouped by their usage description. Counties are displayed on the x-axis, square footage on the y-axis, and colors are used to represent usage descriptions, making it easy to compare building space distribution across counties.

### **2. Encoding Types**  
- **X-axis (Nominal)**: Represents county names as categorical values.
- **Y-axis (Quantitative)**: Displays total square footage, showing the cumulative size of buildings for each county.
- **Color (Nominal)**: Encodes usage description.
- **Tooltip**: Provides additional details, including county name, usage description, and total square footage when hovering over the bars.

### **3. Color Scheme**  
A categorical color scheme is used to distinguish between usage descriptions. This ensures each category is visually distinct, improving readability and accessibility.

### **4. Data Transformations**  
The dataset was grouped by County and Usage Description to calculate total square footage for each combination. Missing values in the County column were replaced with "Unknown," while undefined entries in "Usage Description 2" and "Usage Description 3" were filled with the most frequent values (mode). These transformations ensured the data was clean and complete for accurate visualization.

### **5. Interactivity**  
A dropdown menu allows users to filter the chart by a specific usage description.

### **6. Impact of Interactivity**  
The dropdown filter by usage description allows users to focus on specific categories, enabling easy comparison across counties and revealing trends in the data.

### **7. Overlaps with Homework #7**
While the same dataset was used, this plot does not overlap with the analysis from previous homework. It focuses on visualizing the total square footage across counties, grouped by usage description, which is a different analysis and visualization approach compared to previous homework.

## Visualization 2: Bubble Chart of Square Footage by Agency and Congressional District
<!-- Embed the JSON chart for Square Footage by Agency and Congressional District -->
<div id="vis2"></div>

<script>
  // Load the JSON specification for Visualization 2
  vegaEmbed('#vis2', 'bubble_chart_building_status.json').catch(console.error);
</script>

**Writeup:**

### **1. Description**  
This bubble chart visualizes the relationship between agencies and congressional districts, with bubble size representing the total square footage of buildings and color indicating the building status. The chart allows for a detailed comparison of building sizes and conditions across agencies and districts.

### **2. Encoding Types**  
- **X-axis (Nominal)**: Represents agency names.
- **Y-axis (Nominal)**: Displays congressional districts.
- **Bubble Size (Quantitative)**: Corresponds to total square footage, with larger bubbles indicating larger spaces.
- **Color (Nominal)**: Encodes building status, using distinct colors to represent conditions like in use, abandon or in progress.
- **Tooltip**: Provides detailed information, including agency name, district, building status, and total square footage on hover.

### **3. Color Scheme**  
A nominal color scheme is applied to differentiate building statuses, ensuring clear visual representation and easy comparison.

### **4. Data Transformations**  
The dataset was grouped by Agency Name, Congress Dist, and Bldg Status to compute the total square footage for each group. Missing values in Congress Dist were replaced with "Unknown Congressional Name". These transformations ensured all data was consistent and ready for meaningful analysis.

### **5. Interactivity**  
A dropdown menu allows users to filter the chart by building status. 

### **6. Impact of Interactivity**  
The filter by building status helps users explore data based on different building conditions, providing deeper insights into how status impacts square footage across agencies and districts.

### **7. Overlaps with Homework #7**
This plot also uses the same dataset but explores the relationship between agencies, congressional districts, and square footage, incorporating building status. It is distinct from the visualizations in previous homework.

#### Resources

- [The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)
- [The Analysis](https://github.com/Tanvilakhani2112/Homework6---IS445/blob/main/Workbook.ipynb)
