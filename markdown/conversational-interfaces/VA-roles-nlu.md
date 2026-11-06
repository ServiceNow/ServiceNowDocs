---
title: \(Legacy\) Virtual Agent roles for NLU
description: Virtual Agent adds several roles for users operating as Virtual Agent administrators.Creates and runs automated tests to confirm proper instance function after making changes to the instance.Sets up the Conversational Analytics dashboard, reconfigures its contents, and creates funnels to review performance of conversation flows.Controls and configures post-chat surveys for gathering feedback on user experience, or for chat queues defined in Advanced Work Assignment.Creates a guided setup to assist users with planning the roll-out of Conversational Interfaces materials, and performs the basic configurations to go live.Configures the delivery of automated task resolution messages in Virtual Agent, email, or SMS.Creates translation requests, and views completed translations in the Localization Framework.Creates NLU models and associated intents in the NLU Workbench.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/VA-roles-nlu.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [NLU technical reference, NLU reference, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Virtual Agent roles for NLU

Virtual Agent adds several roles for users operating as Virtual Agent administrators.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

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

For details on the administration of users, groups, and roles, see [User Administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_UserAdministration.md).

**Parent Topic:**[\(Legacy\) Virtual Agent NLU technical reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-advanced-technical-reference-nlu.md)

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

## Chat analytics administrator \[chat\_analytics\_admin\]

Sets up the Conversational Analytics dashboard, reconfigures its contents, and creates funnels to review performance of conversation flows.

### Contains Roles

List of roles contained within the role: chat\_analytics\_viewer.

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

## NLU administrator \[nlu\_admin\]

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

