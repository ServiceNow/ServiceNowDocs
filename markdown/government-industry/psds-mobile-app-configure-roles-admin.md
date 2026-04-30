---
title: Configure public sector roles and permissions for Mobile Agent app
description: Configure user roles for government service agents to access the Mobile Agent app. This step is mandatory for any government service agent to be able to work from the app.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Mobile Agent for Service Request Playbook, Service Request Playbook, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure public sector roles and permissions for Mobile Agent app

Configure user roles for government service agents to access the Mobile Agent app. This step is mandatory for any government service agent to be able to work from the app.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter **sys\_sg\_applet\_launcher.list** to open the Applet Launchers \[sys\_sg\_applet\_launcher\] table.

2.  From the Launcher screens table, select the **Cases** record.

    The Required Roles record should contain only the Customer Service Agent \(sn\_customerservice\_agent\) role.

3.  If prompted, switch from the Global application to the Customer Service Mobile application.

4.  Select the edit icon \(![Edit icon.](../../configuration-data-management/image/icon-edit-pencil.png)\) under Required Roles and add the following roles:

    -   sn\_gsm.agency\_manager
    -   sn\_gsm.government\_service\_manager
    -   sn\_gsm.constituent\_agent
    -   sn\_gsm.business\_agent
    -   sn\_gsm.agency\_constituent\_agent
    -   sn\_gsm.agency\_agent
5.  Select **Done** to save the roles.

    Agents with the above roles can now log in to the Mobile Agent and work on Service Request cases assigned to them.


