---
title: Configure the workspace URL for contract metadata extraction notifications
description: Configure an extension point to update the workspace URL in email notifications, so that users can navigate to the correct workspace and view the extracted metadata.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-config-ext-wrkspc-email.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure the workspace URL for contract metadata extraction notifications

Configure an extension point to update the workspace URL in email notifications, so that users can navigate to the correct workspace and view the extracted metadata.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, search for `sn_cm_gen_ai.PopulateUrlForMetadataExtractionRequestRecordEXT`.

3.  Select the record.

4.  Select the **Create implementation** related link.

5.  On the Script Include form, fill in the fields.

    \[Omitted image "cmpro-me-workspace-url.png"\] Alt text: Script for workspace URL in metadata extraction email notification.

    For a description of the field values, see [Scripted Extension Point form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/scripted-extension-point-form-fields.md).

6.  In the **Script** field, update the script to define the parent record’s table and specify the workspace URL to be included in the email notifications.

    -   In the `appliesTo` function, add the table name of the parent record.
    -   In the `getWorkspaceUrl` function, add the workspace URL.
7.  Select **Update**.


## Result

The configured workspace URL appears in the metadata extraction email notification.

For more information on enabling the notification for contract metadata extraction, see [Enable notification for contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-config-notf-na-metadata.md).

**Parent Topic:**[Configuring contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-conf-metadata-extraction.md)

**Related topics**  


[Create use cases for contract metadata extraction]()

[Map a use case for contract metadata extraction]()

[Configure system properties for contract metadata extraction]()

[Enable notification for contract metadata extraction]()

[Configure an extension point to add contract metadata]()

