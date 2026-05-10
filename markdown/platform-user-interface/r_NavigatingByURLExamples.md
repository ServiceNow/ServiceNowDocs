---
title: Examples of navigating by URL
description: A list of example URLs that demonstrate ways to open pages in the ServiceNow application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Navigate to a record or module using a URL, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Examples of navigating by URL

A list of example URLs that demonstrate ways to open pages in the ServiceNow application.

## Open a form with preset values

Schema: `https://<baseURL>/nav_to.do?uri=<table name>.do?sys_id=-1&sysparm_query=<field=value>`

|Description|Example|
|-----------|-------|
|Opens a new Incident form in the standard interface with a priority of **1** and an incident state of **Awaiting Problem**.|`https://<instance name>.service-now.com/nav_to.do?uri=incident.do?sys_id=-1&sysparm_query=priority=1^incident_state=3`|
|You can also use JavaScript to access [GlideSystem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/p_GlideServerAPIs.md) methods. The following example creates the same type of incident as above, and also populates the caller ID with the current user ID.|`https://<instance name>.service-now.com/nav_to.do?uri=incident.do?sys_id=-1&sysparm_query=priority=1^incident_state=3^caller_id=javascript:gs.getUserID()`|

## Open an existing record with preset values

Schema: `https://<baseURL>/nav_to.do?uri=<table name>.do?sys_id=<sys_id>`

|Description|Example|
|-----------|-------|
|Opens the incident record with the sys\_id `966c9a414f5593001f6eac118110c75c`|`https://<instance name>.service-now.com/incident.do?sys_id=966c9a414f5593001f6eac118110c75c`|
|Opens the incident record with the number `INC0010001`|`https://<instance name>.service-now.com/incident.do?sysparm_query=number=INC0010001`|

## View a list of incidents

Schemas for the following examples:

-   `https://<baseURL>/nav_to.do?uri=<table name>_list.do`
-   `https://<baseURL>/<table name>_list.do`

|Description|Example|
|-----------|-------|
|Opens a list of all incidents with \(example 1\) the navigation frame.|`https://<instance name>.service-now.com/nav_to.do?uri=incident_list.do`|
|Opens a list of all incidents without the navigation frame.|`https://<instance name>.service-now.com/incident_list.do`|

## View a list of attachments

Schema: `https://<baseURL>/nav_to.do?uri=<table name>_list.do`

|Description|Example|
|-----------|-------|
|Opens the Attachments table in list view.|`https://<instance name>.service-now.com/sys_attachment_list.do`|

## View a filtered list

Schema: `https://<baseURL>/nav_to.do?uri=<table name>_list.do?sysparm_query=<field=value>`

|Description|Example|
|-----------|-------|
|Returns a list of active incidents with high escalation in the standard interface.|`https://<instance name>.service-now.com/nav_to.do?uri=incident_list.do?sysparm_query=active=true^escalation=2`|

## Return a file

Schema: `https://<baseURL>/nav_to.do?uri=<table name>_list.do?sysparm_<sysparmTypeOrField=value>&CSV`

|Description|Example|
|-----------|-------|
|Returns a comma-separated value file of records in the Incident table that meet the query conditions.|`https://<instance name>.service-now.com/nav_to.do?uri=incident_list.do?sysparm_query=active=false&CSV`|

**Parent Topic:**[Navigate to a record or module using a URL](../task/navigate-using-url.md)

