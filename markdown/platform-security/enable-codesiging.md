---
title: Turn on Code Signing
description: Turn on Code Signing in your trusted non-production instance to identify the trusted instances linking to your production instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Turn on Code Signing

Turn on Code Signing in your trusted non-production instance to identify the trusted instances linking to your production instance.

## Before you begin

Roles required: security\_admin, and either sn\_kmf.crypto\_manager or sn\_kmf.admin

As a customer administrator, you can access and install the Code Signing \[com.glide.code\_signing\_enterprise\] plugin from the ServiceNow Plugin portal. To learn more about the use cases of Code Signing, see [Exploring Code Signing](../concept/explore-code-signing.md).

## About this task

Code Signing jobs with signed update sets are used to turn the Code Signing feature on or off. There’s no other method for this functionality. This process includes the following:

-   Create two Code Signing jobs in the trusted instance, one to turn on Code Signing and one to turn off Code Signing.

    -   The **Turn On** scheduled job starts the process of MID Server validation of signed code.
    -   The **Turn Off** scheduled job stops the MID Server validation of signed code.
    By default, Code Signing applies to all MID servers. However, if you need to restrict Code Signing to a specific subset of MID servers, you can achieve this by using the ECC firewall.

    **Note:** When turning off Code Signing, the system property is marked to **false**, but the Code Signing trusted friends list is still available.

-   Put the **Turn on Code Signing Property** job into an update set.
-   Bring the job into production.
-   Use the **Turn on Code Signing Property** job in production if the signature is verified to originate from a trusted instance.

## Procedure

1.  In your trusted instance, navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for "\*Turn" in the name field.

3.  Select **Turn on Code Signing Property**.

    ![Shows the jobs to turn on or off the Code Signing feature for Circle of Trust.](../../key-management-framework/image/turnonoff-codesigning.png)

    The **Scheduled Script Execution** form load. This form contains information to enable the Code Signing property. The jobs create update sets that contain the jobs and validated signatures through the Code Signing process.

    ![Scheduled Script Execution form is loaded.](../../key-management-framework/image/export-signedjob-prod.png)

4.  To execute the script immediately, sign the certificate, create the update set, and select **Export signed job to production**.

    You can also configure the script to run on a designated schedule.

5.  Navigate to **System Update Sets** &gt; **Local Update Sets**.

6.  Open each of the Code Signing property update sets and select **Export to XML**.

7.  Log in to the production instance.

8.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

9.  Select the **Import Update Set from XML** button, and select the Code Signing property update set.

10. Select **Choose File** and upload and commit the update sets.

11. Return to the scheduled jobs list by navigating to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

12. Open the **Turn on Code Signing Property** job record.

13. Select the **Prerequisite Check** button at the top of the form.

    ![Prerequisite Check button](../image/prereq-button.png)

14. Select the **Execute Now** button after the prerequisite check is complete.

    The **Turn on Code Signing Property** scheduled job starts the process of MID Server validation of signed code.

15. In the navigator, enter `sn_kmf_record_signature.list` to open the **KMF Signature Records** list, and filter for records where the **KMF Signature Purpose** is `Circle of Trust`.

    The trust relationship has moved the jobs over and when the jobs are used the signature verification process executes. If the jobs, signatures, and certificates are all part of the Circle of Trust, then Code Signing with Circle of Trust can be turned on.

16. In the navigator, enter `sys_properties.list` to open the system properties list.

17. Search for **com\_snc\_kmf\_signature.validation.flag** and ensure that the value is set to **true**.

18. Verify that a new property **com\_snc\_kmf\_signature.validation.certificate** is listed in the table.

    ![Code Signing certificates available in System Properties.](../../key-management-framework/image/syspropertie-kmf-cert.png "System Properties")

    Use the Circle of Trust job in production to verify the trust relationship. No direct job can be executed in production that attempts to sign code. See [Configuring Code Signing](../concept/config-code-signing.md) for details on configuration options.


**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

