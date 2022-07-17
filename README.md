# Challenge_14

Step 1: Tune the training algorithm by adjusting the size of the training dataset.¶
To do so, slice your data into different periods. Rerun the notebook with the updated parameters, and record the results in your README.md file.

Answer the following question: What impact resulted from increasing or decreasing the training window?

Step 2: Tune the trading algorithm by adjusting the SMA input features.
Adjust one or both of the windows for the algorithm. Rerun the notebook with the updated parameters, and record the results in your README.md file.

Answer the following question: What impact resulted from increasing or decreasing either or both of the SMA windows?

Step 3: Choose the set of parameters that best improved the trading algorithm returns.
Save a PNG image of the cumulative product of the actual returns vs. the strategy returns, and document your conclusion in your README.md file.

DEFAULT: (months = 3)
	Predicted	Actual Returns	Strategy Returns
date			
2015-07-06 10:00:00	1.0	-0.025715	-0.025715
2015-07-06 10:45:00	1.0	0.007237	0.007237
2015-07-06 14:15:00	1.0	-0.009721	-0.009721
2015-07-06 14:30:00	1.0	-0.003841	-0.003841
2015-07-07 11:30:00	1.0	-0.018423	-0.018423
Predicted	Actual Returns	Strategy Returns
date			
2021-01-22 09:30:00	1.0	-0.006866	-0.006866
2021-01-22 11:30:00	1.0	0.002405	0.002405
2021-01-22 13:45:00	1.0	0.002099	0.002099
2021-01-22 14:30:00	1.0	0.001496	0.001496
2021-01-22 15:45:00	1.0	-0.000896	-0.000896

1a. With a shorter window, the strategy returns consistently outpace the actual returns. 

output (months = 1)

Predicted	Actual Returns	Strategy Returns
date			
2015-05-04 10:30:00	1.0	0.012830	0.012830
2015-05-04 11:15:00	1.0	0.000000	0.000000
2015-05-04 14:15:00	1.0	0.003071	0.003071
2015-05-06 10:45:00	-1.0	-0.021049	0.021049
2015-05-06 11:15:00	1.0	-0.001173	-0.001173
Predicted	Actual Returns	Strategy Returns
date			
2021-01-22 09:30:00	1.0	-0.006866	-0.006866
2021-01-22 11:30:00	1.0	0.002405	0.002405
2021-01-22 13:45:00	1.0	0.002099	0.002099
2021-01-22 14:30:00	1.0	0.001496	0.001496
2021-01-22 15:45:00	1.0	-0.000896	-0.000896

output (months = 9)

1b. With a longer window, the variability increased considerably. At times, the strategy underperforms whilst outperforming the actual returns during others. 

output (months = 9) 

Predicted	Actual Returns	Strategy Returns
date			
2016-01-04 09:30:00	-1.0	-0.041851	0.041851
2016-01-04 10:15:00	-1.0	0.003083	-0.003083
2016-01-04 10:30:00	-1.0	-0.003586	0.003586
2016-01-04 11:00:00	-1.0	-0.002057	0.002057
2016-01-04 11:45:00	-1.0	0.001546	-0.001546
Predicted	Actual Returns	Strategy Returns
date			
2021-01-22 09:30:00	1.0	-0.006866	-0.006866
2021-01-22 11:30:00	1.0	0.002405	0.002405
2021-01-22 13:45:00	1.0	0.002099	0.002099
2021-01-22 14:30:00	1.0	0.001496	0.001496
2021-01-22 15:45:00	1.0	-0.000896	-0.000896



2. Default (short = 4, long = 100)
	Predicted	Actual Returns	Strategy Returns
date			
2015-07-06 10:00:00	1.0	-0.025715	-0.025715
2015-07-06 10:45:00	1.0	0.007237	0.007237
2015-07-06 14:15:00	1.0	-0.009721	-0.009721
2015-07-06 14:30:00	1.0	-0.003841	-0.003841
2015-07-07 11:30:00	1.0	-0.018423	-0.018423
Predicted	Actual Returns	Strategy Returns
date			
2021-01-22 09:30:00	1.0	-0.006866	-0.006866
2021-01-22 11:30:00	1.0	0.002405	0.002405
2021-01-22 13:45:00	1.0	0.002099	0.002099
2021-01-22 14:30:00	1.0	0.001496	0.001496
2021-01-22 15:45:00	1.0	-0.000896	-0.000896

(short = 8, long = 200)

Predicted	Actual Returns	Strategy Returns
date			
2015-09-14 10:30:00	1.0	-0.003279	-0.003279
2015-09-14 11:00:00	1.0	-0.000470	-0.000470
2015-09-14 13:15:00	1.0	-0.002821	-0.002821
2015-09-14 13:45:00	1.0	0.002357	0.002357
2015-09-14 15:45:00	1.0	-0.001881	-0.001881
Predicted	Actual Returns	Strategy Returns
date			
2021-01-22 09:30:00	1.0	-0.006866	-0.006866
2021-01-22 11:30:00	1.0	0.002405	0.002405
2021-01-22 13:45:00	1.0	0.002099	0.002099
2021-01-22 14:30:00	1.0	0.001496	0.001496
2021-01-22 15:45:00	1.0	-0.000896	-0.000896

When we increase both windows, the strategy underperforms and is consistently below the actual values. 

![bokeh plot](https://github.com/dcha314/Challenge_14/blob/main/bokeh_plot.jpg)
