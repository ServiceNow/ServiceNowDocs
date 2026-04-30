---
title: Manage supplier details
description: As a supplier manager, view all the information about a supplier, view supplier locations, manage cases, and view procurement information.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Manage supplier details

As a supplier manager, view all the information about a supplier, view supplier locations, manage cases, and view procurement information.

Open the Source-to-Pay Workspace Details page by navigating to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

Under Quick Actions, select **Manage my suppliers**, and then in the Legal name column of the My suppliers form, select the link to the legal name of the supplier to view more details about the supplier.

The Details page contains the following tabs that display relevant information related to the supplier.

-   **About**
-   **Details**
-   **Emails**
-   **Related work**
-   **Spend**
-   **Risk**
-   **Stakeholders**
-   **Performance**
-   **KPI management**
-   **Subsidiaries**
-   **Documents**

## About tab

The **About** tab displays information about the supplier, supplier relationship, similar suppliers, and supplier locations.

<table id="table_gzt_tfd_jsb"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Sections

</td></tr><tr><td>

Supplier details

</td><td>

Displays supplier details, such as legal name, DUNS number, country of registration, stock symbol, number of employees. You can edit the supplier details, if needed.

</td></tr><tr><td>

Relationship summary

</td><td>

Displays details about whether the supplier has been onboarded, who onboarded the supplier and on which date, and who is the supplier relationship manager.

</td></tr><tr><td>

Relationship manager

</td><td>

Person responsible for managing the relationship with this supplier. Select the email icon \(![Email icon.](../image/email-icon.png)\) to send an email to the relationship manager.

</td></tr><tr><td>

Similar suppliers

</td><td>

Displays suppliers that provide products and services similar to the one that you’re currently viewing.

</td></tr><tr><td>

Supplier news

</td><td>

Displays news and significant events related to the suppliers that you manage, so that you can take action to reduce the impact to the business. For example, news related to mergers and acquisitions, cybersecurity events, fines and sanctions, bankruptcy, negative news, and so on.By default, Supplier Lifecycle Operations retrieves supplier news and activities using the Bing News Search API.

 The News Integration for Supplier Lifecycle Operations plugin \(com.snc.sn\_supplier\_news\) provides you with the flexibility to dynamically fetch news and activities related to a supplier by using any API of your choice. For more information, see [Configuring a custom API to dynamically fetch supplier news](config-supplier-news-api.md).

</td></tr><tr><td>

Related Links

</td><td>

Displays links that enable you to view additional information pertaining to suppliers:-   Banking information
-   Product codes
-   Email domains
-   Contracts
-   Supplier products

</td></tr><tr><td>

Supplier locations

</td><td>

Displays the geographical location of the suppliers on a map.

 **Note:** The Map UI component for threat and alert data feeds \(com.sn\_fam\_map\) plugin enables you to view and manage this section. Verify that you have configured the FAM map properties. For more information, see [Configure properties for Supplier Case Management](../reference/config-prop-supp-mgmt.md).

 You can do the following:

-   Select the add supplier location icon \(![Add supplier location icon.](../image/add-key-contacts.png)\) to add a supplier location. For more information, see [Add a supplier location from the Source-to-Pay Workspace](../task/add-supplier-location.md).
-   Select the toggle list view icon \(![Toggle list view icon.](../image/location-list-icon.png)\) to open the list view, which displays a list of all the supplier locations. Select the toggle map view icon \(![Toggle map view icon.](../image/location-map-icon.png)\) to return to the map view.
-   Select the toggle full screen view icon \(![Toggle fullscreen view icon.](../image/toggle-full-icon.png)\) to view the map in full screen. Select the toggle full screen view icon \(![Toggle fullscreen view icon.](../image/toggle-exit-full-icon.png)\) to exit the full screen mode.

</td></tr><tr><td>

Stakeholders

</td><td>

Displays internal stakeholders and supplier contacts associated with a supplier. Internal stakeholders are internal users with a unique relationship type such as Procurement manager or Category manager. To view a list of all the internal stakeholders, select the **View stakeholders** option. For more information on adding and managing internal stakeholders, see [Manage internal stakeholders](manage-internal-stakeholders.md)Supplier contacts are associated external users. Primary supplier contact is indicated with a Primary tag. To view a list of all the external stakeholders, select the **View supplier contacts** link. For more information on adding and managing supplier contacts, see [Manage supplier contacts from the Source-to-Pay Workspace](managing-contacts-smw.md).

**Note:** The **View stakeholders** and **View supplier contacts** links are displayed only if the supplier has more than five internal stakeholders or supplier contacts respectively.

</td></tr><tr><td class="sub-head" colspan="2">

Option

</td></tr><tr><td>

Contextual side panel

</td><td>

This panel appears below the UI actions. Select the supplier overview icon \(![Supplier overview icon.](../image/supp-overview-icon.png)\) to open the following panels:

-   Supplier overview: Displays information about the supplier.
-   Supplier contacts: Displays information about the supplier contacts. An Admin label next to the contact's name indicates that the contact is a primary contact. If a supplier has more than 5 supplier contacts, the **View all** option is displayed. Select **View all** to view a list of all the contacts for the supplier.

 Select the attachments icon \(![Attachments icon.](../image/attachments-icon.png)\) to open the Attachments panel, which enables you to attach documents to the case.

 Select the agent assist icon \(![Agent Assist icon.](../image/agent-assist-icon.png)\) to open the Agent Assist panel, which enables you to search for information across multiple sources such as catalog items, knowledge articles, supplier cases, problems, and open incidents.

</td></tr><tr><td>

Options to sync supplier data with an external third-party application

</td><td>

Select **Connect to external data**: Enables you to synchronize the supplier data from an external third-party application so that you can view the latest supplier details in the Source-to-Pay Workspace

 Select **Sync with external data** to synchronize with an external third-party application to update the supplier details in the Source-to-Pay Workspace

**Note:** The **Sync with external data** option replaces the **Connect to external data** option after you import supplier details for the first time using the **Connect to external data** option.

 For more information, see [Synchronize supplier data using external third-party application](../task/sync-supp-data-craft.md).

</td></tr><tr><td>

Options to create supplier cases and supplier tasks

</td><td>

Select the **Create** drop-down list to view these options:-   **Create supplier case**: Enables you to create a supplier case.
-   **Create supplier task**: Enables you to create a task for a supplier case. For more information, see [Create a task for a supplier case from the Source-to-Pay Workspace](../task/create-new-task-for-supp-case.md)

</td></tr><tr><td>

Option to save supplier details

</td><td>

If you update the supplier details, select **Save** to save the data to the supplier record.

</td></tr><tr><td>

Option to delete a supplier

</td><td>

Select the see actions icon \(![See actions icon.](../image/see-actions-icon.png)\) and select **Delete** to delete a supplier.

</td></tr></tbody>
</table>## Details tab

The **Details** tab displays information about the supplier.

**Note:** The fields on this tab are editable. You can update the supplier details and select **Save** to save the data.

|Field|Description|
|-----|-----------|
|Supplier|
|Number|An auto-generated number that uniquely identifies a supplier.|
|Legal name|Name of the supplier.|
|ERP supplier code|Company code of the supplier in the ERP system.|
|Parent entity|Name of the parent company of the supplier.|
|Global company|Name of the global company of the supplier.|
|Relationship manager|Person responsible for managing the relationship with this supplier.|
|Relationship status|Business relationship that is designated to the supplier. The options are Strategic, Valued, Tactical, or Excluded.|
|Onboarded|Whether the supplier is onboarded. The options are Yes or No.|
|Preferred|Whether the supplier is preferred. The options are Yes or No.|
|General|
|Street address|Street where the supplier is located.|
|City|City where the supplier is located.|
|State / Province|State or province where the supplier is located.|
|Country|Country where the supplier is located.|
|Industry|The type of industry the supplier belongs to.|
|Website|Website of the supplier.|
|Image|Option to attach an image of the supplier logo. Select **Attach image** and select the image you want to attach.|

## Emails tab

The **Emails** tab displays the list of emails sent to and received from the supplier. It includes all emails related to tasks, cases, and other interactions related to the supplier.

## Related work tab

The **Related work** tab displays information about cases, tasks, sourcing requests, risk assessments, purchase requisitions, and shipments.

The **Related work** tab contains the Lists section on the left, which contains the modules that display information about cases, tasks, sourcing requests, risk assessments, purchase requisitions, and shipments. The Lists section displays the count of records in each module. You can select a module to view a list of records in that module.

In the Number column, select the record number link to view more details pertaining to that record.

<table id="table_y2n_ykj_xsb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cases

</td><td>

Displays a list of cases for the supplier.

</td></tr><tr><td>

Tasks

</td><td>

Displays a list of tasks for the supplier.

</td></tr><tr><td>

Contracts

</td><td>

Displays a list of contracts created for suppliers.

</td></tr><tr><td>

Action plans

</td><td>

Displays a list of existing action plans.

</td></tr><tr><td>

Risk assessments

</td><td>

Displays a list of risk assessments for the supplier.**Note:** This module is displayed only if you have installed the Vendor Risk Management \(com.sn\_vdr\_risk\_asmt\) plugin.

</td></tr><tr><td>

Purchase requisitions

</td><td>

Displays a list of purchase requisitions for the supplier.**Note:** This module is displayed only if you have installed the Sourcing and Purchasing Automation \(com.snc.sn\_pr\) plugin.

</td></tr><tr><td>

Purchase orders

</td><td>

Displays a list of purchase orders for the supplier.**Note:** This module is displayed only if you have installed the Sourcing and Purchasing Automation \(com.snc.sn\_pr\) and Source-to-Pay Common Architecture \(com.snc.sn\_shop\) plugins.

</td></tr><tr><td>

Shipments

</td><td>

**Note:** This module is displayed only if you have installed the Supply Chain Exception Management \(com.snc.sn\_scm\_core\) plugin.

</td></tr><tr><td>

Invoices

</td><td>

Displays a list of invoices for the supplier.**Note:** This module is displayed only if you have installed the Sourcing and Purchasing Automation \(com.snc.sn\_pr\) and Source-to-Pay Common Architecture \(com.snc.sn\_shop\) plugins.

</td></tr></tbody>
</table>## Spend tab

The **Spend** tab displays information about open purchase orders, open invoices, your total spend, total savings, and the trend of your spend and savings over time.

**Note:**

The **Spend** tab becomes available in the Source-to-Pay Workspace only if you install the Source-to-Pay Common Architecture \(com.snc.sn\_shop\) plugin. The **Spend** tab displays information about open purchase orders, open invoices, your total spend, total savings, and a graphical representation of the trend of your spend and savings over time.

For detailed information about each component, select an individual widget or chart.

![Spend tab on the Details page](../image/ws-details-spend.png "Spend tab")

<table id="table_mhj_dkb_zsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Summary - Total Spend

</td></tr><tr><td>

All Time

</td><td>

Widget

</td><td>

View the total spend till date.

</td></tr><tr><td>

This Year

</td><td>

Widget

</td><td>

View the total spend for the year.

</td></tr><tr><td>

This Quarter

</td><td>

Widget

</td><td>

View the total spend for the quarter.

</td></tr><tr><td>

This Month

</td><td>

Widget

</td><td>

View the total spend for the quarter.

</td></tr><tr><td class="sub-head" colspan="3">

Summary - Total Savings

</td></tr><tr><td>

All Time

</td><td>

Widget

</td><td>

View the total savings till date.

</td></tr><tr><td>

This Year

</td><td>

Widget

</td><td>

View the total savings for the year.

</td></tr><tr><td>

This Quarter

</td><td>

Widget

</td><td>

View the total savings for the quarter.

</td></tr><tr><td>

This Month

</td><td>

Widget

</td><td>

View the total savings for the quarter.

</td></tr><tr><td class="sub-head" colspan="3">

Summary

</td></tr><tr><td>

Spend vs. Savings over time

</td><td>

Graph

</td><td>

Displays a graphical presentation of spend versus savings over a given period of time.

</td></tr><tr><td class="sub-head" colspan="3">

Credit card savings estimator

</td></tr><tr><td>

Last saved estimate

</td><td>

View

</td><td>

Displays the value of the last estimate of potential savings from credit card payments calculated using the savings calculator.

</td></tr><tr><td>

View previous estimates

</td><td>

Widget

</td><td>

Displays a list of the last estimates calculated using the savings calculator.

</td></tr><tr><td>

Launch savings estimator

</td><td>

Widget

</td><td>

Launches the commercial card savings value calculator. The saving estimation tool can be used to calculate potential savings from credit card payments. The tool uses default values and allows users to modify billing cycles and other parameters to create new estimates.

</td></tr><tr><td class="sub-head" colspan="3">

Purchase orders

</td></tr><tr><td>

Number

</td><td>

Column

</td><td>

An auto-generated number that uniquely identifies the purchase order.In the Number column, select the link to the record number to view more details.

</td></tr><tr><td>

Display name

</td><td>

Column

</td><td>

Name of the purchase order for a supplier product.

</td></tr><tr><td>

Total amount

</td><td>

Column

</td><td>

The total cost of purchase requisition calculated as the sum from all related purchase lines.

</td></tr><tr><td>

Status

</td><td>

Column

</td><td>

State of the purchase order.

</td></tr><tr><td>

Created

</td><td>

Column

</td><td>

Date on which this purchase order is created.

</td></tr><tr><td>

Created by

</td><td>

Column

</td><td>

Person who created the purchase order.

</td></tr><tr><td class="sub-head" colspan="3">

Invoices

</td></tr><tr><td>

Number

</td><td>

Column

</td><td>

An auto-generated number that uniquely identifies the invoice.In the Number column, select the link to the record number to view more details.

</td></tr><tr><td>

Purchase order

</td><td>

Column

</td><td>

Purchase order with which this invoice is associated.

</td></tr><tr><td>

State

</td><td>

Column

</td><td>

Status of the invoice.

</td></tr><tr><td>

Invoice date

</td><td>

Column

</td><td>

Date on which this invoice is created.

</td></tr><tr><td>

Created by

</td><td>

Column

</td><td>

Person who created the invoice.

</td></tr><tr><td class="sub-head" colspan="3">

Contracts

</td></tr><tr><td>

Number

</td><td>

Column

</td><td>

An auto-generated number that uniquely identifies the contract record.In the Number column, select the link to the record number to view more details.

</td></tr><tr><td>

Name

</td><td>

Column

</td><td>

Short description of the contract.

</td></tr><tr><td>

Total cost

</td><td>

Column

</td><td>

Final cost of the contract.

</td></tr><tr><td>

State

</td><td>

Column

</td><td>

Current state of the contract.

</td></tr><tr><td>

Substate

</td><td>

Column

</td><td>

Current substate of the contract.

</td></tr><tr><td>

Start date

</td><td>

Column

</td><td>

Date on which the contract takes effect.

</td></tr><tr><td>

End date

</td><td>

Column

</td><td>

Date on which the contract expires

</td></tr></tbody>
</table>## Risk tab

The **Risk** tab displays third-party name and process information, summary reports, risk intelligence scores, and tracking data for issues and tasks. On most reports, you can select an item to view the underlying data.

The **Risk** tab is displayed only if you have installed the Third-party Risk Management \[com.sn\_vdr\_risk\_asmt\] and GRC: Vendor Risk Management Workspace \(com.sn\_vdr\_risk\_asmt\_workspace\) plugins.

To know more about the information displayed on the **Risk** tab, see [Viewing summarized risk information for a third party](https://www.servicenow.com/docs/access?context=tprm-ws-tab-tp-risk-overview&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

## Performance

The **Performance** tab displays the Dashboard which enables monitoring and managing supplier performance effectively and making data-driven decisions. You can view the overall supplier score, risk score, individual KPI scores, and domain-specific scores.

The **Performance** tab is displayed only if you have installed the KPI Framework \(com.snc.sn\_kpi\) and Supplier Relationship and Performance Management \(com.snc.sn\_slm\_perf\) plugins.

![Performance dashboard details page](../image/kpi-dashboard.png)

To know more about the information displayed on the **Performance** tab, see [View supplier performance dashboard](../task/view-supplier-performance-dashboard.md).

## KPI Management

The **KPI Management** tab provides comprehensive visibility into the performance scores of all KPIs. KPIs are grouped by domains \(such as Inventory and Quality\) and include critical details such as weight, frequency, and status.

The **KPI Management** tab is displayed only if you have installed the KPI Framework \(com.snc.sn\_kpi\) and Supplier Relationship and Performance Management \(com.snc.sn\_slm\_perf\) plugins.

![KPI Management tab details page](../image/kpi-mgmt-tab.png)

To know more about the information displayed on the **KPI Management** tab, see [Manage supplier KPIs from the supplier record page of the Source-to-Pay Workspace](../task/kpi-mgmt-tab-supplier.md).

## Subsidiaries tab

The **Subsidiaries** tab displays all the subsidiaries of the supplier.

The **Subsidiaries** tab contains the **Add** option, which enables you to quickly add a subsidiary of the supplier. For more information, see [Add a subsidiary for a supplier from the Source-to-Pay Workspace](../task/add-subsidiary.md).

## Stakeholders

The **Stakeholders** tab helps you manage internal stakeholders and supplier contacts associated with a supplier. You can complete the following operations from this tab:

-   View a list of internal stakeholders and supplier contacts
-   Add internal stakeholders with a unique relationship type to the supplier
-   Remove or update internal stakeholder details
-   Add, remove, or update supplier contacts
-   Manage access for primary contact role

![Stakeholders details tab.](../image/stakeholders-overview.png)

For more information on the stakeholders tab, see [Manage internal stakeholders](manage-internal-stakeholders.md) and [Manage supplier contacts from the Source-to-Pay Workspace](managing-contacts-smw.md).

## Documents tab

The **Documents** tab displays information about the required documents that the suppliers upload by either using this tab or from the Supplier Collaboration Portal.

The **Documents** tab contains the **Link Documents** option, which enables you to quickly add an already uploaded document without creating a new one. Access to the **Link Documents** option is controlled by the user criteria you set on the **Manage access** tab when creating the supplier document configuration. For more information, see [Create a supplier document configuration](../task/create-doc-config.md).

-   **[Add a supplier location from the Source-to-Pay Workspace](../task/add-supplier-location.md)**  
Add a supplier location to visualize the geographical location that suppliers run their operations from.
-   **[Edit supplier details from the Source-to-Pay Workspace](../task/edit-supplier-details.md)**  
Add or modify the details of an existing supplier.
-   **[Manage documents from the Source-to-Pay Workspace](../task/upload-doc-ws.md)**  
Manage documents by uploading, updating and downloading the required documents from the Source-to-Pay Workspace.
-   **[Playbook for updating the supplier primary data](primary-playbook-cases.md)**  
Source-to-Pay Workspace includes a playbook that you use for updating the supplier primary data.
-   **[Review supplier information using Relish](review-supp-info-relish.md)**  
Using Relish integration, checking supplier's banking details, physical addresses, and sanction screening can be done efficiently.

**Parent Topic:**[Using Source-to-Pay Workspace](use-supp-mgr-wsp.md)

**Related topics**  


[Create a supplier from the Source-to-Pay Workspace](../task/new-supplier.md)

[Manage internal stakeholders](manage-internal-stakeholders.md)

[Manage supplier contacts from the Source-to-Pay Workspace](managing-contacts-smw.md)

[Manage supplier cases from the Source-to-Pay Workspace](managing-cases.md)

[Manage supplier tasks from the Source-to-Pay Workspace](managing-tasks.md)

[Offboard a supplier from the Source-to-Pay Workspace](../task/offboard-supplier.md)

[Accept an incoming chat request from the Source-to-Pay Workspace](../task/accept-chat-supp-ws.md)

[Interaction Management in Supplier Lifecycle Operations](interaction-mgmt-supplier-mgr-ws.md)

[Composing emails with predefined content from the Source-to-Pay Workspace](email-composer-slm-workspace.md)

[Overall supplier dashboard](overall-supplier-db.md)

[Create supplier case from Universal Request](../task/create-supplier-case.md)

[Emails view for supplier managers](../task/enabling-emails-view-for-contacts.md)

