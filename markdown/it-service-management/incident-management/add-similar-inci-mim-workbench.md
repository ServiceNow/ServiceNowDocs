---
title: Add similar incidents from major incident workbench
description: Add similar incidents to a major incident so that the support teams can work on the parent record for a coordinated response process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-management/add-similar-inci-mim-workbench.html
release: zurich
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Major incident workbench, Manage major incidents, Incident Management, IT Service Management]
---

# Add similar incidents from major incident workbench

Add similar incidents to a major incident so that the support teams can work on the parent record for a coordinated response process.

## Before you begin

Role required: itil, major\_incident\_manager, communication\_manager, incident\_manager, or admin

-   Activate the Predictive Intelligence plugin \(com.glide.platform\_ml\).
    -   Configure Predictive Intelligence and train the solution definition with the name **ml\_sn\_global\_similar\_incidents\_mim**. For more information on how to train a solution definition, refer to [Create and train a similarity solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intelligence/create-similarity-solution.md).
-   Ensure that there is an active ML solution at **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions** with the solution name **ml\_sn\_global\_similar\_incidents\_mim**.

## Procedure

1.  Navigate to [Major incident workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/major-incident-workbench.md).

2.  Select the **Summary** tab.

3.  In the Child Incidents section, select \[Omitted image "mim-ellipses.png"\] Alt text: MIM ellipses and then select **Find Similar**.

4.  From the Add Similar Incidents dialog box, select the similar incidents that you want to relate to the major incident and then select **Add Selected**.

    The similar child incidents appear under the Child Incidents section.


**Parent Topic:**[Major incident workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/major-incident-workbench.md)

