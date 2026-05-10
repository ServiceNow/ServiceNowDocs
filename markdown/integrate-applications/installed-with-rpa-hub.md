---
title: Components installed with RPA Hub
description: Several types of components are installed with the activation of the RPA Hub plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Reference, RPA Hub, Workflow Data Fabric]
---

# Components installed with RPA Hub

Several types of components are installed with the activation of the RPA Hub plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this plugin.

## Roles installed

**Note:** RPA role requires access to the cmdb\_rel\_ci table. If there are any customizations to the cmdb\_rel\_ci ACLs, provide the relevant read access role to the following RPA roles.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

RPA admin\[sn\_rpa\_fdn.rpa\_admin\]

</td><td>

Sets up RPA Hub application configurations and manages RPA Hub system property settings in various environments.

</td><td>

-   fd\_read
-   itil
-   sn\_rpa\_fdn.rpa\_user
-   cmdb\_read

</td></tr><tr><td>

RPA assisted user\[sn\_rpa\_fdn.rpa\_assisted\_user\]

 **Note:**

Assisted user is attended user.

</td><td>

Executes attended automations.

</td><td>

None

</td></tr><tr><td>

RPA business user\[sn\_rpa\_fdn.rpa\_business\_user\]

</td><td>

Manages data like work items, credentials, and so on. Extracts reports.

</td><td>

-   sn\_rpa\_fdn.rpa\_user
-   cmdb\_read

</td></tr><tr><td>

RPA developer\[sn\_rpa\_fdn.rpa\_developer\]

</td><td>

Builds automation packages, tests the automation projects, and handles exceptions in the RPA Desktop Design Studio.Publishes packages to RPA Hub.

 Creates and deploys automations in a low-code environment.

</td><td>

-   fd\_read
-   sn\_rpa\_fdn.rpa\_user
-   cmdb\_read

</td></tr><tr><td>

RPA elevated privileges \[sn\_rpa\_fdn.rpa\_elevated\_privileges\]

</td><td>

Users with this role and along with other roles \(RPA developer, RPA support user, or RPA admin\) can access sensitive logs that are captured in Process Execution Log table.

</td><td>

None

</td></tr><tr><td>

RPA release manager\[sn\_rpa\_fdn.rpa\_release\_manager\]

</td><td>

Manages data, schedules, and other configuration parameters.

</td><td>

-   itil
-   sn\_rpa\_fdn.rpa\_user
-   cmdb\_read

</td></tr><tr><td>

RPA robot\[sn\_rpa\_fdn.rpa\_robot\]

</td><td>

Role that is assigned to a service account for the unattended robot to successfully execute automations.

</td><td>

cmdb\_read

</td></tr><tr><td>

RPA support user\[sn\_rpa\_fdn.rpa\_support\_user\]

</td><td>

Identifies, diagnoses, and resolves the issues that are related to bot processes.Performs first-level troubleshooting.

</td><td>

-   sn\_rpa\_fdn.rpa\_user
-   cmdb\_read

</td></tr><tr><td>

RPA user\[sn\_rpa\_fdn.rpa\_user\]

</td><td>

Qualifier role that is required for users to access to RPA Hub.

</td><td>

-   canvas\_user
-   sn\_change\_read
-   fd\_read
-   uxframework\_user

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Machine Lookup value change

</td><td>

Validates the values in the **Machine Name Lookup** field and **Machine Name** field. If the value is different, the schedule job updates the **Machine Name** \(String field\) with the value of the **Machine Name Lookup** field.

 Schedule runs every 3 hours and runs only when the **sn\_rpa\_fdn.enable\_unattended\_robot\_machine\_name\_lookup** system property is set to **Yes**.

 When the schedule job updates the **Machine Name** field, the life cycle stage status of the robot is moved to **In Maintenance**.

</td></tr><tr><td>

RPA: Purge Process Jobs

</td><td>

Schedule runs every day to purge process jobs and associated execution logs that are based on the information from a job's purging days and created date.

</td></tr><tr><td>

RPA: Purge Work Items

</td><td>

Schedule runs every day to purge queue items that are based on a queue's purge after days and the purge status.Purge after days is the number of days after which the work items get purged based on the created date.

</td></tr><tr><td>

RPA: Purge Alert Rule Triggers

</td><td>

Schedule runs every day to purge alert rule trigger records.

</td></tr><tr><td>

RPA: Purge Alerts

</td><td>

Schedule runs every day to purge alerts.

</td></tr><tr><td>

Re-evaluate License Distribution

</td><td>

Schedule runs on demand to validate the distribution of license records.For more information, see [Re-evaluate license distribution by executing RPA scripts](../task/execute-rpa-script.md).

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Extends

</th></tr></thead><tbody><tr><td>

Alerts\[sn\_rpa\_fdn\_alert\]

</td><td>

Contains the alerts that are generated from the alert rules and the information about the alert message, the associated alert rule name, and the trigger type.

</td><td>

 

</td></tr><tr><td>

Alert Rule\[sn\_rpa\_fdn\_alert\_rule\]

</td><td>

Contains the rules that are defined for the alerts to be generated and the information about the type and priority of the alert rule, the alert trigger, and the alert message.

</td><td>

Application file

</td></tr><tr><td>

Application Credentials\[sn\_rpa\_fdn\_application\_credentials\]

</td><td>

Contains the user name and password of business application used by the bot process at the time of execution on a robot.

</td><td>

Credentials

</td></tr><tr><td>

Attended Configuration\[sn\_rpa\_fdn\_attended\_configuration\]

</td><td>

Contains the details like the associated bot process name, table, action label, and conditions to trigger the attended bot process \(automation\) from the corresponding ServiceNow form.

</td><td>

Application file

</td></tr><tr><td>

Attended User Group\[sn\_rpa\_fdn\_rda\_user\_group\]

</td><td>

Contains the details like the associated bot process name, the assigned user for the attended bot process, and the assigned group for the selected assigned user.

</td><td>

 

</td></tr><tr><td>

Authorized User\[sn\_rpa\_fdn\_authorized\_user\]

</td><td>

Contains details of mapping between process credential mapping and an authorized user who can access the associated credential group.

</td><td>

 

</td></tr><tr><td>

Automation Logsn\_rpa\_fdn\_automation\_log

</td><td>

Contains the live log and give real-time visibility of the status of the running process jobs.

</td><td>

 

</td></tr><tr><td>

Assigned Studio Usersn\_rpa\_fdn\_assigned\_studio\_user

</td><td>

Defines if a robot is available for impersonation in RPA Desktop Design Studio for an assigned user.RPA release manager and RPA admin can create this record and add assigned user.

</td><td>

 

</td></tr><tr><td>

Bot Process Configuration\[sn\_rpa\_fdn\_bot\_process\_config\]

</td><td>

Contains the bot process settings.

</td><td>

Application file

</td></tr><tr><td>

Bot Process\[cmdb\_ci\_rpa\_process\]

</td><td>

Contains the configuration details of a process that runs on a robot. Details include the package, package version, assigned robots, process credential mappings, process robot credential sets, assigned business applications, process parameters, and attended users or groups.

</td><td>

Base Bot Process

</td></tr><tr><td>

Credential Group\[sn\_rpa\_fdn\_credential\_group\]

</td><td>

Contains details like the credential group name and the associated robot credentials.

</td><td>

 

</td></tr><tr><td>

Credential Group Application Credential\[sn\_rpa\_fdn\_m2m\_credential\_group\_application\]

</td><td>

Contains details like the credential group and the associated application credentials.

</td><td>

 

</td></tr><tr><td>

Code Quality Rule\[sn\_rpa\_fdn\_code\_quality\_rule\]

</td><td>

Contains the details of compliance rules for code quality check feature.

</td><td>

 

</td></tr><tr><td>

External Credential Vault\[sn\_rpa\_fdn\_external\_credential\_vault\]

</td><td>

Contains the details that enable you to register your external credential vault for further usage by the unattended robot.

</td><td>

 

</td></tr><tr><td>

Field Parameter Mapping\[sn\_rpa\_fdn\_field\_parameter\_mapping\]

</td><td>

Contains the details that enable you to map ServiceNow form fields of the associated attended configuration table to the process field parameters used in the attended automations.

</td><td>

Application file

</td></tr><tr><td>

Installed RPA Plugin\[sn\_rpa\_fdn\_rpa\_plugin\]

</td><td>

Contains the details of the plugins that are available on the instance which can be used with RPA Desktop Design Studio, Attended Robot, and Unattended Robot.

</td><td>

 

</td></tr><tr><td>

Installed RPA Plugin Version\[sn\_rpa\_fdn\_rpa\_plugin\_version\]

</td><td>

Contains the details of the different versions that are available for the installed RPA plugins.

</td><td>

 

</td></tr><tr><td>

Maintenance Request\[sn\_rpa\_fdn\_maintenance\_request\]

</td><td>

Contains the details that tracks the status of the scheduled maintenance days on the robot calendar.

</td><td>

 

</td></tr><tr><td>

MFA Authenticator\[sn\_rpa\_fdn\_mfa\_authenticator\]

</td><td>

Contains the details of the authenticator and token length that acts as an enabler for the Time-based One-time Password \(TOTP\) authentication.

</td><td>

 

</td></tr><tr><td>

Package\[sn\_rpa\_fdn\_package\]

</td><td>

Contains a set of resource files that include the robot files required for an automation execution.

</td><td>

Application file

</td></tr><tr><td>

Package Version\[sn\_rpa\_fdn\_package\_version\]

</td><td>

Contains the version details of a package.

</td><td>

Application file

</td></tr><tr><td>

Process Credential Mapping\[sn\_rpa\_fdn\_process\_credential\_mapping\]

</td><td>

Contains details of a credential group and associated bot process.

</td><td>

 

</td></tr><tr><td>

Process Execution Log\[sn\_rpa\_fdn\_execution\_log\]

</td><td>

Contains the execution type and associated process job details.

</td><td>

 

</td></tr><tr><td>

Process Job\[sn\_rpa\_fdn\_process\_job\]

</td><td>

Contains the details of the execution of a process on a robot. Details include the process job name, the state of the process job, the associated bot process name, the assigned robot of the bot process, the execution log status, the start and end time, and the date of the process job.

</td><td>

 

</td></tr><tr><td>

Process Field Parameter\[sn\_rpa\_fdn\_process\_field\_parameter\]

</td><td>

Contains the details that enable you to create dynamic parameters that are required in the attended automations.

</td><td>

Application file

</td></tr><tr><td>

Process Parameter\[sn\_rpa\_fdn\_process\_parameter\]

</td><td>

Contains the details of the variables that are used within a bot process and across bot processes.

</td><td>

Application file

</td></tr><tr><td>

Process Robot Credential\[sn\_rpa\_fdn\_process\_robot\_cred\]

</td><td>

Contains the details of a credential group that a robot uses to perform the automation for the given bot process.

</td><td>

 

</td></tr><tr><td>

Process Schedule\[sn\_rpa\_fdn\_schedule\]

</td><td>

Contains the details that enable users to execute jobs in a planned manner at regular intervals. Details include the name and interval type of the schedule and the start and end date of the schedule.

</td><td>

Application file

</td></tr><tr><td>

Process Skill Mapping\[sn\_rpa\_fdn\_m2m\_process\_skill\_mapping\]

</td><td>

Contains details about mapped package version and overridden version of the skill package for a bot process configuration.

</td><td>

 

</td></tr><tr><td>

Robot\[cmdb\_ci\_rpa\_robot\]

</td><td>

Contains the details of a software agent that runs a bot process that is built in the RPA Desktop Design Studio. Details include the name, type, and department of the robot, the machine name that is used to install the Unattended Robot, and the attended user.

</td><td>

Base Robot

</td></tr><tr><td>

Robot Credentials\[sn\_rpa\_fdn\_credentials\_set\]

</td><td>

Contains the login credentials that the robot uses to log in to a Windows machine and perform the automation.

</td><td>

Credentials

</td></tr><tr><td>

Robots License Distribution\[sn\_rpa\_fdn\_license\_distribution\]

</td><td>

Contains the details of consumption and distribution of licenses in your organization.

</td><td>

 

</td></tr><tr><td>

Robots Pool\[sn\_rpa\_fdn\_robot\_pool\]

</td><td>

Contains the details of the number of robots selected for robot pool option.

</td><td>

 

</td></tr><tr><td>

Skill Mapping\[sn\_rpa\_fdn\_m2m\_package\_version\_skill\_mapping\]

</td><td>

Contains attended and unattended package version and associated skill package version details.

</td><td>

 

</td></tr><tr><td>

TOTP Authenticator\[sn\_rpa\_fdn\_totp\_authenticator\]

</td><td>

Contains the details of MFA authenticator and seed which is the secret key of the authenticator that is used to generate the TOTP.

</td><td>

 

</td></tr><tr><td>

Work Queue\[sn\_rpa\_fdn\_work\_queue\]

</td><td>

Contains the details of a repository that can hold a number of work items. Details include the name, department, and description of the work queue, and purge-work item details.

</td><td>

Application file

</td></tr><tr><td>

Work Item\[sn\_rpa\_fdn\_work\_queue\_item\]

</td><td>

Contains the details about the multiple types of data that are stored, such as the transaction information, the customer details, or the information from a document. Details include the name, status, and priority of the work item, and associated work queue name.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

