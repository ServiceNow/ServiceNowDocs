---
title: Exploring Access Analyzer
description: Analyze identities on the ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access Analyzer, Access Management]
---

# Exploring Access Analyzer

Analyze identities on the ServiceNow AI Platform instance.

ServiceNow AI Platform Access Analyzer is an access diagnostic tool designed for AI administrators or creators to validate the access controls configured within various resources and agentic assets \(agentic workflows and AI agents\).

**Note:**

-   Access Analyzer is a ServiceNow Store product. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps and for information about submitting requests to the store.
-   Access Analyzer impersonates the identity record to retrieve details about the permissions and doesn’t read or store any personal or sensitive data of the identity.
-   Access Analyzer evaluation results are the same irrespective of any access policies defined for the users such as zero trust access \(ZTA\). The policies are only evaluated during the actual user login and aren’t evaluated during the Access Analyzer flow.
-   Access Analyzer has limitations in accurately evaluating access of the resources related to managed scope resources and delegated developer.

## Evaluate Access

Evaluate Access is a capability of the ServiceNow AI Platform Access Analyzer, which helps the administrators to view permissions for the selected user, role, group, agentic workflow, and AI agents.

You can analyze and view the permissions of users, groups, roles for a table, client callable script includes, UI pages, and REST endpoints.

Using Access Analyzer, organizations can improve their security posture, identity governance, risk management, achieve their compliance goals, and understand who \(identity\) has access to what \(resources\).

## Compare Access

Compare Access is a capability of the ServiceNow AI Platform Access Analyzer V2, which enables administrators to compare user access and determine the right level of access for the users on your ServiceNow AI Platform instance.

Compare Access can be performed between the users for the user records and access control.

You can perform the following analyzes:

-   Level 1: Compare user records to understand the attributes, roles, groups, agentic workflow, and AI agents.
-   Level 2: Compare access controls to run the root cause analysis by finding access issues.

## Benefits

The following are some of the benefits of using Access Analyzer:

-   Analyze access to resources \(tables\).
-   Compare the access of two users.
-   Compare the roles and groups of two users.
-   Generate a report showing whether an identity has access to a resource \(table\).
-   Understand who has access for critical security hygiene.
-   Avoid over-provisioning permissions.
-   Achieve the least privilege principals when implementing access controls.
-   Limit access to certain data, which includes applications, tables, rows or columns, and other resources.
-   Provide reporting capabilities for the analyzer results.
-   Compare access between user records and access controls.
-   Determine the right level of access for users on your ServiceNow AI Platform instance.

