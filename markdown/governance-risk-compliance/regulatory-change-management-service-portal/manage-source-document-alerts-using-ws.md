---
title: Assign a source document alert to a coordinator
description: Log in to the GRC: Regulatory Change Management application, review the source document alert, and assign it to a coordinator. The coordinator then assesses the applicability of the alert and completes the associated regulatory tasks.
locale: en-US
release: xanadu
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Assign a source document alert to a coordinator

Log in to the GRC: Regulatory Change Management application, review the source document alert, and assign it to a coordinator. The coordinator then assesses the applicability of the alert and completes the associated regulatory tasks.

## Before you begin

Roles required: sn\_grc\_reg\_change.manager, sn\_grc\_reg\_change.user

## About this task

As a manager, you can view and assign the source document alerts to users with the sn\_grc\_reg\_change.user role. The user can then perform actions on the source document alerts.

## Procedure

1.  Log in with the sn\_grc\_reg\_change.manager user role.

2.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **Compliance Workspace**.

    The Regulatory Change Management application in the Compliance Workspace is displayed.

3.  Navigate to **Lists** &gt; **Assigned Regulatory Alerts** view.

4.  Select a source document type alert in the list.

5.  In the Details tab, fill in the form.

    |Fields|Description|
    |------|-----------|
    |Title|Title of the source document type of alert as received from the provider. This field is automatically set to display the title.|
    |Citation|Citation number for the source document that is received from the provider. This field is automatically set to display the citation.|
    |Provider URL|URL of the alert provider. This field is automatically set to display the provider URL.|
    |Regulatory body URL|URL of the regulatory body that is associated with the alert. This field is automatically set to display the regulatory body URL.|
    |Provider|Name of the alert provider. This field is automatically set to display the name of the provider.|
    |Type|Type of the regulatory alert. For example, source document alert. This field is automatically set to display the type of the alert.|
    |Coordinator|User that the alert is assigned to.|
    |Dates|
    |Source publication date|Date when an alert is published by the regulatory body. Auto-populated field. This field is automatically set to display the source publication date.|
    |Comments date|Date until when the comments can be provided for the alert. Auto-populated field. This field is automatically set to display the comments date.|
    |Effective date|Date when the alert is going to be applicable. This field is automatically set to display the effective date.|
    |Compliance date|Date by which the alert is going to be compliant. This field is automatically set to display the compliance date.|
    |Expiration date|Expiry date for the alert. This field is automatically set to display the expiration date.|
    |Activity Journal|
    |Additional comments|Additional comments related to the alert.|
    |Compose|
    |Additional comments|Additional comments related to the alert that are added in the Compose section.|
    |Log of the activities|Log of the activities related to the alert. Displays the system generated changes and additional comments.|
    |Highlighted details|
    |Taxonomy|Taxonomy details associated with the alert. This field is automatically set to display the taxonomy details of the alert.|

6.  In the **Coordinator** field, assign it to a user with the sn\_grc\_reg\_change.user user role.

7.  Log in with the sn\_grc\_reg\_change.manager role, open the selected source document alert, and mark the alert using one of the following options.

<table id="choicetable_utb_d4n_brb"><thead><tr><th align="left" id="d197588e337">

Field

</th><th align="left" id="d197588e340">

Description

</th></tr></thead><tbody><tr><td id="d197588e346">

**Applicable**

</td><td>

Marks the alert as applicable.

</td></tr><tr><td id="d197588e355">

**Not applicable**

</td><td>

Marks the alert as not applicable. Select one of the following reasons and select **Submit**:-   No action required on the alert
-   Duplicate alert
-   Other
As a result of this action, the stepper component in the alert page displays the stage as **Completed**.

</td></tr><tr><td id="d197588e382">

**Cancel regulatory alert**

</td><td>

Cancel the regulatory alert.

</td></tr><tr><td id="d197588e391">

**Defer**

</td><td>

Defer the alert to a later date.

</td></tr></tbody>
</table>
## Result

After marking the source document alert as **Applicable**, a new source document import task is created under the Import document tasks related list.

