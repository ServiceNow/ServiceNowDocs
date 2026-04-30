---
title: Workspace API - ServiceNow Fluent
description: The Workspace API defines configurable workspace experiences for organizing and sharing data visually.Create a workspace for managing business entities in a single focused working area that enables users to complete an entire job.Define a UX list menu configuration \[sys\_ux\_list\_menu\_config\] for the navigation structure and list views of a workspace.Define categories of related lists \[sys\_ux\_list\_category\] for a UX list menu configuration.Define list views of table data \[sys\_ux\_list\] with filtering and column configurations for a UX list menu configuration.Define the audience \[sys\_ux\_applicability\] that can view a list in the UX list menu configuration.
locale: en-US
release: xanadu
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api]
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Workspace API - ServiceNow Fluent

The Workspace API defines configurable workspace experiences for organizing and sharing data visually.

The Workspace API creates application metadata in the following tables depending on the workspace definition: UX Application \[sys\_ux\_page\_registry\], UX App Configuration \[sys\_ux\_app\_config\], UX Application Category M2M \[sys\_ux\_registry\_m2m\_category\], UX Page Property \[sys\_ux\_page\_property\], UX Screen Collection \[sys\_ux\_screen\_type\], UX App Route \[sys\_ux\_app\_route\], UX Screen \[sys\_ux\_screen\], and UX Macroponent Definition \[sys\_ux\_macroponent\].

Dashboards can be used as the home page of a workspace by referring to one or more workspaces from the visibilities array of the Dashboard object. To create a dashboard, see [Dashboard API - ServiceNow Fluent](fluent-dashboard-api.md#).

For general information about workspaces, see [Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Workspace object

Create a workspace for managing business entities in a single focused working area that enables users to complete an entire job.

<table id="table_owp_xh2_h3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

title

</td><td>

String

</td><td>

Required. A name for the workspace that appears in navigation and headers.

</td></tr><tr><td>

path

</td><td>

String

</td><td>

Required. The URL path segment of the workspace. Workspace URLs follow the pattern `/now/<path>/<landingPath>` and use kebab case.Workspaces require access control lists \(ACLs\) to secure the workspace routes. The field property of an Acl object must match the value of this property with a wildcard pattern: `{workspace.path}.*`.

</td></tr><tr><td>

tables

</td><td>

Array

</td><td>

Required. A list of table names to manage in the workspace.

</td></tr><tr><td>

listConfig

</td><td>

Reference

</td><td>

Required. The variable identifier of a UxListMenuConfig object that defines the navigation structure of the workspace. For more information, see [UxListMenuConfig object](fluent-workspace-api.md#).

</td></tr><tr><td>

landingPath

</td><td>

String

</td><td>

The URL path segment of the landing page. Workspace URLs follow the pattern `/now/<path>/<landingPath>` and use kebab case.Default: home

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the workspace is accessible to users.Default: true

</td></tr></tbody>
</table>```javascript
import { Workspace } from '@servicenow/sdk/core';

const itsmWorkspace = Workspace({
    $id: Now.ID['itsm_workspace'],
    title: 'IT Service Management',
    path: 'itsm',
    tables: ['incident', 'problem', 'change_request', 'user', 'sys_user_group'],
    listConfig: incidentListConfig
})
```

The UX List Menu Configuration referenced is defined using the UxListMenuConfig object.

## UxListMenuConfig object

Define a UX list menu configuration \[sys\_ux\_list\_menu\_config\] for the navigation structure and list views of a workspace.

A UX list menu configuration organizes data into categories and lists, enabling users to access different views of business data with filtering, column selection, and role-based visibility. This structure appears in the workspace's navigation panel, providing organized access to different data views.

<table id="table_owp_xh2_h3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. A name for the list configuration.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the list configuration.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the list configuration is active.Default: true

</td></tr><tr><td>

categories

</td><td>

Array

</td><td>

A list of top-level groupings in the list configuration. For more information, see [categories array](fluent-workspace-api.md#).

</td></tr></tbody>
</table>```javascript
import { UxListMenuConfig } from '@servicenow/sdk/core';

const incidentListConfig = UxListMenuConfig({
    $id: Now.ID['incident_list_config'],
    name: 'Incident List Configuration',
    description: 'Navigation for Incident Workspace',
    categories: [
        {
            $id: Now.ID['incidents_category'],
            title: 'Incidents',
            order: 10,
            lists: [
                {
                    $id: Now.ID['incidents_open'],
                    title: 'Open',
                    order: 10,
                    condition: 'active=true^EQ',
                    table: 'incident',
                    columns: 'number,short_description,priority,state',
                    applicabilities: [
                        {
                            $id: Now.ID['incidents_open_applicability'],
                            applicability: applicability
                        }
                    ]
                }
            ]
        }
    ]
})
```

### categories array

Define categories of related lists \[sys\_ux\_list\_category\] for a UX list menu configuration.

<table id="table_owp_xh2_h3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

title

</td><td>

String

</td><td>

Required. A title for the category to display in the navigation menu.

</td></tr><tr><td>

lists

</td><td>

Array

</td><td>

Required. A list of list views in the category. For more information, see [lists array](fluent-workspace-api.md#).

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

A number indicating the position of the category in the navigation menu. Categories with lower numbers appear first.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the category is visible in the navigation menu.Default: true

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the category.

</td></tr></tbody>
</table>```javascript
categories: [
    {
      $id: Now.ID["incidents_category"],
      title: "Incidents",
      order: 10,
      lists: [
        {
          $id: Now.ID["incidents_open"],
          title: "Open",
          order: 10,
          condition: "active=true^EQ",
          table: "incident",
          columns: "number,short_description,priority,state",
          applicabilities: [
            {
              $id: Now.ID["incidents_open_applicability"],
              applicability: applicability
            }
          ]
        },
        {
          $id: Now.ID["incidents_all"],
          title: "All",
          order: 20,
          condition: "",
          table: "incident",
          columns: "number,short_description,priority,state",
          applicabilities: [
            {
              $id: Now.ID["incidents_all_applicability"],
              applicability: applicability
            }
          ]
        }
]
```

#### lists array

Define list views of table data \[sys\_ux\_list\] with filtering and column configurations for a UX list menu configuration.

<table id="table_owp_xh2_h3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

title

</td><td>

String

</td><td>

Required. A title for the list to display in the navigation menu.

</td></tr><tr><td>

table

</td><td>

String

</td><td>

Required. The name of a table to use for the list.

</td></tr><tr><td>

columns

</td><td>

String

</td><td>

A comma-separated list of column names to display in the list.

</td></tr><tr><td>

condition

</td><td>

String

</td><td>

An encoded query string to filter the records displayed in the list.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

A number indicating the position of the list within its category. Lists with lower numbers appear first.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the list is visible to users.Default: true

</td></tr><tr><td>

applicabilities

</td><td>

Array

</td><td>

A list of variable identifiers of Applicability objects that control which roles can view the list. For more information, see [Applicability object](fluent-workspace-api.md#).

</td></tr></tbody>
</table>```javascript
lists: [
        {
          $id: Now.ID["assets_active"],
          title: "Active",
          order: 10,
          condition: "install_status=1",
          table: "alm_asset",
          columns: "asset_tag,display_name,model_category,assigned_to",
          applicabilities: [
            {
              $id: Now.ID["assets_active_applicability"],
              applicability: assetApplicability
            }
          ]
        },
        {
          $id: Now.ID["assets_all"],
          title: "All",
          order: 20,
          condition: "",
          table: "alm_asset",
          columns: "asset_tag,display_name,model_category,assigned_to",
          applicabilities: [
            {
              $id: Now.ID["assets_all_applicability"],
              applicability: assetApplicability
            }
          ]
  }
]
```

## Applicability object

Define the audience \[sys\_ux\_applicability\] that can view a list in the UX list menu configuration.

<table id="table_owp_xh2_h3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. A name for the applicability rule.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the audience.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the applicability rule is applied.Default: true

</td></tr><tr><td>

roles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or sys\_ids of roles that a user must have to view the list. For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

roleNames

</td><td>

String

</td><td>

A comma-separated list of role names that a user must have to view the list. This property is an alternative to the roles property.

</td></tr></tbody>
</table>```javascript
import { Applicability } from '@servicenow/sdk/core';

const managerApplicability = Applicability({
    $id: Now.ID['manager_applicability'],
    name: 'Managers Only',
    roles: [managerRole]
})
```

The role referenced is defined using the Role object:

```javascript
import { Role } from '@servicenow/sdk/core';

const managerRole = Role({
    $id: Now.ID['manager_user_role'],
    name: 'x_snc_manager.user',
    containsRoles: ['canvas_user']
})
```

