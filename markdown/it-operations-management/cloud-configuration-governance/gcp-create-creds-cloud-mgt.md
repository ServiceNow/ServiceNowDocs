---
title: Specify the credentials that Cloud Provisioning and Governance: Google Cloud Connector uses to access Google Cloud Platform data
description: To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you open the Google Cloud Console to identify the Google Cloud Platform project that will have programmatic access to your Google Cloud Platform data. You then securely store the credentials in a service account in your instance.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Day 1 setup guide for Google Cloud through Cloud Services Catalog Terraform Connector, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Specify the credentials that Cloud Provisioning and Governance: Google Cloud Connector uses to access Google Cloud Platform data

To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you open the Google Cloud Console to identify the Google Cloud Platform project that will have programmatic access to your Google Cloud Platform data. You then securely store the credentials in a service account in your instance.

## Before you begin

Roles required:

-   Operations in the Google Cloud Console require the Google administrator role.
-   Operations in Cloud Provisioning and Governance require the sn\_cmp.cloud\_admin role.

## About this task

Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings.

## Procedure

1.  If you have already generated the credentials that is used by the Google Cloud, skip to the final step.

    Otherwise, continue with the next step.

2.  On the Google Cloud Console dashboard, select the project.

3.  Navigate to **APIs &amp; Services** &gt; **Credentials**.

4.  On the **Credentials** tab, click **Create credentials** &gt; **Service account key**, and then create the key.

    Specify the **JSON** key type.

5.  Identify the credentials that Google Cloud, Discovery, and the Cloud Services Catalog \(CSC\) Terraform Connector should use on your instance to access data from the Google Cloud Platform.

    1.  Open the JSON key file in a text editor.

    2.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Credentials**, click **New** and then select **Google Credentials**.

    3.  Specify the **Name** of the credentials to register with the instance.

        For example, enter `Google credentials-1` and then copy/paste values from the JSON key file into the form fields. Paste the `private_key` value into the **Secret key** field and the `client_email` value into the **EMail** field.

        ![Specifying the Google Cloud Platform credentials in the instance](../image/gcp-copy-cred-to-sn-form.png)

    4.  Select the **Active** check box to use the credentials and then click **Submit**.


