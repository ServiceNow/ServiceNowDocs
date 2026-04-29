---
title: Modules in the GRC integration with Thomson Reuters Regulatory Intelligence application
description: The GRC integration with Thomson Reuters Regulatory Intelligence application includes various modules.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration with Thomson Reuters Regulatory Intelligence \(TRRI\), GRC integrations, Common GRC features, Governance, Risk, and Compliance]
---

# Modules in the GRC integration with Thomson Reuters Regulatory Intelligence application

The GRC integration with Thomson Reuters Regulatory Intelligence application includes various modules.

The following modules are displayed under the GRC integration with Thomson Reuters Regulatory Intelligence application:

<table id="table_q1f_zgp_jnb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Thomson Reuters Guided Setup

</td><td>

Instructions to configure and set up the application.

</td></tr><tr><td>

Connection &amp; Credential Aliases

</td><td>

Connection and credential aliases for SFTP and for OAuth.

</td></tr><tr><td>

Connections

</td><td>

File connection information record from the Thomson Reuters platform. Click Validate to validate the connection. In case you encounter any issues in validating the connection, triage it using an integration log. If you do not want to use a connection, you can move it to the Draft state by clicking **Move to draft**. In the integration, the system uses only the file connection information record that has the Validated state.

</td></tr><tr><td>

OAuth Registry Entry

</td><td>

Record of when the OAuth connection and credential are created via the shipped connection and credential alias.

</td></tr><tr><td>

OAuth Credentials

</td><td>

Record of when the OAuth credentials are created.

</td></tr><tr><td>

Feed Registry

</td><td>

Record for each of the feed files that are located in the source directory of the SFTP location.

</td></tr><tr><td>

Integration Logs

</td><td>

Integration logs with integration details. The log contains errors that occurred in the integration flows, such as, errors that were observed while validating a connection.

</td></tr><tr><td>

Data source

</td><td>

Data source that ingests the feed files from the SFTP location and creates a record automatically in the regulatory feed table.

</td></tr><tr><td>

Scheduled Import

</td><td>

Scheduled import job that scans and searches for the oldest entry in the feed registry.

</td></tr><tr><td>

Taxonomy XML Configuration

</td><td>

Record that is shipped as part of the Thomson Reuters platform. Contains the XPaths and attributes that are required to parse the uploaded Thomson Reuters platform taxonomy file in XML format.

</td></tr><tr><td>

TR \| Regulatory Bodies

</td><td>

External Regulatory Bodies taxonomy records for the Thomson Reuters platform.

</td></tr><tr><td>

TR \| Content Types

</td><td>

External Content Types taxonomy records for the Thomson Reuters platform.

</td></tr><tr><td>

TR \| Jurisdictions

</td><td>

External Jurisdictions taxonomy records for the Thomson Reuters platform.

</td></tr><tr><td>

TR \| Themes

</td><td>

External Themes taxonomy records for the Thomson Reuters platform.

</td></tr><tr><td>

TR \| Sectors

</td><td>

View the external Sectors taxonomy records for the Thomson Reuters platform.

</td></tr><tr><td>

Taxonomy Mapper

</td><td>

Mapping of the Thomson Reuters platform taxonomy to internal taxonomy.

</td></tr></tbody>
</table>The data that is accessed through the application modules is stored in the following tables:

|Table|Field|
|-----|-----|
|sn\_grc\_reg\_change\_external\_theme|External Regulatory Theme|
|sn\_grc\_reg\_change\_external\_regulatory\_body|External Regulatory Body|
|sn\_grc\_reg\_change\_external\_sector|External Regulatory Sector|
|sn\_grc\_reg\_change\_external\_content\_type|External Regulatory Content Type|
|sn\_grc\_reg\_change\_external\_jurisdiction|External Regulatory Jurisdiction|
|sn\_grc\_reg\_change\_ theme|Regulatory Theme|
|sn\_grc\_reg\_change\_ regulatory\_body|Regulatory Body|
|sn\_grc\_reg\_change\_sector|Regulatory Sector|
|sn\_grc\_reg\_change\_ content\_type|Regulatory Content Type|
|sn\_grc\_reg\_change\_ jurisdiction|Regulatory Jurisdiction|

**Parent Topic:**[GRC integration with Thomson Reuters Regulatory Intelligence](../concept/grc-trri-integration.md)

