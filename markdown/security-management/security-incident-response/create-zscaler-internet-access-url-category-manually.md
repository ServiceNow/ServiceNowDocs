---
title: Add Zscaler Internet Access URL category lists
description: Add the URL categories that are available in the Zscaler Internet Access product to the ServiceNow AI Platform instance to specify an action for each URL so that you have easy access for granular filtering and policy creation.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add Zscaler Internet Access URL category lists

Add the URL categories that are available in the Zscaler Internet Access product to the ServiceNow AI Platform instance to specify an action for each URL so that you have easy access for granular filtering and policy creation.

## Before you begin

Role required: sn\_si.admin

## About this task

The Security Incident Response integration with Zscaler provides a default allow list and deny list URL category lists to help filter content.

The URL categories that you add in the ServiceNow AI Platform instance should already be in your Zscaler Internet Access environment. You can't use Security Incident Response integration with Zscaler to create URL categories on Zscaler.

**Note:** For more information on URL category lists in the Zscaler product, see the [Zscaler documentation on URL Categories](https://help.zscaler.com/zia/about-url-categories).

## Procedure

1.  Navigate to **All** &gt; **ZScaler Integration** &gt; **ZScaler URL Category Lists**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Name of the server. You can view only the previously configured Zscaler Internet Access servers from the URL category list.

</td></tr><tr><td>

Active

</td><td>

Indicator that the URL category list is active.

</td></tr><tr><td>

URL Category

</td><td>

Field that is enabled after you select the source. You can view the list of URL categories that are created in Zscaler.

</td></tr><tr><td>

Expiration Period \(days\)

</td><td>

Expiration period of the URL category list. 0 \(by default\) indicates that the URL category list entry never expires.

 By changing this value, any observable that was added to this URL category is active for the number of days that you enter. You can enter a minimum value of 1.

 For example, if you set the expiration period to 30 days, the entries are removed from the category list after 30 days.

</td></tr><tr><td>

Display Tag

</td><td>

Security tag that appears on the SIR security incident. When you enable the **Display Tag** option, the Zscaler Tag for observables field is available on the form.

</td></tr><tr><td>

Create Change Request

</td><td>

Change request and change tasks in your ServiceNow AI Platform instance for the records that are attached to the URL category list.When you enable the **Create Change Request** option, the **Change Request** field is available on the form.

</td></tr><tr><td>

Require Approval

</td><td>

List of approver groups. After you submit a request, an approval is required from the group to complete the request.When you enable the **Require Approval** option, the **Approvers for adding observables** and **Approvers for removing observables** fields are available on the form.

-   **Approvers for adding observables**: Select the approvers using the look up to add the observables from the **Zscaler URL Category List** page. This option will allow you to add the user group\(s\) for approvals.
-   **Approvers for removing observables**: Select the approvers for removing the observables using the look up from the **Zscaler URL Category List** page. This option will allow you to remove the user group\(s\) from the approval list.


</td></tr><tr><td>

Description

</td><td>

Description of the Zscaler URL category list. Use this field for adding more details about the URL category record.

</td></tr></tbody>
</table>4.  Click **Submit**.

    A successful submission triggers an email notification to the approval group.


