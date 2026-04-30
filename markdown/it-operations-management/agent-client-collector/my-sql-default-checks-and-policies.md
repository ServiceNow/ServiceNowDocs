---
title: MySQL default checks and policies
description: The Agent Client Collector provides the following default checks and policies for MySQL Metrics monitoring.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# MySQL default checks and policies

The Agent Client Collector provides the following default checks and policies for MySQL Metrics monitoring.

<table id="table_qpq_zv4_tyb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and Usage example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Event

</td><td>

app.mysql.check-mysql-alive

</td><td>

Verifies the length of a result set from a MySQL query.

</td><td>

check-mysql-query-result-count.rb \(options\)-c, --critical COUNT COUNT critical threshold for number of items returned by the query \(required\)

-d, --database DATABASE MySQL database \(required\)

-h, --host HOST MySQL Host to connect to \(required\)

-i, --ini VALUE My.cnf ini file

--ini-section VALUE Section in my.cnf ini file. To enable connection to MySQL thru the .ini file, provide the values against the properties 'user' and 'password' in the **client** section in the .ini file.

-P, --port PORT MySQL Port to connect to

-q, --query QUERY Query to execute \(required\)

-w, --warning COUNT Count warning threshold for number of items returned by the query \(required\)

-S, --socket UNIX socket to connect to \(required if host specified is 'localhost' on UNIX - like systems\)

**Usage Example**

`check-mysql-query-result-count.rb -h 127.0.0.1 -P 3306 -d mysql -q "select * from user" -w 5 -c 8`

</td><td>

MysqlQueryCountCheck OK/CRITICAL/WARNING: message regarding ratio between query length and threshold values

</td></tr><tr><td>

Event

</td><td>

app.mysql.check-mysql-threads

</td><td>

Verifies the MySQL DB number of running threads and assigns a status of OK/WARNING/CRITICAL depending on input values.

</td><td>

check-mysql-threads.rb \(options\)-h, --hostname HOST Hostname to login to

-i, --ini VALUE My.cnf ini file

--ini-section VALUE Section in my.cnf ini file \(Needed if .ini path provided\). To enable connection to MySQL thru the .ini file, provide the values against the properties 'user' and 'password' in the **client** section in the .ini file.

-c, --critnum NUMBER Number of running threads upon which an alert is issued

-w, --warnnum NUMBER Number of running threads upon which a warning is issued

-P, --port PORT MySQL Port to connect to

-S, --socket UNIX socket to connect to \(required if host specified is 'localhost' on UNIX - like systems\)

**Usage Example**

`check-mysql-threads.rb -h 127.0.0.1 -P 3306 -l 0 -m 1 -c 25 -w 20`

</td><td>

CheckMySQLHealth OK/Critical/Warning and number of running threads

</td></tr><tr><td>

Event

</td><td>

util.check-mysql-query

</td><td>

Verifies whether MySQL DB is running.

</td><td>

check-mysql-threads.rb \(options\)-h, --hostname HOST Hostname to login to

-i, --ini VALUE My.cnf ini file

--ini-section VALUE Section in my.cnf ini file \(Needed if .ini path is provided\). To enable connection to MySQL thru the .ini file, provide the values against the properties 'user' and 'password' in the **client** section in the .ini file.

-c, --critnum NUMBER Number of running threads upon which an alert is issued

-w, --warnnum NUMBER Number of running threads upon which a warning is issued

-l, --critlow NUMBER Number of running threads under which an alert is issued

-m, --warnlow NUMBER Number of running threads under which a warning is issued

-P, --port PORT MySQL Port to connect to

-s, --socket UNIX socket to connect to \(required if host specified is 'localhost' on UNIX - like systems\)

**Usage Example**

`check-mysql-threads.rb -h 127.0.0.1 -P 3306 -l 0 -m 1 -c 25 -w 20`

</td><td>

CheckMySQLHealth OK/Critical/Warning and number of running threads

</td></tr></tbody>
</table><table id="table_hnk_5rc_5yb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and Usage Example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

app.mysql.metrics-mysql

</td><td>

Returns metrics on the MySQL DB.

</td><td>

/usr/local/bin/metrics-mysql-graphite.rb \(options\)-h, --host HOST MySQL host to connect to \(required\)

-i, --ini VALUE My.cnf ini file

--ini-section VALUE Section in my.cnf ini file \(Needed if .ini path is provided\). To enable connection to MySQL thru the .ini file, provide the values against the properties 'user' and 'password' in the **client** section in the .ini file.

-P, --port PORT MySQL port to connect to.

-s, --scheme SCHEME Metric naming scheme, text to append to metric

-S, --socket UNIX socket to connect to \(required if host specified is 'localhost' on UNIX - like systems\)

-v, --verbose Show errors \(if generated\) regarding secondary status copies. Add -v to the Command to activate.

**Usage Example**

`check-mysql-threads.rb -h 127.0.0.1 -P 3306 -l 0 -m 1 -c 25 -w 20`

</td><td>

MysqlQueryCountCheck OK/CRITICAL/WARNING: message regarding ratio between query length and threshold values

</td></tr><tr><td>

Metric

</td><td>

app.mysql.check-mysql-threads

</td><td>

Verifies the MySQL DB number of running threads and assigns a status of OK/WARNING/CRITICAL depending on input values.

</td><td>

/usr/local/bin/metrics-mysql-graphite.rb \(options\)-h, --hostname HOST Hostname to connect to \(required\)

-i, --ini VALUE My.cnf ini file

--ini-section VALUE Section in my.cnf ini file \(Needed if .ini path is provided\). To enable connection to MySQL thru the .ini file, provide the values against the properties 'user' and 'password' in the **client** section in the .ini file.

-c, --critnum NUMBER Number of running threads upon which an alert is issued

-w, --warnnum NUMBER Number of running threads upon which a warning is issued

-l, --critlow NUMBER Number of running threads under which an alert is issued

-m, --warnlow NUMBER Number of running threads under which a warning is issued

-P, --port PORT MySQL Port to connect to

-s, --socket UNIX socket to connect to \(required if host specified is 'localhost' on UNIX - like systems\)

**Usage Example**

`metrics-mysql-graphite.rb -h 127.0.0.1 -P 3306`

</td><td>

hostname.mysql.general.abortedClients 7600 1649630975

 hostname.mysql.general.abortedConnects 247 1649630975

 hostname.mysql.general.txBytes 752733902 1649630975

 hostname.mysql.commands.admin\_commands 1631 1649630975

 hostname.mysql.commands.alter\_table 0 1649630975

</td></tr><tr><td>

Metric

</td><td>

app.mysql.metrics-mysql-processes

</td><td>

Returns various metrics regarding MySQL DB processes

</td><td>

/usr/local/bin/metrics-mysql-processes.rb \(options\)

 -h, --host MySQL host to connect to

 -i, --ini VALUE My.cnf ini file

 --ini-section VALUE Section in my.cnf ini file \(Needed if .ini path is provided\). To enable connection to MySQL thru the .ini file, provide the values against the properties 'user' and 'password' in the **client** section in the .ini file.

 -P, --port PORT MySQL Port to connect to

 -s --scheme SCHEME Metric naming scheme, text to append to metric

 -s, --socket UNIX socket to connect to \(required if host specified is 'localhost' on UNIX - like systems\)

 **Usage Example**

 `metrics-mysql-processes.rb -h 127.0.0.1 -P 3306`

</td><td>

processes, commands they're running and the databases they're running the commands on

 **Example:**

 -   hostname.mysql.database.mysql 1 1649631113
-   hostname.mysql.command.Daemon 1 1649631113
-   hostname.mysql.command.Sleep 4 1649631113
-   hostname.mysql.command.Query 1 1649631113

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

