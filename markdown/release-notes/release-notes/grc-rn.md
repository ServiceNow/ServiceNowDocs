---
title: Common Governance, Risk, and Compliance feature release notes
description: The ServiceNow Governance, Risk, and Compliance \(GRC\) application enables an organization to continue to provide its business services during adverse operational events, such as a pandemic, extreme weather, or hacking. Governance, Risk, and Compliance was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# Common Governance, Risk, and Compliance feature release notes

The ServiceNow® Governance, Risk, and Compliance \(GRC\) application enables an organization to continue to provide its business services during adverse operational events, such as a pandemic, extreme weather, or hacking. Governance, Risk, and Compliance was enhanced and updated in the Xanadu release.

## GRC highlights for the Xanadu release

-   Group issues within your workspaces to organize and manage related issues, and streamline the issue grouping process with the confidentiality and inheritance enhancements.
-   Select an existing standalone issue to serve as the parent for other related issues during issue grouping.
-   Track license consumption across different product families using the GRC Licensing Overview dashboard.
-   Use the new GRC Employee role to report or request GRC workflows, and read and acknowledge policies from the Employee Center \(Only applicable to customers who are entitled to and have installed the GRC Employee User application\).
-   Read and approve audits, and read audit related tables with the enhanced Lite Operator changes.
-   Update and add content using Microsoft 365 for ServiceNow Reporting now integrated with the Document designer application.

See [Governance, Risk, and Compliance](https://www.servicenow.com/docs/access?context=r_WhatIsGRC&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** GRC is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Management method in issue grouping](https://www.servicenow.com/docs/access?context=issue-grouping-in-workspaces&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Group and manage issues from a parent issue, or manage child issues independently using the group issue management method. When you select the Management method as **Manage parent**, the child issues inherit the values of the **State**, **Response**, and **Explanation** fields from the parent issue. When **Manage child** is selected, the child issue maintains its own **State**, **Response**, and **Explanation** fields individually.

    As a part of this feature, the following two new fields were added on the issue record in the Issue grouping section:

    -   **Group level**: Identifies whether an issue is a child, parent, or a standalone issue.
    -   **Management method**: Indicates whether the issue is managed from a parent issue or as an individual child issue.
-   **[Confidentiality and inheritance enhancements in issue grouping](https://www.servicenow.com/docs/access?context=confidential-records&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Streamline the issue grouping process with the following enhancements:

    -   Add confidential child issues only under a confidential parent issue.
    -   Add nonconfidential child issues under a confidential or nonconfidential parent issue.
    -   Change a confidential parent issue to nonconfidential. This action will remove all confidential child issues under the parent issue, making them standalone issues after you save the record.

        **Note:** When you change a nonconfidential child issue to confidential, which is under a nonconfidential parent issue, this action removes the child issue from the nonconfidential parent issue. The child issue becomes a standalone issue and no longer linked to the parent issue.

-   **[GRC Licensing Overview dashboard](https://www.servicenow.com/docs/access?context=grc-licensing-summary-dashboard&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use the self-service GRC Licensing Overview dashboard to track license usage trends and next month's projected usage based on role allocation. You can see the monthly aggregated counts of license consumption across different product families including Integrated Risk Management, Business Continuity Management, and Privacy Management. The following infrastructure enhancements were made:

    -   Expanded the unique user usage table capacity from 9 months to 12 months.
    -   License consumption details are archived for five years.
    -   Aggregated monthly counts of license usage are stored.
-   **[Introducing GRC Employee role](https://www.servicenow.com/docs/access?context=grc-common-roles&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Install the new GRC Employee User application and assign the GRC Employee role to your employees. The users with the GRC Employee role can perform the following activities from the Employee Center:

    -   Read and acknowledge organizational policies.
    -   Report risk events and issues.
    -   Request policy exceptions.
    -   Report a compliance case to the Compliance team.
    -   Raise inquiries and requests to the Compliance team.
    **Note:** This update is only applicable to customers who are entitled to and have installed the GRC Employee User application. For more details, review the entitlement on the subscription dashboard or contact ServiceNow.

-   **[Lite operator role enhancements](https://www.servicenow.com/docs/access?context=grc-common-roles&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    The sn\_audit.reader and sn\_audit.approver roles were added as Lite Operator roles. These new roles are available to all customers.

    The following Operator roles are reclassified as Lite Operator roles when GRC Employee User application and GRC Business User Lite applications are installed:

    -   sn\_grc.business\_user
    -   sn\_risk\_advanced.ara\_assessor
    -   sn\_irm\_cont\_auth.authorization\_official
    -   sn\_irm\_cont\_auth.reader
    -   sn\_irm\_cont\_auth.executive\_read
    **Note:** This reclassification is only applicable to customers who are entitled to and have installed the GRC Employee User application. For more details, review the entitlement on the subscription dashboard or contact ServiceNow.

-   **[Entity filter deletion or modification warning](https://www.servicenow.com/docs/access?context=what-is-an-entity-filter&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Avoid the unintended consequences of deleting or modifying an entity filter with a warning message. This message includes an impact analysis of the affected entity, risk, and control records.

-   **[Document designer integration](https://www.servicenow.com/docs/access?context=configuring-audit-word-based-templates&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    You can update and add content using Microsoft 365 for ServiceNow Reporting now integrated with the Document designer application to insert data and reports into a Microsoft Word document.

-   **[Role attribution to licensing mapping tab](https://www.servicenow.com/docs/access?context=grc-licensing-summary-dashboard&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use the Role attribution to licensing mapping tab on the GRC Licensing Overview dashboard to understand how licensing applies to roles and users. This tab helps you with the following:

    -   Identify the license treatment for all the default GRC roles.
    -   Determine the license treatment of a specific user based on their assigned roles.
    -   Determine the license treatment for a specific combination of roles.
-   **[Map stakeholders in entity](https://www.servicenow.com/docs/access?context=entities-in-risk-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use the Stakeholders related list in the entity form to define stakeholders with customizable roles relevant to single and composite entities. This feature enables effective team involvement in risk assessments and risk assessment projects. You can add persona, group, and users in the stakeholder list.


## Activation information

Install GRC by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

