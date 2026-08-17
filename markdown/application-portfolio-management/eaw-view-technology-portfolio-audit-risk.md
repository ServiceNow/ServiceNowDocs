---
title: Working with technology portfolio audit details
description: The  Technology portfolio audit tab shows audit information for your applications. An entry in this table indicates that at least one lifecycle for that software product or hardware model was either approximated, or not found, or doesn’t exist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-view-technology-portfolio-audit-risk.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace, Exploring Technology Portfolio view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Working with technology portfolio audit details

The  **Technology portfolio audit** tab shows audit information for your applications. An entry in this table indicates that at least one lifecycle for that software product or hardware model was either approximated, or not found, or doesn’t exist.

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The data in the Technology portfolio audit table is fetched from the TPM Technology Lifecycle Exception \[sn\_apm\_tpm\_technology\_lifecycle\_exception\] table.

As an admin user, you can run the **Populate TPM Discovered Technologies and Lifecycles** scheduled job on-demand to calculate the technology lifecycle risk for your application portfolio. The scheduled job executes the script to generate lifecycle risk dates by querying the ITAM content library. These dates include end of support, end of extended support, and end of life for your software products and hardware models.

For more details, see [Run a scheduled job to generate TLM lifecycle data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-scheduled-job-update-tpm-data.md).

Whether the script runs on demand or scheduled, you can view the results in the **Enterprise Architecture Workspace** &gt; **Setup** &gt; **Logs**.

## Benefits of running a technology portfolio audit

If the software product full version is 9.2.1, it may be that the **End of Support** lifecycle version in the Software Asset Management content library was only full version 9.2. This audit table helps you to evaluate the lifecycle matching information based on the details of the products being used in your organization. The table helps you to identify exact lifecycle version matches. It also identifies when no valid lifecycle version could be found against the software product or hardware model version used in your organization.

**Parent Topic:**[Manage the Technology Lifecycle Management \(TLM\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-tpm.md)

**Related topics**  


[View technology portfolio audit risk details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-audit-risk-details.md)

[Technology portfolio audit form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-technology-portfolio-audit-form.md)

