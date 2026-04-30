---
title: SPO list page
description: As a Procurement Case Management \(PCM\) Agent, view and work with your procurement cases, and view the knowledge base. When logged in as a Procurement Specialist however, you can also view and work with the various case types, knowledge base, orders, receipt acknowledgments, interactions, and primary data.
locale: en-US
release: xanadu
product: Source-to-Pay Workspace
classification: source-to-pay-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Source-to-Pay Workspace list page, Exploring Source-to-Pay Workspace, Source-to-Pay Workspace, Source-to-Pay Operations, Finance and Supply Chain]
---

# SPO list page

As a Procurement Case Management \(PCM\) Agent, view and work with your procurement cases, and view the knowledge base. When logged in as a Procurement Specialist however, you can also view and work with the various case types, knowledge base, orders, receipt acknowledgments, interactions, and primary data.

With an additional supplier role of sn\_supplier.fulfiller, a Procurement Specialist can view, work on, and also create supplier cases from the list view of Source-to-Pay Workspace.

**Note:** The app-supplier \(com.snc.sn\_supplier\_mgmt\) and app-supplier-common \(com.snc.sn\_slm\) plugins must also be installed to view supplier cases.

You can select each module and submodule to view the details in a list. Here, you can adjust the column widths, copy the URL, apply filters, and export the list to a desired file type. You can also edit a selected record or create a new record as required.

You can then open the record number link to view more details pertaining to that record, including related lists displayed as tabs, and the activity stream for that record that contains comments, work notes, and emails.

## Related list grouping

As a sourcing manager working on certain procurement objects, you can view all the similar related lists grouped at one place for your easy reference, under the **Related work**, **Agreements**, and **Sourcing approach** tabs. The following information is usually grouped under these tabs:

-   **Related work**
    -   Approval plans
    -   Purchasing tasks
    -   Purchasing SLAs
    -   Task SLAs
    -   Contract requests

        **Note:** This tab is available for sourcing requests, negotiation events, negotiations, purchase requisitions, and purchase lines, only if you have the Source-to-Pay Operations with Contract Management Pro plugin \(com.snc.sn\_spend\_clm\) installed.

    -   Cases
    -   Interaction-related records

        **Note:** This tab is typically available for cases.

-   **Agreements**
    -   Related contracts
    -   Signed contracts
    -   Draft contracts
    -   Other legal documents
-   **Sourcing approach**

    -   Sourcing requests
    -   Negotiations
    -   Purchase lines
    **Note:** This tab is typically available for negotiation events.

-   **Emails**
    -   Draft emails
    -   Sent emails

**Note:** You can customize the related lists to be displayed in these related work item tabs by updating the necessary client-side variables in the standard Record page that is shipped with Source-to-Pay Workspace.​ Any conflicts arising from previous customizations with the record page can be handled by identifying the difference in the macroponent file and merging the changes as required.​

## Form grouping

As sourcing and purchasing fulfillers working on sourcing requests in the Source-to-Pay Workspace, view the sourcing request form data in organized sections as follows, making it easier for you to find the information that you must focus on.

-   Sourcing Request
-   Requested Product
-   Negotiation Event

The Purchase Lines and Contract Requests related lists also display the information that are most important for the sourcing and purchasing fulfillers.

Further, the purchase line \(PRL\) form is organized into sections, displaying relevant fields, based on whether you’re viewing it as part of the sourcing and negotiating processes, or the purchasing process.

Here are the section details of a purchase line with details of the relevant fields.

-   Purchase Line

    **Note:** In case a purchase line is canceled as part of the sourcing process, this section provides details on the cancellation reason and canceled by. This information isn’t provided for active purchase lines.

-   Supplier and Pricing

    **Note:** As part of a purchase requisition, pricing related information such as starting unit price, negotiated unit price, total line amount, and so on, are provided for the purchase line.

-   Delivery

    **Note:**

    -   For goods to be sourced, the requested delivery date is displayed.
    -   For services to be sourced, requested start and end dates are displayed.
    -   This section isn’t available for purchase lines of type handing fee.
-   Accounting, Receiving, and Payment

To debug why a particular field is visible or hidden, navigate to Form Builder from the sourcing request form and select each field to understand which UI Policy is applicable​.

## Contextual information

From the contextual side panel, you can view relevant information such as Agent Assist, attachments, templates, and procurement cases and tasks associated with that procurement record via dynamic related records.

For information on Agent Assist, see [Agent assist in Source-to-Pay Workspace](agent-assist-procurement-workspace.md). For information on procurement and supplier case creation, see [Create a procurement case](../task/create-procurement-case.md) and [Create a supplier case](../task/create-supplier-case.md). For information on procurement task creation, see [Create a procurement task](../task/create-procurement-task.md).

As sourcing managers and fulfillers, you also get a contextual view of supplier profile cards for procurement objects​ such as purchase requisitions​, sourcing requests​, negotiation event​s, negotiations​, and procurement cases​. These supplier profile cards help you with key relevant information such as supplier name, industry, onboarded flag, website, supplier contact, if any, and so on​. All the relevant suppliers for each procurement object are visible in the contextual side panel. For example, if a sourcing request is being worked on with three suppliers, then all the three supplier profile cards are visible in the contextual panel. ​You can further drill down into the supplier 360-degree view by selecting the individual supplier cards, and gather details about them.

As administrators, you can customize the look and feel or the information to be displayed in these supplier profile cards, from the supplier manager workspace experience in UI Builder. You can also add these supplier cards to more procurement objects in Source-to-Pay Workspace by modifying the conditions of the object record pages. Any conflicts arising from previous customizations with the record page can be handled by identifying the difference in the macroponent file and merging the changes as required.​

## Sidebar and Microsoft Teams for Source-to-Pay Workspace

Sidebar enables stakeholders to collaborate with others by getting into discussions when working on task-based records. You can create a Sidebar discussion by selecting **Discuss** from your procurement object details page on the Source-to-Pay Workspace list page. Other stakeholders are notified when you add them to a discussion. They can join the discussion from the Sidebar discussions icon. For more information, see [Sidebar and Microsoft Teams](https://www.servicenow.com/docs/access?context=sidebar-teams-overview&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

For more information on Sidebar, see [Sidebar](https://www.servicenow.com/docs/access?context=sidebar-landing&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

To learn more about how to use Sidebar, see [Using Sidebar](https://www.servicenow.com/docs/access?context=using-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

For information on activity stream in Sidebar, see [Activity stream in Sidebar](https://www.servicenow.com/docs/access?context=activity-stream-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

For detailed information on integrating and enabling Sidebar with Microsoft Teams, see [Integrate Sidebar and Microsoft Teams](https://www.servicenow.com/docs/access?context=integrating-sidebar-teams&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) and [Enable or configure the Microsoft Teams integration](https://www.servicenow.com/docs/access?context=enable-teams-integration&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Configure your workspace list page

You can configure the list page, define different audiences for the page, and even add, remove, or modify the different modules, if you want. However, it’s recommended that you create a duplicate of the page before modifying it. For detailed information, see Setting up list view.

**Parent Topic:**[Source-to-Pay Workspace list page](../../source-to-pay-operations/concept/source-to-pay-list-page.md)

**Related topics**  


[SLO list page](../../supplier-lifecycle-operations/concept/supp-workspace-list-page.md)

[APO list page](../../accounts-payable-operations/concept/acc-pay-workspace-list-page.md)

