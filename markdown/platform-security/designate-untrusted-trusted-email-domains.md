---
title: Designate email domains as untrusted or trusted
description: Designate specific email domains as untrusted or trusted so that you can monitor the metrics for incoming emails from these sources in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/designate-untrusted-trusted-email-domains.html
release: australia
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 3
breadcrumb: [Email metrics, Monitor instance metrics, Instance Security Center, Platform Security]
---

# Designate email domains as untrusted or trusted

Designate specific email domains as untrusted or trusted so that you can monitor the metrics for incoming emails from these sources in your instance.

## Before you begin

Role required: security\_dashboard\_user or admin

## About this task

**Important:** Instance Security Center \(ISC\) reached end of sales in September 2024 and is a legacy product. ServiceNow Security Center is the recommended replacement. For more information, see [Migrating to Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-center-to-security-center-migration.md).

This procedure applies to instances still running ISC. If you have migrated to ServiceNow Security Center, email monitoring is available by navigating to **Security Center** &gt; **Metrics** &gt; **Email**. The trusted and untrusted email domain designation feature described in this topic is not available in Security Center.

When untrusted or trusted domains send emails to your instance, their daily counts appear on the **Untrusted Incoming Email** or **Trusted Incoming Email** metrics on the Email page. You can then track email activity from these domains and use email logs to view specific incoming emails. You can also specify a user, usually a manager, or a security analyst, to notify whenever activity occurs from the untrusted or trusted domain.

**Note:** Designating an email domain as untrusted is for security tracking purposes only. Administrators can also set up a system address filter to ignore emails from untrusted domains. To learn about filtering emails to block their delivery, see [System address filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-address-filters.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Instance Security Center**.

2.  On the Instance Security Center homepage, select **Email** from the **Metrics** menu.

    \[Omitted image "select-trusted-emails-menu.png"\] Alt text: Email option from the Metrics menu.

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

Name of the user to notify by email when activity occurs in the untrusted or trusted domain. Click the spotlight search icon \( \[Omitted image "Search.png"\] Alt text: Search\) to search for the name of the user. Leave the **Notify** field blank if you do not want notifications sent.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

Untrusted or trusted email domain information is also added to the **Untrusted And Trusted Domains** listing on the Email page.

**Parent Topic:**[Email metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-sec-center-email-metrics.md)

**Related topics**  


[Instance Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-center.md)

[Email metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-sec-center-email-metrics.md)

