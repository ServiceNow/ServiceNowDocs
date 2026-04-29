---
title: Target tables for the n8n
description: When you complete setting up the connection, you can configure the integration to periodically pull data from a n8n project. The data is saved in tables that extend from the CMDB CI classes and other non-CMDB classes.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [n8n, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Target tables for the n8n

When you complete setting up the connection, you can configure the integration to periodically pull data from a n8n project. The data is saved in tables that extend from the CMDB CI classes and other non-CMDB classes.

## Target tables for AI systems

cmdb\_ai\_system\_component\_product\_model

The following attributes in the n8n Datacenter \[cmdb\_ai\_system\_component\_product\_model\] table are populated by collected data.

<table id="table_im4_jvm_m3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

name \(workflow\) or name \(agent\)

</td></tr><tr><td>

Version

</td><td>

version

</td><td>

Type version

</td></tr></tbody>
</table>alm\_ai\_system\_digital\_asset

The following attributes in the n8n Datacenter \[alm\_ai\_system\_digital\_asset\] table are populated by collected data.

<table id="table_ibz_lvm_m3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

External Ref id

</td><td>

external\_ref\_id

</td><td>

Connection Url + data or connection Url + data+ nodes

</td></tr><tr><td>

Display Name

</td><td>

display\_name

</td><td>

Name

</td></tr><tr><td>

Install Status

</td><td>

Install\_status

</td><td>

Data is Archived

</td></tr><tr><td>

AI Models

</td><td>

ai\_models

</td><td>

AI Language model

</td></tr></tbody>
</table>cmdb\_ci\_function\_ai

The following attributes in the n8n Datacenter \[cmdb\_ci\_function\_ai\] table are populated by collected data.

<table id="table_adv_xqr_v3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

display name

</td></tr><tr><td>

Object ID

</td><td>

object\_id

</td><td>

external reference id

</td></tr><tr><td>

Install status

</td><td>

install\_status

</td><td>

Install status

</td></tr><tr><td>

Model ID

</td><td>

model\_id

</td><td>

model

</td></tr><tr><td>

Vendor

</td><td>

vendor

</td><td>

vendor

</td></tr><tr><td>

Sys id

</td><td>

asset

</td><td>

asset

</td></tr></tbody>
</table>## Target tables for AI model

cmdb\_ai\_model\_product\_model

The following attributes in the n8n Datacenter \[cmdb\_ai\_model\_product\_model\] table are populated by collected data.

<table id="table_m4f_xvm_m3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

Model name

</td></tr><tr><td>

Version

</td><td>

version

</td><td>

Type version

</td></tr></tbody>
</table>alm\_ai\_model\_digital\_asset

The following attributes in the n8n Datacenter \[alm\_ai\_model\_digital\_asset\] table are populated by collected data.

<table id="table_vyk_zvm_m3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

External Ref ID

</td><td>

external\_ref\_id

</td><td>

Connection URL, model name, type version

</td></tr></tbody>
</table>## Target tables for AI prompts

cdmb\_ai\_prompt\_product\_model

The following attributes in the n8n Datacenter \[cdmb\_ai\_prompt\_product\_model\] table are populated by collected data.

<table id="table_wkz_dwm_m3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

Name

</td></tr><tr><td>

Prompt Info

</td><td>

prompt\_info

</td><td>

Parameters system message

</td></tr></tbody>
</table>alm\_ai\_prompt\_digital\_asset

The following attributes in the n8n Datacenter \[alm\_ai\_prompt\_digital\_asset\] table are populated by collected data.

<table id="table_rkp_fwm_m3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

External Ref ID

</td><td>

external\_ref\_id

</td><td>

Asset type, asset id

</td></tr></tbody>
</table>## Target tables for AI tools

sn\_ent\_ai\_tool

The following attributes in the n8n Datacenter \[sn\_ent\_ai\_tool\] table are populated by collected data.

|Attribute label|Attribute name|n8n attribute|
|---------------|--------------|-------------|
|External ref id|external\_ref\_id|workflow +node|
|Name|name|Nodes +toolType|
|Description|description|nodes|
|Active|active|nodes|

## Target tables for AI Subcomponents

sn\_ent\_ai\_system\_subcomponent\_m2m

The following attributes in the n8n Datacenter \[sn\_ent\_ai\_system\_subcomponent\_m2m\] table are populated by collected data.

<table id="table_egl_4wm_m3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

AI System

</td><td>

ai\_system

</td><td>

connectionUrl + workflowld + +nodeld or n8n

</td></tr><tr><td>

AI Subcomponent

</td><td>

ai\_subcomponent

</td><td>

connectionUrl + workflowld + nodeld \(for sub sysems\) or workflowld+ nodeld \(for tools\)

</td></tr><tr><td>

AI subcomponent reference table

</td><td>

ai\_subcomponent\_reference\_table

</td><td>

agents or tools

</td></tr></tbody>
</table>## Target tables for AI Usage

sn\_ai\_disc\_ai\_usage

The following attributes in the n8n Datacenter \[sn\_ai\_disc\_ai\_usage\] table are populated by collected data.

<table id="table_sf4_zwm_m3c"><tbody><tr><td>

Attribute label

</td><td>

Attribute name

</td><td>

n8n attribute

</td></tr><tr><td>

AI System

</td><td>

ai\_system

</td><td>

connectionUrl+ workflowld + nodeld

</td></tr><tr><td>

Session ID

</td><td>

session\_id

</td><td>

data.id

</td></tr><tr><td>

Time

</td><td>

time

</td><td>

runData.executions

</td></tr><tr><td>

Count

</td><td>

count

</td><td>

runData.executions.length

</td></tr></tbody>
</table>