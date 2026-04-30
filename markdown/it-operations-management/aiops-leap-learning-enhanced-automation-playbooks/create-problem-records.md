---
title: Create AIOps LEAP problem records
description: Create problem records for AIOps LEAP from available incident clusters, also known as automation opportunities, for further analysis.
locale: en-US
release: xanadu
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2025-03-16"
reading_time_minutes: 1
breadcrumb: [Using AIOps LEAP, AIOps Learning Enhanced Automation Playbook \(LEAP\), Now Assist for IT Operations Management \(ITOM\), IT Operations Management]
---

# Create AIOps LEAP problem records

Create problem records for AIOps LEAP from available incident clusters, also known as automation opportunities, for further analysis.

## Before you begin

Role required: AIOps LEAP admin

## About this task

The problem record creation process automatically transfers critical information from incidents to problem records. When a problem record is created, AIOps LEAP includes all relevant information, such as the incident group description, the incident group link, and resolution steps. The automated data transfer is characterized with:

-   **Root cause documentation**

    AIOps LEAP populates the cause notes section of the problem record with the same details as available in existing incident records.

-   **Incident attachment**

    All incidents associated with the group are automatically linked to the problem record for comprehensive tracking.

-   **Async processing**

    Problem records are generated efficiently without manual intervention even during high-volume scenarios.


## Procedure

1.  Select **Workspaces** &gt; **AIOps LEAP**.

2.  On the AIOps LEAP landing page, select an automation opportunity.

    ![Automation opportunity details page](../images/leap-details-page.png)

3.  If a list of resolution steps don't appear in the Overview tab, select **Generate resolution steps**.

4.  Select the **Create problem record** button to create a record for further in-depth analysis.

    ![Create problem record](../images/create-problem-record.png)


