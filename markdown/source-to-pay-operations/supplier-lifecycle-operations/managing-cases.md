---
title: Manage supplier cases from the Source-to-Pay Workspace
description: You can create and manage supplier cases for suppliers in the Source-to-Pay Workspace.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Manage supplier cases from the Source-to-Pay Workspace

You can create and manage supplier cases for suppliers in the Source-to-Pay Workspace.

On the Source-to-Pay Workspace List page, navigate to **Lists** &gt; **Cases** and select any of the sub-modules to view a list of cases. Select the link to the case in the Number column to open the Case Details page.

For more information about viewing cases in the Source-to-Pay Workspace, see [View a supplier case from the Source-to-Pay Workspace](../task/view-supp-case-ws.md).

The Case Details page contains the following options.

<table id="table_zxk_1nb_nsb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Multi-tab interface

</td><td>

When you select a link for a case, each case opens in a separate tab in the top-left corner, which enables you to easily navigate between multiple open cases. Each case displays information in the following tabs:

-   **Playbook** tab: Displays either the playbook to onboard a supplier or the generic playbook depending on the case type. For more information, see [Use the supplier onboarding playbook to onboard suppliers](use-playbooks-onboard-supp.md#) and [Case playbook for specific supplier case types](gen-playbook-cases.md).
-   **Details** tab: Contains the Supplier Case, Summary Details, and Resolution Information sections.
    -   Supplier Case: Displays information about the supplier case.
    -   Summary Details: Displays the parent case, related location, start and end dates for the case.
    -   Resolution Information: Displays the resolution information and close notes for the case.
-   **Supplier Information** tab: Displays information about the supplier. For more information about this tab, see [Supplier Information tab](supp-info-tab.md).
-   **Supplier Tasks** tab: Lists the supplier tasks for the supplier case.
-   **Related Cases** tab: Lists the child supplier cases related to the parent supplier case.

If you've not installed Third-party Risk Management, the playbook creates supplier cases of types **Risk assessment** and **Tiering assessment**. The Supplier Risk Assessment and Supplier Tiering Assessment cases are child cases of the parent **Onboard a Supplier** case and are displayed on the **Related Cases** tab. The supplier owner or supplier manager assigns these assessment cases to the TPR assessor.

-   **Approvals** tab: Lists the approval records, their approval status, and the persons who need to approve this case.

**Important:** Supplier Lifecycle Operations creates an approval record if the "Ask For Approval" action is a part of any SLO flow. This approval record can be approved by the user who belongs to the Supplier Administrators group \(sys\_user\_group table\). For more information, see [Add a user to a group](https://www.servicenow.com/docs/access?context=t_AddAUserToAGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   **Risk Assessments** tab: Displays the risk assessments for a supplier.

If you have installed Third-party Risk Management, the playbook creates the risk assessment records and displays them in this tab.

-   **Tiering Assessments** tab: Displays the tiering assessments for a supplier.

If you have installed Third-party Risk Management, the playbook creates the tiering assessment records and displays them in this tab.

**Note:** The **Risk Assessments** and **Tiering Assessments** tabs are shown only for a supplier case of type **Supplier onboarding**.

-   **Draft Emails** tab: Displays a list of emails you saved as draft.
-   **Documents** tab: Enables you to manage supplier documents by uploading, updating and downloading the required documents

</td></tr><tr><td>

Compose section

</td><td>

Contains the Comments and Work notes \(Private\) widgets. The text that you enter in the Comments section are visible to everyone. However, the text that you enter in the Work notes \(Private section\) are visible only to internal users; customers cannot view them.

</td></tr><tr><td>

Activity stream

</td><td>

Displays all the processing activities, conversations, and changes that have happened since the case was opened. You can filter activities by post types, field changes, and flagged activities.

</td></tr><tr><td>

Contextual side panel

</td><td>

This panel appears below the UI actions. Select the supplier overview icon \(![Supplier overview icon.](../image/supp-overview-icon.png)\) to open the following panels:

-   Supplier overview: Displays the following information about the supplier.
    -   **Supplier**: Name of the supplier.
    -   **Short description**: Brief description about the supplier.
    -   **Risk rating**: The risk rating of the supplier.

The risk rating scale helps business users better understand risk assessment results. For example, in the default settings, risk scores in the 20 through 39 range indicate high risk, while scores in the 60 through 79 range indicate low risk.

Depending on the risk score of the supplier, the following risk ratings are displayed:

        -   1 - Very High
        -   2 - High
        -   3 - Moderate
        -   4 - Low
        -   5 - Very Low
For more information about risk ratings and risk scores, see [Set up risk rating scales for scoring](https://www.servicenow.com/docs/access?context=tprm-risk-rating-scales-config&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).

    -   **Onboarded**: Status of whether the supplier is onboarded into the ERP system. The options are Yes or No.
    -   **DUNS number**: Unique, 9-digit identifier for a supplier.
    -   Website: Website of the supplier.
    -   **Industry**: Industry to which the supplier belongs.
    -   **Country of Registration**: The country in which the supplier is registered.
-   Supplier contacts: Displays information about the supplier contacts. An Admin label next to the contact's name indicates that the contact is a primary contact. If a supplier has more than five supplier contacts, the **View all** option is displayed. Select **View all** to view a list of all the contacts for the supplier.

 Select the attachments icon \(![Attachments icon.](../image/attachments-icon.png)\) to open the Attachments panel, which enables you to attach documents to the case.

 Select the agent assist icon \(![Agent Assist icon.](../image/agent-assist-icon.png)\) to open the Agent Assist panel, which enables you to search for information across multiple sources such as catalog items, knowledge articles, supplier cases, problems, and open incidents.

</td></tr></tbody>
</table>-   **[Supplier Information tab](supp-info-tab.md)**  
The **Supplier Information** tab shows details about the supplier and the supplier contact, a summary of all the open and overdue cases, and a list of all the cases by their priority.
-   **[Sidebar for supplier cases in the Source-to-Pay Workspace](sidebar-smw.md)**  
Sidebar enables stakeholders to collaborate with others by getting into discussions when working on supplier cases.
-   **[Configure due dates for supplier cases](../task/configure-case-due-date.md)**  
Configure due dates for different case types so that the **Due date** field is auto-populated when you create supplier cases.
-   **[Case playbook for specific supplier case types](gen-playbook-cases.md)**  
Source-to-Pay Workspace includes a generic case playbook to complete supplier cases of specific case types.
-   **[Create a case on behalf of a supplier from the Source-to-Pay Workspace](../task/create-new-supplier-case.md)**  
Create a supplier case to track the progress of supplier tasks, resolve issues related to supplier products or services, and request additional information from a supplier.
-   **[Assign a supplier case to yourself from the Source-to-Pay Workspace](../task/assign-supp-case.md)**  
As a supplier manager, assign a case to yourself and start working on it.
-   **[Submit a supplier case from the Source-to-Pay Workspace](../task/submit-supplier-case.md)**  
Submit a supplier case in Draft state to indicate that it is ready to be worked on.
-   **[Complete a supplier case from the Source-to-Pay Workspace](../task/complete-supplier-case.md)**  
You can mark a supplier case as complete when you finish all the tasks related to that case.
-   **[Reopen a supplier case from the Source-to-Pay Workspace](../task/reopen-supplier-case.md)**  
Reopen a closed supplier case if you are not satisfied with the case resolution.
-   **[Add a related case to a supplier case from the Source-to-Pay Workspace](../task/add-related-case.md)**  
If a supplier case has related cases, you can add them to that supplier case from the Source-to-Pay Workspace.
-   **[View a supplier case from the Source-to-Pay Workspace](../task/view-supp-case-ws.md)**  
As a supplier manager, view a supplier case that requires your input or approval.

**Parent Topic:**[Using Source-to-Pay Workspace](use-supp-mgr-wsp.md)

**Related topics**  


[Create a supplier from the Source-to-Pay Workspace](../task/new-supplier.md)

[Source-to-Pay Workspace Supplier page](supp-ws-details-page.md)

[Manage internal stakeholders](manage-internal-stakeholders.md)

[Manage supplier contacts from the Source-to-Pay Workspace](managing-contacts-smw.md)

[Manage supplier tasks from the Source-to-Pay Workspace](managing-tasks.md)

[Offboard a supplier from the Source-to-Pay Workspace](../task/offboard-supplier.md)

[Accept an incoming chat request from the Source-to-Pay Workspace](../task/accept-chat-supp-ws.md)

[Interaction Management in Supplier Lifecycle Operations](interaction-mgmt-supplier-mgr-ws.md)

[Composing emails with predefined content from the Source-to-Pay Workspace](email-composer-slm-workspace.md)

[Overall supplier dashboard](overall-supplier-db.md)

[Create supplier case from Universal Request](../task/create-supplier-case-ur.md)

[Emails view for supplier managers](../task/enabling-emails-view-for-contacts.md)

[Configure due dates for supplier cases](../task/configure-case-due-date.md)

[Case playbook for specific supplier case types](gen-playbook-cases.md)

[Playbook for updating the supplier primary data](primary-playbook-cases.md)

[Create a case on behalf of a supplier from the Source-to-Pay Workspace](../task/create-new-supplier-case.md)

