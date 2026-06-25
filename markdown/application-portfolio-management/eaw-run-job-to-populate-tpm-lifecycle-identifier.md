---
title: Run a scheduled job to populate Technology Portfolio Management lifecycle record identifier
description: Run the Populate Number field in TPM Discovered Technologies job to populate missing Technology Portfolio Management \(TPM\) lifecycle record identifiers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-run-job-to-populate-tpm-lifecycle-identifier.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with Technology Portfolio Management \(TPM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Run a scheduled job to populate Technology Portfolio Management lifecycle record identifier

Run the Populate Number field in TPM Discovered Technologies job to populate missing Technology Portfolio Management \(TPM\) lifecycle record identifiers.

## Before you begin

Ensure the Technology Portfolio Management \(sn\_apm\_tpm\) plugin version 1.9.0. is installed and activated.

Role required: admin

## About this task

TPM lifecycle record identifiers are automatically generated on creating a TPM record using the Technology Portfolio Management \(sn\_apm\_tpm\) plugin version 1.9.0. However, for TPM lifecycle records generated using previous versions of the TPM plugin don't have any lifecycle record identifiers. The TPM record identifiers of these TPM lifecycle records must be generated using the Populate Number field in TPM Discovered Technologies job.

\[Omitted image "tpm-lifecycle-record.png"\] Alt text: TPM lifecycle record identifier highlighted on the Technology Portfolio page.

On selecting a TPM lifecycle record identifier, more information on the TPM lifecycle record is displayed.

## Procedure

1.  Navigate to **All** &gt; ** System Definition ** &gt; ** Scheduled Jobs**.

2.  Find and open the  scheduled job **Populate Number field in TPM Discovered Technologies**.

3.  Select  ** Execute Now**.

    **Note:** You must verify that your application scope is set to Technology Portfolio Management. For information on how to change the application scope, see [Select an application from the application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_SelectAnAppFromTheAppPicker.md)


## Result

The missing TPM lifecycle record identifiers are generated for the older TPM lifecycle records.

**Parent Topic:**[Working with Technology Portfolio Management \(TPM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Activate the Technology Portfolio Management \(TPM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-install-tpm.md)

[Manage the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-tpm.md)

[Update TPM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/update-tpm-data.md)

