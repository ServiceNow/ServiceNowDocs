---
title: Configure the match content for the incident
description: Provide the configuration to store the sensitive information internally, on the ServiceNow storage, or on the external cloud storage, such as Azure Storage or AWS S3 bucket. Retrieve the stored content while accessing the DLP IR Incident.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-02-03"
reading_time_minutes: 1
breadcrumb: [Create a new incident profile for Microsoft DLP integration, Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Configure the match content for the incident

Provide the configuration to store the sensitive information internally, on the ServiceNow® storage, or on the external cloud storage, such as Azure Storage or AWS S3 bucket. Retrieve the stored content while accessing the DLP IR Incident.

## Before you begin

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst

## Procedure

1.  On the progress bar, click the **Match Content Configuration** step.

2.  On the form, fill in the fields.

<table id="table_ott_mkl_nwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Store Match Content

</td><td>

Option to store the matched content. **Important:** Enable this option to store the match content, and retrieve and display the match content when a DLP incident is opened in the workspace.

For information on the External Cloud Storage configuration, see [Install and configure the Microsoft DLP integration](install-configure-microsoft-dlp-integration.md).

</td></tr><tr><td>

Storage Source for Match content

</td><td>

Option to choose whether to store the matched content internally, on the ServiceNow® storage, or externally, on the cloud storage.

</td></tr><tr><td>

External Cloud Credentials

</td><td>

The External Cloud Storage where the match content gets stored. You can refer to the External Cloud Credentials added for the Storage configuration. This option is visible only when the **Store Match Content** field is selected.

</td></tr><tr><td>

Delete Match Content on Incident Deletion

</td><td>

Option to delete the incident match content from the external cloud storage. This option is visible only when the **Store Match Content** field is selected.

</td></tr></tbody>
</table>3.  Click **Continue** and move to the Scheduling section.


**Parent Topic:**[Create a new incident profile for Microsoft DLP integration](create-profile-microsoft-dlp-integration.md)

