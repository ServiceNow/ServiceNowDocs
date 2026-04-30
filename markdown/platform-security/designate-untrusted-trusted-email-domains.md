---
title: Designate email domains as untrusted or trusted
description: Designate specific email domains as untrusted or trusted so that you can monitor the metrics for incoming emails from these sources in your instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Email metrics, Monitor instance metrics, Instance Security Center, Platform Security]
---

# Designate email domains as untrusted or trusted

Designate specific email domains as untrusted or trusted so that you can monitor the metrics for incoming emails from these sources in your instance.

## Before you begin

Role required: security\_dashboard\_user or admin

## About this task

When untrusted or trusted domains send emails to your instance, their daily counts appear on the **Untrusted Incoming Email** or **Trusted Incoming Email** metrics on the Email page. You can then track email activity from these domains and use email logs to view specific incoming emails. You can also specify a user, usually a manager, or a security analyst, to notify whenever activity occurs from the untrusted or trusted domain.

**Note:** Designating an email domain as untrusted is for security tracking purposes only. Administrators can also set up a system address filter to ignore emails from untrusted domains. To learn about filtering emails to block their delivery, see [System address filters](https://www.servicenow.com/docs/access?context=system-address-filters&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Instance Security Center**.

2.  On the Instance Security Center homepage, select **Email** from the **Metrics** menu.

    ![Email option from the Metrics menu.](../image/select-trusted-emails-menu.png)

3.  On the Email page, in the Untrusted And Trusted Domains section, click **New**.

4.  On the form, fill in the fields.

<table id="table_kxg_qzk_ddb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain

</td><td>

Name of the email domain that you are designating as untrusted or trusted. For example, enter `servicenow.com` to designate ServiceNow employees can send trusted emails to the instance.

</td></tr><tr><td>

Category

</td><td>

Category that indicates if the email domain is untrusted or trusted:-   **Untrusted**

Designates that the email domain as untrusted. You use it to identify domains that send suspicious or emails that pose a potential security threat to the instance.

-   **Trusted**

Designates that the email domain as trusted. You use it to identify domains when your metrics indicate that the incoming emails from it pose no security threats. Designating the domain as trusted enables you to track its inbound email activity over time.

</td></tr><tr><td>

Active

</td><td>

Check box for enabling or disabling the designated untrusted or trusted status for the specified email domain.

</td></tr><tr><td>

Notify

</td><td>

Name of the user to notify by email when activity occurs in the untrusted or trusted domain. Click the spotlight search icon \( ![Search](../image/Search.png)\) to search for the name of the user. Leave the **Notify** field blank if you do not want notifications sent.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

Untrusted or trusted email domain information is also added to the **Untrusted And Trusted Domains** listing on the Email page.

**Parent Topic:**[Email metrics](../concept/instance-sec-center-email-metrics.md)

**Related topics**  


[Instance Security Center](../concept/instance-security-center.md)

[Email metrics](../concept/instance-sec-center-email-metrics.md)

