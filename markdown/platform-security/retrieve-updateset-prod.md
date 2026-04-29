---
title: Import and install certificates for Circle of Trust
description: Retrieve the update set in production to establish the trust relationship between the two instances. The certificates that have been created to represent trust in the trusted instance must be accepted into the protected instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Import and install certificates for Circle of Trust

Retrieve the update set in production to establish the trust relationship between the two instances. The certificates that have been created to represent trust in the trusted instance must be accepted into the protected instance.

## Before you begin

Roles required: admin, security\_admin

## Procedure

1.  In the protected instance, navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

2.  Select the **Import Update Set from XML** button on the bottom-left corner of the screen.

    ![Import XML screen to retrieve update set.](../../key-management-framework/image/import-update-set-1.png)

3.  Select **Choose File** and browse to select the XML file that you exported in [Prepare Circle of Trust certificates](create-updateset-nonprod.md).

    ![Import XML screen to retrieve update set.](../../key-management-framework/image/retrieve-update-set.png)

4.  Select **Upload**.

    The Code Signing update set is added to the Retrieved Update Sets table.

    ![Loaded update set to production.](../../key-management-framework/image/loaded-updateset-prod.png)

    **Note:** If you don’t see your update set, filter your list for records in the Loaded state, and sort the list by the **Loaded** field.

5.  Open the update set record to verify that the Customer Updates table contains the following three records:

    -   Two KMF Signature Records
    -   X.509 Certificate
    ![Shows the imported certificate and signature records into production.](../../key-management-framework/image/prod-customer-updates-retrieved.png)

6.  Select **Preview Update Set**.

7.  Select **Commit Update Set**.

    ![Shows the State updated to Committed.](../../key-management-framework/image/committed-updateset.png)

    The Retrieved Update Set **State** updates to Committed.

8.  In the navigator, enter `sn_kmf_record_signature.list` to open the **KMF Signature Records** list.

9.  Locate the two KMF signature records.

    These records are the most recently created records where the **KMF Signature Purpose** field has a value of `Circle of Trust`. You may need to add the **Created** field to your list, or filter for records created on the current date.

10. In the navigator, enter `sys_certificate.list` and open the record with a **Short description** value of `code_signing_key` and a **Type** value of `Trust Store Cert`.

11. Select **Install Trusted Code Signing cert**.

    ![X.509 form to install trusted Code Signing cert.](../../key-management-framework/image/install-trusted-code-signing-cert.png)

    The certificate type updates to `Trusted CodeSigning Cert`.

    **Important:** Repeat these steps for your second certificate. Remember that there’s a certificate for both the cm\_code\_attest and cm\_code\_signing cryptographic modules.


## Result

The trust relationship is established between trusted and protected instances. You’re ready to enable Code Signing. See [Turn on Code Signing](enable-codesiging.md) to complete the steps.

**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

