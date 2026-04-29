---
title: Create a data domain
description: A data domain is a collection of information objects. Relate an information object to the database catalog of a database instance to collect the physical data. ServiceNow Discovery finds the database catalog that lists all the catalog objects, or databases, discovered for an instance of a database.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create a data domain

A data domain is a collection of information objects. Relate an information object to the database catalog of a database instance to collect the physical data. ServiceNow Discovery finds the database catalog that lists all the catalog objects, or databases, discovered for an instance of a database.

## Before you begin

**Important:**

Starting with the Xanadu release, the data domains module has been deprecated from Enterprise Architecture \(formerly Application Portfolio Management\). However, if you’re an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still use the data domains module. If you’re a new activation user, the data domains module isn’t available.

You can leverage the same feature by using the Enterprise Architecture Workspace. To learn more, see [Exploring data domains](../concept/eaw-concept/eaw-data-domains.md).

Role required: sn\_apm.apm\_user

Although an Enterprise Architecture user \(sn\_apm.apm\_user\) can create a data domain, the access control on the Data Domain \[sn\_apm\_data\_domain\] table is limited to its different users.

-   The Application Portfolio Analyst and Application Portfolio Administrator with sn\_apm.apm\_admin role have create, write, and delete privileges.
-   The Application Portfolio User with sn\_apm.apm\_user role has read access only.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Information Portfolio** &gt; **Data Domains**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For field information, see [Data Domain form](../reference/data-domain-form.md).

4.  Select **Submit**.


## What to do next

Create an information object and link the data domain with the information object.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

