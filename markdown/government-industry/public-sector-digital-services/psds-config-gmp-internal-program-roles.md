---
title: Configure custom internal program team roles
description: By default, five internal program team personas are included as part of the Grants Management application: Approver, Collaborator, Observer, Program Co-lead, and Program Lead. Set up new roles in the internal program team activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/public-sector-digital-services/psds-config-gmp-internal-program-roles.html
release: zurich
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Create internal program team, Set up a grant program, Grants Management Program Setup, Grants Management, Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Configure custom internal program team roles

By default, five internal program team personas are included as part of the Grants Management application: Approver, Collaborator, Observer, Program Co-lead, and Program Lead. Set up new roles in the internal program team activity.

## Before you begin

Role required: admin

## Procedure

1.  From the navigation menu, search and open **Resource Roles** and select **New**.

2.  Enter the name of the internal program team role you want to add, specify the hourly rate, and select **Submit**.

3.  From the navigation menu, search for and select **Client scripts**, and open the **NameRoleView Field labels/attributes** record.

4.  In the **Messages** field, enter the name of the role that was added, and add a line in the script to include the option.

    \[Omitted image "psds\_config\_internalprogramteam\_script.png"\] Alt text:


## Result

The new role will appear in the dropdown to be selected during the internal program team activity. To configure read/write access for these roles, see [Configure read/write access roles for the Grants Management internal program team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-internal-team-default-roles.md).

