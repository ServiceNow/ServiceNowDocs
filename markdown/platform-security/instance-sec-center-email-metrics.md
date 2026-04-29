---
title: Email metrics
description: Analyze your email metrics to look for anomalous behaviors that are related to the incoming emails to your instance. For example, if the metrics indicate a spike in spam emails from specific domains, you can define inbound actions that prevent their delivery to the instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor instance metrics, Instance Security Center, Platform Security]
---

# Email metrics

Analyze your email metrics to look for anomalous behaviors that are related to the incoming emails to your instance. For example, if the metrics indicate a spike in spam emails from specific domains, you can define inbound actions that prevent their delivery to the instance.

For each email metric, a count appears for each type of email that is delivered or sent to the instance during the calendar day.

<table id="table_rpk_b5z_4lb"><thead><tr><th>

Notification preference

</th><th>

Description

</th></tr></thead><tbody><tr><td>

External Incoming Email

</td><td>

Number of incoming emails for the calendar day that were delivered to the instance from external email domains. **Note:** The external email domains are those domains that are not listed in the **security.list.internal.domains** system property, because this property tracks only your internal email domains. To learn more about this property, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Spam

</td><td>

Number of incoming emails for the calendar day that were delivered to the instance and marked as spam. A number that is out of line with historical trends may indicate that attempts are being made to compromise your instance security.

</td></tr><tr><td>

Trusted Incoming Email

</td><td>

Number of incoming emails to the instance for the calendar day from email domains designated as trusted.

</td></tr><tr><td>

Untrusted Incoming Email

</td><td>

Number of incoming emails to the instance for the calendar day from email domains designated as untrusted. You can designate untrusted or trusted email domains in the Untrusted And Trusted Domain form so that you can track your inbound emails that are sent from them. To learn how to designate untrusted or trusted email domains, see [Designate email domains as untrusted or trusted](../task/designate-untrusted-trusted-email-domains.md).

</td></tr></tbody>
</table>After you click an email metric, you can learn about the possible email security issues in your instance by clicking one of the following:

|Command|Description|
|-------|-----------|
|Chart|Incoming email counts and count trends over time for the selected email type \(spam, incoming external, untrusted, or trusted\).|
|Records|Individual email records that compromise the daily count for the selected email type.|
|More Info|Additional information for the selected email type.|

**Note:** The email metrics apply only to your incoming emails to the instance. The metrics do not apply to the normal traffic that is processed through your enterprise-wide email servers. To learn about defining inbound actions and how they impact the processing of your inbound emails, see [Inbound email actions](https://www.servicenow.com/docs/access?context=c_InboundEmailActions&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

-   **[Designate email domains as untrusted or trusted](../task/designate-untrusted-trusted-email-domains.md)**  
Designate specific email domains as untrusted or trusted so that you can monitor the metrics for incoming emails from these sources in your instance.

**Parent Topic:**[Monitor instance metrics](monitoring-user-email-antivirus-metrics.md)

