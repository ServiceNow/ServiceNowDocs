---
title: Installed with teamspaces
description: The tables and roles that are installed with project teamspaces are prefixed with an abbreviation based on the name of teamspace.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Teamspaces in Project Management, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Installed with teamspaces

The tables and roles that are installed with project teamspaces are prefixed with an abbreviation based on the name of teamspace.

## Tables

The tables are extended from the Project, Idea, and Demand base application tables.

<table id="table_htr_pgv_cs"><thead><tr><th>

Tables

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Idea \[prefix\_idea\]

</td><td>

Stores ideas.

</td></tr><tr><td>

Demand \[prefix\_demand\]

</td><td>

Stores demands.

</td></tr><tr><td>

Project \[prefix\_project\]

</td><td>

Store projects.

</td></tr><tr><td>

Portfolio \[prefix\_portfolio\]

</td><td>

Stores portfolios.

</td></tr><tr><td>

Project Task \[prefix\_project\_task\]

</td><td>

Stores project tasks.

</td></tr><tr><td>

Portfolio Goal \[prefix\_portfolio\_goal\]

</td><td>

Stores portfolio goals.

</td></tr><tr><td>

Portfolio Issues \[prefix\_portfolio\_issue\]

</td><td>

Stores portfolio issues.

</td></tr><tr><td>

Portfolio Risk \[prefix\_portfolio\_risk\]

</td><td>

Stores portfolio risks.

</td></tr><tr><td>

Portfolio Project \[prefix\_portfolio\_project\]

</td><td>

Stores portfolio projects.

</td></tr><tr><td>

Project Template \[prefix\_project\_template\]

</td><td>

Stores project templates.**Note:** Project templates that are created in a teamspace area are not available in the main Project Management application any longer. They are only available to the teamspace in which they were created.

</td></tr><tr><td>

Project Template Task \[prefix\_project\_template\_task\]

</td><td>

Stores project template tasks.

</td></tr><tr><td>

Stakeholder Register \[prefix\_stakeholder\_register\]

</td><td>

Stores the stakeholders.

</td></tr><tr><td>

Program \[prefix\_pm\_program\]

</td><td>

Stores programs.

</td></tr><tr><td>

Program Task \[prefix\_pm\_program\_task\]

</td><td>

Stores program tasks.

</td></tr><tr><td>

Program Task \[prefixpm\_program\_task project\_status\]

</td><td>

Stores program task project status.

</td></tr></tbody>
</table>## Roles

|Role|Description|
|----|-----------|
|prefix\_demand\_manager|Managers of the demand features for the teamspace.|
|prefix\_demand\_user|Users of the demand features for the teamspace.|
|prefix\_project\_manager|Managers of the project features for the teamspace.|
|prefix\_project\_portfolio\_user|Users of the project portfolios for the teamspace.|
|prefix\_project\_user|Users of the project features for the teamspace.|
|prefix\_program\_manager|Managers of the program features for the teamspace.|
|prefix\_portfolio\_manager|Managers of the portfolio features for the teamspace.|

The teamspace application uses the same views that are provided in the Project, Idea, and Demand base applications.

**Note:** Default client scripts that these base applications use are inherited by the extended tables in the teamspace application. If you created custom client scripts for any of the base applications, select the **Inherited** options on each Client Script form before you create the teamspace.

**Parent Topic:**[Using Teamspaces in Project Management](../concept/c_Teamspaces.md)

**Related topics**  


[Activate teamspaces](../task/t_ActivateTeamspaces.md)

[Configure teamspace settings](t_EnableATeamspace.md)

[Using Teamspaces in Project Management](../concept/c_Teamspaces.md)

