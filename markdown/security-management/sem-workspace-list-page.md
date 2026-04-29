---
title: Security Exposure Management Workspace List view
description: The List view in the Security Exposure Management Workspace permits vulnerability and security managers and analysts to view remediation progress on records, drill down into records, and view the status of their approval requests and exceptions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Security Exposure Management Workspace, Explore, Unified Security Exposure Management, Security Operations]
---

# Security Exposure Management Workspace List view

The List view in the Security Exposure Management Workspace permits vulnerability and security managers and analysts to view remediation progress on records, drill down into records, and view the status of their approval requests and exceptions.

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

These lists and links provide you with easy access to records and tasks. It contains two tabs:

-   **Lists** tab: Displays the default lists for remediation efforts, remediation tasks, vulnerable items, configuration test results, solutions, exceptions, and libraries.
-   **My Lists** tab: Displays any lists that you’ve renamed from the Lists tab and any lists that you create.

    You can also create your own list to monitor remediation progress. For more information, see [Create a customized list of records](../task/sem-create-custom-list.md).


## Lists tab

The following table shows the lists available in the Lists tab of the List page:

**Tip:**

If the **sn\_vul\_cmn\_ws.navigate\_to\_workspace** system property is set to `true` by an admin, upon selecting the predefined filter links in the Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response and Configuration Compliance modules from the **All** menu, these links open in the List page of the Security Exposure Management Workspace based on your role.

For example, if you select **Assigned to My Groups** by navigating to **All** &gt; **Security Exposure Management** &gt; **Remediation Tasks** &gt; **Assigned to My Groups**, this link is redirected to the Security Exposure Management Workspace. The **Assigned to My Groups** list in the **Remediation Tasks** module opens in the List page of the Security Exposure Management Workspace if you have the vulnerability admin or analyst role. To view the host remediation tasks group the tasks by Record Type.

You can hide the record count on the lists using the **glide.ui.list.seismic.omit.count** system property. For more information on how to turn off/on the record count on a list, see the [KBB0010402](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KBB0010402) KB article.

<table id="table_gkm_1lr_55b"><thead><tr><th>

List item

</th><th>

Description

</th><th>

Modules

</th><th>

Roles Required

</th></tr></thead><tbody><tr><td>

Remediation efforts \(REs\)

</td><td>

List of **Active** REs and **All** the REs assigned to your assignment groups.Group the remediation efforts by **Record Type** to categorize them by host vulnerable items, application vulnerable items, container vulnerable items and configuration test results.

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin for container vulnerable items \(CVITs\)
-   sn\_vulc.admin for configuration test results \(CTRs\)

</td></tr><tr><td>

Impacted Assets

</td><td>

Contains the following lists:-   **Assigned to me**: List of impacted assets assigned to you for remediation.
-   **Assigned to my group**: Impacted assets assigned to your assignment groups for remediation.

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

</td></tr><tr><td>

Remediation tasks

</td><td>

Contains the following lists:-   **Active**: List of all the active host, application, container and Test result remediation tasks.
-   **All**: List of both active and inactive host, application, container and Test result remediation tasks.
-   **Assigned to me**: List of Remediation tasks assigned to you for remediation.
-   **Assigned to my group**: Remediation tasks assigned to your assignment groups for remediation.
-   **Multiple Deferrals**: Lists findings that you've deferred multiple times.

Group the remediation tasks by **Record Type** to categorize them by host vulnerable items, application vulnerable items, container vulnerable items and configuration test results.

**Note:** The Remediation tasks list includes tasks generated during the Remediation Effort creation in the Security Exposure Management Workspace, as well as those created manually and by remediation task rules and other processes in the classic UI. The Remediation effort column will be empty for any remediation tasks that were not created as part of the Remediation Effort.

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin for container vulnerable items \(CVITs\)
-   sn\_vulc.admin for configuration test results \(CTRs\)

</td></tr><tr><td>

Host Vulnerable items

</td><td>

Contains the following lists-   **Active**: List of all the active host vulnerable items.
-   **All**: List of both active and inactive host vulnerable items.
-   **Assigned to me**: List of host vulnerable items assigned to you for remediation.
-   **Assigned to my group**: List of host vulnerable items assigned to your assignment groups for remediation.

</td><td>

Vulnerability Response

</td><td>

sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin

</td></tr><tr><td>

Application Vulnerable items

</td><td>

Contains the following lists:-   **Active**: List of all the active application vulnerable items.
-   **All**: List of both active and inactive application vulnerable items.
-   **Assigned to me**: List of application vulnerable items assigned to you for remediation.
-   **Assigned to my group**: List of application vulnerable items assigned to your assignment groups for remediation.

You can create a new application vulnerable item by selecting the **New** button.

</td><td>

Application Vulnerability Response

</td><td>

sn\_vul.app\_sec\_manager

</td></tr><tr><td>

Container Vulnerable items

</td><td>

Contains the following lists:-   **Active**: List of all the active container vulnerable items.
-   **All**: List of both active and inactive container vulnerable items.
-   **Assigned to me**: List of container vulnerable items assigned to you for remediation.
-   **Assigned to my group**: List of container vulnerable items assigned to your assignment groups for remediation.

</td><td>

Container Vulnerability Response

</td><td>

sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin

</td></tr><tr><td>

Configuration Test Results

</td><td>

Contains the following lists:-   **Active**: List of all the active test results.
-   **All**: List of both active and inactive test results.
-   **Assigned to me**: List of test results assigned to you for remediation.
-   **Assigned to my group**: List of test results assigned to your assignment groups for remediation.

</td><td>

Configuration Compliance

</td><td>

sn\_vulc.admin

</td></tr><tr><td>

Solutions

</td><td>

Contains the following lists:-   **All**: Shows all the available solutions which you can use to remediate the host vulnerable items.
-   **Highest Supersedence**: Shows all the solutions which is used to populated Preferred Solutions.
-   **With Vulnerable items**: Shows the solutions which are being used as Preferred Solution on Vulnerable Items.

</td><td>

Vulnerability Response

</td><td>

sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin

</td></tr><tr><td>

Exceptions

</td><td>

Shows the approval states for all the exception and false positive requests associated with your assignment groups.-   **All**: List of the exception, false positive, and unassign approval requests related to VITs, AVITs, and CVITs and their remediation tasks \(VUL, AVUL, and CVUL\).
-   **My requests**: List of all the exception, false positive, and unassign approval requests raised by you for host, application, and container vulnerable items and their remediation tasks.
-   **All \(Configuration Compliance\)**: List of the exceptions, false positive, and unassign approval requests related test results and remediation tasks \(CTR\#\).
-   **My requests \(configuration compliance\)**: List of all the exception, false positive, and unassign approval requests raised by you for the test results and their remediation tasks that you are working on.

Group the exceptions by **Record type** to categorize them by host vulnerable items, application vulnerable items, container vulnerable items and configuration test results.

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin for container vulnerable items \(CVITs\)
-   sn\_vulc.admin for configuration test results \(CTRs\)

</td></tr><tr><td>

Approvals

</td><td>

**Assigned to me**: Shows the approval requests assigned to you for processing. To process your approvals in the workspace, see [Approve or reject requests in the Security Exposure Management Workspace](../task/sem-approve-requests.md).

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin for container vulnerable items \(CVITs\)
-   sn\_vulc.admin for configuration test results \(CTRs\)

</td></tr><tr><td>

Libraries

</td><td>

Consists of the following lists:-   **CVEs \(NVD\)**: List of all the Common Vulnerability and Exposures \(CVEs\) from Vulnerability Response, Application Vulnerability Response, and Container Vulnerability Response.

**Note:** Starting with v30.3 of Vulnerability Response, it is renamed to Vulnerabilities.

-   **TPEs**: List of imported third-party vulnerabilities in your instance. Contains a list of related references, vulnerable items, exploits, and CVEs.
-   **CWEs**: List of all the Common Weakness Enumerations \(CWEs\) from Vulnerability Response, Application Vulnerability Response, and Container Vulnerability Response.
-   **Vulnerable Software**: List of all the software vulnerable entries.
-   **App vulnerabilities**: List of all the third-party application vulnerability entries.
-   **Test Groups**: List of all the Configuration Compliance test groups. You can view the percentage of CI compliance and test results compliance for a Test Group in the record view.
-   **Tests**: List of all the tests from Configuration Compliance. You can view the percentage of test results compliance for a test in the record view.
-   **Compensating Controls**: List of all the compensating controls which can be used for risk reduction requests. You can add a compensating control by clicking **New**. For more information on how to add a compensating control, see [Add a compensating control to the library](../task/sem-create-compensatory-control.md).

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin for container vulnerable items \(CVITs\)
-   sn\_vulc.admin for configuration test results \(CTRs\)

</td></tr><tr><td>

CMDB

</td><td>

Contains the following lists-   **Discovered items**:List of all the discovered items.
-   **Discovered container images**: List of Container images. These container images provide information on the image ID, Docker image, and the image repository along with the layer information.
-   **Discovered Applications**: List of all discovered applications, including details such as application name, source, state, integration instance, and more.

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin for container vulnerable items \(CVITs\)
-   sn\_vulc.admin for configuration test results \(CTRs\)

</td></tr><tr><td>

Penetration Test Assessment Requests

</td><td>

Contains the following lists:-   **Active**: List of active Penetration Test Assessment Requests.
-   **All**: List of both active and inactive Penetration Test Assessment Requests
-   **Assigned to me**: List of Penetration Test Assessment Requests raised by you.
-   **Assigned to my group**: List of Penetration Test Assessment Requests raised by the users in your assignment groups.

For information on how to create a penetration test assessment request, see [Create a new penetration testing assessment request](../../vulnerability-app-vuln-mgmt/task/create-new-pen-test-assesment-req.md).

</td><td>

Application Vulnerability Response

</td><td>

sn\_vul.app\_sec\_manager

</td></tr><tr><td>

Penetration Test Findings

</td><td>

Contains the following lists:-   **Active**: List of all the active Penetration Test Findings.
-   **All**: List of both active and inactive Penetration Test Findings.
-   **Assigned to me**: List of Penetration Test Findings assigned to you for remediation.
-   **Assigned to my group**: List of Penetration Test Findings assigned to your assignment groups for remediation.
-   **Validation Pending**: List of Penetration Test Findings that are pending validation after remediation.

For information on how to create a penetration test findings, see [Create penetration test findings based on an assessment questionnaire](../../vulnerability-app-vuln-mgmt/task/create-penetration-test-findings.md).

</td><td>

Application Vulnerability Response

</td><td>

sn\_vul.app\_sec\_manager

</td></tr><tr><td>

Patches

</td><td>

**All**: List of all the available patches that can be used to remediation host vulnerable items.

</td><td>

Vulnerability Response

</td><td>

sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin

</td></tr><tr><td>

Supporting Data

</td><td>

Contains the following lists:-   **Authoritative Sources**: List of authoritative sources that provide summary information which is useful to research the source publications.
-   **Technologies**: List of technologies that provide the summary information about each authoritative sources and citation \(also known, in Qualys, as a framework\).

</td><td>

Configuration Compliance

</td><td>

sn\_vulc.admin

</td></tr></tbody>
</table>**Related topics**  


[Use the List view in the Security Exposure Management Workspace](../task/sem-ws-list-view.md)

