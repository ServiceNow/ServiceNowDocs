---
title: Manage and assign source document alerts
description: Assign source document alerts that are received from the regulatory intelligence provider to an appropriate user. You can review other properties of the source document alert.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Regulatory alerts, Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Manage and assign source document alerts

Assign source document alerts that are received from the regulatory intelligence provider to an appropriate user. You can review other properties of the source document alert.

## Before you begin

Role required: sn\_grc\_reg\_change.manager

## About this task

As a manager, you can view and assign the source document alerts to users with the sn\_grc\_reg\_change.user role. The user can then perform actions on the source document alerts.

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Regulatory Change Management** &gt; **Regulatory Alerts** &gt; **Unassigned Alerts**.

    All the regulatory alerts in your instance are displayed. You can view the unassigned alerts and assign them to a specific user. An incoming alert is automatically assigned to the New state.

2.  In the regulatory alert list, select a source document alert by using the Type column.

    The alert record for the source document alert is displayed.

3.  To assign the alert, set the **Coordinator** field to the appropriate user.

    You can review the other properties of the alert to help you determine the appropriate user to assign to.

    |Fields|Description|
    |------|-----------|
    |Title|Title of the source document type of alert as received from the provider.|
    |Citation|Citation number for the source document that is received from the alert provider.|
    |Provider URL|Provider URL for the alert.|
    |Regulatory body URL|URL of the regulatory body that is associated with the alert.|
    |Provider|Name of the alert provider.|
    |Coordinator|User who is assigned the alert.|
    |State|State of the alert.|
    |Type|Type of the regulatory alert. For example, source document.|
    |Taxonomy|
    |Regulatory body|Organization that exercises a regulatory function, such as a government agency.|
    |Sector|Different business segments for your organizations, such as banking and insurance.|
    |Theme|Broad topics that you can use to classify your regulatory content. Possible themes are Privacy, Operational Resilience, and Regulatory Filings.|
    |Jurisdiction|Location where a regulatory or legal body can extend the legal authority.|
    |Content type|Different categories of content that a regulatory body can issue, such as legislative materials, regulations, and rules.|
    |Dates|
    |Source publication date|Date when the particular regulatory event is actually published by the regulatory body.|
    |Effective date|Date when the particular regulatory event will be applicable.|
    |Expiration date|Date when the particular regulatory event will expire.|
    |Comments date|Date until when the comments can be provided for the regulatory event.|
    |Compliance date|Date by which the regulatory event will be compliant.|
    |Activity Journal|
    |Additional comments|Additional comments related to the alert.|
    |Activities|Log of the activities related to the alert.|

4.  Select **Update**.


## Result

The source document alert is assigned to the selected user and it is listed under the **All Assigned Alerts** module in the application.

**Parent Topic:**[Regulatory alerts](../concept/regulatory-feeds.md)

**Related topics**  


[Perform actions on regulatory alerts](perform-actions-reg-event-feeds.md)

[Add an AI-recommended citation to a regulatory alert](add-recommended-citations-to-a-regulatory-alert.md)

[Manage and assign regulatory event alerts](manage-regulatory-feeds.md)

[Train and use the similarity solution to recommend citations on regulatory alerts](retrain-ml-reg-compliance-mapping.md)

