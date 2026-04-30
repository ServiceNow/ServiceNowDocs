---
title: Supported SQL functions
description: Common SQL functions used in SQL API for querying and analyzing incident data.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-10"
reading_time_minutes: 4
breadcrumb: [Explore, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Supported SQL functions

Common SQL functions used in SQL API for querying and analyzing incident data.

ServiceNow supports a variety of SQL functions for querying and analyzing data in tables such as the incident table. This abbreviated list covers common SQL functions organized by category, with sample use cases and queries focused on incident management scenarios.

**Note:** The query engine only supports INNER and LEFT OUTER joins currently.

|Category|Function Name|Sample Use Case|Sample Query|
|--------|-------------|---------------|------------|
|Aggregate Fn|AVG|Calculate average priority level of resolved incidents to measure severity trends|SELECT AVG\(CAST\(priority AS FLOAT\)\) AS avg\_priority\_level FROM incident WHERE state = 7;|
|Aggregate Fn|COUNT|Count total open incidents by priority level|SELECT priority, COUNT \(\*\) AS incident\_count FROM incident WHERE state IN \(1,2,3\) GROUP BY priority;|
|Aggregate Fn|SUM|Calculate total number of updates across all P1 incidents|SELECT SUM\(sys\_mod\_count\) AS total\_updates FROM incident WHERE priority = 1;|
|Aggregate Fn|MAX|Find the highest priority value in open incidents|SELECT MAX\(priority\) AS highest\_priority FROM incident WHERE state IN \(1,2,3\);|
|Clauses|CASE|Categorize incidents by priority for dashboard visualization|SELECT number, CASE WHEN priority = 1 THEN 'Critical' WHEN priority = 2 THEN 'High' WHEN priority = 3 THEN 'Medium' ELSE 'Low' END AS priority\_label FROM incident WHERE state IN \(1,2,3\);|
|Clauses|TOP|Identify top 10 most modified incidents for quality review|SELECT TOP 10 number, sys\_mod\_count FROM incident ORDER BY sys\_mod\_count DESC;|
|Clauses|GROUP BY|Analyze incident volume by category for trending|SELECT category, COUNT\(\*\) AS count FROM incident WHERE state IN \(1,2,3\) GROUP BY category;|
|Clauses|HAVING|Find assignment groups with more than 50 open incidents for capacity planning|SELECT assignment\_group , COUNT\(\*\) AS open\_count FROM incident WHERE state IN \(1,2,3\) GROUP BY assignment\_group HAVING COUNT\(\*\) &gt; 50;|
|Clauses|LEFT JOIN|List incidents with assigned user details for team performance report|SELECT i.number, i.priority, u.name AS assigned\_to, u.department FROM incident i LEFT JOIN sys\_user u ON i.assigned\_to = u.sys\_id WHERE i.state IN \(1,2,3\);|
|Clauses|ORDER BY ASC|Retrieve oldest incidents by opened date for escalation review|SELECT number, short\_description, opened\_at FROM incident WHERE state IN \(1,2,3\) ORDER BY opened\_at ASC;|
|Clauses|DISTINCT|Get unique list of categories from recent incidents|SELECT DISTINCT category FROM incident WHERE state IN \(1,2,3\);|
|Clauses|SUBQUERY \(FROM\)|Calculate average incident count per user from active assignments|SELECT AVG\(incident\_count\) AS avg\_per\_user FROM \(SELECT assigned\_to, COUNT\(\*\) AS incident\_count FROM incident WHERE assigned\_to IS NOT NULL GROUP BY assigned\_to\) AS user\_stats;|
|Clauses|SUBQUERY \(WHERE\)|Find incidents assigned to active IT Support users|SELECT number, short\_description, assigned\_to FROM incident WHERE assigned\_to IN \(SELECT sys\_id FROM sys\_user WHERE department = 'IT Support' AND active = 1\) AND state IN \(1,2,3\);|
|Clauses|UNION|Combine high priority and unassigned incidents for urgent action list|SELECT number, 'P1-Critical' AS reason, assigned\_to, priority, state FROM incident WHERE priority = 1 AND state IN \(1,2,3\) UNION SELECT number, 'Unassigned' AS reason, assigned\_to, priority, state FROM incident WHERE assigned\_to IS NULL AND state IN \(1,2,3\);|
|DateTime FN|date\_part|Analyze incident creation patterns by year for historical trending|SELECT date\_part\('year', opened\_at\) AS year, COUNT\(\*\) AS incidents FROM incident GROUP BY date\_part\('year', opened\_at\) ORDER BY date\_part\('year', opened\_at\);|
|DateTime FN|date\_trunc|Group incidents by month for executive monthly trend report|SELECT date\_trunc\('month', opened\_at\) AS month, COUNT\(\*\) AS total FROM incident GROUP BY month ORDER BY month;|
|Numeric FN|ABS|Calculate absolute difference between priority values for normalization|SELECT number, ABS\(priority - 3\) AS priority\_deviation FROM incident WHERE state IN \(1,2,3\);|
|Numeric FN|CEILING|Round up priority division for weighted scoring calculations|SELECT number, priority, CEILING\(CAST\(sys\_mod\_count AS FLOAT\) / 3\) AS update\_score FROM incident WHERE state IN \(1,2,3\);|
|Numeric FN|FLOOR|Calculate floored average of modification counts for baseline metrics|SELECT assignment\_group, FLOOR\(AVG\(CAST\(sys\_mod\_count AS FLOAT\)\)\) AS avg\_updates FROM incident GROUP BY assignment\_group;|
|Operators|IN|Filter incidents for business-critical categories for executive dashboard|SELECT number, category, priority, state FROM incident WHERE category IN \('Network', 'Database', 'Security', 'Application'\);|
|Operators|IS NOT NULL|Find incidents with configuration item assignments for CMDB analysis|SELECT number, cmdb\_ci, category, assignment\_group FROM incident WHERE cmdb\_ci IS NOT NULL;|
|Operators|LIKE|Search for password reset and access-related incidents for self-service analysis|SELECT number, short\_description, caller\_id FROM incident WHERE short\_description LIKE '%password%' OR short\_description LIKE '%login%';|
|Operators|NOT BETWEEN|Identify incidents with unusual priority values for data quality audit|SELECT number, priority, short\_description FROM incident WHERE priority NOT BETWEEN 2 AND 4;|
|ServiceNow Specific FN|DV|Display human-readable reference field values in reports|SELECT number, DV\(assignment\_group\) AS group\_name, DV\(assigned\_to\) AS assignee\_name FROM incident WHERE state IN \(1,2,3\);|
|String FN|CONCAT\_WS|Create formatted incident summaries for external ticketing systems|SELECT concat\_ws\(' - ', number, category, short\_description\) AS formatted\_summary FROM incident WHERE state = 7;|
|String FN|LOWER|Standardize category names for case-insensitive grouping and analysis|SELECT LOWER\(category\) AS category\_normalized FROM incident;|
|String FN|REPLACE|Transform incident numbers for external system integration|SELECT REPLACE\(number, 'INC', 'TICKET-'\) AS external\_id, short\_description FROM incident WHERE state = 7;|
|String FN|SUBSTR|Extract incident prefix for categorization and reporting|SELECT number, SUBSTR\(number, 1, 3\) AS prefix, SUBSTR\(number, 4, 20\) AS sequence FROM incident;|
|String FN|TRIM|Clean white space from descriptions for data quality improvement|SELECT number, TRIM\(short\_description\) AS clean\_description FROM incident WHERE short\_description IS NOT NULL;|
|Windows FN|RANK\(\)|Rank incidents by number of updates to identify most frequently modified tickets|SELECT number, sys\_mod\_count, assignment\_group, RANK\(\) OVER \(ORDER BY sys\_mod\_count DESC\) AS modification\_rank FROM incident WHERE assignment\_group IS NOT NULL;|

**Parent Topic:**[Getting started with ServiceNow SQL API](../concept/getting-started-with-servicenow-sql-api.md)

