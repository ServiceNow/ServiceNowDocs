---
title: List page in the IT Remediation Workspace
description: The List view in the IT Remediation Workspace permits remediation owners to view the records \(VITs, AVITs, CVITs, and TRs\) assigned to them and their assignment groups, and remediate these vulnerabilities and misconfigurations. You can also view the list of preferred solutions that are recommended for remediating the host vulnerable items. Along with these lists, you can view the list of the exception requests and penetration test assessment requests raised by you, penetration test findings associated with your penetration test assessment requests, supported libraries and other supported data.
locale: en-US
release: xanadu
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Exploring the IT Remediation Workspace, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# List page in the IT Remediation Workspace

The List view in the IT Remediation Workspace permits remediation owners to view the records \(VITs, AVITs, CVITs, and TRs\) assigned to them and their assignment groups, and remediate these vulnerabilities and misconfigurations. You can also view the list of preferred solutions that are recommended for remediating the host vulnerable items. Along with these lists, you can view the list of the exception requests and penetration test assessment requests raised by you, penetration test findings associated with your penetration test assessment requests, supported libraries and other supported data.

Roles required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(TRs\)

The lists and links on the List page provide you with easy access to records and tasks. It contains two tabs:

-   **Lists** tab: Displays the default lists for remediation efforts, remediation tasks, vulnerable items \(VITs, AVITs, and CVITs\), solutions, exceptions, and configuration test results \(TRs\), etc. For more information, see the following table.
-   **My Lists** tab: Displays any list that you’ve renamed from the List tab and any list that you create.

    You can also create your own list of records. For more information, see [Create a list in the IT Remediation Workspace](../../vulnerability-response/task/vr-ws-IT-list-view.md).


**Tip:**

If you set the **sn\_vul\_cmn\_ws.navigate\_to\_workspace** system property to `true`, upon selecting the predefined filter links in the Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Test Results module in Configuration Compliance under the **All** menu, these links open in the List page in the IT Remediation Workspace.

For example, if you select **Assigned to My Groups** by navigating to **All** &gt; **Vulnerability Response** &gt; **Remediation Tasks** &gt; **Assigned to My Groups**, this link is redirected to the IT Remediation Workspace. The Assigned to my group list in the Remediation Tasks module opens in the List page of the IT Remediation Workspace if you have a remediation owner role. To view the host remediation tasks, group the tasks by **Record Type**.

You can hide the record count on a list using the **glide.ui.list.seismic.omit.count** system property. For more information on how to turn off/on the record count display on a list, see the [KBB0010402](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KBB0010402) KB article.

## Lists tab

The following lists are displayed:

<table id="table_gkm_1lr_55b"><thead><tr><th>

List item

</th><th>

Description

</th><th>

Applications required

</th><th>

Role Required

</th></tr></thead><tbody><tr><td>

**Remediation Tasks**

</td><td>

View the list of remediation tasks and navigate to the desired task to start working on them. The following lists are available:-   **Assigned to you**: Lists all the host, application, container and Test result remediation tasks that are assigned to you.
-   **Assigned to my group**: Lists all the host, application, container and Test result remediation tasks that are assigned to the assignment groups to which you belong to.

Group the tasks by the Record type to categorize them into host, application, container and configuration test results remediation tasks. Remediation tasks that are created by the remediation task rules in the classic UI have an empty Remediation effort.

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(TRs\)

</td></tr><tr><td>

**Impacted assets**

</td><td>

View the list of assets that are impacted. The following lists are available:-   **Assigned to you**: Lists all the host, application, container and Test result remediation tasks that are assigned to you.
-   **Assigned to my group**: Lists all the host, application, container and Test result remediation tasks that are assigned to the assignment groups that you belong to.

</td><td>

Vulnerability Response

</td><td>

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(TRs\)

</td></tr><tr><td>

**Host Vulnerable items**

</td><td>

View the list of host vulnerable items and navigate to the desired item to start working on them. This lists are available:-   **Assigned to me**: List of host vulnerable items assigned to you for remediation.
-   **Assigned to my group**: List of host vulnerable items assigned to the assignment groups that you belong to.

</td><td>

Vulnerability Response

</td><td>

sn\_vul.remediation\_owner for host vulnerable items \(VITs\)

</td></tr><tr><td>

**Application Vulnerable items**

</td><td>

View the list of host vulnerable items and navigate to the desired item to start working on them. The following lists are available:-   **Assigned to me**: List of application vulnerable items assigned to you for remediation.
-   **Assigned to my group**: List of application vulnerable items assigned to the assignment groups to which you belong to.

</td><td>

Application Vulnerability Response

</td><td>

sn\_vul.app\_security\_champion

</td></tr><tr><td>

**Container Vulnerable items**

</td><td>

View the list of container vulnerable items and navigate to the desired item to start working on them. This list view contains:-   **Assigned to me**: List of container vulnerable items assigned to you for remediation.
-   **Assigned to my group**: List of container vulnerable items assigned to the assignment groups to which you belong to.

</td><td>

Container Vulnerability Response

</td><td>

sn\_vul\_container.remediation\_owner

View the list of assessments needed to perform post incident review.

</td></tr><tr><td>

**Configuration Test Results**

</td><td>

View the list of test results and navigate to the desired record to start working on them. This list view contains:-   **Assigned to me**: List of configuration test results assigned to you for remediation.
-   **Assigned to my group**: List of configuration test results assigned to the assignment groups that you belong to.

</td><td>

Configuration Compliance

</td><td>

sn\_vulc.remediation\_owner

</td></tr><tr><td>

**Solutions**

</td><td>

Lists the solutions from the solution management application. The Solutions list is displayed if the Vulnerability Solution Management application is installed.

 -   **All**: Shows all the available solutions which you use to remediate the host vulnerable items.
-   **Highest Supersedence**: Shows all the solutions which are used to populated Preferred Solutions.
-   **With Vulnerable items**: Show the solutions which are being used as Preferred Solution on Vulnerable Items.

</td><td>

Vulnerability Response

</td><td>

sn\_vul.remediation\_owner

</td></tr><tr><td>

**Exception requests**

</td><td>

-   **My requests**: List of all the exception, false positive, and unassign approval requests raised by you for host, application, and container vulnerable items and their remediation tasks.
-   **My requests \(configuration compliance\)**: List of all the exception, false positive, and unassign approval requests raised by you for the test results and their remediation tasks that you are working on.

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(TRs\)

</td></tr><tr><td>

**Libraries**

</td><td>

-   **NVDs**: A comprehensive library of vulnerability intelligence maintained by the National Institute of Standards and Technology \(NIST\). List of vulnerabilities found by NVD and includes security checklists, security-related software flaws, misconfigurations, product names, and impact metrics including exploits.
-   **CWEs**: List of community-developed software weakness types. Each CWE record also includes an associated knowledge article that describes the weakness.
-   **App Vulnerabilities**:
-   **TPEs**: List of imported third-party vulnerabilities in your instance. Contains a list of related references, vulnerable items, exploits, and CVEs.
-   **Tests**: Tests imported from the third party integrations with which the test results must comply.
-   **Test Groups**: List of test groups/policies imported from the third party integrations. A test group contains a set of tests.

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(TRs\)

</td></tr><tr><td>

**CMDB**

</td><td>

-   **Discovered items**: List of all the discovered items.
-   **Discovered container images**:

</td><td>

Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance

</td><td>

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(TRs\)

</td></tr><tr><td>

**Penetration Test Assessment Requests**

</td><td>

Penetration testing assessment requests submitted to security team by you for performing a security assessment of any business application. This list contains:-   **Assigned to Me**: List of Penetration Test Assessment Requests raised by you.
-   **Assigned to My Groups**: List of Penetration Test Assessment Requests raised by the users in your assignment groups.

</td><td>

Application Vulnerability Response

</td><td>

sn\_vul.app\_security\_champion

</td></tr><tr><td>

**Penetration Test Findings**

</td><td>

List of vulnerabilities identified during the Pen Test Assessment performed by the security team:-   **Assigned to Me**: List of Penetration Test Findings assigned to you for remediation.
-   **Assigned to My Groups**: List of Penetration Test Findings assigned to your assignment groups for remediation.

</td><td>

Application Vulnerability Response

</td><td>

sn\_vul.app\_security\_champion

</td></tr><tr><td>

**Supporting Data**

</td><td>

This list view contains:-   **Authoritative Sources**: List of authoritative sources that provide the summary information which is useful to research the source publications that were used to create the record.
-   **Technologies**: List of technologies that provide the summary information about each authoritative sources and citation \(also known, in Qualys, as a framework\).

</td><td>

Configuration Compliance

</td><td>

sn\_vulc.remediation\_owner

</td></tr></tbody>
</table>**Related topics**  


[Use the List view in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/task/vr-ws-vmws-list-view-duplicate.md)

