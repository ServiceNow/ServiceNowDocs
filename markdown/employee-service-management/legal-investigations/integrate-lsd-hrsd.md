---
title: Set up Legal Investigations with HR Service Delivery Employee Relations
description: Set up Legal Investigations with HR Service Delivery Employee Relations to enable complaint requests to be transferred between Legal and HR departments.
locale: en-US
release: australia
product: Legal Investigations
classification: legal-investigations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Set up Legal Investigations with HR Service Delivery Employee Relations

Set up Legal Investigations with HR Service Delivery Employee Relations to enable complaint requests to be transferred between Legal and HR departments.

## Before you begin

Ensure you have the following ServiceNow® apps installed:

-   Legal Investigations \(sn\_lg\_investigate\)
-   Universal Request \(com.snc.universal\_request\)
-   HR Service Delivery Employee Relations \(com.sn\_hr\_employee\_relations\)

    **Note:** You must approve the requested Restricted Caller Access \(RCA\) with source scope as Legal Investigations and target scope as Human Resources Employee Relations and Evidence Management.


Optionally, you can install the Anonymous Reporting Center \(ARC\) plugin \(com.sn\_anonymous\_report\_center\) to enable transfer of tickets between Legal and Human Resource \(HR\) departments. ARC requires a HRSD Pro/Enterprise license in addition to the Legal Investigations subscription.

Role required: admin

## Procedure

1.  Activate the record producers for complaints submission via the **Quick Link** in Employee Center.

    For more information, see [Record producers for legal investigations](../reference/record-producers-legal-investigation.md).

    1.  Navigate to **All** &gt; **Service Catalog** &gt; **Record Producers**.

    2.  Search and open record producers with the name **Ethics Complaints**.

    3.  Verify that **Universal Request \[universal\_request\]** is selected in the **Table name** field.

        There are two record producer records that enable the ethics complaint submission options: one via the Employee Center portal's **Quick Link** and another via the Anonymous Report Center portal.

    4.  Select **Active** to activate the record producers for universal requests.

    5.  Click **Update**.

    **Note:** You must deactivate the record producers mapped to the Ethics \[sn\_lg\_ops\_ethics\] table.

2.  Review the base system assignment group, **Compliance**, to which the ethics complaint requests will be assigned by default, and make the required changes.

    1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

    2.  Open the assignment group that you want to configure to assign the compliant requests by default.

    3.  In the Roles related list, verify that the following roles are assigned to the assignment group.

        -   agent\_workspace\_user
        -   sn\_uni\_req.routing\_agent
        -   interaction\_agent
    4.  In the Group Members related list, add users to triage and work on the submitted complaints.

        These users must be assigned the sn\_uni\_req.sensitiveinfo\_agent role and the following department-specific roles:

        -   sn\_lg\_investigate.fulfiller, for users in the Legal department
        -   sn\_hr\_er.case\_writer, for users in the HR department
    For more information, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  If you configured an assignment group other than the base system assignment group, make it the default assignment group for ethics complaint requests by updating the system property.

    1.  Copy the sys\_id of the assignment group configured in the last step.

    2.  Navigate to **All** &gt; **Legal Administration** &gt; **Legal Investigations Admin** &gt; **Properties**.

    3.  Paste the sys\_id of the assignment group in the **Default assignment group** field.

4.  Configure the Universal Request property to determine how the primary ticket should be handled while transferring between the departments.

    1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration** &gt; **Properties**.

    2.  Under **Transfer type**, update the **Select the transfer type to determine how the primary ticket is handled** property \(**sn\_uni\_req.transfer\_type**\) to **Service**.

        **Note:** If a service isn’t selected while transferring the ticket, then the transfer happens to the default service configured for the selected transfer department.​

    For more information, see [Universal Request properties](../../universal-request/reference/ur-properties.md).

5.  For Legal to HR complete data copy to execute, activate **HRERDepartmentTransferPostProcessor**.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

    2.  Search for the **HRERDepartmentTransferPostProcessor** script include and activate it.

6.  If the **Ethics Complaint** quick link is not visible in the **Quick links** section of Employee Center portal, manually run the **addQuickLinkToECPortal** fix script.


