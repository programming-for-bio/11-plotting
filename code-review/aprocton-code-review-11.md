# aprocton-code-review-11.md
### Alexander M. Procton / 4.16.2018
### Reviewing code by [nehasavant](https://github.com/programming-for-bio/11-plotting/blob/master/assignment/nb-11-5-nehasavant-assignment.ipynb)

1. __Combining scatterplot coordinates with further styling of the markers using size or color variation can provide additional information about the points. In this plot, the y position should correspond with the size of markers. Do you think this is a useful way to emphasize information in a plot? Could it possibly be misinterpreted or misleading in some way? Did your peer create plot as instructed, and did they use the same method as you?__

   For some reason this plot does not show the points, even though the code that was used to produce it looks consistent with the other examples. Although I created `Canvas` objects with individual `axes` for each graph, Neha called `toyplot.scatterplot()` with the relevant inputs, without creating a `Canvas`. This may be part of the problem with this graph.

   I think that marker size mapped to y-values could be useful if there is some nonlinear effect due to the y variable where another variable increases exponentially with that y. Otherwise, it might be confusing and overemphasize those data at the expense of others.

2. __Here points are also colored using a colormap mapping to the x value of the points, and the size is random. There is not likely to be a good reason to make the size of points random in a real plot, but it does make for an interesting looking figure here. Think of and describe an example scatterplot in which there are 4 values you wish to represent, and you would use size, color, and x, and y coordinates to display information about all four.__

   If visualizing a set of basketball games between two rival teams, the x-axis could represent some relevant attribute of one team (e.g. win-loss record), the y-axis would represent the same variable for the other team, size would represent the total number of points scored, and the color could represent the winner (or even the relative difference in the number of points scored, using a diverging colormap).

3. __Modifying the placement of tick marks and axes labels is often a difficult task, and is done a bit differently in every plotting library. It is important that ticks marks are spaced out and made to an appropriate size to be readable. Did your peer add tick marks as described? Did they use a different method than you did?__

   Neha's tick marks are as described, and she even adjusted the marks, whereas I only adjusted the labels. Neha used `toyplot.locator.Integer()` with a step size of 11, whereas I used `toyplot.locator.Explicit()` to place labels at the mean x value of the distribution and every 10 units away (one standard deviation).

4. __Barplots are used to show a distribution of binned data points. The default styling of barplots is often used, but modifying the size of bins, their color, or the spacing between them can often make for a much nicer looking plot. Did your peer bin the data into 15 bins? Did they apply a colormap to the bars? Given this distribution, which type of colormap do you think would be most appropriate, i.e., a linear map, a diverging map?__

   Neha did create a histogram with 15 bins and a colormap, but the colormap was not mapped to the height of the data, but rather to the x position of the bar. Mapping the color to the height can be accomplished by using the first row of the data returned by `np.histogram()` only.

5. __Creating plot layouts that combine multiple plots onto a single canvas is an important skill to learn to begin to make complex plots that display a lot of information. This plot should show a histogram on the left, and a corresponding scatterplot on the right. The density of points should match up between the two. Which of the two plots do you think is more informative about the distribution of the data? Did your peer use a different method than you did, and how do they differ?__

   Our methods match up, although I accidentally generated 5000 data points. In this case, the histogram is likely more informative, because the values were randomly generated and there is no trend when plotted in order. If there were some autocorrelation, the scatterplot would be more useful.
   