---
title: Configuring Healthcare Operations Core
description: Set up the Healthcare Operations Core application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-configuring.html
release: yokohama
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Configuring Healthcare Operations Core

Set up the Healthcare Operations Core application.

## Configuration overview

1.  [Install Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/activate-hco-core.md)

    The application includes demo data for Healthcare Operations Core and installs related ServiceNow Store applications and plugins if they aren’t already installed.

2.  [Assign roles to Healthcare Operations Core users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/assign-roles-cto-users.md)

    Assign specific roles to give Healthcare Operations Core users visibility into healthcare organizations and the hierarchies they manage.

3.  [Create a group for all team members in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hco-create-team-members-group.md)

    Create a group for team members with the sn\_hco.care\_team\_member role assigned so that users added to this group will inherit the collection of roles for Healthcare Operations Core.

4.  [Create a group for all team managers in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hco-create-team-manager-group.md)

    Create a group for team members with the sn\_hco.care\_team\_manager role assigned so that users added to this group inherits the collection of roles for Healthcare Operations Core.

5.  [Create a healthcare location in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-create-healthcare-locations.md)

    Create healthcare locations to designate the locations in which your care teams operate.

6.  [Example - Organizing your healthcare locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/untitled3.md)

    Your healthcare locations should be organized based on the physical layouts of the locations in which your care teams operate.

7.  [Create a healthcare organization in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-create-healthcare-organization.md)

    Create a healthcare organization for use with Healthcare Operations Core.

8.  [Create healthcare providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-create-healthcare-providers.md)

    Create a healthcare provider and associate it with a parent healthcare organization and a common location.

9.  [Create healthcare departments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-create-healthcare-departments.md)

    Create a healthcare department and associate it with a parent healthcare organization and a common location.

10. [Create organizational teams in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hco-create-organizational-teams.md)

    Create a healthcare organization to associate with your healthcare department.

11. [Example - Organizing your healthcare organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/example-organizing-hcls-organizations.md)

    Properly organize your healthcare organizations to reflect your team hierarchies.

12. [Add or remove members in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-edit-members-admin.md)

    Add or remove members from your healthcare organizations.

13. [Configure global system properties to edit members in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-configure-properties-edit-members.md)

    Add or remove members from your healthcare organizations.

14. [Associate locations with a healthcare organization in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-associate-locations.md)

    Use the Healthcare organization location association table to associate locations with healthcare organizations.

15. [Associate assignment groups with a healthcare organization in Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hco-assign-roles-responsibilities-members.md)

    Create assignment groups for your healthcare organizations to determine which user groups are associated with specific healthcare organizations.

16. [Configure the abstract case type for Healthcare Operations Core case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/configure-abstract-case-type-hco.md)

    Extend the Healthcare Operations case \[sn\_hco\_case\] to create custom case types for use with Healthcare Operations Core and related plugins by creating a child table from the Healthcare Operations Core case type.

17. [Add menu items into the Care Team Portal with Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hco-add-menu-items.md)

    Add more menu items into the Care Team Portal for easy user access.

18. [Embedding Care Team Portal in Epic Hyperspace via Hyperdrive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/configure-care-team-portal.md)

    Configure the Care Team Portal by embedding it into Epic Hyperspace via Hyperdrive and enabling OIDC authentication.

19. [Update variables in record producers to capture tokenized data from Epic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hco-update-variables-portal.md)

    Update the variable values in existing record producers to capture tokenized data from Epic.

20. [Configure iFrame embedding for Care Team Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/configure-iframe-portal.md)

    For the Care Team Portal to successfully launch in Hyperspace via Hyperdrive, the portal must be configured to work within an iFrame.

21. [Enable Multi-Provider SSO for your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hcls-cto-enabling-oidc.md)

    Ensure that Multiple Provider SSO is enabled and configured correctly for Care Team Portal to authenticate with Epic Hyperspace via Hyperdrive.

22. [Authenticate SMART on FHIR for use with the Care Team Portal in Hyperspace via Hyperdrive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/hco-authenticate-portal.md)

    Set up your FHIR app with the correct configurations to allow single sign-on for EPIC users to access the Care Team Portal inside EPIC Hyperspace via Hyperdrive.

23. [Create an Identity Provider on your ServiceNow instance for Healthcare Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/create-identity-provider-hco.md)

    Set up an Identity Provider in your ServiceNow instance to enable OIDC for Healthcare Operations Core.

24. [Configure your Identity Provider for Care Team Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/configure-identity-provider-hco.md)

    Configure your Identity Provider to ensure successful user authentication in Care Team Portal.

25. [Configure the integration settings in the Hyperdrive Client Test Harness for Care Team Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/healthcare-life-sciences/healthcare-operations-core/configure-hyperspace-hco.md)

    Once the Care Team Portal is configured, create a launch URL that can then be configured inside the Epic Hyperdrive Client Test Harness for testing.


