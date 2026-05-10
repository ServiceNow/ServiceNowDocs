---
title: Components installed with Security Incident Response
description: Several types of components are installed when you download and activate the Security Incident Response application, including user roles, tables, properties, and scheduled jobs.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Components installed with Security Incident Response

Several types of components are installed when you download and activate the Security Incident Response application, including user roles, tables, properties, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Properties installed

Users with the System Administrator \[admin\] role can view the properties. Users with the Security Administrator \[sn\_si.admin\] role can modify them.

<table id="table_q4b_y2c_ks"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

The default category nodes that are displayed in the Relationship Graph tab within the Workspace. The default values represent the table names corresponding to the related records.sn\_si\_aw.defaultCategories

</td><td>

-   **Type**: string
-   **Default value**: sn\_ti\_m2m\_task\_observables,sn\_si\_m2m\_task\_affected\_user,sn\_si\_incident

</td></tr><tr><td>

Default start time for all agents when no schedule is set, formatted as 08:00sn\_si.default.start.time

</td><td>

-   **Type**: string
-   **Default value**: 08:00
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Default end time for all agents when no schedule is set, formatted as 17:00sn\_si.default.end.time

</td><td>

-   **Type**: string
-   **Default value**: 17:00
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Include Destination type observables along with other context type observables in the security incident user and CI relationshipssn\_si.link\_dest\_ip

</td><td>

Determines whether a security incident observable with a context type of Destination is displayed under the **Configuration Items** or **Affected Users** tabs. By default, observables with a Destination context type are excluded. To include the observables, choose Yes.

</td></tr><tr><td>

Allow customization when creating a Problem or Change Request from a Security Incidentsn\_si.popup

</td><td>

When a problem or change is created, this property opens a pop-up window to modify the request.

 If this properties are set to **false**, the problem or change request has the same priority, short description, and description as the security incident without the option to add or edit those fields.

 -   **Type**: true \| false
-   **Default value**: true
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Associate Sightings Search results with CIs in the CMDB.sn\_si.associate\_ci\_with\_sighting\_search

</td><td>

When set to true, sightings search results include associated configuration items that are in your CMDB. -   **Type**: true \| false
-   **Default value**: true
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Risk score in the range is highlighted green, formatted as 0-49sn\_si.risk.score.green

</td><td>

In the Security Incidents list, security incidents with a risk score between 0 and 49 are marked with a green dot.

</td></tr><tr><td>

Risk score in the range is highlighted orange, formatted as 50-79sn\_si.risk.score.orange

</td><td>

In the Security Incidents list, security incidents with a risk score between 50 and 79 are marked with an orange dot.

</td></tr><tr><td>

Risk score in the range is highlighted red, formatted as 80-100sn\_si.risk.score.red

</td><td>

In the Security Incidents list, security incidents with a risk score between 80 and 100 are marked with a red dot.

</td></tr><tr><td>

This parameter enables or disables Sightings Search Configurations that have implemented this feature.sn\_si.enable\_sighting\_search

</td><td>

When set to true, sightings searches can be performed on activated integrations. -   **Type**: true \| false
-   **Default value**: true
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

The number of rows of raw data that are saved when a Sighting Search is performed. Range 0-100sn\_si.sighting\_search\_raw\_data\_rows

</td><td>

This property defaults to 50 rows of raw data. Half of the result rows are reported from the beginning of the search time frame and half from the end of the search time frame. So, if you select 50 rows, 25 come from the start of the search time frame and 25 from the end of the search time frame.

</td></tr><tr><td>

Automatically advance the Incident State to Contain when a Response Task advances to Work In Progresssn\_si.rollup\_task\_state

</td><td>

While using flows or workflows, consider setting this property to **false**. This enables you to control the Incident State from within flows or workflows. It also helps avoid any potential conflicts while transitioning from one incident state to another.-   **Type**: true \| false
-   **Default value**: true
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td colspan="2">

**Assignment properties for Security Incident Response**

</td></tr><tr><td>

Location Weightsn\_si.location.weight

</td><td>

A rating used when calculating the criteria to use for auto-assigning a security analyst. If, for example, location is considered for a task, the location weight value is added to the security analyst rating.-   **Type**: integer
-   **Default value**: 10
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Skills Weightsn\_si.skills.weight

</td><td>

A rating used when calculating the criteria to use for auto-assigning a security analyst. If, for example, skills are considered for a task, the skills weight value is added to the security analyst rating.-   **Type**: integer
-   **Default value**: 10
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Set the maximum number of security analysts to be processed by auto-assignment at a time sn\_si.max.agents.processed

</td><td>

The system has an absolute limit of 300 security analysts. If you specify more than 300, it sets the value to that level. The system cannot auto-dispatch a task for a dispatch group that contains more security analysts than the value configured.-   **Type**: integer
-   **Default value**: 100
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Time Zone Weightsn\_si.timezone.weight

</td><td>

A rating used when calculating the criteria to use for auto-assigning a security analyst. If, for example, the security analyst time zone is considered for a task, the time zone weight value is added to the security analyst rating.-   **Type**: integer
-   **Default value**: 10
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Amount of time \(in minutes\) to add between the end of a task and the travel start of the next.sn\_si.work.spacing

</td><td>

An example of a valid time value is 10.-   **Type**: integer
-   **Default value**: 0
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Specified journal fields containing `code` tags that render content as HTML.sn\_si.journal\_field.html\_enabled

</td><td>

-   **Type**: string
-   **Default value**: work\_notes, comments
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Calculate the Impacted services in background.sn\_si.refresh\_impacted.event

</td><td>

Affected Services/Impacted CIs related list is generated through events. When enabled the refresh gets executed in the background and security tags are added to the incident.Set the value to **true** to perform the operation in background.

-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Retrieve the critical service from a pre-calculated data.sn\_si.critical\_service.calculator.use\_cache

</td><td>

Enables the critical service calculator to use a pre-calculated data of configuration items.

 Set the value to **true** to lookup from a pre calculated data

 -   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Security Incident** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Security Incident Administrator\[sn\_si.admin\]

</td><td>

Full control over all Security Incident Response data. Also administers territories and skills, as needed.**Note:** In the base system, the administrator also has access to sn\_si.admin. Security Incident Response can be restricted from the administrator as long as at least one other user is assigned the security administrator role.

</td><td>

-   assessment\_admin
-   catalog\_admin
-   decision\_table\_admin
-   decision\_table\_reader
-   filter\_admin
-   flow\_designer
-   pd\_author
-   pd\_content\_author
-   pd\_operator
-   skill\_admin
-   skill\_model\_admin
-   sn\_si.analyst
-   sn\_si.ingestion\_profile\_admin
-   sn\_si.knowledge\_admin
-   sn\_si.manager
-   sn\_sec\_cmn.admin
-   sn\_si.restriction\_access\_manager
-   sn\_si.special\_access\_read\_manager
-   sn\_si.special\_access\_write\_manager
-   sn\_ti.malicious\_attachment\_access
-   sn\_ti.observable.admin
-   tags\_admin
-   template\_admin
-   territory\_admin
-   treemap\_admin
-   user\_admin

</td></tr><tr><td>

Profile Admin\[sn\_si.ingestion\_profile\_admin\]

</td><td>

Configure the plugins, create, edit, delete, and manage profiles for Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.**Note:** Users with the sn\_si.admin role can perform all operations available to a Profile Admin, as the sn\_si.admin role inherits the required permissions by default.

The sn\_si.ingestion\_profile\_admin role is assignable to users by the sn\_si.admin.

</td><td>

N/A

</td></tr><tr><td>

Security Incident Analyst\[sn\_si.analyst\]

</td><td>

Manage security incidents. Underlying role for basic Security access. Users with this role can create and update security incidents, requests, and tasks, as well as problems, changes, and outages related to their incidents.

</td><td>

-   pd\_operator
-   snc\_platform\_rest\_api\_access
-   sn\_msi.promoter
-   sn\_msi.proposer
-   sn\_si.basic
-   sn\_ti.malicious\_attachment\_access
-   awa\_agent

</td></tr><tr><td>

Security Incident Basic\[sn\_si.basic\]

</td><td>

Underlying role for basic Security access. Users with this role can create and update security incidents, requests, and tasks, as well as problems, changes, and outages related to their incidents.

</td><td>

-   canvas\_user
-   document\_management\_user
-   email\_composer
-   flow\_operator
-   inventory\_user
-   pa\_viewer
-   service\_fullfiller
-   skill\_user
-   sn\_sec\_cmn.write
-   sn\_si.read
-   sn\_ti.observable.read
-   sn\_ti.observable.write
-   sn\_ti.read
-   task\_activity\_writer
-   task\_editor
-   treemap\_user

</td></tr><tr><td>

Chief Information Security Officer \(CISO\)\[sn\_si.ciso\]

</td><td>

View and manipulate the CISO dashboard. Also, if the Vulnerability Response plugin is activated, users with this role can add vulnerability significance definition treemaps to the dashboard. You can also do the same with Security Incident Response plugin.

</td><td>

-   pa\_viewer
-   sn\_si.basic
-   sn\_si.read

</td></tr><tr><td>

Security Incident External\[sn\_si.external\]

</td><td>

View any security incidents that belong to their particular group.**Note:** The following two rules are applicable throughout ServiceNow irrespective of scoped admin or scope app.

-   When you add any user to a group, you are also assigning roles to that group. Similarly, when you remove a user from a group, the inherited roles will also get removed.
-   Every role is assignable by some higher precedence role.

</td><td>

service\_fulfiller

</td></tr><tr><td>

Security Incident Integration User\[sn\_si.integration\_user\]

</td><td>

External tools can provide new security incident records and update security incident records.

</td><td>

import\_transformer

</td></tr><tr><td>

Security Incident Knowledge Administrator\[sn\_si.knowledge\_admin\]

</td><td>

Manage, update, and delete the information in the Security Incident knowledge base.

</td><td>

-   knowledge\_admin
-   sn\_si.read

</td></tr><tr><td>

Security Incident Manager\[sn\_si.manager\]

</td><td>

Same access as security analysts.

</td><td>

-   pd\_author
-   pd\_operator
-   sn\_si.basic

</td></tr><tr><td>

Security Incident Read\[sn\_si.read\]

</td><td>

Read security incidents.

</td><td>

-   canvas\_user
-   sn\_sec\_cmn.read
-   sn\_templated\_snip.template\_snippet\_reader
-   sn\_ti.observable.read
-   workspace\_user

</td></tr><tr><td>

Security Restriction Access Manager \[sn\_si.restriction\_access\_manager\]

</td><td>

Allows users or groups to 'enforce restriction' on security incidents. This is applicable only for field change.

</td><td>

N/A

</td></tr><tr><td>

Security Incident Special Accesssn\_si.special\_access

</td><td>

Provides access to specific security incidents to users outside of the Security Operations organization.

</td><td>

N/A

</td></tr><tr><td>

Security Special Access Enabler \[sn\_si.special\_access\_enabler\]

</td><td>

Provides special access role to a user outside of the Security Operations organization to specific security incidents.

</td><td>

N/A

</td></tr><tr><td>

Security Incident Special Access Read Manager \[sn\_si.special\_access\_read\_manager\]

</td><td>

Manage the Security Incident Special Access \[sn\_si.special\_access\] role. Use this role to modify the **Read access** field in the security incident form. This role is assignable by sn\_si.admin.

</td><td>

sn\_si.special\_access\_enabler

</td></tr><tr><td>

Security Incident Special Access Writer Manager \[sn\_si.special\_access\_write\_manager\]

</td><td>

Manage the Security Incident Special Access \[sn\_si.special\_access\] role. Use this role to modify the **Privileged access** field in the security incident form. This role is assignable by sn\_si.admin.

</td><td>

sn\_si.special\_access\_enabler

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Lookup Security Incident Observables|Performs a lookup for observables on a user-defined schedule.|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

News Feed Configuration\[sn\_si\_feed\_configuration\]

</td><td>

Configuration records used to define the content displayed in the security incident news feed.

</td></tr><tr><td>

Post Incident Review Assignment Rule\[sn\_si\_pir\_condition\]

</td><td>

Automates selection of participants of a post incident review survey when a security incident is closed.

</td></tr><tr><td>

Security Incident\[sn\_si\_incident\]

</td><td>

Stores a security incident, the responses to the incident, all linked tasks, changes, problems, and incidents related to this security incident.

</td></tr><tr><td>

Security Incident Attack Vectors\[sn\_si\_attack\_vector\]

</td><td>

Attack vector options.

</td></tr><tr><td>

Security Incident Audit Log\[sn\_si\_audit\_log\]

</td><td>

Stores security incident enrichment audit logs.

</td></tr><tr><td>

Security Incident Calculator\[sn\_si\_calculator\]

</td><td>

A calculator to set certain security incident fields when certain conditions are met.

</td></tr><tr><td>

Security Incident Calculator Group\[sn\_si\_calculator\_group\]

</td><td>

A grouping of security incident calculators. The order of the calculator group determines which group is evaluated first, and in each group, one calculator at most is used.

</td></tr><tr><td>

Security Incident Enrichment Firewall\[sn\_si\_enrichment\_firewall\]

</td><td>

Extends from the base table \(sn\_sec\_cmn\_enrichment\_data\_base\) and includes all enrichment records specific to Palo Alto Networks Firewall.

</td></tr><tr><td>

Security Incident Enrichment Malware Results\[sn\_si\_enrichment\_malware\]

</td><td>

Extends from the base table \(sn\_sec\_cmn\_enrichment\_data\_base\) and includes all enrichment records specific to malware.

</td></tr><tr><td>

Security Incident Enrichment Network Statistics\[sn\_si\_enrichment\_network\_statistics\]

</td><td>

Extends from the base table \(sn\_sec\_cmn\_enrichment\_data\_base\) and includes all enrichment records specific to network statistics.

</td></tr><tr><td>

Security Incident Enrichment Running Processes\[sn\_si\_enrichment\_running \_processes\]

</td><td>

Extends from the base table \(sn\_sec\_cmn\_enrichment\_data\_base\) and includes all enrichment records specific to running processes.

</td></tr><tr><td>

Security Incident Enrichment Running Services\[sn\_si\_enrichment\_running\_service\]

</td><td>

Extends from the base table \(sn\_sec\_cmn\_enrichment\_data\_base\) and includes all enrichment records specific to running services.

</td></tr><tr><td>

Security Incident Email Search\[sn\_si\_m2m\_incident\_email\_search\]

</td><td>

Maps email search records to security incidents.

</td></tr><tr><td>

Security Incident Import\[sn\_si\_incident\_import\]

</td><td>

Import table for security incidents. Used to create security incidents from external systems.

</td></tr><tr><td>

Security Incident Process Definition\[sn\_si\_process\_definition\]

</td><td>

Stores configuration for Security Incident process flows.

</td></tr><tr><td>

Security Incident Process Definition Selector\[sn\_si\_process\_definition\_selector\]

</td><td>

Stores the Security Incident Process Definition to use for security incidents.

</td></tr><tr><td>

Security Incident Related Customer Service Case\[sn\_si\_m2m\_incident\_customerservice\_case\]

</td><td>

Maps customer service cases and security incidents

</td></tr><tr><td>

Security Incident Related Enrichment Data\[sn\_si\_m2m\_incident\_enrichment\]

</td><td>

Maps security incidents and related enrichment data records.

</td></tr><tr><td>

Security Incident Response Task\[sn\_si\_task\]

</td><td>

Manages subtasks related to handling a security incident. These tasks can be assigned to security personnel, or to people in other departments, to manage interdepartmental communication and task tracking.

</td></tr><tr><td>

Security Incident Response Task Template\[sn\_si\_task\_template\]

</td><td>

Used to create a Security Incident Response task. These templates are often used in catalog entries, to automatically create a set of appropriate subtasks for a particular type of security incident.

</td></tr><tr><td>

Security Incident Runbook Document\[sn\_si\_runbook\_document\]

</td><td>

Associates security incident conditions or filters with a knowledge article. Used to specify runbook procedures for security incident remediation.

</td></tr><tr><td>

Security Incident Template\[sn\_si\_incident\_template\]

</td><td>

Used to create a security incident. These templates are often used in catalog entries to create a prebuilt security incident.

</td></tr><tr><td>

Security Request\[sn\_si\_request\]

</td><td>

A security-related request to the security team.

</td></tr><tr><td>

Security Scan Request\[sn\_si\_scan\_request\]

</td><td>

A request for a threat lookup.

</td></tr><tr><td>

Severity Calculatorsn\_si\_severity\_calculator

</td><td>

Defines the severity, impact, risk, and criticality values for a security incident.

</td></tr><tr><td>

Task Affected User\[sn\_si\_m2m\_task\_affected\_user\]

</td><td>

A many-to-many table associating security incidents with affected users.

</td></tr><tr><td>

Template Workflow Activity Outcome Evaluator \[sn\_si\_wf\_activity\_outcome\_evaluator\]

</td><td>

Maps a capability with an evaluation script. A new subflow can be added to a template workflow to set a response task outcome rather than having an analyst manually set it.

</td></tr></tbody>
</table>