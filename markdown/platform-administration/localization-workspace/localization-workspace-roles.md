---
title: Localization Workspace Roles
description: Localization Workspace is installed with these roles.Upload, review, and manage glossaries in the Language Asset Management area of Localization Workspace.Assign this role to any user working in Localization Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-workspace/localization-workspace-roles.html
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: reference
last_updated: "2026-06-03"
reading_time_minutes: 1
breadcrumb: [Localization Workspace reference, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Localization Workspace Roles

Localization Workspace is installed with these roles.

## Localization Framework roles used in Localization Workspace

Many roles used in Localization Workspace are inherited from Localization Framework. For detailed information about the following, see [Localization Framework Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/roles-localization-framework.md).

|User|Name|
|----|----|
|Localization administrator|localization\_admin|
|Localization editor|localization\_editor|
|Localization fulfiller|localization\_fulfiller|
|Localization manager|localization\_manager|
|Localization requester|localization\_requestor|

**Parent Topic:**[Localization Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/localization-workspace-reference.md)

## Terminology Manager \(sn\_lw.terminology\_manager\)

Upload, review, and manage glossaries in the Language Asset Management area of Localization Workspace.

### Contains Roles

List of roles contained within the role.

-   import\_transformer
-   content\_admin
-   import\_set\_loader

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

The sn\_lw.terminology\_manager role is available from version 3.1.0 of Localization Workspace. With version 3.1.0, the following roles that had previously been contained in sn\_lw.user are transferred to sn\_lw.terminology\_manager: import\_transformer, content\_admin, import\_set\_loader.

This role does not contain the sn\_lw.user role. Be sure to also assign sn\_lw.user to any user working in Localization Workspace.

## Localization Workspace user \(sn\_lw.user\)

Assign this role to any user working in Localization Workspace.

### Contains Roles

List of roles contained within the role, before version 3.1.0.

-   import\_transformer
-   content\_admin \(from version 3.0.0\)
-   import\_set\_loader
-   canvas\_user \(from version 2.0.0\)

From version 3.1.0, the roles contained within this role:

canvas\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** From version 3.1.0, the following contained roles are transferred from sn\_lw.user to sn\_lw.terminology\_manager: import\_transformer, content\_admin, import\_set\_loader.

The sn\_cd.content\_admin role is required to see Content Publishing items from Localization Workspace. The sn\_cd.content\_admin role is different from the content\_admin role. For more information about sn\_cd.content\_admin, see [Types of Localizable content in Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-localizable-content.md).

