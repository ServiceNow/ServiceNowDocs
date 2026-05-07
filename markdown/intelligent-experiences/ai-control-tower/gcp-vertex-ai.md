---
title: AI Service Graph Connector for Google Cloud Platform \(GCP\) Vertex AI
description: Use the  AI Service Graph Connector for GCP Vertex AI to create AI connections to discover AI assets such as AI assets such as AI systems, agents, models, prompts, tools, and datasets as well as usage data for these AI assets into AI Control Tower. This usage information is consumed by the AI Control Tower's value dashboard.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Google Cloud Platform \(GCP\) Vertex AI

Use the  AI Service Graph Connector for GCP Vertex AI to create AI connections to discover AI assets such as AI assets such as AI systems, agents, models, prompts, tools, and datasets as well as usage data for these AI assets into AI Control Tower. This usage information is consumed by the AI Control Tower's value dashboard.

## Download apps from the Store

Visit the  [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to download the AI Service Graph Connector for GCP Vertex AI app.

## Supported ServiceNow versions

-   Australia
-   Zurich patch 7
-   Yokohama patch 11

## User roles

Roles required in the ServiceNow environment:

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## Prerequisites from GCP Vertex

**Prerequisites:**

Review the setup instructions to create a service account, assign roles, bind roles to the service account, enable APIs, create a JKS file, and register it in your ServiceNow instance. For information on setup instructions and used APIs, see the [Service Graph connector for GCP Vertex AI- Setup Instructions \[KB2731256\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2731256)

## Data Mapping

The following table lists the data sources, the staging tables, and the target tables  CMDB CI classes and non-CMDB classes where data is stored for a  GCP Vertex AI  project.

<table id="table_pps_vnk_m3c"><tbody><tr><td>

**Data source**

</td><td>

**Staging table**

</td><td>

**Target tables**

</td></tr><tr><td>

SG-GCPVertexAI- Execution

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_execution

</td><td>

sn\_ai\_disc\_ai\_usage

</td></tr><tr><td>

SG-GCPVertexAI-System

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_system

</td><td>

cmdb\_ai\_system\_component\_product\_model

 alm\_ai\_system\_digital\_asset

 cmdb\_ci\_function\_ai

 cmdb\_rel\_asset\_ci

</td></tr><tr><td>

SG-GCPVertexAI- Mode

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_model

</td><td>

cmdb\_ai\_model\_product\_model

 alm\_ai\_model\_digital\_asset

</td></tr><tr><td>

SG-GCPVertexAI- Tool

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_tool

</td><td>

sn\_ent\_ai\_tool

</td></tr><tr><td>

SG-GCPVertexAI- Prompt

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_prompt

</td><td>

cmdb\_ai\_prompt\_product\_model

 alm\_ai\_prompt\_digital\_asset

</td></tr><tr><td>

SG-GCPVertexAI- System Subcomponent M2M

</td><td>

sn\_ai\_disc\_gcp\_sgc\_sg\_gcp\_ai\_system\_subcomponent\_m2m

</td><td>

sn\_ent\_ai\_system\_subcomponent\_m2m

</td></tr></tbody>
</table>