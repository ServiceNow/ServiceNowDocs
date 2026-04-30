---
title: Certification tasks
description: A certification task represents the work of verifying the data associated with a particular record.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Certification tasks

A certification task represents the work of verifying the data associated with a particular record.

Task owners are responsible for performing the certification tasks. Tasks have an associated workflow that sends reminders to the task owner and, if necessary, the manager of the owner at regular intervals.

![Viewing a certification task to verify data](../image/CertificationTask.png "Certification task")

**Note:** If the message

```
Record cannot be certified until the instance is finished creating all certification tasks and elements. Reload the page to try again
```

appears, it signifies that:

-   A large amount of data is present in the cmbd\_ci and cmdb\_ci\_server tables.
-   Data certification task processing is not complete \(Data Certification jobs are still in process\).

As directed, reload the page and wait for the processing to complete.

## Clean up invalid elements

Use the **Clean up invalid elements** UI action to query and delete certification elements that reference invalid records. Each certification task has a certification schedule, and each certification schedule has Table and Filter fields. When you use this UI action, it performs the following processing:

1.  Collects all available records from Table field in the certification schedule with filters that are available in certification schedule.
2.  Collects all certification elements associated with the current certification task.
3.  Deletes the certification elements that are no longer available for the data collected in the previous step.
4.  After deleting invalid records, it recomputes the certification completion percentage using the following formula:

    \(1 - \(number of certification elements pending / total no of certification elements associated\)\) \* 100;\)

5.  If there are no certification elements with a Pending status, it marks the associated certification task as Closed, and deactivates it.
6.  If there are remaining certification elements with a Pending status, it activates the associated certification task and changes its status to Work in Progress.

