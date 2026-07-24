---
title: Manage consumer access to replication data in Instance Data Replication
description: Approve a consumer's request to access replication data in Instance Data Replication \(IDR\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/instance-data-replication-idr/approve-consumer.html
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Manage consumer access to replication data in Instance Data Replication

Approve a consumer's request to access replication data in Instance Data Replication \(IDR\).

## Before you begin

Role required: admin, idr\_admin

## About this task

You can review consumer access requests for all of your producer replication sets or for a specific producer replication set. The administrators of consumer sets must apply for access before they can receive the replication data.

## Procedure

1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Consumers Pending Approval**.

2.  Select the option for each consumer replication set that you want to approve.

3.  On the Actions on selected rows list, select **Approve**.

    The approved consumer sets start receiving the replicated data.

    **Note:** You can change the Consumer Approval Status to Denied to prevent the consumer from receiving the replicated data.

4.  Approve a consumer access request for a specific producer replication set.

    1.  On the producer instance, navigate to **Instance Data Replication** &gt; **Producer Replication Sets**.

    2.  Select the producer replication set where you want to approve consumer access.

    3.  Under Related Links, on the **Consumer Subscriptions** tab, select the option for the consumer replication set that you want to approve.

    4.  On the Actions on selected rows list, select **Approve**.

        The approved consumer set starts receiving replicated data.

        **Note:** You can change the Consumer Approval Status to Denied to prevent the consumer from receiving the replicated data.


-   **[Revoke access to replicated data for Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/revoke-consumer-sets.md)**  
Revoke a consumer's access to replicated data if you believe that consumer instance should no longer receive data in Instance Data Replication \(IDR\).
-   **[Restore access to replication data for Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/restore-access.md)**  
Restore Instance Data Replication \(IDR\) access to replicated data by sending a request to the producer replication set admin.

**Parent Topic:**[Administering Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/instance-data-replication-idr/administering-instance-data-replication.md)

**Related topics**  


[Comparing replicated data between instances in Instance Data Replication]()

[Deploying a replication configuration from one instance to another in Instance Data Replication]()

[Cloning options with Instance Data Replication]()

[Monitoring replication status in Instance Data Replication]()

[Monitoring queues in Instance Data Replication]()

[Avoiding insert and update errors in Instance Data Replication]()

[Resolving data replication errors in Instance Data Replication]()

