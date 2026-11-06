---
title: Access analyzer capabilities
description: Analyze identities on the ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/explore-access-analyzer.html
release: zurich
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Access analyzer, Access Management]
---

# Access analyzer capabilities

Analyze identities on the ServiceNow instance.

ServiceNow Access analyzer is an app that helps the administrators to view permissions for the selected user, role, or group.

**Note:**

-   Access analyzer is a ServiceNow Store product. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store.
-   Access analyzer impersonates the identity record to retrieve details about the permissions and doesn’t read or store any personal or sensitive data of the identity.
-   Access analyzer evaluation results are the same irrespective of any access policies defined for the users such as Zero trust access \(ZTA\). The policies are only evaluated during the actual user login and aren’t evaluated during the access analyzer flow.
-   Access analyzer has limitations in accurately evaluating access of the resources related to managed scope resources and delegated developer.

## Access evaluation

Evaluate Access is a capability of the ServiceNow Access Analyzer, which helps the administrators to view permissions for the selected user, role, or group.

It enables you to analyze and view the permissions of users, groups, roles for a table, client callable script includes, UI pages, and REST endpoints.

Using Access Analyzer, organizations can improve their security posture, identity governance, risk management, support their compliance goals, and understand who \(identity\) has access to what \(resources\).

## Access comparison

Compare Access is a capability of the ServiceNow Access analyzer V2, which enables administrators to compare user access and determine the right level of access for the users on your ServiceNow instance.

Compare Access can be performed between the users for the user records and access control.

Compare Access enables you to perform the following analysis:

-   Level 1: Compare user records to understand the attributes, roles, and groups.
-   Level 2: Compare access controls to run the root cause analysis by finding access issues.

## Benefits

The following are some of the benefits of using the Access analyzer:

-   Analyze access to resources \(tables\).
-   Compare the access of 2 users.
-   Compare the roles and groups of 2 users.
-   Generate a report showing whether an identity has access to a resource \(table\).
-   Understand who has access for critical security hygiene.
-   Help avoid over-provisioning permissions.
-   Achieve the principle of least privilege when implementing access controls.
-   Limit access to certain data, which includes applications, tables, rows or columns, and other resources.
-   Provide reporting capabilities for the analyzer results.
-   Compare access between user records and access controls.
-   Determine the right level of access for users on your ServiceNow instance.

