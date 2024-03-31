# matplotlib-challenge

## This is the repo for the Module 5 Challenge

The code for this challenge was completed with knowledge learned during class and with the help of ChatGPT. I used AI to help me in 2 sections: Quartiles, Outliers and BoxPlots, and Correlation and Regression.

In the Quartiles section, I got help with this part of the code:

`tumor_vol_data.append(tumor_volume)`

`# Determine outliers using upper and lower bounds`
`quartiles = tumor_volume.quantile([.25,.5,.75])`
`lowerq = quartiles[0.25]`
`upperq = quartiles[0.75]`
`iqr = upperq - lowerq`

`lower_bound = lowerq - (1.5*iqr)`
`upper_bound = upperq + (1.5*iqr)`

 `outliers = tumor_volume.loc[(tumor_volume < lower_bound) | (tumor_volume > upper_bound)]`

 In the Correlation section, I mainly got help with the first part of the code

`correlation = round(st.pearsonr(mouse_weight, capomulin_avg_tumor_volume)[0],2)`

`(slope, intercept, rvalue, pvalue, stderr) = linregress(mouse_weight, capomulin_avg_tumor_volume)`
`regress_values = mouse_weight * slope + intercept`
`line_eq = "y = " + str(round(slope,2)) + "x + " + str(round(intercept,2))`