---
title: Relate the information object to the database catalog
description: The information object draws the physical data from the database catalog, which references the database instances. Hence, create a relationship that is suggested between the information object and the database catalog.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Relate the information object to the database catalog

The information object draws the physical data from the database catalog, which references the database instances. Hence, create a relationship that is suggested between the information object and the database catalog.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

Suggested cmdb CI relationship, Depends on::Used by, relates the information object to the database catalog. The relationship works by drawing the physical data from the database and stores it as logical data in the information object table, which references the data domain.

For example, employee payroll details depends on Oracle database instance. If the relationship is reversed between the configuration items, then Oracle database instance is used by employee payroll.

-   IT Operations Management Discovery discovers all servers, instances, and databases.
-   Database Catalog is a list of all the databases.
-   The Database Catalog \(cmdb\_ci\_db\_catalog\) lists all the catalog objects or databases that are discovered from an instance of a database. For example, Oracle catalog and MySQL catalog are child tables of the database catalog.
-   The Database Instance \(cmdb\_ci\_db\_instance\) is the parent table. Oracle Instance \(cmdb\_ci\_db\_ora\_instance\) and MySQL instance are child tables of the Database Instance.
-   The reference between a database instance and a database catalog is one to many.
-   Since the database instance is hosted on the Server \(cmdb\_ci\_server\), it can access all the underlying configuration items.

**Note:**

You may have applications, the data of which are not stored in a conventional database. You can also track such unstructured data stored in configuration item tables such as configuration file \(cmdb\_ci\_config\_file\), file system \(cmdb\_ci\_file\_system\), and exchange mail box \(cmdb\_ci\_exchange\_mailbox\). Use the same Depends On::Used by relationship type between the information object and the unstructured data sources to track the data.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Information Portfolio** &gt; **Information Objects**.

2.  To create a suggested relationship between the information object and the database catalog, open the information object record.

3.  In the Related Items section of the Information Object form, click the add CI relationship icon \(![CI relationship icon](../image/RelationshipEditorIcon.png)\) to launch the relationship editor and create the CI relationship.

    The filter is automatically applied on the database catalog.

4.  Select the Depends on::Used By suggested relationship type.

5.  In the Configuration Items section, select the record that is of a catalog class.

6.  In the Relationships section, click the CI relationship icon \(![CI relationship icon](../image/RelationshipEditorIcon.png)\).

7.  Click **Save and Exit**.

    Ensure that the database catalog table has a reference of the database instance.


## What to do next

Click the show dependency views icon \(![Show dependency icon](../image/ShowDependencyIcon.png)\) in the **Information Object** related items to view the dependency of the business application that is using the information object, which is running on a database server.

![Dependency view of the information object](../image/DependencyViewInfoPortfolio.png "Dependency view of the information object")

Apply the information portfolio for auditing. [Integrate with GRC](apm-grc-integration-identify-risks.md#) \(Governance, Risk, and Compliance\) and use the information object as an entity. GRC uses any entity such as a database, server, or a business application to audit. Associating the information object as an audit entity gives you the complete profile of the business application that uses the information object and its source of data.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

