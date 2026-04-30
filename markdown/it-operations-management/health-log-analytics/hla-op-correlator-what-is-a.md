---
title: Using log correlators to detect relationships in log data
description: Log correlators are keys or values in log data that detect correlations between alerts. For example, a log correlator could detect when the interface ID of a particular network device occurs simultaneously in multiple warnings across different service instances.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Using log correlators to detect relationships in log data

Log correlators are keys or values in log data that detect correlations between alerts. For example, a log correlator could detect when the interface ID of a particular network device occurs simultaneously in multiple warnings across different service instances.

## Types of log correlators

Most log lines include a metadata portion plus a message portion. Some log lines, however, include only message text with metadata included in the text.

The two types of log correlators, free text correlators and log property correlators, analyze the different portions of each log to identify relationships between log data from multiple log sources.

**Tip:** If two separate alerts mention the same term in their attributed events, consider specifying that term as a log correlator. For more information, see [Add a log correlator to identify relationships in logs](../task/hla-op-correlator-define.md).

-   **Free text correlators**

    Free text correlators analyze the text within the log message portion of log lines that are associated with an anomaly. The system uses free text correlators to identify correlations between alerts. You use free text correlators to add a term that you expect to appear within log messages. A good choice is a term that is not structured and would not otherwise be extracted as a log property. For example, “policy-id” or “ thread-id”.

    You also typically add free text correlators for the names of systems, applications, and services that are unique to your environment. Because such a value can be referred to by multiple sources, layers, middleware, or databases, the free text correlator can be an effective detector of correlated alerts. For example, if your organization's service is called TeaTime, then you might add "teatime" as a free text correlator. The correlator would identify alerts that are related because they were generated for resources that support the TeaTime service, such as a database lock or a connection failure between TeaTime components.

-   **Log property correlators**

    Log property correlators analyze the metadata portion of log lines. For example, the correlator can analyze the name of a service instance, the interface ID of a network device, or the request ID of a web-facing component. A log property correlator could flag a correlation when the interface ID of a network device simultaneously occurs in multiple warnings in different log sources. Log property correlators are specific to the business context of your environment.


## Specifying the log sources for a log correlator

You can specify the set of log sources whose log data are analyzed by a log correlator. Choices are as follows:

-   **Only new sources**: The system applies the log correlator only to log lines from log sources that were created after this log correlator is activated.
-   **All sources**: The system applies the log correlator to log lines from all log sources.
-   **Specified source**: For a log correlator, the system analyzes only log lines from the log source that you specify.

For instructions for specifying the set of log sources, see [Add a log correlator to identify relationships in logs](../task/hla-op-correlator-define.md).

-   **[Add a log correlator to identify relationships in logs](../task/hla-op-correlator-define.md)**  
Detect related alerts in log data by adding log correlators. The base system includes several log correlators and you can define custom log correlators.
-   **[Exclude a source from a log correlator](../../health-log-analytics-admin/task/hla-correlators-exclude-source.md)**  
Prevent the system from analyzing log lines from a specific source by excluding that source from the log correlator.

**Parent Topic:**[Using Health Log Analytics](../reference/hla-op-guide-binder.md)

