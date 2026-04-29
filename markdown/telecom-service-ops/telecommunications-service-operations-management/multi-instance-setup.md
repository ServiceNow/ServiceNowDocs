---
title: Set up multiple Nokia Altiplano instances
description: Learn how to configure and manage multiple Nokia Altiplano instances within a single ServiceNow environment. This enables administrators and integrators to create independent connection aliases and import schedules customized to specific filtering or frequency needs.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Nokia Altiplano SGC, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Set up multiple Nokia Altiplano instances

Learn how to configure and manage multiple Nokia Altiplano instances within a single ServiceNow environment. This enables administrators and integrators to create independent connection aliases and import schedules customized to specific filtering or frequency needs.

## Before you begin

Role required: TSOM Visibility admin

## About this task

Confirm you have:

-   You’re operating in the Service Graph Connector for NOKIA Altiplano application scope.
-   Installed the Service Graph Connector for Nokia Altiplano.
-   Completed the guided setup for the initial Altiplano instance.
-   MID Server set up and validated.

You can configure additional Nokia Altiplano instances or reuse the same Altiplano instance with different connection aliases and import schedules. To add a new Altiplano instance, rerun the Guided setup to configure a new connection alias. Go through all connectivity stages in the setup for each new alias.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Nokia Altiplano** &gt; **Setup**.

2.  On the Getting Started page, select **Get Started**.

    Repeat all the steps under the Configured Connectivity section. It creates configuration entries for the new instance of Nokia Altiplano. For more information, see [Set up Nokia Altiplano](initial-setup-procedure.md).

3.  Configure the connectivity by creating a connection alias, credentials, and HTTP connection.

    1.  In the Configure Connectivity section, select Get Started.

    2.  Select Configure to create a new connection alias by entering a unique alias name \(for example, `Altiplano_Prod_01`\).

    3.  Select **Submit** and mark the step as complete.

4.  Configure credentials for the new Altiplano instance.

    1.  Specify a user name and password for the Altiplano Controller.

    2.  Submit and mark the step as complete.

5.  Configure an HTTP connection.

    1.  Provide the connection name.

    2.  Select the newly created credentials and connection alias.

    3.  Enter the connection URL of the Nokia Altiplano instance.

    4.  Enable use MID Server and choose the appropriate MID option.

    5.  Select **Submit** and mark the step as complete.

6.  Schedule data imports using either bulk or filtered discovery by configuring the import schedule.

    1.  Fill in the fields.

        For more information, see [Set up Nokia Altiplano](initial-setup-procedure.md).

    2.  In the **Use connection** field, choose the new Altiplano instance.

7.  Select **Submit**.


## Result

To confirm that your new instance setup is successful, you can verify the configuration.

-   Navigate to All &gt; Service Graph Connectors &gt; Nokia Altiplano &gt; Connection &amp; Credential Aliases and confirm that the new alias is listed.
-   Navigate to All &gt; Service Graph Connectors &gt; Nokia Altiplano &gt; Import Schedule and confirm that the new import schedule is listed and confirm that corresponding jobs exist for each alias.

You can configure multiple connection aliases over the same Nokia Altiplano instance. This flexibility enables you to run imports at different frequencies and apply different filters to each alias.

Example: Altiplano\_Weekly\_OLT\_10.10.10.\*: Runs weekly, filters OLTs with IPs in the 10.10.10.\* range. Altiplano\_Daily\_Prod: Runs daily, filters OLTs whose name contains "prod\_olt".

**Related topics**  


[Configure concurrent import and parallel loading for Nokia Altiplano](configure-concurrent-import-and-parallel-loading.md)

[Mapping Nokia Altiplano CIs and Relationships in CMDB](../concept/data-mapping.md)

[System components installed with Nokia Altiplano](../reference/properties-installed-with-nokia-altiplano.md)

