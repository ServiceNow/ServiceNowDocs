---
title: Virtual Agent roles
description: Virtual Agent adds several roles for users operating as Virtual Agent administrators.Configures the delivery of automated task resolution messages in Virtual Agent, email, or SMS.Controls and configures post-chat surveys for gathering feedback on user experience, or for chat queues defined in Advanced Work Assignment.Launches the Workflow Studio app, to automate tasks with sequences of related steps.Accesses Entity View Action Mapping, to standardize display of different data sources in cards or lists.Fetches branding settings via scripted rest API.Creates subscribable objects and subscribes to activities on those objects.Launches the Workflow Studio app, to create multi-step workflows.Creates and runs automated tests to confirm proper instance function after making changes to the instance.Creates NLU models and associated intents in the NLU Workbench.Installs external apps such as Slack, Microsoft Teams, and Workplace.Accesses and reads ACE records.Creates a guided setup to assist users with planning the roll-out of Conversational Interfaces materials, and performs the basic configurations to go live.Creates translation requests, and views completed translations in the Localization Framework.Performs CRUD operations on Pattern and Activity configuration and the Deflection data tables.Manages image files on the Images \[db\_image\] table.Inserts data into, updates, and deletes search-UX related configuration tables including: \[sys\_search\_context\_config\], \[sys\_search\_source\], \[m2m\_search\_context\_config\_search\_source\], \[sys\_search\_facet\], and \[sys\_search\_filter\]. The AI Search administrator \[ais\_admin\] role is included in this role to perform AI Search configuration.Sets up the Conversational Analytics dashboard, reconfigures its contents, and creates funnels to review performance of conversation flows.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Installed with Virtual Agent, Activate Virtual Agent, Activate and get started, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent roles

Virtual Agent adds several roles for users operating as Virtual Agent administrators.

To learn more about managing subscriptions, see Managing per-user subscriptions in Subscription Management and contact your account representative.

## Role description

Roles that are installed with Virtual Agent are listed below with the following information:

-   **Role title \[name\]**

    Name of the role. Text within brackets matches the **Name** field in the Roles \[sys\_user\_role\] table.

-   **Description**

    Description of the role and its intended use.

-   **Contains Roles**

    List of roles contained within the role.

-   **Groups**

    List of groups this role is assigned to by default.

-   **Considerations**

    Warnings or other considerations for administrators.


## Installed roles

**Note:**

Simplify user administration by creating groups that contain all the roles necessary for specific personas rather than to individual users. You can then assign individual users to those groups. When users transition to new roles, you can then re-assign their group memberships, and avoid scenarios where users retain unexpected roles.

For details on the administration of users, groups, and roles, see User Administration.

## Issue auto resolution administrator \[iar\_admin\]

Configures the delivery of automated task resolution messages in Virtual Agent, email, or SMS.

### Contains Roles

List of roles contained within the role.

-   evam\_admin
-   search\_application\_admin

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Chat survey administrator \[chat\_survey\_admin\]

Controls and configures post-chat surveys for gathering feedback on user experience, or for chat queues defined in Advanced Work Assignment.

### Contains Roles

List of roles contained within the role: survey\_admin.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Workflow Studio \[action\_designer\]

Launches the Workflow Studio app, to automate tasks with sequences of related steps.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## EVAM administrator \[evam\_admin\]

Accesses Entity View Action Mapping, to standardize display of different data sources in cards or lists.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Virtual Agent branding \[va\_branding\]

Fetches branding settings via scripted rest API.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Activity subscriptions administrator \[actsub\_admin\]

Creates subscribable objects and subscribes to activities on those objects.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Flow designer \[flow\_designer\]

Launches the Workflow Studio app, to create multi-step workflows.

### Contains Roles

List of roles contained within the role.

-   decision\_table\_reader
-   flow\_operator
-   rest\_api\_builder

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Automated testing framework designer \[atf\_test\_designer\]

Creates and runs automated tests to confirm proper instance function after making changes to the instance.

### Contains Roles

List of roles contained within the role: impersonator.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## NLU Administrator \[nlu\_admin\]

Creates NLU models and associated intents in the NLU Workbench.

### Contains Roles

List of roles contained within the role.

-   sn\_nlu\_workbench.nlu\_feedback\_admin
-   nlu\_editor
-   nlu\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## External application installation administrator \[external\_app\_install\_admin\]

Installs external apps such as Slack, Microsoft Teams, and Workplace.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

Any user assigned this role can alter or delete topics created in the Virtual Agent Designer system, including topics that other topics refer to or have as dependencies.

## Automated Customer Experiences \(ACE\) user \[sn\_ace.ace\_user\]

Accesses and reads ACE records.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Conversational Interfaces guided setup administrator \[sn\_ci\_gs\_content.ci\_guided\_setup\_admin\]

Creates a guided setup to assist users with planning the roll-out of Conversational Interfaces materials, and performs the basic configurations to go live.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Localization requestor \[localization\_requestor\]

Creates translation requests, and views completed translations in the Localization Framework.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Self-service manager \[sn\_ssa\_core.self\_service\_manager\]

Performs CRUD operations on Pattern and Activity configuration and the Deflection data tables.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Image administrator \[image\_admin\]

Manages image files on the Images \[db\_image\] table.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Search application administrator \[search\_application\_admin\]

Inserts data into, updates, and deletes search-UX related configuration tables including: \[sys\_search\_context\_config\], \[sys\_search\_source\], \[m2m\_search\_context\_config\_search\_source\], \[sys\_search\_facet\], and \[sys\_search\_filter\]. The AI Search administrator \[ais\_admin\] role is included in this role to perform AI Search configuration.

### Contains Roles

List of roles contained within the role.

-   ais\_admin
-   personalize\_dictionary

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Chat analytics administrator \[chat\_analytics\_admin\]

Sets up the Conversational Analytics dashboard, reconfigures its contents, and creates funnels to review performance of conversation flows.

### Contains Roles

List of roles contained within the role: chat\_analytics\_viewer.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

