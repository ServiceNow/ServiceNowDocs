---
title: View audits with warnings and errors
description: The Domain Separation Center provides details about audit errors and warnings.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Domain Separation Center, Domain separation for service providers, Access Management]
---

# View audits with warnings and errors

The Domain Separation Center provides details about audit errors and warnings.

## Before you begin

Role required: admin

## About this task

On the Domain Separation Center dashboard, **Errors** and **Warnings** provide detailed information about audits that encountered problems. Logs related to domain separation reside on your server in the syslog\_domain table. Errors are issues that require immediate attention. Warnings do not lead to failures but present best practices, for example, not making the domain name too long.

## Procedure

1.  In the Domain Separation Center, click the number in the **Errors** or **Warnings** box.

    The **Errors** or **Warnings** page appears.

2.  Click one of the audits in the list.

    The page displays detailed information about problems with the audit you selected. The messages in **Audit Result Details** refer to values in the syslog\_domain table on the server for table audits that revealed errors or warnings.

3.  To see the logs on the server that provide information about warning or error audits:

    1.  Copy the **Detail ID** value in the left panel of a warning or error.

    2.  On the instance running the Domain Separation Center, in the **Filter navigator**, enter `syslog_domain.list`.

        The Domain Log page appears.

    3.  In the search field of the **Source** column, enter `=<Detail-ID>` \(no space after the equals sign\), for example, `=f6a00fd29a85b300a9503a81b9169678`.

        The Domain Log page displays only the logs related to the audit with the Detail ID you specified. Each row in the table specifies a different record the audit found problems in. Notice that the **Message** field on this page matches the values displayed in the **Message** column of the Domain Service Center. The information included in the message matches the audit type.

4.  Select one of the following:

    -   **Rerun Audit** — Rerun an audit to see if it still encounters a warning or error.
    -   **Deactivate Audit** — Inactivate an audit.
    -   **Copy Details** — Copy audit details to the clipboard.

