---
title: Combined Common Governance, Risk, and Compliance feature release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Common Governance, Risk, and Compliance feature from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-commongovernanceriskandcompliancefeature-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Common Governance, Risk, and Compliance feature release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Common Governance, Risk, and Compliance feature from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Common Governance, Risk, and Compliance feature release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Common Governance, Risk, and Compliance feature to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Common Governance, Risk, and Compliance feature.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[System-generated recommendations for Workspace issue management](https://servicenow-staging.fluidtopics.net/access?context=issues-in-workspace&family=washingtondc&ft:locale=en-US)**
    -   Use system-generated recommendations for a remediation task that is related to an issue. User responses are recorded in the action history of the remediation task.
    -   Use system-generated recommendations that are listed on the **Details** tab of an issue. You can refer to the top three recommendations when assigning an issue in the **Assigned to** field.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Management method in issue grouping](https://servicenow-staging.fluidtopics.net/access?context=issue-grouping-in-workspaces&family=xanadu&ft:locale=en-US)**

Group and manage issues from a parent issue, or manage child issues independently using the group issue management method. When you select the Management method as **Manage parent**, the child issues inherit the values of the **State**, **Response**, and **Explanation** fields from the parent issue. When **Manage child** is selected, the child issue maintains its own **State**, **Response**, and **Explanation** fields individually.

As a part of this feature, the following two new fields were added on the issue record in the Issue grouping section:

    -   **Group level**: Identifies whether an issue is a child, parent, or a standalone issue.
    -   **Management method**: Indicates whether the issue is managed from a parent issue or as an individual child issue.
-   **[Confidentiality and inheritance enhancements in issue grouping](https://servicenow-staging.fluidtopics.net/access?context=confidential-records&family=xanadu&ft:locale=en-US)**

Streamline the issue grouping process with the following enhancements:

    -   Add confidential child issues only under a confidential parent issue.
    -   Add nonconfidential child issues under a confidential or nonconfidential parent issue.
    -   Change a confidential parent issue to nonconfidential. This action will remove all confidential child issues under the parent issue, making them standalone issues after you save the record.

**Note:** When you change a nonconfidential child issue to confidential, which is under a nonconfidential parent issue, this action removes the child issue from the nonconfidential parent issue. The child issue becomes a standalone issue and no longer linked to the parent issue.

-   **[GRC Licensing Overview dashboard](https://servicenow-staging.fluidtopics.net/access?context=grc-licensing-summary-dashboard&family=xanadu&ft:locale=en-US)**

Use the self-service GRC Licensing Overview dashboard to track license usage trends and next month's projected usage based on role allocation. You can see the monthly aggregated counts of license consumption across different product families including Integrated Risk Management, Business Continuity Management, and Privacy Management. The following infrastructure enhancements were made:

    -   Expanded the unique user usage table capacity from 9 months to 12 months.
    -   License consumption details are archived for five years.
    -   Aggregated monthly counts of license usage are stored.
-   **[Introducing GRC Employee role](https://servicenow-staging.fluidtopics.net/access?context=grc-common-roles&family=xanadu&ft:locale=en-US)**

Install the new GRC Employee User application and assign the GRC Employee role to your employees. The users with the GRC Employee role can perform the following activities from the Employee Center:

    -   Read and acknowledge organizational policies.
    -   Report risk events and issues.
    -   Request policy exceptions.
    -   Report a compliance case to the Compliance team.
    -   Raise inquiries and requests to the Compliance team.
**Note:** This update is only applicable to customers who are entitled to and have installed the GRC Employee User application. For more details, review the entitlement on the subscription dashboard or contact ServiceNow.

-   **[Lite operator role enhancements](https://servicenow-staging.fluidtopics.net/access?context=grc-common-roles&family=xanadu&ft:locale=en-US)**

The sn\_audit.reader and sn\_audit.approver roles were added as Lite Operator roles. These new roles are available to all customers.

The following Operator roles are reclassified as Lite Operator roles when GRC Employee User application and GRC Business User Lite applications are installed:

    -   sn\_grc.business\_user
    -   sn\_risk\_advanced.ara\_assessor
    -   sn\_irm\_cont\_auth.authorization\_official
    -   sn\_irm\_cont\_auth.reader
    -   sn\_irm\_cont\_auth.executive\_read
**Note:** This reclassification is only applicable to customers who are entitled to and have installed the GRC Employee User application. For more details, review the entitlement on the subscription dashboard or contact ServiceNow.

-   **[Entity filter deletion or modification warning](https://servicenow-staging.fluidtopics.net/access?context=what-is-an-entity-filter&family=xanadu&ft:locale=en-US)**

Avoid the unintended consequences of deleting or modifying an entity filter with a warning message. This message includes an impact analysis of the affected entity, risk, and control records.

-   **[Document designer integration](https://servicenow-staging.fluidtopics.net/access?context=configuring-audit-word-based-templates&family=xanadu&ft:locale=en-US)**

You can update and add content using Microsoft 365 for ServiceNow Reporting now integrated with the Document designer application to insert data and reports into a Microsoft Word document.

-   **[Role attribution to licensing mapping tab](https://servicenow-staging.fluidtopics.net/access?context=grc-licensing-summary-dashboard&family=xanadu&ft:locale=en-US)**

Use the Role attribution to licensing mapping tab on the GRC Licensing Overview dashboard to understand how licensing applies to roles and users. This tab helps you with the following:

    -   Identify the license treatment for all the default GRC roles.
    -   Determine the license treatment of a specific user based on their assigned roles.
    -   Determine the license treatment for a specific combination of roles.
-   **[Map stakeholders in entity](https://servicenow-staging.fluidtopics.net/access?context=entities-in-risk-ws&family=xanadu&ft:locale=en-US)**

Use the Stakeholders related list in the entity form to define stakeholders with customizable roles relevant to single and composite entities. This feature enables effective team involvement in risk assessments and risk assessment projects. You can add persona, group, and users in the stakeholder list.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Common Governance, Risk, and Compliance feature features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Issue management privileges](https://servicenow-staging.fluidtopics.net/access?context=grc-common-roles&family=washingtondc&ft:locale=en-US)**
    -   For managing an issue, the same levels of privileges are assigned to the GRC manager and the GRC user. If you have the GRC manager role, the GRC user role, the Business User role, or the Business User Lite role, you can create an issue.
    -   Create or update a remediation task if you're an Issue persona or if the remediation task is assigned to you.
-   **[Domain separation in GRC](https://servicenow-staging.fluidtopics.net/access?context=grc-domain-separation&family=washingtondc&ft:locale=en-US)**

The following changes have been made to the domain assignment process to manage data segregation by the Managed Service Providers related to entities, and other related objects, such as risks, controls, and control objectives:

    -   Profile generation job uses a domain iterator to generate entities and other related objects into the correct domains.
    -   Revised domain inheritance and assignment logic by adding new business rules to assign the correct domain when creating entities, risks, controls, and related objects.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Common Governance, Risk, and Compliance feature features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Common Governance, Risk, and Compliance feature features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Common Governance, Risk, and Compliance feature.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install GRC by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install GRC by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Common Governance, Risk, and Compliance feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Common Governance, Risk, and Compliance feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Common Governance, Risk, and Compliance feature, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Common Governance, Risk, and Compliance feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Common Governance, Risk, and Compliance feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Assign remediation tasks using system-provided suggestions for remediation and potential assignees in the **Assigned to** field.
-   Update an issue if you have either the Issue manager role, the Issue manager group role, the Assigned to role, or the Assignment group role.

 See [Governance, Risk, and Compliance](https://servicenow-staging.fluidtopics.net/access?context=r_WhatIsGRC&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Group issues within your workspaces to organize and manage related issues, and streamline the issue grouping process with the confidentiality and inheritance enhancements.
-   Select an existing standalone issue to serve as the parent for other related issues during issue grouping.
-   Track license consumption across different product families using the GRC Licensing Overview dashboard.
-   Use the new GRC Employee role to report or request GRC workflows, and read and acknowledge policies from the Employee Center \(Only applicable to customers who are entitled to and have installed the GRC Employee User application\).
-   Read and approve audits, and read audit related tables with the enhanced Lite Operator changes.
-   Update and add content using Microsoft 365 for ServiceNow Reporting now integrated with the Document designer application.

 See [Governance, Risk, and Compliance](https://servicenow-staging.fluidtopics.net/access?context=r_WhatIsGRC&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

