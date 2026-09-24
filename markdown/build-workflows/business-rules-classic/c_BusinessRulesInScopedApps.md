---
title: Business rules in scoped applications
description: Every business rule is assigned to either a private application scope or to the global scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/business-rules-classic/c\_BusinessRulesInScopedApps.html
release: brazil
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Classic Business rules, Build workflows]
---

# Business rules in scoped applications

Every business rule is assigned to either a private application scope or to the global scope.

The types of business rules you can create and how you can access those rules varies depending on the scope of the business rule and the scope of the table it runs on.

**Note:** The term global can refer to two different aspects of a business rule: the table it runs on and the scope it runs in. Business rules can either run on specific tables or be global. In addition, they can be in the global scope or in a private application scope.

## Business rules on specific tables

Most business rules run on a specific table, which is defined in the **Table** field. You can create business rules on tables in the same scope and on tables that allow configuration records from another application scope.

For tables that are in a different scope than the business rule record, the types of rules are limited.

-   You can create a rule where **When is async** with any of the following options:
    -   **Insert**, **Update**, and **Delete** database operations. You cannot select **Query**.
    -   **Set field values** actions and scripts \(the **Script** field\).
-   You can create a rule where When is before with any of the following options:
    -   **Insert**, **Update**, and **Delete** database operations. You cannot select **Query**.
    -   **Set field values** actions only. You cannot write scripts and you cannot abort the database transaction.
-   You cannot create any other types of business rules on tables in a different scope.

Business rules on specific tables cannot be accessed by other business rules or scripts.

## Global business rules

**Warning:** Consider using script includes instead of global business rules. Script includes load only on request while global business rules load on every page in the system.

Global business rules are business rules where the **Table** field is set to **Global**. Global business rules may be accessible on multiple tables and from other scripts, depending on their scope protection. For a global business rule, define the scope protection by setting the **Accessible from** field:

-   **This application scope only**: prevents applications in a different scope than the business rule from calling this business rule.
-   **All application scopes**: allows any application to call this business rule.

    **Note:** Global business rules do not support domain separation.


## Scripts in scoped business rules

When you write a script in a business rule, you can access:

-   Any script includes and global business rules in the same scope as the business rule.
-   Script includes and global business rules that allow applications in a different scope to call them. To call functions from another scope, you must specify the scope of the function.
-   For business rules in a unique scope, you can access the scoped system APIs only.

**Parent Topic:**[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_BusinessRules.md)

