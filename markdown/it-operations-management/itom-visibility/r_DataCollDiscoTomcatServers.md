---
title: Tomcat server discovery
description: Discovery identifies and classifies information about Tomcat server Web applications running on UNIX machines.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Tomcat server discovery

Discovery identifies and classifies information about Tomcat server Web applications running on UNIX machines.

Discovery can identify and classify Web applications present in either the `CATALINA_BASE` directory or the `CATALINA_HOME` directory.

The classifier that finds Tomcat server processes uses the condition: \[Parameters\] \[contains\] \[org.apache.catalina.startup.Bootstrap\].

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Credentials

Configure these credentials:

-   [Applicative credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/applicative-creds.md)
-   [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md)

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Classifier, pattern, and probes

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Tomcat

</td><td>

-   Horizontal pattern: launches patterns
-   SSHCommand-Tomcat - Find web.xml List\*
-   SSHCommand-Tomcat - Get server.xml\*
-   SSHCommand-Tomcat - Get Version\*

</td><td>

Tomcat

</td></tr></tbody>
</table>\*Probes inactive on new instances.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

Discovery collects the following data on the Tomcat \[cmdb\_ci\_app\_server\_tomcat\] table for both Unix and Windows:

|Label|Field name|Source|
|-----|----------|------|
|Name|name|server.info|
|Install Directory|install\_directory|server.xml|
|Version|version|server.info|
|Server Port|server\_port|server.xml|
|Attributes|attributes|server.xml|

The following data is collected on the Tomcat Connector \[cmdb\_ci\_tomcat\_connector\] table for both Unix and Windows:

|Label|Field name|Source|
|-----|----------|------|
|Tomcat|tomcat|server.xml|
|Port|port|server.xml|

The following data is collected on the Web Application \[cmdb\_ci\_web\_application\] table for both Unix and Windows:

|Label|Field name|Source|
|-----|----------|------|
|Description|description|web.xml|
|Document base|document\_base|web.xml|
|App server|app\_server|web.xml|

## Relationships

|Parent class|Relationship|Child class|
|------------|------------|-----------|
|cmdb\_ci\_app\_server\_tomcat|Contains::Contained by|cmdb\_ci\_web\_application|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

