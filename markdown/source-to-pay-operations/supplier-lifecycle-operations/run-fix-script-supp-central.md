---
title: Run the fix script to enable access to Supplier Collaboration Portal
description: After you install the Supplier Collaboration Portal, you must run the fix script to enable access to the portal.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enable access to Supplier Collaboration Portal, Post-upgrade tasks, Install Supplier Collaboration Portal, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run the fix script to enable access to Supplier Collaboration Portal

After you install the Supplier Collaboration Portal, you must run the fix script to enable access to the portal.

## Before you begin

Role required: admin

## About this task

Download the `SCP_Contact_User_Access.xml` file from the ServiceNow Store.![Location of the XML file fix script to enable access to the portal.](../image/xml-scp-access.png)

After you download the script file, perform the following steps.

## Procedure

1.  Navigate to **System Definition** &gt; **Fix Scripts**.

    Ensure that the application scope is set to **Global**.

2.  Right-click the Name column and select **Import XML**.

3.  Select **Choose file** and select the XML file that you downloaded.

4.  Select **Upload**.

5.  Search for and select the `Add Supplier Roles` script record to open it.

6.  Select **Run Fix Script**.

    You can now access the Supplier Collaboration Portal.


**Parent Topic:**[Enable access to Supplier Collaboration Portal](enable-access-supp-central.md)

**Related topics**  


[Enable access to Supplier Collaboration Portal](enable-access-supp-central.md)

