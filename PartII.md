# Data Challenge Part 2

Final Answer:

1. I think the most logical thing would be to track the number of times a driver picked up in one city versus another on a daily basis (or some other time unit --  maybe weekly basis?) That is the ratio of the absolute value of the difference to the toral rate:

 (|pickup_rate(Gotham) - pickup_rate(Ultimate Metropolis)|)/(pickup_rate(Gotham) + pickup_rate(Ultimate Metropolis)) for each driver.

When the driver is only picking up in one city the metric will be 1.
When the driver is picking up equally in both cities the metric will be 0.

If reimbursed tolls are encouraging a driver that typically drives in once city to start picking up in another, then we should see our metric decrease from 1 to a smaller value. So this metric could be used as a statistic which is what we will talk about next.

2. a) and b) 

Do a two-sample t-test. Collect data and calculate metric for each driver for a reasonable period of time with the tolls as they are. Then, start reimbursing the tools. Then for an equal period of time get the rates of pick up in each city and calculate the metric for each driver.

Now we have two populations. One before the toll was reimbursed and one after. We can do a one-sided two-sample t-test to figure out whether the mean of our metric is significantly lower (in a statistical sense) after the tolls were reimbursed than before. We set the statistical significance threshold for the t-test at p < 0.5. If the p-value meets this criterion: then we claim that averaged over the drivers, the difference in the pickup rate in Gotham vs. Ultimate Metropolis has moved closer to parity. Which is what we wanted.

c)
If there is a statistically significant difference in the mean of our metric between the two populations, I would advise the Ultimate managers to weigh the cost of reimbursing tolls with the increased revenue from drivers being equispread across the two cities and that if that checks out to start reimbursing the toll.






