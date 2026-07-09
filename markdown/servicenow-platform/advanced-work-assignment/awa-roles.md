---
title: Advanced Work Assignment roles
description: Advanced Work Assignment \(AWA\) is installed with these roles.The AWA administrator configures and manages AWA.The AWA agent handles customer interactions and manages workload across multiple service channels.The AWA integration user uses the AWA integration APIs.The AWA manager monitors the performance of agents across all service channels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/advanced-work-assignment/awa-roles.html
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Advanced Work Assignment roles

Advanced Work Assignment \(AWA\) is installed with these roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[Advanced Work Assignment reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/advanced-work-assignment/reference-awa.md)

**Related topics**  


[Assignment Rule form]()

[Domain separation and Advanced Work Assignment]()

[Components installed with Advanced Work Assignment]()

[Properties for Advanced Work Assignment]()

[Advanced Work Assignment monitoring page]()

## AWA administrator \[awa\_admin\]

The AWA administrator configures and manages AWA.

### Contains Roles

List of roles contained within the role.

-   chat\_survey\_admin
-   interaction\_agent
-   quickactions\_user
-   sn\_ace.ace\_user
-   sn\_ci\_gs\_content.ci\_guided\_setup\_admin

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## AWA agent \[awa\_agent\]

The AWA agent handles customer interactions and manages workload across multiple service channels.

### Contains Roles

List of roles contained within the role.

-   quickactions\_user
-   sn\_templated\_snip.template\_snippet\_reader

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## AWA integration user \[awa\_integration\_user\]

The AWA integration user uses the AWA integration APIs.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## AWA manager \[awa\_manager\]

The AWA manager monitors the performance of agents across all service channels.

### Contains Roles

List of roles contained within the role.

-   interaction\_agent
-   quickactions\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

