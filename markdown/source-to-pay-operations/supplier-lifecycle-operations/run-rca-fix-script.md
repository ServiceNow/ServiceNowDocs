---
title: Run the fix script for RCA approvals
description: After you install the Supplier Collaboration Portal application from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Restricted caller access approvals, Install Supplier Collaboration Portal, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run the fix script for RCA approvals

After you install the Supplier Collaboration Portal application from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.

## Before you begin

Role required: admin

## About this task

The RCAs that are generated after the installation are in the **Requested** state and you must manually mark the RCAs as **Allowed**, which can be time-consuming.

To automate the RCA approvals for any record, you can run the **SCP\_BULK\_RCAs\_Approval.xml** script where the source scope is Supplier Collaboration Portal.

Download the **SCP\_BULK\_RCAs\_Approval.xml** file from the [ServiceNow Store](https://store.servicenow.com/store/frame/app?pp=1a96d3851bab6010593876a61a4bcb01).

**Note:** This file is a standalone script to reduce the manual effort involved.

After you download the script file, perform the following steps.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Right-click the Name column and choose **Import XML**.

3.  Select **Choose file** and select the **SCP\_BULK\_RCAs\_Approval.xml** file that you downloaded.

4.  Select **Upload**.

5.  Search for and select the `SCP_BULK_RCAs_Approval` script record to open it.

6.  Select **Run Fix Script** to approve all the requested RCAs.

    RCA fix script can approve the RCAs which exist at the time of execution. After running the RCA script, if you install any new plugins, rerun the RCA script to approve the new RCAs.


**Parent Topic:**[Restricted caller access approvals for Supplier Collaboration Portal](../concept/rca-approvals.md)

**Related topics**  


[Approve restricted caller access privileges manually](approve-rca-for-supp-central.md)

[Approve restricted caller access privileges manually](approve-rca-for-supp-central.md)

