---
title: Run a scheduled job to populate Technology Lifecycle Management lifecycle record identifier
description: Run the Populate Number field in TPM Discovered Technologies job to populate missing Technology Lifecycle Management \(TLM\) lifecycle record identifiers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-run-job-to-populate-tpm-lifecycle-identifier.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Run a scheduled job to populate Technology Lifecycle Management lifecycle record identifier

Run the **Populate Number field in TPM Discovered Technologies** job to populate missing Technology Lifecycle Management \(TLM\) lifecycle record identifiers.

## Before you begin

Ensure the Technology Lifecycle Management \(sn\_apm\_tpm\) plugin version 1.9.0. is installed and activated.

Role required: admin

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

TLM lifecycle record identifiers are automatically generated on creating a TLM record using the Technology Lifecycle Management \(sn\_apm\_tpm\) plugin version 1.9.0. However, for TLM lifecycle records generated using previous versions of the TLM plugin don't have any lifecycle record identifiers. The TLM record identifiers of these TLM lifecycle records must be generated using the **Populate Number field in TPM Discovered Technologies** job.

\[Omitted image "tpm-lifecycle-record.png"\] Alt text: TLM lifecycle record identifier highlighted on the Technology Portfolio page.

On selecting a TLM lifecycle record identifier, more information on the TLM lifecycle record is displayed.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Find and open the scheduled job **Populate Number field in TPM Discovered Technologies**.

3.  Select **Execute Now**.

    **Note:** You must verify that your application scope is set to Technology Lifecycle Management. For information on how to change the application scope, see [Select an application from the application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_SelectAnAppFromTheAppPicker.md)


## Result

The missing TLM lifecycle record identifiers are generated for the older TLM lifecycle records.

**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-work-with-tpm.md)

**Related topics**  


[Activate the Technology Lifecycle Management \(TLM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-install-tpm.md)

[Manage the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-tpm.md)

[Update TLM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/update-tpm-data.md)

