# Getsafe Analytics Engineer Case Study

**I. Monthly Closing**

1. Please write a dbt model (or models) that generates a data mart from the dataset
provided with the following columns:
a. party
b. month
c. premium
2. Describe a process to compare the finance results with the accounting closing
information and generate a report on any discrepancies.
3. Are there discrepancies between the two sources? If there are, please discuss what
could be potential solutions.

**II. KPI calculation**

1. Number of active customers per day and product group in a given date range.
For example, if a customer starts on Jan 1st and churns on March 31st, the
customer is considered active between Jan 1st and March 31st, and is not
considered active outside of that period.
2. Premium collected from active customers in a given date range. If the customer
starts on Jan 1st and churns on March 31st, we will collect the premium between
Jan 1st and March 31st only.
3. Accumulated acquired premium from the beginning of time until a given date.

**Assumptions:**
  - The data mart produced should allow generating the metrics in the BI tool with
  minimal aggregations. The only aggregations to be done in the BI tool are the
  operations sum and count.
  - The input dataset can become very big, so, consider scalability and flexibility in the
  date ranges.
  - There are processes that can change data retroactively. For example, we might allow
  a customer to cancel his contract effectively in the past, and we will refund the money
  they paid. That means that a value that was reported in the past can be different now.
