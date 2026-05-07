---
title: Publish a draft Data Manager policy
description: Publish the draft policies to activate them.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure certification policies, Configure EA Workspace using the Setup page, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Publish a draft Data Manager policy

Publish the draft policies to activate them.

## Before you begin

Role required: system admin

## About this task

After importing the legacy certification schedules, you can activate the draft policies by publishing them.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CMDB Workspace**.

2.  Select **Management** in the CMDB Workspace menu bar.

3.  Select the Data Manager link in Management tools, in the Manage section.

4.  Select Policies in the left-side bar in the Data Manager overview page.

5.  Select the Draft policies list view on the Data Manager policies page.

    ![Draft policies in the Data Manager policies page](../../image/eaw-image/cmdb-draft-policies.png)

    The following is the list of Enterprise Architecture Workspace certification policies:

    -   Application Service Software Model Certification On Demand
    -   Business Application Certification On Demand
    -   Business Application Certification Quarterly
    -   Software Product Lifecycle Internal Source Certification on Demand
6.  Select the policy that you want to publish and then, on the policy form, select **Edit Policy**.

    ![Draft policy details](../../image/eaw-image/cmdb-edit-policy.png)

7.  Review any policy settings by selecting the pages to review in the left-side bar.

8.  Select Review in the left-side bar and then select **Publish Policy** to activate the policy.

    ![Publish a draft policy](../../image/eaw-image/cmdb-publish-policy.png)

    The CMDB Data Management Certification Policies \(sn\_cmdb\_ws\_dm\_certification\_policy\) table gets populated with the list of published certification policies.

9.  Run the following scheduled jobs to populate the The CMDB Data Management Task \(cmdb\_data\_management\_task\) table:

    -   Business Application Certification Quarterly Policy Processor
    -   Business Application Certification On Demand Policy Processor
    -   Software Product Lifecycle Internal Source Certification on Demand Policy Processor
    -   Application Service Software Model Certification On Demand Policy Processor

## Result

The Certifications tab in the Needs Attention section fetches and displays the data from the CMDB Data Management Policy \(cmdb\_data\_management\_policy\) table.

**Parent Topic:**[Configure certification policies](../../concept/eaw-concept/eaw-setup-cert-policies.md)

**Related topics**  


[Import certification schedules in to Data Manager](eaw-convert-cert-schedules-to-cert-policies.md)

[Add or edit a certification policy](eaw-manage-cert-schedules.md)

[View all certification policies](eaw-view-all-cert-schedules.md)

