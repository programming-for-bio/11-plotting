#### [Problem 1] Combining scatterplot coordinates with further styling of the markers using size or color variation can provide additional information about the points. In this plot, the y position should correspond with the size of markers. Do you think this is a useful way to emphasize information in a plot? Could it possibly be misinterpreted or misleading in some way? Did your peer create plot as instructed, and did they use the same method as you?

This format doesn't make a ton of sense because it doesn't convey any additional information (like frequency of data points or something), but it does look nice and it isn't necessarily confusing unless someone interprets it as a weighted distribution or something. This student used toyplot, where as I used matplotlib but the results were the same!

#### [Problem 2] Here points are also colored using a colormap mapping to the x value of the points, and the size is random. There is not likely to be a good reason to make the size of points random in a real plot, but it does make for an interesting looking figure here. Think of and describe an example scatterplot in which there are 4 values you wish to represent, and you would use size, color, and x, and y coordinates to display information about all four.

Random size definitely isn't helpful, and neither is a colormap of the x values. I think it might be helpful to add size and color components in the form of time at collection and frequency/popularity of data points (and x and y can refer to a traditional explanatory and response variables).

#### [Problem 3] Modifying the placement of tick marks and axes labels is often a difficult task, and is done a bit differently in every plotting library. It is important that ticks marks are spaced out and made to an appropriate size to be readable. Did your peer add tick marks as described? Did they use a different method than you did?

The tick marks aren't here, there are just the labels on the x acis. This was done and toyplot and I think mine were there by default in matplotlib.

#### [Problem 4] Barplots are used to show a distribution of binned data points. The default styling of barplots is often used, but modifying the size of bins, their color, or the spacing between them can often make for a much nicer looking plot. Did your peer bin the data into 15 bins? Did they apply a colormap to the bars? Given this distribution, which type of colormap do you think would be most appropriate, i.e., a linear map, a diverging map?

This bar plot does have 15 bins and the colormap is a logical one to use. A linear color map would make no sense, but diverging is helpful in reinforcing the frequency pattern.

#### [Problem 5] Creating plot layouts that combine multiple plots onto a single canvas is an important skill to learn to begin to make complex plots that display a lot of information. This plot should show a histogram on the left, and a corresponding scatterplot on the right. The density of points should match up between the two. Which of the two plots do you think is more informative about the distribution of the data? Did your peer use a different method than you did, and how do they differ?

These plots look great! I definitely struggled with this and it looks a little simpler to understand using toyplot. The only thing I see that might be a place to change is the y axis on the second plot. Removing the labels on this plot makes it clearer that these two plots are subplots, rather than two seperate plots. I think the histogram is a more helpful and visually simpler plot, but both are useful and work well together. 
