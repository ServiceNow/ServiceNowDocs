---
title: Configuring Healthcare Operations Core
description: Set up the Healthcare Operations Core application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-operations-core/hcls-cto-configuring.html
release: brazil
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Configuring Healthcare Operations Core

Set up the Healthcare Operations Core application.

## Configuration overview

1.  [Install Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/activate-hco-core.md)

    The application includes demo data for Healthcare Operations Core and installs related ServiceNow Store applications and plugins if they aren’t already installed.

2.  [Install ServiceNow Otto for Care Team Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-now-assist-install.md)

    Optional: Install the ServiceNow Otto for Care Team Operations application to let care team members create requests conversationally.

3.  [Configure agentic workflows for Care Team Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-otto-workflows-config.md)

    Optional: Activate the Request care team assistance agentic workflow and its agents for the chat and voice channels.

4.  [Assign roles to Healthcare Operations Core users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/assign-roles-cto-users.md)

    Assign specific roles to give Healthcare Operations Core users visibility into healthcare organizations and the hierarchies they manage.

5.  [Create a group for all care team members in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-create-team-members-group.md)

    Create a group for team members with the sn\_hco.care\_team\_member role assigned so that users added to this group will inherit the collection of roles for Healthcare Operations Core.

6.  [Create a group for all care team managers in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-create-team-manager-group.md)

    Create a group for team members with the sn\_hco.care\_team\_manager role assigned so that users added to this group inherits the collection of roles for Healthcare Operations Core.

7.  [Create a healthcare location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hcls-sm-configure-healthcare-location.md)

    Create healthcare locations to designate the locations in which your care teams operate.

8.  [Create a healthcare organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hcls-sm-configure-healthcare-organizations.md)

    Create a healthcare organization for use with Healthcare Operations Core.

9.  [Create a healthcare organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hcls-cto-create-healthcare-organization.md)

    Create a healthcare provider, healthcare department, or organizational team, and associate it with a parent healthcare organization and a common location.

10. [Add or remove members in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hcls-cto-edit-members-admin.md)

    Add or remove members from your healthcare organizations.

11. [Configure global system properties to edit members in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hcls-cto-configure-properties-edit-members.md)

    Add or remove members from your healthcare organizations.

12. [Associate healthcare locations with a healthcare organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hcls-sm-associate-healthcare-locations-organization.md)

    Use the Healthcare organization location association table to associate locations with healthcare organizations.

13. [Associate assignment groups with a healthcare organization in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-assign-roles-responsibilities-members.md)

    Create assignment groups for your healthcare organizations to determine which user groups are associated with specific healthcare organizations.

14. [Configure the abstract case type for Healthcare Operations Core case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/configure-abstract-case-type-hco.md)

    Extend the Healthcare Operations case \[sn\_hco\_case\] to create custom case types for use with Healthcare Operations Core and related plugins by creating a child table from the Healthcare Operations Core case type.

15. [Add menu items into the Care Team Portal with Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-add-menu-items.md)

    Add more menu items into the Care Team Portal for easy user access.

16. [Embedding Care Team Portal in Epic Hyperspace via Hyperdrive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/configure-care-team-portal.md)

    Configure the Care Team Portal by embedding it into Epic Hyperspace via Hyperdrive and enabling OIDC authentication.

17. [Capture Additional Data From Epic Within ServiceNow Record Producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/hco-update-variables-portal.md)

    Update the variable values in existing record producers to capture tokenized data from Epic.

18. [Configure iFrame embedding for Care Team Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/configure-iframe-portal.md)

    For the Care Team Portal to successfully launch in Hyperspace via Hyperdrive, the portal must be configured to work within an iFrame.

19. [Enable Multi-Provider SSO for your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/hcls-cto-enabling-oidc.md)

    Ensure that Multiple Provider SSO is enabled and configured correctly for Care Team Portal to authenticate with Epic Hyperspace via Hyperdrive.

20. [In Epic: Build the FHIR App to Authenticate with ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/hco-authenticate-portal.md)

    Set up your FHIR app with the correct configurations to allow single sign-on for EPIC users to access the Care Team Portal inside EPIC Hyperspace via Hyperdrive.

21. [Create and Configure an Identity Provider in ServiceNow to Authenticate with Epic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/create-identity-provider-hco.md)

    Set up an Identity Provider in your ServiceNow instance to enable OIDC for Healthcare Operations Core.


