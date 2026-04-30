---
title: Assign a regulatory event alert to a coordinator
description: Log in to the GRC: Regulatory Change Management application, review the regulatory event alert, update the details, and assign it to a coordinator.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Assign a regulatory event alert to a coordinator

Log in to the GRC: Regulatory Change Management application, review the regulatory event alert, update the details, and assign it to a coordinator.

## Before you begin

Role required: sn\_grc\_reg\_change.manager, sn\_grc\_reg\_change.user

## About this task

In the following procedure, step 4 and after describe various actions that users with the sn\_grc\_reg\_change.manager role or sn\_grc\_reg\_change.user role can perform.

## Procedure

1.  Log in with the sn\_grc\_reg\_change.manager user role.

2.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **Compliance Workspace**.

    The Regulatory Change Management application in the Compliance Workspace is displayed.

3.  Navigate to **Lists** &gt; **Assigned Regulatory Alerts** view.

4.  In the Assigned Alerts list, select a regulatory event alert.

    The detailed view for the selected regulatory event alert is displayed.

5.  In the Details tab, fill in the form.

    |Fields|Description|
    |------|-----------|
    |Title|Title of the alert as received from the provider. This field is automatically set to display the title.|
    |Description|Description and a summary of the event. This field is automatically set to display the description.|
    |Provider URL|URL of the alert that is received from the provider. This field is automatically set to display the provider URL.|
    |Regulatory body URL|URL of the regulatory body that is associated with the alert. This field is automatically set to display the regulatory body URL.|
    |Provider|Name of the alert provider. This field is automatically set to display the name of the alert provider.|
    |Type|Type of regulatory alert. This field is automatically set to display the type of the alert.|
    |Coordinator|User that the alert is assigned to.|
    |Overall impact|Overall impact of the alert.|
    |Dates|
    |Source publication date|Date when the regulatory event is published by the regulatory body. This field is automatically set to display the source publication date.|
    |Comments date|Date until when the comments can be provided for the regulatory event. This field is automatically set to display the comments date.|
    |Effective date|Date when the regulatory event is going to be applicable. This field is automatically set to display the effective date.|
    |Compliance date|Date by which the regulatory event is going to be compliant. This field is automatically set to display the compliance date.|
    |Expiration date|Expiry date for the regulatory event. This field is automatically set to display the expiration date.|
    |Series data|
    |Series name|Series name of the alert. This field is automatically set to display the series name from the provider.|
    |Sequence number|Sequence number of the alert. This field is automatically set to display the sequence number from the provider.|
    |Activity Journal|
    |Additional comments|Additional comments related to the alert.|
    |Compose|
    |Compose section|Additional comments related to the alert.|
    |Activities|Log of the activities related to the alert.|
    |Highlighted details|
    |Taxonomy|Taxonomy details associated with the alert. This field is automatically set to display the taxonomy details of the alert.|

    **Note:** Beginning with the ServiceNow® Zurich release, the taxonomy section in the form is not available to the new installations.

6.  In the **Coordinator** field, assign the regulatory event alert to a coordinator with the sn\_grc\_reg\_change.user user role and select **Save**.


## Result

The regulatory event alert is assigned to the selected coordinator.

## What to do next

[Assess the impact of a regulatory event alert](assess-impact-of-reg-change-using-ws.md)

