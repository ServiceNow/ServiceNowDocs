---
title: Run fix-script for RCA approvals
description: After you install or upgrade to the latest Employee Experience applications from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Post installation troubleshooting, Admin configurations, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Run fix-script for RCA approvals

After you install or upgrade to the latest Employee Experience applications from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.

## Before you begin

Role required: admin

## About this task

Install the following Employee Experience applications and subscriptions.

-   Employee Center Core
-   Employee Center
-   Employee Center Pro
-   Content Experiences
-   Content Publishing

The RCAs that are generated after the installation are in the **Requested** state and you must manually mark the RCAs as **Allowed**, which can be time-consuming.

To automate the RCA approvals for any record, you can run the **EC bulk RCAs approval** script where the source scope is one of the given Employee Experience applications.

Download the following **EC bulk RCAs approval** file from the ServiceNow Store.![EC bulk RCAs approval script file on ServiceNow store](../images/rca-script-store.jpg)

**Note:** This file is a standalone script to reduce the manual effort involved.

After you download the script file, perform the following steps.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Right-click the header and choose **Import XML**.

3.  Click **Choose file** and select the XML file that you downloaded.

4.  Search and find the **EC bulk RCAs approval** script record.

5.  Click **Run Script** to allow all the requested RCAs.


**Parent Topic:**[Post installation troubleshooting](../concept/post-install-steps.md)

**Related topics**  


[Run fix scripts to update Employee Center](run_scripts_manually_config-search.md)

