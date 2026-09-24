---
title: Make project tasks available to a store team
description: Install the App SPM Retail plugin and give your store personas the roles and organization membership they need before project tasks appear in Retail.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-spm-project-tasks-enable.html
release: brazil
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 2
keywords: [App SPM Retail, enable project tasks, location\_project\_stakeholder]
breadcrumb: [Project tasks in Retail, Retail]
---

# Make project tasks available to a store team

Install the App SPM Retail plugin and give your store personas the roles and organization membership they need before project tasks appear in Retail.

## Before you begin

Role required: sn\_customerservice.projectmanager, sn\_service\_org.project\_manager or sn\_customerservice.projectstakeholder

## About this task

Project tasks reach a store team only when three things are true: the plugin is installed, the persona holds a project stakeholder role, and the persona belongs to the retail organization for their store. Retail has no separate setting that turns the feature on or off.

## Procedure

1.  Install the App SPM Retail application on your instance.

    The project task surfaces install with the plugin. When the plugin isn't present, none of the artifacts are installed and no activation errors occur.

2.  Grant a project stakeholder role to each store persona who needs project task access.

    Assign sn\_bus\_loc.location\_project\_stakeholder to a store associate, or sn\_bus\_loc.location\_manager\_project\_stakeholder to a store manager. These roles come from the App SPM Retail dependency. No retail role includes them, so a persona who holds only a retail role sees nothing. For the procedure, see [Assign roles to Retail users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-assign-roles-users.md).

3.  Confirm that each persona belongs to the retail organization for their store.

    Project task access is scoped to the persona's service organization, so a persona who isn't a member of their store's organization sees no project tasks. For the procedure, see [Configure your organizational structure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-configure-organizational-structure.md).

4.  Ask the project manager to set the **Visible to customer** field on the project tasks that the store team should work.

    This is done on the headquarters side. A project task without the field set doesn't appear in the portal or the mobile application, whatever roles the persona holds. For more information, see [Explore retail projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/explore-retail-projects-spm-r.md).


## Result

Store personas see the project tasks for their own store, and can act on them in the portal and in the mobile application. For what each persona can do, see [Roles and visibility for project tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-roles.md).

**Parent Topic:**[Project tasks in Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-overview.md)

