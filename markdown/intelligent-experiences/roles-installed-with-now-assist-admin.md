---
title: AI Admin Hub roles
description: Certain roles are required to use AI Admin Hub functionality. The base admin \(sys\_admin\) role does not automatically grant or include the following roles, so assign these directly to users who require them.Can create and update the AI Admin Hub experience by editing and configuring skills.Can access AI Admin Hub to view skills and their configurations, but can't make modifications.Users who have access to the Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/roles-installed-with-now-assist-admin.html
release: brazil
topic_type: reference
last_updated: "2026-09-16"
reading_time_minutes: 1
keywords: [Now Assist Admin, roles, Generative AI, Gen AI, Now Assist Admin, edit, configure, skills, roles, groups, special considerations, ace\_user, sn\_nowassist\_admin.nsa\_admin, Now Assist, panel, user, access, roles, groups, special, considerations, Generative AI, Gen AI, sn\_nowassist\_admin.user, Now Assist, panel, user, access, roles, groups, special, considerations, Generative AI, Gen AI]
breadcrumb: [Now Assist reference, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# AI Admin Hub roles

Certain roles are required to use AI Admin Hub functionality. The base admin \(sys\_admin\) role does not automatically grant or include the following roles, so assign these directly to users who require them.

**Parent Topic:**[Now Assist reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-reference-landing.md)

## Now Assist Admin \[sn\_nowassist\_admin.nsa\_admin\]

Can create and update the AI Admin Hub experience by editing and configuring skills.

### Contains Roles

List of roles contained within the role.

-   agent\_role\_config\_admin
-   pa\_viewer
-   sn\_ace.ace\_user
-   sn\_na\_analytics.admin
-   ui\_action\_admin

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Avoid granting an admin role when more specialized roles are available. For detailed comparison of roles, see [Roles and responsibilities for AI administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-roles-responsibilities-ai-admin.md).

## AI Admin Hub console user \[sn\_nowassist\_admin.user\]

Can access AI Admin Hub to view skills and their configurations, but can't make modifications.

### Contains Roles

List of roles contained within the role.

-   agent\_role\_config\_viewer
-   pa\_viewer
-   sn\_ace.ace\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

For detailed comparison of roles, see [Roles and responsibilities for AI administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-roles-responsibilities-ai-admin.md).

## Now Assist panel user \[now\_assist\_panel\_user\]

Users who have access to the Now Assist panel.

### Contains Roles

List of roles contained within the role.

sn\_dyn\_guidance\_user.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

