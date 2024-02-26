
# Performance Testing (Restful Booker)

Hello and welcome! This GitHub repository contains the performance testing documentation for restful-booker.herokuapp.com, for a collection of API with various HTTP methods. Here, performance testing is done using Jmeter to determine the maximum load capacity of this collection of API to be called without any errors when a huge number of concurrent threads(users) are made. 

All the test files (jmx, jtl & html files) are included in this repository and the following is a report of all the test procedures and reports.
## Summary

- While executing 1000 concurrent threads(users), a total of 6000 requests are made with error rate 0.00%.

![](https://github.com/SultanaMargia/Performance_Testing/blob/main/Picture/t1000.png)

- While executing 2200 concurrent threads(users), a total of 13200 requests are made with error rate 0.00%.

![](https://github.com/SultanaMargia/Performance_Testing/blob/main/Picture/t2200.png)

- While executing 3000 concurrent threads(users), a total of 18000 requests are made with error rate 0.00%.

![](https://github.com/SultanaMargia/Performance_Testing/blob/main/Picture/t3000.png)

- While executing 4000 concurrent threads(users), a total of 24000 requests are made with error rate 0.00%.

![](https://github.com/SultanaMargia/Performance_Testing/blob/main/Picture/t4000.png)

- While executing 5000 concurrent threads(users), a total of 30000 requests are made with error rate 0.00%.

![](https://github.com/SultanaMargia/Performance_Testing/blob/main/Picture/t5000.png)

- While executing 5500 concurrent threads(users), a total of 33000 requests are made with error rate 0.15%.

![](https://github.com/SultanaMargia/Performance_Testing/blob/main/Picture/t5500.png)
## Collection of API

A set of API for restful-booker.herokuapp.com covering various HTTP methods i.e. POST, GET, DELETE, and PUT are used for test data. Data is set, called, then updated using token and then deleted using token all within this set of API for this test coverage.

![](https://github.com/SultanaMargia/Performance_Testing/blob/main/Picture/thread5000.png)

## Load Testing

For finding the maximum load capacity of restful-booker.herokuapp.com when reqesting a collection of API, Jmeter is used where Thread Groups of huge number of threads(users) are made. For this test, Thread Groups of 5100, 5150 and 5200 threads are found to be suitable data. For all Thread Groups, Ramp-up period is set to 10s with loop count of 1.

![](https://github.com/SultanaMargia/Performance_Testing/blob/main/Picture/thread5000.png)

Using the command-line interface, the following command-line is used for making JTL files where we can see the load testing results in command-line interface.

```bash
  jmeter -n -t report1000.jmx -l report\report1000.jtl
```

![]()

Afterwards using the above JTL files, using the command-line interface the following command-line is used for making HTML reports.

```bash
  jmeter -n -t jmeter -report\report1000.jtl -o report\report1000.html
```

## Conclusion

Therefore from this in-depth performance testing of restful-booker.herokuapp.com for a collection of API using  Thread Groups, it is determined that the maximum load capacity of running the aforementioned collection of APIs without any errors is 5500 concurrent threads and with very minor errors (less than 1%) is 5500 concurrent threads. Using threads any more than this causes significant amount of errors.


