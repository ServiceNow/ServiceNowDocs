---
title: Engagement home page
description: This page provides detailed information of an engagement including internal and external stakeholders, upcoming touchpoints, initiatives, and blueprints.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Customer success, Use, Customer Success Management]
---

# Engagement home page

This page provides detailed information of an engagement including internal and external stakeholders, upcoming touchpoints, initiatives, and blueprints.

To view this page, follow these steps:

1.  Login as a user with the `sn_acct_lc.customer_success_agent` role.
2.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workpace** and select the **List** icon.
3.  Navigate to **Customer Success** &gt; **All Engagements** and select **Number** column to open the engagement record. You can also navigate to this page from the [Success portfolio dashboard](account-lifecycle-success-landing.md).

The following options are available:

-   Discuss: Select **Discuss** to start a sidebar discussion about this engagement. In the pop-up window, select the participants who must participate in the discussion, enter a brief message, and select **Start discussion**. A window appears with a link to the record for this engagement. Select **Open record** and start the discussion. When the discussion has been completed, you can see the details in the **Activity stream**.
-   Refresh Health: Select this option to update the health score for this engagement.
-   Create success play: See [Create a success play](../task/account-lifecycle-create-success-play.md)
-   Internal play: See [Create an internal play playbook](../task/account-lifecycle-create-internal-play-playbook.md).
-   Risk signal: See [Create a risk signal](../task/account-lifecycle-create-risk-signal.md).
-   Success case: See [Create a customer play](../task/account-lifecycle-create-success-case-playbook.md).
-   Touchpoint: See [Create a touchpoint](../task/account-lifecycle-create-touchpoint.md).

The Engagement record page contains the following tabs:

-   **Overview**
-   **Health**
-   **Success blueprint**
-   **Product adoption**
-   **Renewal and expansion**
-   **Engagement hierarchy**

![Engagement page.](../image/customer-success-engagement-related-item.png)

## Overview \(engagement\)

This tab provides a high-level overview of the engagement. It includes the following details:

-   Header: The header section shows the health score of the engagement over the last six weeks and the last active touchpoint.
-   Engagement details: Shows the contract value, engagement stage, go-live date, account with which it’s associated, and the renewal date. Select the Edit icon to modify the engagement details and select **Save**.
-   Customer team: Shows the key customer contact that you have specified for this engagement. This information is also displayed in the Related Items section under Applicable Customer Teams.
-   Squad: Shows the squad members associated with the engagement.
-   Account team: The team members handling the account. This information is also displayed in the Related Items section under Applicable Account Teams.
-   Upcoming touchpoints: Shows any upcoming touchpoints for this engagement. Select the link to drill down to the Touchpoint record page.
-   Risk signals and issues: Shows any new, overdue, high priority, or unaddressed risks or issues.
-   Work items: This section shows the activities and tasks associated with this engagement. You can sort the list by Priority or Due Date. You can view all the work items or view items belonging to a specific category by selecting one of the following filters from the **View** drop-down list:

    -   Internal plays
    -   Internal play tasks
    -   Success case
    -   Success initiative
    -   Success task
    To filter this list further, select one of the work items filters like New, Blocked to view specific items in the list.


## Health

In this tab, you can see the current health score and the health of the engagement over the last 12 weeks. This helps identify gaps and issues that need attention. Select **Refresh Health** to view the updated health score.

![Engagement health score.](../image/account-lifecycle-engagement-health.png)

In the Indicators section, you see the metrics used to calculate the health score for this engagement. See [Calculate the engagement health score](../task/account-lifecycle-setup-health-defn.md). For each metric, you’ll the target score, weight, and gap percentage. Select the **Sort by** option to sort the metrics listed by score, weight, and gap.

## Success blueprint

In this tab, you can view the success objectives associated with this engagement. You can view the high-level details of each success objective including Due date, Start date, Key contact, Assigned to, and Products. If the success blueprint hasn’t been defined, select **Create success blueprint**. See [Create a success blueprint](../task/account-lifecycle-create-blueprint.md) for instructions on creating a success blueprint. You can do the following:

-   Sort by: You can sort the list by Due date of the objectives.
-   View by State: Select one of the states from the drop-down list. This can be:
    -   All
    -   In Progress
    -   Paused
    -   Closed
    -   New
    -   Canceled
-   Select the ![](../../../reuse/icons/product-icons/open-link-right-outline-24.svg) icon to drill down to the [Success objective record page](account-lifecycle-view-success-object.md).
-   View initiative roadmap: Select this link to view the success initiative roadmap, which the engagement details including the current health, stage, and the next renewal date for the engagement.

![success blueprint.](../image/customer-success-blueprint.png)

## Product adoption

In this tab, you can view the product adoption score for all applicable sold products associated with this engagement. The adoption score is determined using the calculated metrics that have been configured for the sold products. See [Define a calculated metric data source](../task/account-lifecycle-define-data-source-calculate.md) for more details.

![product adoption](../image/product-adopt.jpg)

The following details are included:

-   The chart displays product adoption scores across the past 12 weeks, broken down by week. By hovering over data points, you can view the quantity of products sold within each adoption category \(Low, Medium, High, and None\) for any given week.
-   The pie chart shows a snapshot of current adoption score distribution as of today's date. Select Total products to drill down to view the Product Usage list. You can drill down to a specific product usage record.
-   The list of sold products associated with this engagement is displayed. Select ![](../../../reuse/icons/product-icons/open-link-right-outline-24.svg) to drill down to the [Product usage record](account-lifecycle-prod-cap-usage.md) page.
    -   View by: You can filter the list displayed by:
        -   All
        -   Activated
        -   Planned
        -   No plan
        -   Deactivated
    -   Sort by: You can sort the list by:
        -   Customer priority
        -   Adoption score
        -   Business criticality
        -   Activation status

## Renewal and expansion

In this tab, you can view a list of all active contracts associated with this engagement. You can view the high-level details of each contract and select the link to drill down to the Contract page. ![renewal expansion.](../image/customer-success-renewal-expansion.png)

## Engagement hierarchy

![engagement hierarchy.](../image/engagement-hierarchy-overview.png)

This tab provides an overview of customer's engagement health. This tab is a conditional tab by default isn’t visible. To view this tab, one child engagement must be available in the related engagement. It includes the following details:

-   Total engagements: Shows the total number of engagements and total contract value related to the account.
-   Risk signals by probability: Shows the risks associated with this account.
-   Squad work by status: Shows the work status of the team involved with this account.
-   Engagement hierarchy: Shows the active engagements for this account. In the engagements, shows the parent and child relationship.

Any hierarchy that forms a cycle isn’t a valid hierarchy.

## Customer timeline

The customer timeline tracks and shows all the related activities of the engagement record. To support the application 23 activities are shipped out of box in the engagement record.

![customer timeline.](../image/customer-timeline-engagement.png)

To configure the activities in the engagement record, see [Configure activity types for the Customer History view](https://www.servicenow.com/docs/access?context=configure-activity-types-ca&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Contextual side panel component

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Engagement record page includes the following tabs.

<table id="table_zjq_nmb_wfc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Recommended Actions**

</td><td>

The Recommended Actions tab includes [AI search](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) functionality. Agents can use AI search to find relevant resources or resolutions for customer issues.The search feature displays an initial set of search results based on the text in the case short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search.

From the list of search results, agents can do the following:

-   Select a source to see search results of that type.
-   Filter the list of search results.
-   Sort the list of search results.
-   Open the search results in full view in a record subtab.
-   Take the following actions:
    -   View and attach article
    -   Perform other actions such as reading articles in full view, flagging articles, or marking articles as helpful or unhelpful.
-   View successful actions by selecting the Actions history icon.

For more information, see [Use AI search in Recommended Actions to resolve cases](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](https://www.servicenow.com/docs/access?context=nba&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

</td></tr><tr><td>

**Activity Stream**

</td><td>

The activity stream component displays a list of the activities occurring on a case record.

</td></tr><tr><td>

**Related Items**

</td><td>

The Related Items tab provides access the case-related lists.The Engagement record page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of records available in a related list. When expanded, the records in a related list are displayed in card format.

</td></tr><tr><td>

**Attachment**

</td><td>

The Attachments tab provides access to case-related attachments. From this tab, agents can view and download attachments.

</td></tr><tr><td>

**Email Templates**

</td><td>

The Email Templates tab provides access to available email templates. These templates contain default values for fields that agents can add to email messages. These default values can include the recipients \(email addresses in the To, Cc, and Bcc fields\), the sender, the subject of the email, and text to include in the message body.

</td></tr><tr><td>

**Template**

</td><td>

The Templates tab provides access to available form templates that enable agents to automatically populate fields on new records. Agents can manually apply a template when creating a record such as an incident or change.

</td></tr><tr><td>

**Record Information**

</td><td>

The Record Information tab shows overview of the engagement record.

</td></tr><tr><td>

**Customer timeline**

</td><td>

The Customer timeline tab shows visual display of the Engagement records activities.

</td></tr></tbody>
</table>-   **[Success objective record page](account-lifecycle-view-success-object.md)**  
This page provides a detailed view of the success objective and its related outcomes and initiatives as defined in the success blueprint.
-   **[Primary success outcome record page](account-lifecycle-view-sucess-outcome.md)**  
A primary success outcome refers to the result or goal that is used to measure the achievement of a success objective.

**Parent Topic:**[Customer success](account-lifecycle-use-cust-success.md)

