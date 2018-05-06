## Code Review of chloehacker

### Problem 1
#### Their graph was mostly correct, however the size of their data points did not correspond with y through variation in either size or color. I created my graph in matplotlib, so the methods we used were slightly different. To set the marker to the y value i used the argument 's = y' . I think that this could potentially be a useful way to portray data. It definetely emphasizes the smaller values of the y-axis. However, looking at it, the data points with large x-values also have smaller points. While it is logical when looking at the axes, I feel like this could be misleading since they don't take into account the x variable. It is also hard to see the data points that correspond to very small y-values. 

### Problem 2
#### They created the data correctly. The markers also varied with x along a colormap. Again, they didn't change the size of their markers and the markers didnt randomly vary. Size of the dots could correspond to a population size, x and y coordinates could correspond to geographic coordinates, and the color of the dot could correspond to different habitat types within the geographic region. These four variables might be used in a study looking at populations across different habitats within a broader region. 

### Problem 3
#### Only three tick marks show up on their x axes. So they did not manage to get the evenly spaced tick marks to appear. In my graph, the x axis was showing up with 7 tick marks without any modification, so I didn't write any code to change that setting. 

### Problem 4 
#### The data is binned into 15 bins. They also applied a colormap to the bars. However, the colormap that was applied didn't correspond to the height of the bar. Because of the distribution, there should have been similarly colored bars on either side of the barplot. Because of this, I think a divergant colormap would be most appropiate since it would show distinct differences between low and high values. 

### Problem 5
#### I think that the scatterplot is most informative about the distribution of the data. I find the histogram easier to look at and understand, however there are some outlying points in the scatterplot that aren't represented in the histogram. In fact, if the scatterplot wasn't there, I probably wouldn't have realized that those points were there. I do like having the histogram next to it, since I felt that it provided an easy to understand representation of the data. The person I'm code reviewing used toyplot to create their graphs. I did all my graphs in matplotlib so the methods we used were different from each other. 

