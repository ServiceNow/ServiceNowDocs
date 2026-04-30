---
title: RCA approvals for Now Assist for HR Service Delivery \(HRSD\)
description: After you install Now Assist for HR Service Delivery \(HRSD\), you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# RCA approvals for Now Assist for HR Service Delivery \(HRSD\)

After you install Now Assist for HR Service Delivery \(HRSD\), you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request.

## Before you begin

-   Role required: admin
-   The RCAs that are generated after the installation are in the **Requested** state and you must manually mark the RCAs as **Allowed**, which can be time-consuming.

    To automate the RCA approvals for any record, you can run the **Now Assist for HRSD Bulk RCA approval** script where the source scope is Now Assist for HR Service Delivery \(HRSD\). Download the **Now Assist for HRSD Bulk RCA approval** file from the **Supporting Links and Docs** section in Now Assist for HR Service Delivery \(HRSD\) application in ServiceNow Store. This file is a standalone script to reduce the manual effort involved. After you download the script file, perform the following steps:


## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Right-click the header and choose **Import XML**.

3.  Click **Choose file** and select the XML file that you downloaded.

4.  Search and find the **Now Assist for HRSD Bulk RCA approval** script record.

5.  Click **Run Script** to allow all the requested RCAs.


**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

**Related topics**  


[Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)](../concept/now-assist-hrsd-skill-inputs.md)

[Restrict Now Assist capabilities for employee relations cases](restrict-now-assist-skills-er-cases.md)

[Configure resolution notes generation for Now Assist for HRSD](resolution-notes-nacm-config.md)

[Configure sensitivity detection](config-na-sd-filters.md)

[Configure Gen AI Virtual Agent for HRSD](use-genai-ec.md)

[Configure the Now Assist for HRSD Virtual Agent topics](config-va-topics.md)

[Configure HCM agents for HR Service Delivery AI Agent Collection](configure-hcm-agents.md)

[Configure Now Assist AI Helper – Galileo Inside](configuring-galileo-inside.md)

