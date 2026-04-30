---
title: Correlation
description: Establish a synchronization relationship between records that reside on separate instances.
locale: en-US
release: yokohama
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub Remote Process Sync, Data and Automation]
---

# Correlation

Establish a synchronization relationship between records that reside on separate instances.

A correlation identifies record data from a remote instance you want to use on a local instance. An integration can use data from a correlated remote record to update a local record. Typically, integrations correlate records to synchronize them and ensure that record changes propagate across instances.

There are two types of correlation available.

-   Classic correlation field
-   Integration Hub Correlation records

## Classic correlation field

Prior to Integration Hub Remote Process Sync, you could only create correlations with a limited set of record types that had a Correlation ID field. By default, the Correlation ID field is only available to Configuration Item, Service, and Task records. The Correlation ID field stores the globally unique ID of a matching remote record. The Correlation ID identifies the remote record whose data values should be used to update the local record. For example, suppose incident record INC100001 correlates to problem record PRB123456 on a remote instance. Whenever changes are made to fields in remote problem PRB123456, the system uses the Correlation ID to identify that local incident INC100001 receives the same field updates.

A classic correlation creates a one-to-one relationship between a record on the local system and a record on a remote system. One local record can only ever correlate to one remote record. The correlation provides no information about the remote system nor the current state of the correlation. Administrators manually manage classic correlations from the records being updated.

![A classic correlation between Incident record INC100001 and Problem record PRB123456.](../images/correlation-classic-example.png "Sample classic correlation field")

## Integration Hub Correlation records

Integration Hub Remote Process Sync extends the functionality of classic correlation with the introduction of dedicated Correlation \[ih\_sync\_correlation\] records.

A Correlation record contains these fields.

-   **Local Correlation ID**

    The globally unique ID that identifies the correlation on the local system. By default, Integration Hub Remote Process Sync generates a unique sys\_id value for this field. The distinct sys\_id acts as an alias which prevents the correlation from breaking due to changes in the local record. When Integration Hub Remote Process Sync sends this ID value to a remote system, the receiving instance uses it as the Remote Correlation ID.

-   **Remote Correlation ID**

    The globally unique ID that identifies the correlation on the remote system. By default, Integration Hub Remote Process Sync generates a unique sys\_id value for this field. The distinct sys\_id acts as an alias which prevents the correlation from breaking due to changes in the remote record. When Integration Hub Remote Process Sync sends this ID value to a remote system, the receiving instance uses it as the Local Correlation ID.

-   **Local Table**

    The table where the correlation creates or updates records. An Integration Hub Remote Process Sync capture definition monitors this table for record changes. Integration Hub Remote Process Sync uses this field to find correlations by table name.

-   **Local Record**

    The record created or updated by a correlation. This field stores the same value as the Correlation ID field from a classic correlation. When other business logic makes changes to this record, the changes do not overwrite the correlation.

-   **Remote System**

    The remote instance where Integration Hub Remote Process Sync sends and receives record changes. Each correlation record can only refer to one remote instance. To correlate the same local record to multiple remote systems simultaneously, you can create multiple correlation records.

-   **State**

    The synchronization state of the correlation. Active correlations receive additions and updates. Inactive correlations do not produce additions or updates, but can be queried for auditing purposes and reactivated as needed.


**Danger**

Integration Hub Remote Process Sync manages correlation records for you. Directly editing correlation records may prevent synchronization of records, and may result in data loss.

![](../images/correlation-record-example.png "Sample Integration Hub Correlation record")

Correlation records offer several advantages over a single correlation field.

-   Allow management of correlations by Remote Process Sync
-   Identify the remote system associated with a correlation
-   Provide separate Correlation ID values for the local and remote systems
-   Allow correlation of a single local record with multiple remote systems
-   Allow correlations to be deactivated and reactivated as needed
-   Allow Correlation ID values to be distinct from the sys\_id of a remote record

