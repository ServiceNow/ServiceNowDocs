---
title: Example system log messages for transactions
description: An example of system log messages for transactions.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Platform performance reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Example system log messages for transactions

An example of system log messages for transactions.

-   At every heartbeat interval, which is one second by default, the Quota Manager prints the running transactions:

    ```
    2012-02-13 12:34:08 (096) glide.quota.manager SYSTEM URL= /incident_list.do?
    sysparm_userpref_module=b55fbec4c0a800090088e83d7ff500de&active=true&sysparm_query=active=true^EQ, 
    THREAD= http-bio-8080-exec-3, FG= true, TYPE= 1, STATE= 2, USER= null, TIME= 8,807, MEM= 0, ATTRIBUTES= {}
    ```

-   Every time the Quota Manager matches a quota to a transaction, it prints a message similar to the following example:

    ```
    2012-02-13 13:25:31 (900) glide.quota.manager SYSTEM QuotaFinder: Assigning quota
    "TEST PROBLEM FORM" with filter: type=form^urlLIKEsys_id=46fb9e31a9fe198101492060c2a4f8cb^EQ to
    transaction: URL= /problem.do?sys_id=46fb9e31a9fe198101492060c2a4f8cb, THREAD= http-bio-8080-exec-1,
    FG= true, TYPE= 1, STATE= 4, USER= null, TIME= 1,121, MEM= 0, ATTRIBUTES= {}
    ```

-   Every time the Quota Manager cancels a transaction, it prints a message similar to the following example:

    ```
    2012-02-13 13:25:33 (930) glide.quota.manager SYSTEM WARNING *** WARNING ***
    Transaction: Cancelling transaction /problem.do (maximum execution time exceeded):
    Thread http-bio-8080-exec-1
    ```


**Parent Topic:**[Platform performance reference](platform-performance-references.md)

