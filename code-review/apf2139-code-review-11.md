# Code Review by Alex Ferrena (apf2139)

I reviewed kuratanp's code instead of my assigned reviewee, mvanack

### 1

This could be a useful way to call attention to outliers in a plot containing a ton of data. It could be misleading in that it might assign visual importance to y-value outliers even if they are simply due to random chance. The reviewee used Bokeh while I used toyplot. (unfortunately I totally missed the part about assigning size of points to increasing Y axis values!)

### 2

It is indeed a cool looking plot. AN example of a plot using all four of these visual properties could include a plot to examine the fruits and trees of different species of the genus Artocarpus, which includes the jackfruit and breadfruit trees.

The x axis could be the age of the tree; the y axis could be the height of the tree; the color of the points could denote species (red for jackfruit, A. heterophyllus, and blue for breadfruit, A. altilis). The size of the points could denote the weight of the fruit. I imagine such a plot would show a positive correlation between the x and y axes.

### 3

The reviewee's tickmarks look great! While we both used toyploy, the reviewee's shows actual tick marks on the x axis while mine just has the tick labels below. Furthermore, the reviewee's tick labels are not angled, whereas for some reason mine were being clipped off so I had to rotate them to a 90 degree angle, making them a pain to look at.

### 4

The reviewee's data is binned into 15 bars. There is a colormap applied to the plot, although it lacks the black strokes separating the bars. I think a proper colormap to use might be a diverging colormap, given the normal distibution of the data.

### 5

The scatterplot on the right has more information than the barplot on the left. This is due to dataloss from binning. The reveiwee and I both used toyplot to generate this plot, but we did it slightly differently. FOr example, to generate the two plots, my peer used the "grid" method while I used the "bounds" method.