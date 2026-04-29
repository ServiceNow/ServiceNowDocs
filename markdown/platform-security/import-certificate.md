---
title: Import the revocation request configuration
description: Import the update set into the protected instance to initiate the certificate revocation process. Approvers receive email notifications and they should complete the approval workflow before the certificate is revoked. The approval means that the revocations are confirmed, authorized, and traceable for security and compliance purposes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Quorum Controlled Certificate Revocation, Configure, Code Signing, Platform Security]
---

# Import the revocation request configuration

Import the update set into the protected instance to initiate the certificate revocation process. Approvers receive email notifications and they should complete the approval workflow before the certificate is revoked. The approval means that the revocations are confirmed, authorized, and traceable for security and compliance purposes.

## Before you begin

Role required: sn\_cse.codesigning\_admin, sn\_cse.quorum\_requester, security\_admin

## Procedure

1.  Log in to your protected instance and navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets** &gt; **Import XML**.

    The Import XML page appears.

2.  Select **Choose file** and select the configuration XML file from your local system.

3.  Select **Upload**.

4.  Return to the code signing configuration page at **All** &gt; **Code Signing** &gt; **Code Signing Configuration**.

    1.  Review the following configuration files in the **Customer Updates in Batch** tab.

        -   Code Signing Configuration Property \(`time_window`\)
        -   Code Signing Configuration Property \(`approver_email_ids`\)
        -   Code Signing Configuration Property \(`minimum_approvals`\)
        -   Code Signing Configuration Property\(`restart_mid_servers`\)
        -   Code Signing Quorum Request \(`CSEQCxxxxxxx`\)
        -   Code Signing Transaction \(`CSETRANSxxxxxxx`\)
        -   KMF Signature Records
    2.  Select **Batch Update Set Preview** &gt; **Commit Update Set Batch**.

5.  Return to the code signing configuration page at **All** &gt; **Code Signing** &gt; **Configuration** &gt; **Guided Setup**.

6.  In the **Instance type** field, select **Protected instance** and select **Next**.

    The **Start or continue your configuration** page appears.

7.  Select the **Confirm that the Code Signing configuration update set was imported and committed.** check box and select **Next**.

    In the Quorum Control Configuration page, review the information that you entered and select **Trigger Quorum Approval**.

8.  In the Protected instance, select **Certification Revocation Status** in the Trigger Quorum Approval page to review updates on the quorum control request approvals.

9.  Select **Approver details** and review the status of the quorum requests.


**Parent Topic:**[Quorum Controlled Certificate Revocation](../concept/certificate-revocation.md)

