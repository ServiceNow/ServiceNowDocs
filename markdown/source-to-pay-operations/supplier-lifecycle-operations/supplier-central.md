---
title: Supplier Collaboration Portal
description: The ServiceNow Supplier Collaboration Portal application provides a seamless unified employee portal experience for supplier contacts.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Exploring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier Collaboration Portal

The ServiceNow® Supplier Collaboration Portal application provides a seamless unified employee portal experience for supplier contacts.

Supplier Collaboration Portal enables you to do the following:

-   Resolve supplier inquiries using self-service and Knowledge articles
-   Improve supplier data quality by enabling suppliers to manage their own data
-   Accelerate case resolution by enabling suppliers to complete tasks and upload required prerequisite documents

As a supplier contact, you must first self-register to access the Supplier Collaboration Portal. For more information, see [Self-register to the Supplier Collaboration Portal](../task/self-reg-to-supp-central.md).

In the Supplier Collaboration Portal, you can view the requests assigned to you, open to-dos, and Knowledge articles.

**Note:** The Supplier Collaboration Portal is supported on mobile devices. To access the Supplier Collaboration Portal on a mobile device, open a mobile browser, and then navigate to your instance URL and append the /supplier suffix to the end of the URL. For example, `https://example.com/supplier`.

For more information about installing the Supplier Collaboration Portal, see [Install Supplier Collaboration Portal](../task/install-supp-central.md).

## Supplier Collaboration Portal header

The portal header contains the following options:

<table id="table_e4s_mmj_lsb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

My Company

</td><td>

Opens the Supplier Profile page, which shows the supplier details. You can submit a request to update the details by selecting **Request Change**.For more information, see [Update company profile using the supplier catalog](../task/update-supp-profile.md).

**Important:** From Xanadu December 2024 release onwards, after enabling M2M mapping between supplier contact and suppliers, the list of suppliers linked with the contact are displayed on selecting **My Company**. You can select a supplier from the list which opens the company-specific Supplier Profile page.

</td></tr><tr><td>

Tasks

</td><td>

Contains the following submenus.**Note:** Only the primary contact can see the Tasks menu and its submenus in the portal header.

-   My Tasks: Opens the My To-dos page, which lists all the tasks that are assigned to the logged-in user.

**Note:** The secondary contact can view only the My Tasks option in the portal header.

-   All Tasks: Opens the Supplier Task List page, which lists all the tasks that are assigned to the supplier.

For more information, see [Viewing supplier contact tasks from the Supplier Collaboration Portal](my-to-dos.md).


</td></tr><tr><td>

My Requests

</td><td>

Opens the My Requests page, which lists all the requests assigned to you. For more information, see [View all your requests from the Supplier Collaboration Portal](../task/view-supp-case-sc.md).

</td></tr><tr><td>

Raise a request

</td><td>

Option that enables you to raise a request by navigating to the General category in the Supplier catalog.For more information, see [Raising requests from the Supplier Collaboration Portal](supp-catalog-req.md).

</td></tr></tbody>
</table>## Supplier Collaboration Portal widgets

The Supplier Collaboration Portal contains the following widgets.

<table id="table_orp_d2c_lsb"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

How can we help?

</td><td>

Lets you search for any information that you're looking for.

</td></tr><tr><td>

My active items

</td><td>

As a supplier contact, you can view and work on specific items. The information that is displayed in the tiles depends on the plugins that you have installed. Selecting a tile in the widget opens the page that provides more information about it.

-   Tasks
-   Requests
-   Surveys
-   Issues
-   Risk Assessments
-   Contracts
-   Supplier Products
-   Purchase Orders
-   Shipments
-   Invoices

 The Risk Assessments tile is displayed if you have installed the Third-party Risk Management plugin.

 The Contracts, Supplier Products, Purchase Orders, Shipments, and Invoices tiles are displayed if you have installed the Sourcing and Purchasing Automation \(com.snc.sn\_pr\) and Source-to-Pay Common Architecture \(com.snc.sn\_shop\) plugins.

 **Important:**

The data for **My active items** is sourced from the **Activity Configurations** table. For all the new custom records added to **Activity Configurations** that need to be shown in **My active items**, the corresponding ACLs for sn\_slm\_contact must also be explicitly added.

Also, for restricting the data appearing in **My active items**, you can configure the user criteria by updating the **Activity Access** list of the **Activity Configurations** table.

</td></tr><tr><td>

My tasks

</td><td>

Displays a list of supplier tasks assigned to you. Selecting a task directly opens it on the My To-dos page so that you can work on that task. Select **View All** to view a list of all the tasks assigned to you.**Important:** The data for **My tasks** is sourced from the **To-dos Configurations** table. For all the new custom records added to **To-dos Configurations** that need to be shown in **My tasks**, the corresponding ACLs for sn\_slm\_contact must also be explicitly added.

</td></tr><tr><td>

My requests

</td><td>

Displays a list of cases that you have submitted. Selecting a case directly opens the My Cases page so that you can work on that case. Select **View All** to view a list of all the cases that you have submitted.

</td></tr><tr><td>

Quick links

</td><td>

Enables the supplier to access internal and external resources related to specific departments within your organization.

</td></tr><tr><td>

My company

</td><td>

This section has the following fields:-   **Number of employees**: The number of people employed by the company.
-   **Founded**: The year the company was founded.
-   **Industry**: The type of industry the company belongs to.
-   **Relationship manager**: The name of the relationship manager for your company.
-   **Onboarded date**: The date your company was onboarded.

 Select **Details** to view details, contact information, payment information, and locations of your company.

</td></tr><tr><td>

My contacts

</td><td>

Displays a list of members on your team. You can call a member directly or send an email to a member by selecting the phone icon \(![Phone icon.](../image/phone-icon.png)\) or the email icon \(![Email icon.](../image/email-icon.png)\) respectively, next to that team member's name. You can also invite new members to register to by selecting **Invite**.**Note:** The **Invite** option is available only to the primary supplier contact and the supplier administrator. Only the primary supplier contact and the supplier administrator can invite new members to access the Supplier Collaboration Portal. For more information, see [Invite a member to access the Supplier Collaboration Portal](../task/invite-member-supp-portal.md).

</td></tr><tr><td>

Most viewed articles

</td><td>

Displays a list of the most viewed articles.

</td></tr></tbody>
</table>For more information about using the Supplier Collaboration Portal, see [Using Supplier Collaboration Portal](use-supp-central.md).

