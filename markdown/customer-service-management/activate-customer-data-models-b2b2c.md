---
title: Activate customer data models for B2B2C
description: Activate the customer data models for the B2B2C plugin \(com.sn\_csm\_b2b\_consumers\) if you have the admin role. If they aren't already installed, the application includes demo data and installs related ServiceNow Store applications and plugins.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure customer data models for B2B2C, Data models, Set up your environment, Configure, Customer Service Management]
---

# Activate customer data models for B2B2C

Activate the customer data models for the B2B2C plugin \(com.sn\_csm\_b2b\_consumers\) if you have the admin role. If they aren't already installed, the application includes demo data and installs related ServiceNow® Store applications and plugins.

## Before you begin

Role required: admin

You must activate the Customer Service Install Base Management \(com.snc.install\_base\) plugin before installing Customer data models for B2B2C.

The Customer data model for B2B2C plugin provides the following roles:

-   Account consumer \(sn\_acct\_consumer.consumer\)
-   Account consumer agent \(sn\_acct\_consumer.agent\)

When the plugin is activated, customer service agents inherit the account consumer agent role. Consumers who are added as account consumers are given as the account consumer role.

## About this task

The following items are installed with customer data models for B2B2C:

-   Business rules: Required account or consumer
-   UI policies
    -   Table: Case
    -   Table: Interaction
    -   Table: Sold Product
    -   Table: Install Base Items
-   Reference qualifiers
    -   Table: Case
    -   Table: Interaction
    -   Table: Sold Produce
    -   Table: Install Base Items

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the customer data models for B2B2C plugin \(com.sn\_csm\_b2b\_consumers\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


