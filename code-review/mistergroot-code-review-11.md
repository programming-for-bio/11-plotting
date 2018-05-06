# Code Review of meairey notebook 11

#### [Problem 1]: 
I don't think corresponding y position with size of marker is a useful way to
emphasize information. I think it looks nice but it can convey an increased
sense of importance for the points that have a larger y value. It might make
some sense if the axis was log-scaled so that a viewer understand that the
y-values are larger than they appear but I don't think it makes any sense when
the data is linear. Montana used the same methods that I did but she forgot to
set the figures to be 300x300. Additionally, in the numpy documentation it says
that when drawing from a random exponential distribution, the scale parameter is
the inverse of the rate parameter, so she should have had `scale=1/3`, not
`scale=3`.

#### [Problem 2]: 
In a case where I'm making a scatterplot and 3 out of 4 datapoints have the same value, I'd use size to represent how many datapoints have that value on the scatterplot. I'd do the same with color. Color and size would represent the weight/number of datapoints at the given x/y value.

#### [Problem 3]:
My peer added tick marks and they were equally spaced but I think this was a result of not using the 300x300 figure size. I think if the figure were resized to 300x300, pyplot wouldn't have spaced the tick marks correctly and she would have had to mess with the formatting to get 7 evenly spaced tick marks. I couldn't figure out how to get 7 evenly spaced tick marks in toyplot so I just messed with the step in the `toyploy.locater.Integer` function until I got 7 evenly spaced tick marks.

#### [Problem 4]:
My peer binned the data into 15 bins and applied the `spectral` colormap to the bars. I'm not sure what colormap would be best for this type of distribution. I think as long as a legend is included, it may not matter. I chose a colormap that would denote higher values with warm colors instead of cool colors (`"BlueYellowRed"`, which is diverging) but I'm not entirely sure if this is the best colormap or what would make a better colormap for this particular distribution.

#### [Problem 5]:
I think the histogram is more informative and easy to understand when compared with the scatterplot. The scatterplot just seems fairly random and its difficult to understand what's going on, but when it's binned into a histogram it becomes easier to understand. My peer used pyplot and I used toyplot but the end result was nearly the same (I think my partner forgot to remove the y-axis on the scatterplot, though). Although they do nearly the same thing, I think I prefer toyplot simply because the code is less abbreviated and makes more sense to me when I read it.
