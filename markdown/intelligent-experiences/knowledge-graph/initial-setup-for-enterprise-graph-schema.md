---
title: Initial setup for Enterprise Graph schema in production instance
description: Setup and use Enterprise Graph Schema, a unified knowledge graph schema, that captures all the ServiceNow and third party tables and their connections.
locale: en-US
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2025-11-21"
reading_time_minutes: 1
breadcrumb: [Using Enterprise graph schema, Knowledge Graph, Enable AI experiences]
---

# Initial setup for Enterprise Graph schema in production instance

Setup and use Enterprise Graph Schema, a unified knowledge graph schema, that captures all the ServiceNow and third party tables and their connections.

## Before you begin

When you install Enterprise Graph, it automatically begins configuring instance tables. This may take several days and until the setup is complete, the schema won’t respond effectively to queries.

If you have already completed the setup in sub-production instance, you can import the generated descriptions to production instance and fasten the process.

Assuming that you have completed the setup in sub-production instance, do the following to complete the initial setup in production instance:

-   Create an integration user, in the sub-production instance. For more information, see [https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/users-and-groups/task/t\_CreateAUser.html](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html)
-   Verify if the descriptions are generated in sub-production instance.
-   Use the following procedure to:
    -   Import the data into production.
    -   Run the associated Transform Maps.
-   Remove tracker records from the production instance.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    ![Connection and credentials navigation](../Images/connection-and-credntials-page.png)

2.  Open the record with name **Description\_Connector**.

3.  Select **Create New Connection &amp; Credential** from the related links section.

    ![Create connection and credentials aliases](../Images/connection-and-credentials-aliases.png)

4.  Enter the required details in the **Create Connection &amp; Credential** form.

    ![Create connection and credentials form](../Images/create-connection-and-credntials.png)

5.  Add the user name and password that was used, while creating the new user.

    See [https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/users-and-groups/task/t\_CreateAUser.html](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/users-and-groups/task/t_CreateAUser.html) for more information.

6.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources**.

7.  In the name field search bar, enter **KG** to view the related tables.

    The following tables are displayed:

    -   KG Choice Picker Description.
    -   KG Column Picker Description.
    -   KG Table Picker Description.
    -   KG Triplet Picker Description.
    ![Picker description options](../Images/choice-tables-kg.png)

8.  Open one of the displayed table and select **Load All Records** from the Related links section.

    Ensure the data is loaded.![KG Table picker](../Images/table-picker-kg.png)

9.  Navigate to **System Import Sets** &gt; **Advanced** &gt; **Import Sets**, once the data is loaded.

    For detailed information, see import set documentation [https://www.servicenow.com/docs/bundle/yokohama-integrate-applications/page/administer/import-sets/reference/import-sets-landing-page.html](https://www.servicenow.com/docs/bundle/yokohama-integrate-applications/page/administer/import-sets/reference/import-sets-landing-page.html)![Import set](../Images/import-set-kg.png)

10. Open the import set and select **Transform** from the Related links section.

    For detailed information, see Transform map documentation [https://www.servicenow.com/docs/bundle/yokohama-integrate-applications/page/script/server-scripting/concept/c\_CreatingNewTransformMaps.html](https://www.servicenow.com/docs/bundle/yokohama-integrate-applications/page/script/server-scripting/concept/c_CreatingNewTransformMaps.html)

11. Select **Transform** to complete the transformation.

    ![Transform option](../Images/transform-page-kg.png)

12. Navigate to the selected table and verify if the data is loaded.

13. Repeat the import set and transformation steps for other three tables.


