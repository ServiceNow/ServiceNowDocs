---
title: Submit block list entries from a security incident for the Check Point NGTP integration
description: Observables attached to a security incident record are submitted for approval as Block List entries to different Block Lists. An optional approval process for Block List entries is part of the preconfigured workflow. The Gateway imports Block List entries — IP addresses, URLs, domains — that are included in Block Lists.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with block lists, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit block list entries from a security incident for the Check Point NGTP integration

Observables attached to a security incident record are submitted for approval as Block List entries to different Block Lists. An optional approval process for Block List entries is part of the preconfigured workflow. The Gateway imports Block List entries — IP addresses, URLs, domains — that are included in Block Lists.

## Before you begin

Role required:

-   Security Incident Analyst \(sn\_si.analyst\) to submit block list entries.
-   Security Incident Administrator \(sn\_si.admin\) to approve block list entries. This authority can be assigned as required by your organization.

## About this task

Users with the sn\_si.analyst role submit Block entries by requesting a block on observables attached to a security incident record. Once submitted, a Block List entry with a status of Pending is generated and sent for approval. The following example shows a block request for a URL observable.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**, and click a security incident record to open it.

2.  Click the **Show IoC** related link.

    ![Show IoC related list](../image/show-ioc.png)

3.  In the Observables related list, select the observables you want to block and, from the **Actions on selected rows** list, select **Block Request**.

    ![Block Request action](../image/action-block-request.png)

4.  In the dialog box that is displayed, click the search icon \(![Magnifying glass icon](../image/magnifier.png)\)

    ![Block request implementation](../image/block-request-implementation.png)

5.  From the list, select the Block List you want to attach this entry to.

    **Note:** For this example, the entry observable type \(IP\) should match the Block List observable type \(IP\).

    ![Integration capability implementation](../image/integ-cap-implementations.png)

6.  In the Block Request dialog box with the Block List name displayed in the Implementation field, click **Block**.

    ![Block Request lookup](../image/lookup-using-list.png)

7.  From the list that is displayed, select the Block List you want to attach this entry to.

    **Note:** For this example, the entry observable type \(IP\) should match the Block List observable type \(IP\).

    ![Integration capability implementation](../image/integ-cap-implementations.png)

8.  In the Block Request dialog box with the Block List name displayed in the **Implementation** field, click **Block**.

    ![Block Request lookup](../image/lookup-using-list.png)

9.  Navigate to **Check Point NGTP Integration** &gt; **Block Request List Entries**, and click **Block Request List Entries**.

    ![Block request list entries](../image/pending-in-redbox.png)

10. In the Check Point Block Request List Entries list, click your observable in the **Entry value** column to open the record.

    For this example, the record for **74.125.34.95** is displayed.

    ![the Check Point Block Request List Entries](../image/sys-admin-redbox.png)

    The status is Pending, the Active check box is cleared, and the work notes show that there is a request to add the observable. This Block List Entry request is ready for approval.

    The icon next to the Observable field is a link to the ServiceNow AI Platform Observable table.

    The value in the Observable field \(74.125.34.95\) links to the Observable table, and it matches the format that was brought over from the Security Incident Response incident-triggering event.


