---
title: Getting started with checks
description: Checks are singular focused rules that detect anomalies or opportunities in an instance. These checks can run against tables, records, or metadata. Checks are defined to identify security, upgrade best practices, manageability, user experience and performance vulnerabilities.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Instance Scan, Maintain and monitor, Administer]
---

# Getting started with checks

Checks are singular focused rules that detect anomalies or opportunities in an instance. These checks can run against tables, records, or metadata. Checks are defined to identify security, upgrade best practices, manageability, user experience and performance vulnerabilities.

## Check types

You can create your check by selecting one of these types.

-   **Table Check**

    Create a check by selecting **Create a new Table Check** if you know which specific table and conditions you want to test. This check type is applied on only one table at a time. You can also include your own script for more complex capabilities by selecting the **Advanced** option on the form.

-   **Column Type Check**

    Retrieve all records containing a specific column field type from all tables in an instance by selecting **Create a new Column Type Check**. The **Column Type Check** type implements the rule you created to iterate all records matching the target column field type.

-   **Script Only Check**

    Create a check without specifying a table or a column type by selecting **Create a new Script Only Check**. You can verify meta data, configurations, and execute complex checks by writing your own script.

-   **Linter Check**

    Create a linter check to identify any issues in a script. When a linter check is run on a record, an abstract syntax tree for its code is generated. You can use the abstract syntax tree to analyze issues with the code.


