---
title: Run a scheduled job to populate Technology Lifecycle Management lifecycle record identifier
description: Run the Populate Number field in TPM Discovered Technologies job to populate missing Technology Lifecycle Management \(TLM\) lifecycle record identifiers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/eaw-run-job-to-populate-tpm-lifecycle-identifier.html
release: yokohama
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 2
breadcrumb: [Managing the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace, Technology Portfolio view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Run a scheduled job to populate Technology Lifecycle Management lifecycle record identifier

Run the Populate Number field in TPM Discovered Technologies job to populate missing Technology Lifecycle Management \(TLM\) lifecycle record identifiers.

## Before you begin

Ensure the Technology Lifecycle Management \(sn\_apm\_tpm\) plugin version 1.9.0. is installed and activated.

Role required: admin

## About this task

TLM lifecycle record identifiers are automatically generated on creating a TLM record using the Technology Lifecycle Management \(sn\_apm\_tpm\) plugin version 1.9.0. However, for TLM lifecycle records generated using previous versions of the TLM plugin don't have any lifecycle record identifiers. The TLM record identifiers of these TLM lifecycle records must be generated using the Populate Number field in TPM Discovered Technologies job.

\[Omitted image "tpm-lifecycle-record.png"\] Alt text: TPM lifecycle record identifier highlighted on the Technology Portfolio page.

On selecting a TLM lifecycle record identifier, more information on the TLM lifecycle record is displayed.

## Procedure

1.  Navigate to **All** &gt; ** System Definition ** &gt; ** Scheduled Jobs**.

2.  Find and open the  scheduled job **Populate Number field in TPM Discovered Technologies**.

3.  Select  ** Execute Now**.

    **Note:** You must verify that your application scope is set to Technology Lifecycle Management. For information on how to change the application scope, see [Select an application from the application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_SelectAnAppFromTheAppPicker.md)


## Result

The missing TLM lifecycle record identifiers are generated for the older TLM lifecycle records.

**Parent Topic:**[Managing the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-tpm.md)

**Related topics**  


[Activate the Technology Lifecycle Management \(TLM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-install-tpm.md)

[Managing the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-tpm.md)

[Update TPM data for business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/update-tpm-data.md)

