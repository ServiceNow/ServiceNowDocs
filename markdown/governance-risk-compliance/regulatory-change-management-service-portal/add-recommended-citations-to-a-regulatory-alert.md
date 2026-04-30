---
title: Add an AI-recommended citation to a regulatory alert
description: Add an AI-recommended citation to a regulatory alert by using the GRC: Predictive Intelligence application.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Regulatory alerts, Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Add an AI-recommended citation to a regulatory alert

Add an AI-recommended citation to a regulatory alert by using the GRC: Predictive Intelligence application.

## Before you begin

Role required: sn\_compliance\_admin or sn\_compliance\_manager

## About this task

Traditionally, citations were downloaded from a third-party provider but only the users with subscription licenses could download the citations from those third-party-providers or you could create citations from an authority document by using Compliance Workspace.

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **Compliance Workspace**.

2.  Select the list icon ![](../../grc-ai-risk-compliance/image/list-icon-airc-ws.png).

3.  Select **Regulatory alerts**.

4.  Select a regulatory alert to open it.

    Regulatory alerts can be either a regulatory event or a source document.

5.  Select **Recommended actions**.

    **Note:** The **Recommended actions** option is available only for a regulatory-event alert that is categorized as a regulatory-event type.

6.  Within each AI-recommended citation, select **Associate** to associate the citation to the regulatory alert.

    The recommended citation card displays the following details:

    -   A score that indicates the confidence level of the generated citation.
    -   Name of the citation.
    -   Description of the citation.
    -   The authority document to which the citation belongs.
7.  Repeat the previous step for all the citations that you want to associate with the opened regulatory alert.

    The selected citations are associated with the regulatory alert.


**Parent Topic:**[Regulatory alerts](../concept/regulatory-feeds.md)

**Related topics**  


[Perform actions on regulatory alerts](perform-actions-reg-event-feeds.md)

[Manage and assign regulatory event alerts](manage-regulatory-feeds.md)

[Train and use the similarity solution to recommend citations on regulatory alerts](retrain-ml-reg-compliance-mapping.md)

[Manage and assign source document alerts](manage-source-document-feeds.md)

