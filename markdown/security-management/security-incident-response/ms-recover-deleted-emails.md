---
title: Recover deleted emails on the Microsoft Exchange Online service
description: \(Optional\) As a Microsoft Exchange Administrator, you can recover deleted emails if your incident remediation requires that you to recover the emails deleted by the workflow of this integration.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Microsoft Exchange Online integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Recover deleted emails on the Microsoft Exchange Online service

\(Optional\) As a Microsoft Exchange Administrator, you can recover deleted emails if your incident remediation requires that you to recover the emails deleted by the workflow of this integration.

## Before you begin

For more information about how this integration deletes emails, see [Configure the Microsoft Exchange Online integration](msx_configure.md).

For more information about the administrative role in the Microsoft Office 365 product, including information about recovering deleted items in a user mailbox, see [About the Exchange Online admin role](https://support.office.com/en-us/article/about-the-exchange-online-admin-role-097ae285-c4af-4319-9770-e2559d66e4c8).

Role required: admin, Microsoft Exchange Administrator

## About this task

If you select the **Recover Deleted Emails** option in the Additional Settings tab during the configuration step, you enable the recovery of deleted emails in your Microsoft Exchange Online tenant. Emails deleted using the delete workflow of this integration are placed in the Deleted Items sub folder of the Recoverable items folder in the mailbox of the user on the Microsoft Exchange Online service. If the user's account is configured in Microsoft Exchange Online tenant so that the user can view the Deleted Items folder, the user can recover these emails by using the Microsoft Outlook service on the web. Alternatively, the Microsoft Exchange Online administrator can recover deleted emails from a Deleted Items folder of a user. See [Recover deleted items or email in Outlook Web App](https://support.office.com/en-us/article/recover-deleted-items-or-email-in-outlook-web-app-c3d8fc15-eeef-4f1c-81df-e27964b7edd4?ui=en-US&rs=en-US&ad=US) for more information.

Role required: Microsoft Exchange Online administrator or Microsoft Global administrator to recover deleted emails.

Role required: sn\_si.admin in the ServiceNow AI Platform to enable the Recover Deleted Emails option.

Role required: sn\_si.analyst in the ServiceNow AI Platform for completing a successful search for emails and verifying that emails are successfully deleted prior to recovery.

## Procedure

1.  To enable the email recovery option, follow these steps.

    1.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Configurations**.

    2.  Locate the Microsoft Exchange Online tile.

    3.  Click **Configure**.

        ![Microsoft Exchange Online configuration tile.](../image/ms-7-24-config.png)

    4.  In the Microsoft Exchange Online Configuration dialog box that is displayed, click **Configure Exchange Online**.

        ![Configure Exchange Online link highlighted on Microsoft Exchange Online Configuration dialog.](../image/ms-configure-tile.png "Configure Exchange Online")

    5.  On the `Additional Settings` tab under `Recover Deleted Emails`, select the **Enable** check box.



        ![Recover deleted emails on the Microsoft Exchange Online service](../image/ms-settings-recover-deleted.png)

    6.  Verify any other settings and click **Submit**.

    7.  To verify that a search and delete of email messages are successfully completed for the email messages you want to recover, navigate to the security incident that logged the email search and delete workflows.

    8.  Locate the work notes and verify that the system successfully deleted the messages.

        ![Work notes confirming emails were successfully deleted.](../image/ms-924-work-notes-system.png)

    9.  As a Microsoft Exchange Online administrator or Global administrator, log in to your Microsoft Office 365 account.

    10. Follow the steps described in [Recover deleted items or email in Outlook Web App](https://support.office.com/en-us/article/recover-deleted-items-or-email-in-outlook-web-app-c3d8fc15-eeef-4f1c-81df-e27964b7edd4?ui=en-US&rs=en-US&ad=US) on the Microsoft documentation website.


**Parent Topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Previous topic:**[Approve delete email requests for the Microsoft Exchange Online integration](ms-approve-delete.md)

**Next topic:**[Edit security tags for the Microsoft Exchange Online integration](ms-edit-tags.md)

