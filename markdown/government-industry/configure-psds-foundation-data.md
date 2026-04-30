---
title: Configure Public Sector Digital Services foundational data and workflows
description: With the Public Sector Digital Services Core application, you can import or create constituent information including names, addresses, and phone numbers; account and financial details; services contracts and items received; and service entitlements and contracts. You can also assign roles to users and create user relationships.Walk through the guided setup processes to configure Public Sector Digital Services foundational data.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-01-08"
reading_time_minutes: 4
breadcrumb: [Getting Started with Public Sector, Set up your environment, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Public Sector Digital Services foundational data and workflows

With the Public Sector Digital Services Core application, you can import or create constituent information including names, addresses, and phone numbers; account and financial details; services contracts and items received; and service entitlements and contracts. You can also assign roles to users and create user relationships.

Foundation data includes the data that you must configure to support your constituents, contacts, applicants,and households, including information about:

-   Constituents and Applicants \(external users\)
-   Applicant and Household relationships
-   Users \(internal users such as agents and employees\)
-   User roles
-   Service contracts and entitlements
-   Service Definitions
-   Install Base Items

## Configure Public Sector Digital Services Core foundational data using guided setup

Walk through the guided setup processes to configure Public Sector Digital Services foundational data.

### Before you begin

[Install the Public Sector Digital Services Core application](../task/install-public-sector-digital-services-core.md).

Role required: admin

### About this task

The Public Sector Digital Services Core application is built on the Customer Service Management application. As part of the guided setup for the Public Sector Digital Services Core application, you can also use guided setup for Customer Service Management to configure foundation data and workflows.

To create data, such as adding new accounts and contacts, you can use the Public Sector Digital Services application.

### Procedure

1.  Navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**.

    The Welcome to Public Sector Digital Services Guided setup page displays.

2.  Review the **Getting Started** and **Public Sector Digital Services Pre-setup Checklist** sections, which give information on the setup process and the various requirements to consider before implementing Public Sector.

3.  Select **Get Started** to begin the configuration.

    The guided setup reopens with a page of different categories of Public Sector Digital Services features that you can configure.

    ![Guided Setup page view with modules and task completion to set up Public Sector Digital Services.](../image/ps-gs-second-page.png)

4.  In the Guided Setup category, select **Get Started**, then select the Foundation Data category and select Get Started.

5.  To perform a task, select **Configure**.

<table id="table_tth_54l_mlb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import Accounts

</td><td>

In the business-to-business \(B2B\) model, an account is a supported external customer. Import and verify existing account data.

</td></tr><tr><td>

Import Contacts \(B2B\)

</td><td>

A contact is a user who is an employee of an account. Import and verify existing contact data.

</td></tr><tr><td>

Import Users

</td><td>

A user is an individual who can access your instance. Import and verify existing user data.

</td></tr><tr><td>

Import Groups

</td><td>

A group is a set of users who share a common purpose. Import and verify existing group data.

</td></tr><tr><td>

Import Group Members

</td><td>

The users associated with a group are listed as group members. Import and verify existing group member data.

</td></tr><tr><td>

Assign Roles

</td><td>

Roles control access to features and capabilities. The Public Sector Digital Services application provides two types of roles:

-   Internal roles for agents and managers
-   External roles for constituents, business partners, and etc
Assign the necessary roles to internal and external users. For more information, see [Assign roles to Public Sector Digital Services users](psds-config-assign-user-roles.md).

</td></tr><tr><td>

Import Product Models

</td><td>

A product is a type of good or service that your agency provides and supports. Product models identify different types of products, such as a service.

</td></tr><tr><td>

Import Sold Products

</td><td>

Sold products are services and components that have been provided to an account, constituent, or business partner. Importing sold products provides an overview of the complete services and components provided to an account, constituent, or business partner.

</td></tr><tr><td>

Create product model and catalog items relationships

</td><td>

Enable self-service for constituents to request services on products by creating relationships between product models and catalog items.

</td></tr><tr><td>

Import Install Base Items

</td><td>

Install base items represent the instances that have been configured for a constituent. Each install base item references the configuration item record for the constituent.

</td></tr><tr><td>

Create Service Contracts

</td><td>

A service contract contains information about the type of support that is provided to a constituent. It can also include multiple service entitlements and service-level agreements \(SLAs\).

</td></tr><tr><td>

Create Entitlements

</td><td>

An entitlement defines the type of support that a constituent receives as well as the supported communication channels. Entitlements are counted and tracked using two types of units: cases and hours.

</td></tr><tr><td>

Create Account Teams and User Groups

</td><td>

Account teams are made up of employees who fulfill specific jobs or roles for a particular account. Create these roles, or responsibility definitions, and then assign them to employees and contacts. For more information, see .

</td></tr></tbody>
</table>
### What to do next

After you have completed the foundation setup tasks, you can [set up your agent workspace](psds-config-organize-agent-workspaces.md) with other Public Sector applications, such as [Playbooks](psds-install-playbooks-solutions.md) or the [Performance Analytics Content Pack](../../../use/dashboards/application-content-packs/psds-install.md).

