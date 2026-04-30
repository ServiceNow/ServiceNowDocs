---
title: Submit the security incident to the Zscaler URL category list
description: Submit entries directly for observables that are not associated with a specific ServiceNow AI Platform security incident record so that observable entries are in the appropriate allow or deny lists.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit the security incident to the Zscaler URL category list

Submit entries directly for observables that are not associated with a specific ServiceNow AI Platform security incident record so that observable entries are in the appropriate allow or deny lists.

## Before you begin

Role required: sn\_si.admin

## About this task

You can also add observables to the URL category list directly from the Observable record.

## Procedure

1.  Navigate to **All** &gt; **Zscaler Integration** &gt; **Zscaler URL Category List Entries**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entry Value

</td><td>

Observable name. If a matching observable is found, the rest of the form is automatically filled.

 If no matching observable is found, you must fill in the rest of information manually.

</td></tr><tr><td>

Observable

</td><td>

Value \(for example, IP address or hash\) that is associated with the observable.

</td></tr><tr><td>

Observable Type

</td><td>

Observable classification, such as an IP address or file hash.

</td></tr><tr><td>

URL Category List

</td><td>

URL category. For example, if an organization uses example.com for Office 365 services, then Zscaler categorizes example.com as Professional Services and Office 365.

</td></tr><tr><td>

Source

</td><td>

Name of the server. You can view only the previously configured Zscaler servers from the URL category list.

</td></tr><tr><td>

Incident count

</td><td>

Number of incidents that this observable appears in. This value is automatically updated when the observable is added to another incident manually or through a workflow.

</td></tr><tr><td>

Active

</td><td>

Indicator that the URL category list is active.

</td></tr><tr><td>

Status

</td><td>

Status if the observable is approved or rejected.

</td></tr><tr><td>

Expiration Period \(days\)

</td><td>

Expiration period of the URL category list. 0 \(by default\) indicates that the URL category list entry never expires.

 By changing this value, any observable that you add to this URL category is active for the number of days that you enter. You can enter a minimum value of 1.

 For example, if you set the expiration period to 30 days, the entries are removed from the category list after 30 days.

 **Note:** If you change the default expiration period of the URL category list entry, you see a warning that the period differs from the period that is configured in the selected URL category list.

</td></tr><tr><td>

Additional Information

</td><td>

Field where you can add more details about the observable.

</td></tr></tbody>
</table>4.  Click **Submit**.


