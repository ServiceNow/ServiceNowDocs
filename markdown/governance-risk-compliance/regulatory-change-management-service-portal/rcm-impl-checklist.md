---
title: Setup checklist for Regulatory Change Management
description: Complete the tasks that are required to set up the Regulatory Change Management application. When you have completed these tasks, the base system is ready for operation. Optional setup procedures are also included to enhance Regulatory Change Management application functionality.
locale: en-US
release: xanadu
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Setup checklist for Regulatory Change Management

Complete the tasks that are required to set up the Regulatory Change Management application. When you have completed these tasks, the base system is ready for operation. Optional setup procedures are also included to enhance Regulatory Change Management application functionality.

## Before you begin

Role required: sn\_grc\_reg\_change.admin

Ensure that the following applications are installed:

-   ServiceNow® GRC: Policy and Compliance Management application
-   ServiceNow® Advanced Risk application

## Procedure

1.  Install the Regulatory Change Management \(RCM\) application from the Store.

    For details, see [Download and install GRC: Regulatory Change Management](../../grc-rcm/task/activate-grc-rcm.md).

2.  Assign RCM roles to the users.

    For details, see [User roles in Regulatory Change Management](../../grc-rcm/reference/roles-installed-rcm.md).

3.  To set up the feeds, choose one of the following options.

    |Step|Description|
    |----|-----------|
    |**Set up the RSS feeds by using the RCM application.**|For information on setting up the RSS feeds by using the RCM application, see [Setting up the RSS feeds infrastructure](../../grc-rcm/concept/setting-up-rss-feeds-infrastructure.md) .|
    |**Set up the feeds by integrating with the GRC integration with Thomson Reuters Regulatory Intelligence application.**|For more information on setting up third-party integration with the RCM application, see [GRC integration with Thomson Reuters Regulatory Intelligence](../../grc-rcm-trri-integration/concept/grc-trri-integration.md).|

4.  Create and validate the connections and credentials.

    For details, see [Establish an SFTP or REST API connection](../../grc-rcm-trri-integration/task/create-conn-record-tr-int.md).

5.  Activate the integration flows.

    For details, see [GRC integration with Thomson Reuters Regulatory Intelligence](../../grc-rcm-trri-integration/concept/grc-trri-integration.md) and [Setting up the RSS feeds infrastructure](../../grc-rcm/concept/setting-up-rss-feeds-infrastructure.md).

6.  Create an internal regulatory taxonomy and map the taxonomy.

    For details, see [Map the taxonomy](../../grc-rcm/task/manage-taxonomy.md).

7.  Assign regulatory feeds.

    For details, see [Manage and assign regulatory event alerts](../../grc-rcm/task/manage-regulatory-feeds.md).

8.  Assess the impact and assign related regulatory tasks.

    For details, see [Manage the regulatory change tasks](../../grc-rcm/task/manage-regulatory-change-tasks.md).

9.  Prepare an action plan to identify the changes that must be done.

    For details, see [Action tasks in Regulatory Change Management](../../grc-rcm/concept/action-tasks.md).

10. Create action tasks to implement the identified changes, and complete them.

    For details, see [Create an action task](../../grc-rcm/task/manage-reg-action-tasks.md).

11. Provide an overview of the regulatory changes via dashboards and reports.

    For details, see [Regulatory Change Management dashboard](../../grc-rcm/concept/rcm-dashboard.md).


