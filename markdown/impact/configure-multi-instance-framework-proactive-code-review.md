---
title: Configure the Multi-Instance Framework for Proactive Code Check
description: Configuring the Multi-Instance Framework explains how to connect data movement from non-production instances to production instances. The mTLS must be installed and configured to connect non-production instances to production instances to allow data movement and synchronization. Before creating trust profiles, managing instances must also be configured.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-04-24"
reading_time_minutes: 2
breadcrumb: [Configuring Proactive Code Check, Configuring the Impact Store Application, Impact Store Application, Impact]
---

# Configure the Multi-Instance Framework for Proactive Code Check

Configuring the Multi-Instance Framework explains how to connect data movement from non-production instances to production instances. The mTLS must be installed and configured to connect non-production instances to production instances to allow data movement and synchronization. Before creating trust profiles, managing instances must also be configured.

## About this task

The following tasks summarize the steps required to install and configure the Multi-Instance Framework for Proactive Code Check.

-   Submit a   Now Support ticket to enable ADCv2 mTLS, if not enabled.
-   Submit a  Now Support ticket to install the Multi-Instance Framework mTLS \(com.glide.mif.mtls\) plugin.
-   Log in to non-production instances and add required fields.
-   Edit and create required trust profiles in the production instance.
-   Sync the trust profiles to non-production instances.

## Before you begin

ADCv2 mTLS is required alongside the Multi-instance Framework mTLS \(com.glide.mif.mtls\) plugin for data sync to function correctly. See [Cross-instance application trust configuration](https://www.servicenow.com/docs/access?context=grant-access-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for additional information on multi-instance management.

**Important:** Identify the primary production instance and all secondary instances where Impact Proactive Code Check will be used. The primary instance displays a consolidated view of non-production instance scan results.

Role required: admin

## Procedure

1.  Verify if the instance has ADCv2 mTLS enabled by accessing the URL:`<instance>.service-now.com/adcv2/supports_tls`

    ![URL example to verify mTLS installation](../image/verify-mTLS-url.png)

    |Value|Action|
    |-----|------|
    |**True**|Proceed to the next step.|
    |**If not True**|Submit a ticket to enable ADCv2 mTLS. Verify that ADCv2 mTLS has been enabled and then proceed to the next step.|

2.  Submit a  Now Support ticket to install the com.glide.mif.mtls plugin.

3.  Wait for 24 hours after the com.glide.mif.mtls plugin is installed.

4.  Repeat steps 1 to 3 on all of the required production and non-production instances.

5.  Log in to a non-production development instance with the role admin.

    **Note:** Steps 5 - 7 are required for each non-production instance.

6.  Navigate to **All** &gt; **Multi-Instance Management** &gt; **Manager Instances**.

    ![Navigation path to MIF management for manager instances.](../image/multi-instance-manager.png)

7.  Create a record with the following values:

    |Field|Value|
    |-----|-----|
    |Application|Impact Health|
    |Manager Instance|&lt;primary production instance&gt;|

    ![Manager instances form.](../image/pcc-select-mgr-instance.png)

8.  Log in to the primary production instance as admin.

9.  Navigate to **All** &gt; **Multi-Instance Management** &gt; **Managed Instances**.

10. Verify that you see a record for each non-production instance for which Production instance is assigned as manager in the previous steps.

11. Navigate to **All** &gt; **Multi-Instance Management** &gt; **Application Trust profiles**.

12. Open the record **Trust Profile for Impact Health**.

    ![Impact Health Trust Profile in Application Trust Profiles.](../image/pcc-trust-profile.png)

13. Under the Active MIF Trust Profile Items related list, select **New**.

14. Fill in the fields for the trust profile.

    |Field|Field Value|
    |-----|-----------|
    |Capability|Proactive Code Check Data Transfer|
    |Application|Impact Health|
    |Application Capability Version|1.0.0|
    |Active|true|
    |Trusting Instance|&lt;non-production instance1&gt;|
    |Trusted Instance|&lt;primary production instance&gt;|
    |Description|Optional|

    ![PCC New Trust Profile record.](../image/pcc-new-trust-profile.png)

    **Note:** A trust profile must be completed for each non-production instance to be registered as a Trusting Instance.

15. Navigate to **All** &gt; **Multi-Instance Management** &gt; **Application Trust profiles**.

16. Select **Sync Trust Profiles**.

    ![Sync Trust Profiles in Application Trust Profiles.](../image/pcc-sync-trust-profiles.png)

17. Navigate to **All** &gt; **Multi-Instance Management** &gt; **Trusting Instances**.

18. Verify that you see a record for each non-production instance that you added to your trust profile.

    See [Basic trust configuration for data sync applications](https://www.servicenow.com/docs/access?context=grant-access-other-instances&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for additional information.


