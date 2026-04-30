---
title: Security data filter performance analysis tool
description: The security data filter performance analysis tool identifies performance bottlenecks introduced by a security data filter.
locale: en-US
release: yokohama
product: Data Filtration
classification: data-filtration
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 2
breadcrumb: [Security data filters, Access Management]
---

# Security data filter performance analysis tool

The security data filter performance analysis tool identifies performance bottlenecks introduced by a security data filter.

## Before you begin

Role required: security\_admin

## About this task

The performance analysis tool provides feedback on performance impact of a security data filter. It analyzes the query execution when the specified data filter is applied to the table, alongside any encoded query provided for analysis. This identifies potential performance bottlenecks introduced by the new data filter, enabling informed decision-making to balance security requirements with optimal query performance.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Set the property `glide.security.data_filter.diagnostic_enabled` to **true**.

    If the property does not exist in the System Properties table, read [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) and add the property manually.

3.  Navigate to **All** &gt; **System Security** &gt; **Security Data Filters**.

4.  Select a security data filter to analyze.

5.  Select **Analyze Performance** under **Related Links**.![Analyze performance related link](../image/secdf-analyzeperflink.svg)

6.  In the form, fill in the fields as needed.![Data filter example](../image/secdf-analyzeperfconfig.svg)

<table id="table_o2q_yyz_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Filter

</td><td>

The selected data filter for analysis

</td></tr><tr><td>

Related active data filters

</td><td>

The number of currently active data filters that may impact performance. Select the information icon \(![information icon](../../security-center/images/info-icon.png)\) to view the active data filters.

</td></tr><tr><td>

Table

</td><td>

The selected table for analysis.

</td></tr><tr><td>

Encoded query

</td><td>

The query for analysis.

</td></tr><tr><td>

Query runs

</td><td>

The number of times to sample the query performance.**Note:** Must be between 10-100.

</td></tr></tbody>
</table>7.  Select **Analyze query performance**.


## Result

The **Performance Summary** section compares the execution of the query times with and without the selected data filter applied. It captures various metrics including **Max, Min, Mean,** and **Median** query execution times and provides a comprehensive analysis of the filter's impact on performance.![Performance summary](../image/secdf-analyzeresult.svg)

The performance impact indicator provides high level guidance to filter performance. The indicator results are calculated from the median change in query execution time. The query execution time often correlates to the complexity of both the filter and user query. See the [security-data-filters.md\#section\_fyq\_jkd\_p2c](security-data-filters.md#section_fyq_jkd_p2c) for more information on security data filter performance.

|Indicator|Message|Explanation|
|---------|-------|-----------|
|**Low**|This data filter doesn't slow down queries or page load times.|The percentage change in the median query execution time is 0% \(no change\).|
|**Medium**|This data filter can slow down existing queries and make pages take longer to load.|The percentage change in the median query execution time is greater than 0% and up to 100%.|
|**Critical**|This data filter takes longer to run. This slows down existing queries and makes pages take longer to load.|The percentage change in the median query execution time is greater than 100%.|

