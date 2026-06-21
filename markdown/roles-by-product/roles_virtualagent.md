---
title: Virtual Agent roles
description: These roles are available for the application
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/roles-by-product/roles\_virtualagent.html
release: australia
topic_type: reference
last_updated: "2024-03-11"
reading_time_minutes: 4
breadcrumb: [Roles for all products]
---

# Virtual Agent roles

These roles are available for the application

<table><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Groups with this role

</th><th>

Special considerations

</th></tr></thead><tbody><tr><td>

Activity subscriptions administrator \[actsub\_admin\]

</td><td>

Creates subscribable objects and subscribes to activities on those objects.

</td><td>

None.

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Automated Customer Experiences \(ACE\) user \[sn\_ace.ace\_user\]

</td><td>

Accesses and reads ACE records.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Automated testing framework designer \[atf\_test\_designer\]

</td><td>

Creates and runs automated tests to confirm proper instance function after making changes to the instance.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Chat analytics administrator \[chat\_analytics\_admin\]

</td><td>

Sets up the Conversational Analytics dashboard, reconfigures its contents, and creates funnels to review performance of conversation flows.

</td><td>

None

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Chat analytics administrator \[chat\_analytics\_admin\]

</td><td>

Provides access to view dashboard-related tables, create custom events, create custom formula overrides, reconfigure the dashboard using UI Builder, and set system parameters.

</td><td>

None

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Chat analytics viewer \[chat\_analytics\_viewer\]

</td><td>

Provides read access to view the dashboard, Conversations \(sys\_cs\_conversation\), and Conversation Consumers \(sys\_cs\_consumer\) tables.

</td><td>

None

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Chat survey administrator \[chat\_survey\_admin\]

</td><td>

Controls and configures post-chat surveys for gathering feedback on user experience, or for chat queues defined in Advanced Work Assignment.

</td><td>

None

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Conversational Interfaces guided setup administrator \[sn\_ci\_gs\_content.ci\_guided\_setup\_admin\]

</td><td>

Creates a guided setup to assist users with planning the roll-out of Conversational Interfaces materials, and performs the basic configurations to go live.

</td><td>

None.

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

EVAM administrator \[evam\_admin\]

</td><td>

Accesses Entity View Action Mapping, to standardize display of different data sources in cards or lists.

</td><td>

None.

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

External application installation administrator \[external\_app\_install\_admin\]

</td><td>

Installs external apps such as Slack, Microsoft Teams, and Workplace.

</td><td>

None.

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

 Any user assigned this role can alter or delete topics created in the Virtual Agent Designer system, including topics that other topics refer to or have as dependencies.

</td></tr><tr><td>

Flow designer \[flow\_designer\]

</td><td>

Launches the Workflow Studio app, to create multi-step workflows.

</td><td>

-   decision\_table\_reader
-   flow\_operator
-   rest\_api\_builder

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Image administrator \[image\_admin\]

</td><td>

Manages image files on the Images \[db\_image\] table.

</td><td>

None.

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Issue auto resolution administrator \[iar\_admin\]

</td><td>

Configures the delivery of automated task resolution messages in Virtual Agent, email, or SMS.

</td><td>

-   evam\_admin
-   search\_application\_admin

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Localization editor \[localization\_editor\]

</td><td>

Edits the translations directly in Virtual Agent Designer. The NLU admin \[nlu\_admin\] and Virtual Agent admin \[virtual\_agent\_admin\] roles contain this role by default.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Localization fulfiller \[localization\_fulfiller\]

</td><td>

Provides translations for the requested Virtual Agent topics. Depending on the flow, duties may include editing the translations in the Localization Framework task, interacting with third parties, and loading, verifying, and publishing translations.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Localization requestor \[localization\_requestor\]

</td><td>

Creates translation requests, and views completed translations in the Localization Framework.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Localization requestor \[localization\_requestor\]

</td><td>

Requests translations for all the Virtual Agent components into one or more languages. Can also view localization insights. The Virtual Agent admin \[virtual\_agent\_admin\] role contains this role by default.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

NLU Administrator \[nlu\_admin\]

</td><td>

Creates NLU models and associated intents in the NLU Workbench.

</td><td>

-   sn\_nlu\_workbench.nlu\_feedback\_admin
-   nlu\_editor
-   nlu\_user

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Now Assist for Creator \[now.assist.creator\]

</td><td>

This role grants users access to Now Assist for Creator skills.

</td><td>

None

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Search application administrator \[search\_application\_admin\]

</td><td>

Inserts data into, updates, and deletes search-UX related configuration tables including: \[sys\_search\_context\_config\], \[sys\_search\_source\], \[m2m\_search\_context\_config\_search\_source\], \[sys\_search\_facet\], and \[sys\_search\_filter\]. The AI Search administrator \[ais\_admin\] role is included in this role to perform AI Search configuration.

</td><td>

-   ais\_admin
-   personalize\_dictionary

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Self-service manager \[sn\_ssa\_core.self\_service\_manager\]

</td><td>

Performs CRUD operations on Pattern and Activity configuration and the Deflection data tables.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

UI builder administrator \[ui\_builder\_admin\]

</td><td>

Enables you to add, remove, and rearrange dashboard contents. Needs UI Builder, which is a separate ServiceNow product.

</td><td>

-   workspace\_admin
-   canvas\_user

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Virtual Agent admin \[virtual\_agent\_admin\]

</td><td>

Contains the localization requestor and localization editor roles by default.

</td><td>

None.

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Virtual Agent administrator \[virtual\_agent\_admin\]

</td><td>

Provides read and write access to all dashboard-related tables, for example, sys-conversation.

</td><td>

-   chat\_analytics\_admin
-   ui\_builder\_admin
-   chat\_analytics\_viewer

</td><td>

None.

</td><td>

**Note:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

Virtual Agent branding \[va\_branding\]

</td><td>

Fetches branding settings via scripted rest API.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr><tr><td>

Workflow Studio \[action\_designer\]

</td><td>

Launches the Workflow Studio app, to automate tasks with sequences of related steps.

</td><td>

None.

</td><td>

None.

</td><td>

None.

</td></tr></tbody>
</table>**Parent Topic:**[Roles for all products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/roles-by-product/roles-for-all-products.md)

