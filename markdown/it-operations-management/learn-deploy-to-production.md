---
title: Learn how to deploy Event Management to production
description: Understand the process and considerations for deploying Event Management configurations from development to production environments using update sets.
locale: en-US
release: australia
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 2
keywords: [Event Management, deployment, production, update sets]
breadcrumb: [ITOM Configuration console for Event Management, Now Assist for Setup \(AIOps\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Learn how to deploy Event Management to production

Understand the process and considerations for deploying Event Management configurations from development to production environments using update sets.

Deploying Event Management configurations to production requires careful planning and execution to maintain system stability and performance. Update sets provide a controlled method for moving configurations between environments.

## Deployment planning

Before deploying to production, verify that all configurations work correctly in your development or staging environment. Test alert automation rules, integration accounts, and role assignments to confirm they function as expected.

## Update set process

[Update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/system-update-sets.md) capture configuration changes made in your development environment and allow you to transfer them to production. This includes Event Management automation rules, user roles, integration settings, and custom configurations.

The deployment process involves creating an update set, capturing your changes, exporting the update set, and importing it into your production environment. Always review the update set contents before deployment.

When deploying Event Management to production via update set, it is important to understand what is and is not automatically captured.

<table id="table_c2w_g4h_cjc"><thead><tr><th>

Category

</th><th>

Components

</th></tr></thead><tbody><tr><td>

Included in update sets

</td><td>

-   Custom tables and fields
-   Form and list layouts, form sections
-   Business rules, client scripts, UI actions, UI policies, UI pages, UI macros, and UI scripts
-   Script includes and workflows
-   System properties \(except those tagged as Private\)
-   Reports and views
-   Access Control Lists \(ACLs\)

</td></tr><tr><td>

Not included in update sets

</td><td>

-   Transactional data records \(incidents, problems, change requests, knowledge articles\)
-   Users, groups, and group memberships
-   Configuration Items \(CIs\) and CMDB data
-   Scheduled jobs and schedulesHomepages \(unless manually added\)
-   Email and notification logs
-   Number counter records \(sys\_number\_counter\)
-   System properties tagged as Private
-   Plugin-specific elements and business rules in deactivated applications

</td></tr></tbody>
</table>## Deployment considerations

-   Schedule deployments during maintenance windows to minimize impact on operations
-   Back up your production environment before applying updates
-   Test automation rules in production with a limited scope before full activation
-   Verify that integration accounts and credentials are properly configured in production
-   Confirm that all required plugins are installed in the production environment
-   Review role assignments to confirm they align with your production security model

## Post-deployment verification

After deployment, monitor your Event Management system to confirm that alerts are processed correctly and automation rules function as expected. Check integration connections and verify that incidents are created appropriately.

## Additional resources

For detailed guidance on update sets and deployment procedures, refer to the ServiceNow documentation on application deployment and change management processes.

