### Data for replication

---
The keywords used for collecting the issue reports are:
```
speedup, overhead, long time, lock, expensive, performance issue, performance issues, performance test, performance tests, performance regressed, performance regression, performance problem, performance problems,  response time, Performance improvements, perf, slow, hang, latency, throughput, expensive, costly, inefficient, laggy, freeze, unresponsive, stall, delays, sustained, overheads, performance regression,  performance problems, Degraded performance, performance degradation, optimize, speed up, performance improvements, performance improvement, delays, sluggish
```

There are two project folders in this package, `cassandra` and `hadoop`. Each project folder contains 2 sub-folders, `RQ1` and `RQ3`.

#### cassandra folder
- `RQ1` contians the files for the first research question:
    - `raw-data-cassandra-final.json` is the folder of all the performance data collected during the tests running. It is in json format, and the keys are `performance metrics(cpu, memory, etc.)`, `the performance bug fixing commit ID`, `its parent commit ID` and the `tests`.
    - `cassandra-labeling.csv` is the manual labeling of the perferformance issue. The first column is the `issue ID`, the left columns is the labels of the performance metrics changes,  `1` means that there should be performance improvement. Here, we only care about the improvenments.
    - `commits_issue_cassandra.json`, is the json file that contains the performance issue fixing commit and the issue id.
    - `commits_parent_cassandra.json` is the json file that contians the performance issue fixing commit and its parent commit.
    - `impacted-tests-lines-final.json` is the json file of the impacted test, the keys are `performance issue fixing commit`, `its parent commit` and the test, the values are arrays, the first index is whether it is a impacted test, `1` means it is an impacted test.
    - `lines-changed.json` is the file that contains the code changes information during the commit, the keys are `performance issue fixing commit`, `its parent commit` and `the name of changed file`, the values are the the line numbers that are changed in in this file.
    - `analysis-cassandra-rank-no-outliers-final.json` is the file of the Mann–Whitney U test result. Its format is `performance issue fixing commit`, `its parent commit`, `performance metrics`, the values are a list, here, we conly care about the last two columns. If the 4th column is `True`, it means that there is an improvement, the 5th column is the effect size.
- `RQ3` contians the files for the third research question: it contains 5 csv files, which are the metrics extracted from different categories. The last column is the labels `1` and `0`.


#### hadoop folder
- `RQ1` contians the files for the first research question:
    - `raw-data-final.json` is the folder of all the performance data collected during the tests running. It is in json format, and the keys are `performance metrics(cpu, memory, etc.)`, `the performance bug fixing commit ID`, `its parent commit ID` and the `tests`.
    - `hadoop-labeling.csv` is the manual labeling of the perferformance issue. The first column is the `issue ID`, the left columns is the labels of the performance metrics changes,  `1` means that there should be performance improvement. Here, we only care about the improvenments.
    - `commits_issue_hadoop_all.json`, is the json file that contains the performance issue fixing commit and the issue id.
    - `commits_parent_hadoop_all.json` is the json file that contians the performance issue fixing commit and its parent commit.
    - `impacted-tests-lines-final.json` is the json file of the impacted test, the keys are `performance issue fixing commit`, `its parent commit` and the test, the values are arrays, the first index is whether it is a impacted test, `1` means it is an impacted test.
    - `lines-changed.json` is the file that contains the code changes information during the commit, the keys are `performance issue fixing commit`, `its parent commit` and `the name of changed file`, the values are the the line numbers that are changed in in this file.
    - `analysis-hadoop-rank-final.json` is the file of the Mann–Whitney U test result. Its format is `performance issue fixing commit`, `its parent commit`, `performance metrics`, the values are a list, here, we conly care about the last two columns. If the 4th column is `True`, it means that there is an improvement, the 5th column is the effect size.
- `RQ3` contians the files for the third research question: it contains 5 csv files, which are the metrics extracted from different categories. The last column is the labels `1` and `0`.