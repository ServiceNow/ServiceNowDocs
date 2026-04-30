---
title: Base system roles
description: Administrators can assign one or more base system user roles to grant access to base system platform features and applications.
locale: en-US
release: zurich
product: User Administration
classification: user-administration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 42
breadcrumb: [Managing roles, User admin, Configure core features, Administer]
---

# Base system roles

Administrators can assign one or more base system user roles to grant access to base system platform features and applications.

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md) and contact your account representative.

**Important:** Avoid granting an admin role when more specialized roles are available.

## Administrator \[admin\]

The administrator role. This role has access to all system features, functions, and data because administrators can override access control list \(ACL\) rules and pass all role checks. Avoid assigning this role to your users when more targeted roles are available.

-   **Contains Roles**

    List of roles contained within the role.

    -   ais\_admin
    -   announcement\_admin
    -   catalog
    -   catalog\_admin
    -   catalog\_builder\_editor
    -   catalog\_lookup\_admin
    -   catalog\_template\_editor
    -   chat\_admin
    -   evam\_admin
    -   image\_admin
    -   import\_admin
    -   import\_scheduler
    -   import\_set\_loader
    -   import\_transformer
    -   live\_feed\_admin
    -   ml\_admin
    -   ml\_labeler
    -   nlu\_admin
    -   nlu\_editor
    -   nlu\_user
    -   pa\_data\_collector
    -   pa\_viewer
    -   personalize\_dictionary
    -   platform\_ml\_create
    -   platform\_ml\_read
    -   platform\_ml\_write
    -   search\_application\_admin
    -   search\_relevancy\_model\_admin
    -   sn\_ace.ace\_user
    -   sn\_employee.admin
    -   sn\_hr\_sp.admin
    -   sn\_hr\_sp.esc\_admin
    -   sn\_nlu\_workbench.nlu\_feedback\_admin
    -   sn\_templated\_snip.template\_snippet\_admin
    -   sn\_templated\_snip.template\_snippet\_reader
    -   sn\_templated\_snip.template\_snippet\_writer
    -   sp\_admin
    -   taxonomy\_admin
    -   user\_criteria\_admin
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    Grant this privilege carefully. If you have sensitive information, such as HR records, that you must protect, create a custom admin role for that area. Train any users authorized to see those records to act as the administrator. Also note the [Special Administrative Roles](r_SpecialAdministrativeRoles.md#).

    **Note:** Users with roles related to the Key Management Framework can only be modified by admins with the kmf\_admin role. For details on KMF roles, see [Roles installed with Key Management Framework](https://www.servicenow.com/docs/access?context=kmf-roles&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).


## Agent administrator \[agent\_admin\]

Agent administrators can download and administer the built-in system agent. They can manage MID Server-related scripts.

-   **Contains Roles**

    List of roles contained within the role.

    -   agent\_security\_admin
    -   view\_changer
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## AI search administrator \[ais\_admin\]

AI search administrators can query, create, update, and delete indexing and search settings and log messages through the [AI Search](../../ai-search/concept/overview-ais.md) application.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Application client company installer \[app\_client\_company\_installer\]

Users assigned the app\_client\_company\_installer role can install applications containing the same company as the currently logged in instance. Assigning this role enables first-time installation of applications for the company associated with the current instance. Users with this role can’t install an application for another company.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Application client user \[app\_client\_user\]

Application client users can install applications containing the same company as the currently logged in instance.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Approval administrator \[approval\_admin\]

Approval administrators can view or modify approval requests not directly assigned to them. Use the approver\_user role to enable approvers to view or modify only requests directly assigned to them.

Fulfillers may approve within the product to which they are subscribed \(ITSM Fulfiller approving within ITSM\). This approval may be in the platform or via email. No additional entitlement is required.

Fulfillers may not approve beyond the product to which they are subscribed \(ITSM Fulfiller approving within Procurement, GRC, etc.\). This approval would need an additional approval entitlement for the user.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Approver users \[approver\_user\]

Approver users can modify requests for approval routed to them. They also have all the capabilities of requesters.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    There’s a fee associated with this role. Don’t assign it to users without confirming your organization has the appropriate entitlement.


## Asset user \[asset\]

Asset users can manage hardware and software assets.

-   **Contains Roles**

    List of roles contained within the role.

    -   inventory\_user
    -   cmdb\_query\_builder
    -   canvas\_user
    -   financial\_mgmt\_user
    -   cmdb\_read
    -   contract\_manager
    -   category\_manager
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Assignment rule administrator \[assignment\_rule\_admin\]

Assignment rule administrators can manage assignment rules.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Business process administrator \[business\_process\_admin\]

Business process admins can create, read, update, and delete all records and their relationships in the business process.

In the context of Governance, Risk, and Compliance \(GRC\), users with the sn\_grc.admin role who manage GRC applications and their setup automatically gain access to this role. This access enables the GRC administrators to administer a business process and its records similar to other GRC tables.

-   **Contains Roles**

    List of roles contained within the role: business\_process\_manager.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    This role is assigned to users who are administrators and have thorough information and training on business processes. None.


## Business process manager \[business\_process\_manager\]

Business process managers can create, read, and update any business process and manage the relationship of business processes with other records. This role is assigned to business process managers who are usually specialists and manage multiple business processes in the organization. Assign this role to users who generally work with other employees and are experts around business processes.

In the context of GRC, users with the sn\_grc.manager role automatically inherit this role that enables them to manage the business processes for the entire organization.

-   **Contains Roles**

    List of roles contained within the role - business\_process\_user.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Business process user \[business\_process\_user\]

Business process users can update the business processes that a user owns and can also read any business process. This role must be assigned to the respective process owners. This role can also be provided to users who are required to view the business processes in the organization and understand them better.

In the context of GRC, users with the sn\_risk.user role are automatically assigned this role. This role enables users to manage the business processes that they own as well as read all business processes.

-   **Contains Roles**

    List of roles contained within the role- cmdb\_read.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Catalog administrator \[catalog\_admin\]

Catalog administrators can manage the Service Catalog application, including catalog categories and items.

-   **Contains Roles**

    List of roles contained within the role.

    -   user\_criteria\_admin
    -   catalog\_builder\_editor
    -   catalog\_template\_editor
    -   catalog
    -   catalog\_lookup\_admin
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Catalog editor \[catalog\_editor\]

Catalog editors can create, modify, and publish items within categories that they’re assigned to.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Catalog item designer \[catalog\_item\_designer\]

Catalog item designers can view the status of their category requests. This role is granted automatically to users when they make a request for an item designer category.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Catalog manager \[catalog\_manager\]

Catalog managers can view and assign catalog editors to their categories. They can also create, modify, and publish items within their categories.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Catalog user \[catalog\]

Catalog users have read and some write access to all Service Catalog Requests, Tasks, and Items.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    -   Catalog Request Approvers &gt; $1000
    -   Catalog Request Approvers for Sales
    -   Field Services
-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Category manager \[category\_manager\]

Category managers can create, edit, and delete model categories.

-   **Contains Roles**

    List of roles contained within the role - model\_manager.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## CMDB administrator \[sn\_cmdb\_admin\]

The configuration management data base \(CMDB\) administrator is a key role required for interacting with the CMDB Workspace. CMDB administrators can access all CMDB data, tools, and UIs within the CMDB Workspace. Users with this role can set policies that an editor can't, such as class manager and app service requirements.

As you drill down in the CMDB Workspace, there are some dashboards and list views that require specific roles in addition to the CMDB Admin, CMDB Editor, or CMDB User roles.

-   **Contains Roles**

    List of roles contained within the role.

    -   canvas\_admin
    -   cmdb\_ms\_admin
    -   data\_manager\_admin
    -   sn\_cmdb\_editor
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## CMDB de-duplication administrator \[cmdb\_dedup\_admin\]

CMDB de-duplication admins can review and remediate CMDB de-duplication tasks.

-   **Contains Roles**

    List of roles contained within the role - cmdb\_read.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## CMDB editor \[sn\_cmdb\_editor\]

A key role required for interacting with CMDB Workspace. CMDB editors can create, edit, and delete CMDB records but can't change policies such as data manager, class manager within CMDB Workspace.

As you drill down in the CMDB Workspace, there are some dashboards and list views that require specific roles in addition to the key CMDB Admin, CMDB Editor, or CMDB User roles.

-   **Contains Roles**

    List of roles contained within the role.

    -   cmdb\_ms\_editor
    -   sn\_cmdb\_user
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## CMDB multi-source administrator \[cmdb\_ms\_admin\]

The CMDB multi-source administrator can create and run a query and can modify CMDB 360 properties. Contains the cmdb\_ms\_write role.

-   **Contains Roles**

    List of roles contained within the role - cmdb\_ms\_editor.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## CMDB multi-source editor \[cmdb\_ms\_editor\]

CMDB multi-source editors can create and query, read, and write CMDB records, but can't perform recomputing actions.

-   **Contains Roles**

    List of roles contained within the role - cmdb\_ms\_user.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## CMDB multi-source user \[cmdb\_ms\_user\]

CMDB multi-source users have read and execute access to the multi-source queries.

-   **Contains Roles**

    List of roles contained within the role - cmdb\_read.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## CMDB reader \[cmdb\_read\]

CMDB reader users can read data from the CMDB hierarchy.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## CMDB user \[sn\_cmdb\_user\]

A key role required for interacting with CMDB Workspace. CMDB users have read-only access to CMDB data and basic UI within CMDB Workspace.

As you drill down in the CMDB Workspace, there are some dashboards and list views that require specific roles in addition to the key CMDB Admin, CMDB Editor, or CMDB User roles.

-   **Contains Roles**

    List of roles contained within the role.

    -   app\_service\_user
    -   canvas\_user
    -   cmdb\_ms\_user
    -   cmdb\_query\_builder
    -   data\_manager\_user
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Contract manager \[contract\_manager\]

Contract managers can create, edit, and delete contracts through the Contract Management application.

-   **Contains Roles**

    List of roles contained within the role.

    -   canvas\_user
    -   financial\_mgmt\_user
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## CreateNow unlimited \[unlimited\_createnow\]

Role for CreateNow unlimited licensed users.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Data classification administrator \[data\_classification\_admin\]

Data classification administrators manage all aspects of the Data Classification application, data classification code setup, and assignment.

-   **Contains Roles**

    List of roles contained within the role - data\_classification\_auditor.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Data classification auditor \[data\_classification\_auditor\]

Data classification auditors audit Data Classification code assignments.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Enterprise CMDB administrator \[ecmdb\_admin\]

Enterprise CMDB administrators can perform administrative tasks and access tables and records in Enterprise CMDB.

-   **Contains Roles**

    List of roles contained within the role - cmdb\_read.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Filter administrator \[filter\_admin\]

Filter administrators can create, edit, and delete filter \[sys\_filter\] records.

-   **Contains Roles**

    List of roles contained within the role.

    -   filter\_global
    -   filter\_group
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Filter group user \[filter\_group\]

Filter group users can create filters that belong to groups of which the user is a member.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Gauge maker \[gauge\_maker\]

Gauge makers can create gauges from reports. Starting with Helsinki, reports are no longer made into gauges.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Global filter user \[filter\_global\]

Global filter users can create global filter \[sys\_filter\] records.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Global template editor \[template\_editor\_global\]

Users with the template\_editor\_global role can create templates for global use.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Group template editor \[template\_editor\_group\]

Users with the template\_editor\_group role can create templates for groups. \(Users must also be assigned the template\_read\_global role\)

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Guided tour administrator \[guided\_tour\_admin\]

Guided tour administrators can create, modify, and delete guided tour \[sys\_embedded\_tour\_guide\] records.

-   **Contains Roles**

    List of roles contained within the role - sn\_tourbuilder.tour\_admin.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Image administrator \[image\_admin\]

Image administrators can create, modify, and delete image \[db\_image\] records.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Impersonator \[impersonator\]

Impersonators can impersonate users.

**Warning:** This role doesn’t enable the impersonation of admin users.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    For details on impersonation, see [Base system roles](r_BaseSystemRoles.md).


## Import administrator \[import\_admin\]

Import administrators can manage all aspects of import set \[sys\_import\_set\] records and imports.

-   **Contains Roles**

    List of roles contained within the role.

    -   import\_set\_loader
    -   import\_transformer
    -   import\_scheduler
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Import scheduler \[import\_scheduler\]

Import schedulers can schedule imports.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    **Warning:** Grant this role carefully. The import\_scheduler can execute scripts with administrator level privileges.


## Import set loader \[import\_set\_loader\]

Import set loader users can load import set \[sys\_import\_set\] records.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Import transformer \[import\_transformer\]

Import transformer users can manage import set transform map \[sys\_transform\_map\] records and run transforms.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Inventory administrator \[inventory\_admin\]

Inventory administrators administer stockrooms, stock models, stock rules.

-   **Contains Roles**

    List of roles contained within the role.

    -   inventory\_user
    -   canvas\_user
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Inventory user \[inventory\_user\]

Inventory users have access to stock information.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## ITIL

Information Technology Infrastructure Library \(ITIL\) users can open, update, close incidents, problems, changes, and read some rules, definitions, and CIs related to CMDB features. This role is the base system technician role. Users with the ITIL role can have tasks assigned to them.

-   **Contains Roles**

    List of roles contained within the role.

    -   agent\_workspace\_user
    -   app\_service\_user
    -   cmdb\_query\_builder
    -   cmdb\_read
    -   dependency\_views
    -   email\_composer
    -   snc\_platform\_rest\_api\_access
    -   sn\_change\_write
    -   sn\_comm\_management.comm\_plan\_viewer
    -   sn\_gd\_guidance.guidance\_user
    -   sn\_incident\_write
    -   sn\_nb\_action.next\_best\_action\_user
    -   sn\_problem\_write
    -   sn\_request\_write
    -   sn\_sow.sow\_list
    -   sn\_sow.sow\_user
    -   sn\_sttrm\_condition\_read
    -   survey\_reader
    -   template\_editor
    -   tracked\_file\_reader
    -   view\_changer
    -   viz\_creator
-   **Groups**

    List of groups this role is assigned to by default.

    -   Field Services
    -   Catalog Request Approvers &gt; $1000
    -   Catalog Request Approvers for Sales
-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## ITIL administrator \[itil\_admin\]

ITIL administrators can delete incidents, problems, changes, and other related records. This role is intended for team leads.

-   **Contains Roles**

    List of roles contained within the role.

    -   assessment\_admin
    -   sn\_bm\_client.benchmark\_data\_viewer
    -   cmdb\_read
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    Avoid granting admin roles when more specialized roles are available.


## Knowledge \[knowledge\]

Knowledge users can write, edit, and review knowledge management articles.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Knowledge administrator \[knowledge\_admin\]

Knowledge administrators can manage knowledge bases.

-   **Contains Roles**

    List of roles contained within the role - knowledge.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## List updater \[list\_updater\]

List updater users can select the **Update Entire List** and **Update Selected** menu options on a list.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Maintenance

This role is reserved for ServiceNow use.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    This role can’t be assigned or impersonated, and is reserved for ServiceNow use.


## MID server \[mid\_server\]

MID server users can access to the tables that MID servers ordinarily use. This role should be granted to your MID servers.

-   **Contains Roles**

    List of roles contained within the role - soap.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    This role should be assigned to user accounts created for MID servers to interact with your instance. For details, see [Create the MID Server user and grant the role](https://www.servicenow.com/docs/access?context=t_SetupMIDServerRole&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).


## Model manager \[model\_manager\]

Model managers can create, modify, and delete base model \[cmdb\_model\] records.

-   **Contains Roles**

    List of roles contained within the role - catalog\_editor.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Personalize \[personalize\]

Users with the personalize role can personalize forms, lists, rules, controls, and scripts.

-   **Contains Roles**

    List of roles contained within the role.

    -   personalize\_control
    -   personalize\_rules
    -   personalize\_dictionary
    -   personalize\_choices
    -   personalize\_styles
    -   personalize\_responses
    -   personalize\_list
    -   personalize\_form
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Personalize choices \[personalize\_choices\]

Users assigned to the personalize\_choices role can personalize the choices for a list field.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Personalize control \[personalize\_control\]

Personalize control users can personalize controls on lists, such as filters, links, and buttons.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Personalize dictionary \[personalize\_dictionary\]

Users with the personalize\_dictionary role can personalize dictionary entries and labels.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Personalize form \[personalize\_form\]

Users with the personalize\_form role can personalize forms.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Personalize list \[personalize\_list\]

Users with the personalize\_list role can personalize lists.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Personalize responses \[personalize\_responses\]

Users with the personalize\_form role can personalize predefined responses for suggestion fields, such as the additional comments field.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Personalize rules \[personalize\_rules\]

Personalize rules users can personalize business rules and scripts. This role contains additional roles for granting selective, administrative access to rules and scripts.

-   **Contains Roles**

    List of roles contained within the role.

    -   ui\_action\_admin
    -   business\_rule\_admin
    -   client\_script\_admin
    -   ui\_policy\_admin
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    Avoid granting this role to users who don’t need access to all the roles contained in this role.


## Personalize styles \[personalize\_styles\]

Users with the personalize\_styles role can personalize field styles.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Personalize UI \[personalize\_ui\]

Users with the personalize\_ui role can personalize forms and lists.

-   **Contains Roles**

    List of roles contained within the role.

    -   personalize\_form
    -   personalize\_list
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Platform Rest API access \[snc\_platform\_rest\_api\_access\]

Allows access to Platform Rest APIs. This role is contained with in the ITIL \[itil\] role.

-   Table API
-   Import Set API
-   Aggregate API
-   Attachment API

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Public \[public\]

No login is required to access features or functions with the public role.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Release administrator \[release\_admin\]

Release administrators can edit the release history for a release.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Report administrator \[report\_admin\]

Report administrators can manage, share, publish, and schedule all reports. Users assigned this role can access the **Reports** &gt; **Administration** module and manage all report-related objects. The report\_admin role inherits all other report roles.

-   **Contains Roles**

    List of roles contained within the role.

    -   gauge\_maker
    -   report\_alias\_admin
    -   report\_global
    -   report\_group
    -   report\_publisher
    -   report\_scheduler
    -   viz\_admin
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Report alias administrator \[report\_alias\_admin\]

Report alias administrators can maintain field and value aliases.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Report global \[report\_global\]

Report global users can manage reports that are shared with everyone \(listed in Global\).

-   **Contains Roles**

    List of roles contained within the role - report\_user.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Report group \[report\_group\]

Report group users can manage and share reports that are shared with them \(listed in Group\).

-   **Contains Roles**

    List of roles contained within the role - report\_user.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Report publisher \[report\_publisher\]

Report publisher users can publish reports any that they can manage. Publishing a report creates a public link to that report. Users with this role must also have another role that grants permission to create, edit, and share reports.

-   **Contains Roles**

    List of roles contained within the role - report\_user.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Report scheduler \[report\_scheduler\]

Report scheduler users can schedule emailing of all reports that they can see, including reports they can’t manage. Users with this role must also have another role that grants permission to create, edit, and share reports.

-   **Contains Roles**

    List of roles contained within the role - report\_user.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Report user \[report\_user\]

Report users can create and view reports that have been shared with them. Users with this role can't share, edit, or delete reports that have been shared with them.

-   **Contains Roles**

    List of roles contained within the role - viz\_creator.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Script fix administrator \[script\_fix\_admin\]

Script fix administrators can manage fix scripts.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Search application administrator \[search\_application\_admin\]

Search application administrators can insert, update, and delete search user experience-related configuration tables:

-   sys\_search\_context\_config
-   sys\_search\_source
-   m2m\_search\_context\_config\_search\_source
-   sys\_search\_facet
-   sys\_search\_filter

Search application admin is granted the ais\_admin role to enable AI search configuration.

-   **Contains Roles**

    List of roles contained within the role.

    -   ais\_admin
    -   personalize\_dictionary
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## SOAP \[soap\]

users with the soap role can query, create, update, and delete records on all tables, as well as execute scripts.

-   **Contains Roles**

    List of roles contained within the role.

    -   soap\_create
    -   soap\_delete
    -   soap\_ecc
    -   soap\_query
    -   soap\_script
    -   soap\_update
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## SOAP create \[soap\_create\]

Users with the soap\_create role can create records in all tables and columns.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## SOAP delete \[soap\_delete\]

Users with the soap\_delete role can delete records in all tables and columns.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## SOAP ECC \[soap\_ecc\]

Users with the soap\_ecc role can query, create, and update on the external communication channel \(ECC\) Queue table only.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## SOAP query \[soap\_query\]

Users with the soap\_query role can query records on all tables and columns.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## SOAP query update \[soap\_query\_update\]

Users with the soap\_query\_update role can query and update all tables and columns.

-   **Contains Roles**

    List of roles contained within the role.

    -   soap\_query
    -   soap\_update
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## SOAP script \[soap\_script\]

Users with the soap\_script role can execute business rule endpoint functions via **script.do**.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## SOAP update \[soap\_update\]

Users with the soap\_update role can update records on all tables and columns.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Survey administrator \[survey\_admin\]

Survey administrators can see all surveys, definitions, questions, and instances created by them and others. Users with this role can use all modules in the **Survey** application menu.

-   **Contains Roles**

    List of roles contained within the role.

    -   assessment\_admin
    -   sn\_bm\_client.benchmark\_data\_viewer
    -   sn\_publications\_recipients\_list\_user
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Survey creator \[survey\_creator\]

Survey creators can manage survey definitions, questions, and instances created by them.

-   **Contains Roles**

    List of roles contained within the role.

    -   sn\_bm\_client.benchmark\_data\_viewer
    -   sn\_publications\_recipients\_list\_user
-   **Groups**

    List of groups this role is assigned to by default - Survey Creators.

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Survey reader \[survey\_reader\]

Survey readers can view surveys and related information, such as survey responses, survey groups, scorecards, and reports. Users with this role can't change or modify surveys or survey responses.

-   **Contains Roles**

    List of roles contained within the role - sn\_bm\_client.benchmark\_data\_viewer.

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Task editor \[task\_editor\]

Task editors can edit protected task fields.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Template editor \[template\_editor\]

Template editors can create templates for personal use, and modify or delete personal templates. This role is included in the itil role in the base system.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Template scheduler \[template\_scheduler\]

Template schedulers can schedule template-based record creation.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Text search administrator \[text\_search\_admin\]

Text search administrators can customize Global Text Search groups and tables.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Timecard administrator \[timecard\_admin\]

Timecard administrators can access all timecard records.

-   **Contains Roles**

    List of roles contained within the role.

    -   timecard\_approver
    -   timecard\_user
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Timecard approver \[timecard\_approver\]

Timecard approvers approve or reject time cards for users.

-   **Contains Roles**

    List of roles contained within the role.

    -   pa\_viewer
    -   timecard\_user
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Timecard user \[timecard\_user\]

Timecard users can create time cards themselves, and view their own time cards.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## User \[user\]

The user role has no functionality and doesn’t grant access to any assets on your instance. Users with this role are counted as licensed fulfillers.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## User administrator \[user\_admin\]

User administrators can administer users, groups, locations, skills, and companies.

-   **Contains Roles**

    List of roles contained within the role.

    -   fsm\_skill\_admin
    -   skill\_admin
    -   territory\_admin
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## View changer \[view\_changer\]

View changers can switch active views.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Workflow administrator \[workflow\_admin\]

Workflow administrators can create, edit, publish, or delete graphical workflows.

-   **Contains Roles**

    List of roles contained within the role.

    -   activity\_creator
    -   itom\_admin
    -   workflow\_creator
    -   workflow\_publisher
-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


## Workflow creator \[workflow\_creator\]

Workflow creators can create graphical workflows.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Workflow publisher \[workflow\_publisher\]

Workflow creators can publish graphical workflows.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Workflow report viewer \[workflow\_report\_viewer\]

Workflow report viewers can access the workflow scratchpad for reports.

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None


## Zing text search administrator \[ts\_admin\]

Users with the ts\_admin role can administer the [Zing text indexing and search engine](../../search-administration/concept/c_ZingTextSearch.md).

-   **Contains Roles**

    List of roles contained within the role.

    None

-   **Groups**

    List of groups this role is assigned to by default.

    None

-   **Elevated**

    Whether the role is an elevated role. Elevated roles aren’t assigned to users or groups, and must be used by elevation. For details, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    No

-   **Special considerations**

    None.


-   **[Special administrative roles](r_SpecialAdministrativeRoles.md#)**  
Certain roles grant specific administrative rights without the full privileges of the admin role. For example, an administrator can grant a user the right to change UI policy but not client scripts.
-   **[Read-only role](../../user-administration/concept/c_ReadOnlyRole.md#)**  
The read-only role \(snc\_read\_only\) restricts a user or a group of users to read-only access on the tables to which the user already has access.
-   **[Application specific roles](application-specific-roles.md)**  
Applications you install on your instance may include additional roles. Follow the links in this section to see roles installed along with applications.

**Parent Topic:**[Managing roles](../concept/ua-creating-roles.md)

