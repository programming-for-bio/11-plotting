# Code Review 11
Review of mistergroot by juliazeh
4.16.18

## Problem 1
I don't think that this is a particularly useful way to emphasize information unless there's something really important about large y values. This plot could be easily misinterpreted and it would be easy to assume that the size of the datapoints is related to the number of data points with those coordinates. It could be misleading because it is hard to see the points with lower y values and hard to tell how many there are. There are fewer points with large y values, but these values appear more important and it looks like there are more of them simply because they are larger. In mistergroot's plot the size of the markers do not correspond with the y position. We used the same method, and they used the parameter `size = y` so I'm not sure why it does not appear that way in their plot. They also used a scale of 1/3 instead of 3 and did not use kwargs, which I used in all of my plots.

## Problem 2 
An example scatterplot could represent the Iris dataset we've used before in class by representing sepal width on the x axis, sepal length on the y axis, petal width by the size of the data points, and class using color. 

## Problem 3
Yes, they do have 7 tickmarks equally spaced at 10 units apart. They used a different method then I did - they used `toyplot.locator.Integer(step=10)` while I used a piece of code I found in the documentation to create 7 equally spaced tickmarks - `toyplot.locator.Heckbert(count=7)`. I'm not sure which is better because the `Integer` method involves estimating what the interval between tickmarks should be, while the `Heckbert` method makes the tickmarks larger than the axis and the datapoints. 

## Problem 4 
Yes, the data is binned into 15 bins. I think the color mapping used here is useful because it draws the eye to the values with similar frequencies at either end of the axis.

## Problem 5
I think the histogram is more useful for looking at the distribution of data because it is a lot clearer which y values have the highest frequencies and how the frequencies of different values compare to each other. Both of us used `canvas.cartesian(bounds)` to place two plots on the same canvas. The only difference between our methods was that they used `toyplot.locator.Integer` again and that the colormapping of the histogram was done using `color=(xhist[0], colormap)` while I used `height1, value1 = np.histogram(population, 15)` and set `color=height1`. They also changed some of the colors while I used the default colors.