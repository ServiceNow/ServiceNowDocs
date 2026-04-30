---
title: Source-to-Pay Workspace Case Details page
description: The Source-to-Pay Workspace Case Details page is displayed when you select the link of a supplier case to view more details about that case.
locale: en-US
release: yokohama
product: Source-to-Pay Workspace
classification: source-to-pay-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [SLO landing page, Source-to-Pay Workspace landing page, Exploring Source-to-Pay Operations Workspace, Source-to-Pay Workspace, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay Workspace Case Details page

The Source-to-Pay Workspace Case Details page is displayed when you select the link of a supplier case to view more details about that case.

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
</table>