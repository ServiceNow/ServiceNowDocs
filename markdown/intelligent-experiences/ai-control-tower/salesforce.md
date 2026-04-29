---
title: AI Service Graph connector for Salesforce
description: Use the  AI Service Graph Connector for Salesforce to discover AI assets such as AI systems, agents, models, tools, and prompts and well as usage data for these AI agents. This usage information is consumed by the AI Control Tower value dashboard.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph connector for Salesforce

Use the  AI Service Graph Connector for Salesforce to discover AI assets such as AI systems, agents, models, tools, and prompts and well as usage data for these AI agents. This usage information is consumed by the AI Control Tower value dashboard.

## Download apps from the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to download the AI Service Graph Connector for Salesforce app.

## Supported ServiceNow versions

-   Australia
-   Zurich patch 7
-   Yokohama patch 11

## User role

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## Salesforce AI Metadata mapping in ServiceNow tables

**AI Agents**

alm\_ai\_system\_digital\_asset -&gt; Model table \(cmdb\_ai\_system\_component\_product\_model\)

<table id="table_xn2_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

Model ID

</td><td>

Model

</td><td>

model\_id

</td></tr><tr><td>

Agent ID

</td><td>

Product instance identifier

</td><td>

agent\_id

</td></tr><tr><td>

Version

</td><td>

External record reference

</td><td>

version\_id

</td></tr><tr><td>

Status

</td><td>

State \(install\_status\)

</td><td>

u\_status

</td></tr><tr><td>

Quantity

</td><td>

Quantity

</td><td>

quantity

</td></tr><tr><td>

Vendor

</td><td>

Vendor

</td><td>

u\_vendor

</td></tr><tr><td>

Company

</td><td>

Company

</td><td>

cleansed\_manufacturer\_ref

</td></tr><tr><td>

Source System

</td><td>

Source System

</td><td>

vendor

</td></tr><tr><td>

Asset Type

</td><td>

Model Category

</td><td>

asset\_type

</td></tr></tbody>
</table>**AI Models**

alm\_ai\_model\_digital\_asset -&gt; Model table \(cmdb\_ai\_model\_product\_model\)

<table id="table_yn2_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

Asset Type

</td><td>

Model category

</td><td>

asset\_type

</td></tr><tr><td>

Foundation Model ID

</td><td>

Base model

</td><td>

foundation\_model\_identifier

</td></tr><tr><td>

Model

</td><td>

Model

</td><td>

base\_model

</td></tr><tr><td>

Status

</td><td>

State \(install\_status\)

</td><td>

u\_status

</td></tr><tr><td>

External Reference ID

</td><td>

External record reference

</td><td>

id

</td></tr><tr><td>

Vendor

</td><td>

Vendor

</td><td>

cleansed\_vendor\_ref

</td></tr><tr><td>

Quantity

</td><td>

Quantity

</td><td>

quantity

</td></tr></tbody>
</table>**AI Tools**

AI subcomponent reference table \(sn\_ent\_ai\_tool\) -&gt; sn\_ent\_ai\_system\_subcomponent\_m2m -&gt; AI system/Model table \(alm\_ai\_system\_digital\_asset\)

<table id="table_zn2_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

Description

</td><td>

Description

</td><td>

description

</td></tr><tr><td>

Type

</td><td>

Type

</td><td>

type

</td></tr><tr><td>

Source Information

</td><td>

Source information

</td><td>

source

</td></tr><tr><td>

Name

</td><td>

Name

</td><td>

developername

</td></tr><tr><td>

Table Name

</td><td>

Target document table

</td><td>

tablename

</td></tr></tbody>
</table>**AI Prompts**

alm\_ai\_prompt\_digital\_asset -&gt; Model table \(cmdb\_ai\_prompt\_product\_model\)

<table id="table_a42_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

Model Name

</td><td>

Model

</td><td>

model

</td></tr><tr><td>

Description

</td><td>

Prompt information

</td><td>

description

</td></tr><tr><td>

Table Name

</td><td>

Servicenow table

</td><td>

table\_name

</td></tr><tr><td>

ID

</td><td>

External record reference

</td><td>

id

</td></tr></tbody>
</table>**AI Agents Usage**

sn\_ai\_disc\_ai\_usage -&gt; AI system/Model table \(alm\_ai\_system\_digital\_asset\)

<table id="table_b42_xps_m3c"><tbody><tr><td>

Required Fields

</td><td>

ServiceNow \(Target\)

</td><td>

Salesforce \(Staging\)

</td></tr><tr><td>

User

</td><td>

User

</td><td>

user

</td></tr><tr><td>

Time

</td><td>

Time

</td><td>

timestamp

</td></tr><tr><td>

Parent ID

</td><td>

Session ID

</td><td>

parentid

</td></tr><tr><td>

Total Invocations

</td><td>

Count

</td><td>

totalinvocations

</td></tr><tr><td>

Conversion Definition ID

</td><td>

AI system

</td><td>

conversationdefinitionid

</td></tr></tbody>
</table>