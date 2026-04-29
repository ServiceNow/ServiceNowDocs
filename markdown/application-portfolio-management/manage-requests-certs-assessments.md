---
title: Managing requests, certifications, and assessments
description: As an Enterprise Architect, you can manage all requests. You can view the status of the certifications, assessments, and technology portfolio audit information.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Managing requests, certifications, and assessments

As an Enterprise Architect, you can manage all requests. You can view the status of the certifications, assessments, and technology portfolio audit information.

## My approvals

The **My Approvals** tab lists the requests that are waiting for your approval.

## My requests

The **My Requests** tab shows the list of requests assigned to you as an approver. By default, it shows all the requests as a paginated result. Select **View All** to see the full list. You can open a request record by selecting it to approve or reject the request.

## My certifications

The **My Certifications** tab shows the list of certifications that are relevant to you. Specifically, the tab displays certifications that meet any of the following criteria:

-   Assigned directly to you
-   Assigned to any group you belong to
-   Assigned to any group you manage
-   Assigned to any of your direct reports

You can use this tab to keep your business applications inventory up to date by periodically certifying the data in the business applications table. Keeping your business application data current helps you assess your business applications accurately, as several indicators depend on this data.

Select **View All** to see the full list of certifications. Select the certification number, certification schedule, or certification instance to see more details.

If you have directly installed the 4.0.0 version of the EA Workspace store application, the data in the My certifications table is fetched from the CMDB Data Management Task \(cmdb\_data\_management\_task\) table.

If you upgraded your EA Workspace from a previous version to the 4.0.0 version, you may see that your certification data is still fetched from the Certification Schedules \(cert\_schedule\) table. In this case, you must migrate your certification policies to the CMDB Data Management Certification Policies \(sn\_cmdb\_ws\_dm\_certification\_policy\) table. For more information, see [Import certification schedules in to Data Manager](../task/eaw-task/eaw-convert-cert-schedules-to-cert-policies.md)and [Publish a draft Data Manager policy](../task/eaw-task/eaw-publish-a-draft-policy.md).

## Assessments

The **Assessments** tab shows the list of assessments for your applications that help you to evaluate and score your business applications based on qualitative inputs. Application indicators are business metrics that assess the applications across dimensions such as cost, quality, technical risk, investments, user satisfaction, and business value.

Each indicator periodically captures related application data that is used to calculate the application score. The assessment of applications is done on an extensible framework, which is based on the various configured indicators. If you require indicators other than the preconfigured ones to calculate the application score, then you can create an indicator based on your business requirements.

You can select **View all** to see the list of assessments. Select the assessment number and metric type to see more details.

## Technology Portfolio audit

The  **Technology Portfolio Audit** tab shows audit information for your applications. An entry in this table indicates that at least one lifecycle for that software product or hardware model was either approximated, or not found, or doesn’t exist. For example, if the software product full version is 9.2.1, it may be that the End of Support lifecycle version in the Software Asset Management Content library was only full version 9.2. This audit table helps you to evaluate the lifecycle matching information based on the details of the products being used in your organization. The table helps you to identify whenever an exact lifecycle version match or no valid lifecycle version could be found against the software product or hardware model version used in your organization.

The data in the Technology Portfolio Audit table is fetched from the TPM Technology Lifecycle Exception \[sn\_apm\_tpm\_technology\_lifecycle\_exception\] table.

As an admin user, you can run the **Populate TPM Discovered Technologies and Lifecycles** scheduled job on-demand to calculate the technology lifecycle risk for your application portfolio. The scheduled job executes the script generating the lifecycle risk dates including end of support date, end of extended support date, and end of life date for your software products and hardware models by querying the ITAM content library. For more details, see [Run a scheduled job to generate TPM lifecycle data](../task/eaw-task/eaw-run-scheduled-job-update-tpm-data.md). Whether the script runs on demand or scheduled, you can view the results in the Portfolio &gt; Technology Portfolio Management &gt; Logs page.

<table id="table_frn_x3m_cxb"><thead><tr><th>

Column name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Application type. Choices are:-   Software
-   Hardware

</td></tr><tr><td>

Software product

</td><td>

Name of the software product.

</td></tr><tr><td>

Product version

</td><td>

Version number of the product.

</td></tr><tr><td>

Product edition

</td><td>

Edition of the product. For example, Standard.

</td></tr><tr><td>

Product full version

</td><td>

Full version of the product.

</td></tr><tr><td>

Hardware model

</td><td>

Hardware model that is associated with the software product.

</td></tr><tr><td>

Verification status

</td><td>

Verification status of the product. Choices are:-   Need to verify
-   Verified
-   Rejected

</td></tr><tr><td>

Comments

</td><td>

Customer comments.

</td></tr><tr><td>

Lifecycle phase

</td><td>

Lifecycle phase of the product.

</td></tr><tr><td>

Phase start date

</td><td>

Lifecycle phase start date.

</td></tr><tr><td>

Edition

</td><td>

Edition of the lifecycle.

</td></tr><tr><td>

Full version

</td><td>

Full version of the lifecycle.

</td></tr><tr><td>

Match notes

</td><td>

Notes by the customer.

</td></tr><tr><td>

Technology lifecycle

</td><td>

TPM technology lifecycle information of the software product or hardware model.

</td></tr></tbody>
</table>## Technical Debt

The  **Technical Debt** tab shows the list of TRM technical debt that are created for the products that are not aligned with the TRM phases and standards. A technical debt indicates either there is no TRM product record for a software product used by one or more business application or the TRM product has one or more internal lifecycle phases that restrict its usage.. In this table, you can view the TRM products and associated business applications details, and the reason for the technical debt. A custom scheduled job **Populate TRM technical debts in the EA Workspace** runs and creates an entry in the TRM Technical Debt table. For more details, see [Manage TRM technical debt](eaw-concept/eaw-manage-trm-technical-debt.md) and [Run a scheduled job to update TRM technical debt data in EA Workspace](../task/eaw-task/eaw-run-job-trm-tech-debts.md).

<table id="table_ak2_5fg_tyb"><thead><tr><th>

Column name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TRM product

</td><td>

Name of the TRM product. A software product that is having version specific life cycles.

</td></tr><tr><td>

Business Application

</td><td>

Name of the business application associated with the TRM product.

</td></tr><tr><td>

Software product model

</td><td>

Name of the software product model related to the TRM product.

</td></tr><tr><td>

TRM phase

</td><td>

Phase of the TRM product. The following TRM phases are available from the base system:-   Approved: The technology is approved for use.
-   Approved with Constraints: The technology can be used within the specified constraints specified in the comments.
-   Divest: A decision was taken to divest from the use of the technology.
-   Evaluation: This technology is being evaluated and can’t be used to production purposes.
-   Unapproved: The technology isn’t permitted to be used.

**Note:** You can modify these phases from the EA Workspace &gt; Setup &gt; TRM Phases page.

</td></tr><tr><td>

TRM level

</td><td>

The level \(Product or Product Lifecycle\) at which the technical debt is created.

</td></tr><tr><td>

Version

</td><td>

Version of the software product. Usually, the name of the Software product model contains this version.

</td></tr><tr><td>

Reason

</td><td>

The reason to explain why the technical debt was created.

</td></tr><tr><td>

Last run

</td><td>

Shows the time stamp when the custom scheduled job **Populate TRM technical debts in the EA Workspace** is run to update the table with technical debt.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Enterprise Architecture Workspace](explore-eaw.md)

**Related topics**  


[Approve or reject a modeling diagram request](../task/eaw-task/eaw-approve-diagram-req.md)

