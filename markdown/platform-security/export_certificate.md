---
title: Export Revocation Request Configuration
description: Start the certificate revocation process by selecting the certificate that you want to revoke. Provide the required configuration properties. Export this transaction as part of an update set, which is imported into the protected instance for approval and execution.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Quorum Controlled Certificate Revocation, Configure, Code Signing, Platform Security]
---

# Export Revocation Request Configuration

Start the certificate revocation process by selecting the certificate that you want to revoke. Provide the required configuration properties. Export this transaction as part of an update set, which is imported into the protected instance for approval and execution.

## Before you begin

Role required: sn\_cse.codesigning\_admin, sn\_cse.quorum\_requester, security\_admin

## Procedure

1.  On your trusted instance, navigate to **All** &gt; **Code Signing** &gt; **Configuration** &gt; **Guided Setup** and open the Code Signing configuration page.

2.  In the **Instance type** field, select **trusted instance**.

3.  Select the **Next** button.

4.  In the **Action** field under **Select the action you’d like to accomplish**, select **Certificate Revocation**.

    The Certification Revocation Request page appears.

5.  In the Select Certificate to Revoke page, select the certificate that you want to revoke and select **Initiate Revocation**.

6.  Configure the approval requirements for certification revocation.

    1.  In the Quorum Requirements menu, enter the appropriate information in the text fields.

<table id="table_ufc_w4t_z2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Minimum approvals

</td><td>

Minimum number of approvers required to approve the certificate revocation request.

</td></tr><tr><td>

Time window

</td><td>

Expiration time for the revocation request.

</td></tr><tr><td>

Approvers

</td><td>

Email address of the users who are authorized to approve the revocation request.

</td></tr></tbody>
</table>    2.  In the **Request description** field, enter the reason for initiating the certificate revocation.

    3.  Select **Save**.

        The Export configuration file menu appears.

    4.  On the Export Configuration file page, select **Export** to create and download a configuration file used to run certificate revocation workflow on your protected instance.


## Result

The export process downloads an XML file to your local machine for use in the steps detailed in [Configure Code Signing Enterprise on your protected instance](cse-ppi-config.md).

**Parent Topic:**[Quorum Controlled Certificate Revocation](../concept/certificate-revocation.md)

