---
title: Spotlight database views
description: Spotlight ensures that a database view joins the Spotlight \[spotlight\] table and the facts table whose records the Spotlight group evaluates. You need this database view to use Spotlight interactive analysis. Administrators can access this database view to create reports or to diagnose problems.
locale: en-US
release: australia
product: Spotlight
classification: spotlight
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering Spotlight, Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Spotlight database views

Spotlight ensures that a database view joins the Spotlight \[spotlight\] table and the facts table whose records the Spotlight group evaluates. You need this database view to use Spotlight interactive analysis. Administrators can access this database view to create reports or to diagnose problems.

After creating the database view, Spotlight adds a reference to it in the related Spotlight Group record on the Spotlight Group \[spotlight\_groups\] table. The reference consists of the primary key field value of the database view, which is in the database\_view column of the record.

**Note:** If you upgrade from an earlier version than London, you start with an empty database\_view value in the database\_view column of your spotlight\_groups records. This empty column has no impact. The column populates as users modify the records in the spotlight\_groups table.

If you are an administrator, you can access the database view directly. To see the database view for a Spotlight Group, click the **Show Database View** related link on the Spotlight Group form. You can also add a **Database View** column to the Spotlight Groups list.

If the database view is missing or invalid, an error message appears on the Spotlight Group record. In this case, you can click the **Generate Database View** related link, which becomes available. A message appears afterwards to inform you whether database generation succeeded.

![Spotlight group form with missing database view warning and highlighted Generate database view link](../image/spotlight-missing-db-view.png "Spotlight group with missing database view")

If you delete a Spotlight group, Spotlight deletes the database view associated with that group if it is safe to do so. To determine whether it is safe to delete the database view, Spotlight checks for the following conditions:

-   Do any other Spotlight groups have a reference to that database view?
-   Are any other Spotlight groups defined with a main indicator that uses the same facts table as the main indicator of the group that you are deleting?

If neither condition is true, Spotlight deletes the database view.

When creating, modifying, or deleting database views, Spotlight runs these business rules:

-   Update Database View
-   Delete Database View
-   Set DB View on Insert

**Parent Topic:**[Administering Spotlight](administering-spotlight.md)

**Related topics**  


[Database views](https://www.servicenow.com/docs/access?context=c_DatabaseViews&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

