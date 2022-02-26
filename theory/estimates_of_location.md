# Estimates of location

variables with measured or count data might have dozen of district values. A besic step in exploring data
is getting "a typical value" for each variable: an estimate of where most of data is located (its cental
tendency)

## Key terms for estimates of location

### Mean (average)
the sum of all values divided by number of values

### Weighted mean (weighted) average:
the sum of all values times a weight devided by the sum of the weight
Why use it?
1. Some values are more variable than others, highly variable observations are given a lower weight example: we have got many sensors and one of them is less acqurated than others. If we do not sign weight, it will distrub our result.
2. The data collected does not equaly represent the different groups that we are interested in measuring. For example we have results of online experiment. But it was wrong conducted, we do not have a set of data
that accurately reflects all groups in the user base. To correct that, we can give a higher weight to the values from groups that were underrepresented

### Median (50th percentile)
the value such that one-half of data lies above and belove. It is the middle number on a sorted list of data. If the number of probes are even, we divided to 2 middle numbers by 2.
Compared to the mean which uses all observations, the median depent onlu on the values in the center of sorted tata. 
There are many cases where median is better location metric than mean. For example if we want look at typical household incomes in California using mean would produce diffrent results because many of bilioners live there. If we use the median, it won't matter how rich are these bilioners - the position of the middle will remain the same.
Median is robus to outliners

### Weighted median:
the value such that one-half of the sum of the weights lies above and belove the sorted data
The waighted median is a vlue such that the sum of weights is equal for the lower and upper halves of the sorted List.
Weighted median is robus to outliners

### Trimmed mean (trucated mean):
the averange of all values after dropping a fixed number of extreme values.
It is used to avoid the influence of outliers. It's a compromise between the median and the mean. 
It is robust to extreme values in the data but uses more data to caclulate the estimate for location.

### Robust (resistant):
not sensitive to extreme values

### Outlier (extreme value)
a data value that is very different from most of the data.
An outlier is any value that is very distant from the other values in the data set. Being outlier
does not mean that data value is invalid or erroneous (for example these bilioneres).
Still outliers are often the result of data erros such as mixing data of different units or bad readings from a sensor. When outliners are the result of bad data, the mean will result in a poor estimate of location, while median will be valid. In evey case outliers should be identified an worthy investigation.

# Anomaly detection:
In anatomy detection the points of interest are the outliers, and the greater mass of data serves primarly
to define "normal" against which anomalies are measured