---
title: Working with technology portfolio audit details
description: The  Technology portfolio audit tab shows audit information for your applications. An entry in this table indicates that at least one lifecycle for that software product or hardware model was either approximated, or not found, or doesn’t exist.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace, Technology Portfolio view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Working with technology portfolio audit details

The  **Technology portfolio audit** tab shows audit information for your applications. An entry in this table indicates that at least one lifecycle for that software product or hardware model was either approximated, or not found, or doesn’t exist.

The data in the **Technology portfolio audit** table is fetched from the TPM Technology Lifecycle Exception \[sn\_apm\_tpm\_technology\_lifecycle\_exception\] table.

As an admin user, you can run the **Populate TPM Discovered Technologies and Lifecycles** scheduled job on-demand to calculate the technology lifecycle risk for your application portfolio. The scheduled job executes the script generating the lifecycle risk dates including end of support date, end of extended support date, and end of life date for your software products and hardware models by querying the ITAM content library.

For more details, see [Schedule a job to generate TPM lifecycle data](../../task/schedule-job-generate-tpm-data.md) and [Run a scheduled job to generate TPM lifecycle data](../../task/run-scheduled-job-update-tpm-data.md).

Whether the script runs on demand or scheduled, you can view the results in the **Enterprise Architecture Workspace** &gt; **Setup** &gt; **Logs**.

## Benefits of running a technology portfolio audit

If the software product full version is 9.2.1, it may be that the **End of Support** lifecycle version in the Software Asset Management content library was only full version 9.2. This audit table helps you to evaluate the lifecycle matching information based on the details of the products being used in your organization. The table helps you to identify whenever an exact lifecycle version match or no valid lifecycle version could be found against the software product or hardware model version used in your organization.

-   **[View technology portfolio audit risk details](../../task/eaw-task/eaw-view-audit-risk-details.md)**  
You can view all your technology portfolio details in the Enterprise Architecture Workspace.

**Parent Topic:**[Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](eaw-tpm.md)

**Related topics**  


[Technology portfolio audit form](../../reference/eaw-reference/eaw-technology-portfolio-audit-form.md)

