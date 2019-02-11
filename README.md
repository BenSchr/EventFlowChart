# EventFlowChart
Webpage for displaying Events with the Google Charts Sankey Diagramm out of a JSON File.

</br>Two frameworks are used to display the events:
</br>Google MDL Template: https://getmdl.io/templates/index.html
</br>Google Charts Sankey Diagramm: https://developers.google.com/chart/interactive/docs/gallery/sankey

</br><img src="./images/Example.png" width="500" height=auto />


# Data

For displaying the Events we need two JSON-Files inside the "data" folder.
</br>In one JSON-File we are holding the events:

</br><img src="./images/EventJsonExample.PNG" width="500" height=auto />

In the over JSON-File we can map the numbers to real Events:

</br><img src="./images/MapJsonExample.PNG" width="500" height=auto />

# Computation

The events will be loaded into Javascript and converted into weight network JSON-Objects for every Steplayer:
</br></br>
{"Events": ["1","2","4"]},{"Events":["1","2","3"]} 
</br></br>
for example will be converted into:</br>
{
</br> 1:[{"from":1, "to":2,"weight":2}],
</br> 2:[{"from":2, "to":4,"weight":1},{"from":2, "to":3,"weight":1}]}
