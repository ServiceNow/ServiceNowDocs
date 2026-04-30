---
title: Define agile structure in EAP
description: Add organizational entities and teams to an Enterprise Agile Planning \(EAP\) configuration so that users can plan work for them in the EAP Backlog and Planning Board.
locale: en-US
release: yokohama
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Define agile structure in EAP

Add organizational entities and teams to an Enterprise Agile Planning \(EAP\) configuration so that users can plan work for them in the EAP Backlog and Planning Board.

## Before you begin

[Activate an EAP configuration](activate-eap-configuration.md).

Ensure that **Application Scope** of your ServiceNow instance is set to **Strategic Planning**.

Role required: sn\_apw\_advanced.eap\_admin

## About this task

Define your Agile team structure in Enterprise Agile Planning. 

Based on your configuration, add entities such as Portfolios, Solutions Trains, ARTs, and Agile Teams to different team levels of the configuration.

**Note:** This task is explained using **Full Configuration** as an example. Use these steps as guidance to add entities and teams to any other configuration in EAP.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  From the **Settings** menu, select **Enterprise Agile Planning** &gt; **Agile structure**.

3.  Add a Portfolio by selecting the + icon \(![Add icon.](../images/eap-add-icon.png)\) next to the configuration name.

    ![Option to add teams to Agile structure.](../images/eap-add-portfolio.png)

    1.  On the SAFe Portfolio form, fill in details such as name, description and parent portfolio.

    2.  Select **Submit**.

    3.  Repeat the action to add as many portfolios as you need.

4.  Repeat this action to add other entities to a Portfolio.

    -   To a portfolio, add Solution Trains.
    -   To a Solution Train, add Agile Release Trains \(ART\).
    -   To an ART, add Agile Teams.

        The teams that you add as Agile Teams must be of the type **Agile**. If you need new teams or cannot find any existing teams, contact your admin. For more information, see [Assignment groups in Agile Development 2.0](../../agile-development/concept/manage-groups-agile-dev.md).

    ![Agile structure for a Full Configuration in EAP.](../images/eap-agile-structure-full-safe.png)


