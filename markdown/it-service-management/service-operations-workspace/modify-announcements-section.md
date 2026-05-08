---
title: Configure the Announcements section on the landing page
description: Customize an existing announcement or add an announcement for additional tables.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Landing page configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the Announcements section on the landing page

Customize an existing announcement or add an announcement for additional tables.

## Before you begin

Role required: admin

## About this task

You can customize how the Entity View Action Mapper \(EVAM\) component is configured for the **Announcements** section. While the data can be customized for the default landing page, the visual styling changes can be done only by creating a copy of the landing page. In the base system, announcements and the corresponding data sources are defined for the following tables:

-   Outage \[cmdb\_ci\_outage\]
-   Banner Announcement \[sys\_ux\_banner\_announcement\]
-   Incident \[incident\]

You can add announcements for additional tables by defining additional data sources in the EVAM definition.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview**.

2.  On the **Overview** tab, from the **Initial Setup** section, select the **Configure the landing page** option.

3.  On the Landing Page form, under **Tier 1** or **Tier 2** sections, select **Configure** next to the **Announcements** option.

    The SOW - Announcements EVAM definition is displayed. For information on EVAM definition, see Create an EVAM definition.

4.  Navigate to **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **EVAM Definitions**.

5.  To edit the data source of an announcement, navigate to the EVAM Datasource M2Ms related list and edit the required data source.

    For information on data source, see Define a datasource.

6.  To create an announcement for an additional table, add a data source for that table.

    For information on data source, see Define a data source. For information on defining a data source, see Define a datasource.

7.  To source custom announcements into the **Announcements** section, create an additional banner announcement configuration for the Banner Announcement \[sys\_ux\_banner\_announcement\] table by performing the following steps.

    1.  Create a banner announcement configuration and the corresponding banner announcements.

        For information on creating a banner announcement configuration, see Next Experience banner announcements.

    2.  Associate the banner announcement configuration with the **sn\_sow.banner\_announcements\_config\_id** property.

        1.  Navigate to sys\_properties.list
        2.  Select the **sn\_sow.banner\_announcements\_config\_id** property.
        3.  On the System Property form, specify the sys\_id of the banner configuration as the property value.
8.  To configure how an announcement should be displayed for a data source, edit an EVAM view configuration and template by performing these steps.

    1.  Navigate to the EVAM View Config Bundle M2Ms related list and select the required configuration bundle.

    2.  On the EVAM View Config Bundle form, navigate to the EVAM View Configs related list and select a configuration for the required data source.

    3.  On the EVAM View Config form, open the template from the **View Template** field.

    4.  On the View Template form, edit the **Template** field.

        For information on editing a template, see Define an EVAM view template.

    5.  Select **Update**.


**Parent Topic:**[Landing page configurations in Service Operations Workspace for ITSM](../concept/landing-page-configurations-sow-itsm.md)

