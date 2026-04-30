---
title: Explore Now Assist AI asset discovery
description: Explore the syncing process of AI assets including models, datasets, prompts, skills, and agentic AI components into the AI Asset Inventory of AI Control Tower.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-12-04"
reading_time_minutes: 1
breadcrumb: [Explore, AI Control Tower, Enable AI experiences]
---

# Explore Now Assist AI asset discovery

Explore the syncing process of AI assets including models, datasets, prompts, skills, and agentic AI components into the AI Asset Inventory of AI Control Tower.

The AI systems are synchronized from source Now Assist skill config record \(sn\_nowassist\_skill\_config\).

1.  The out of the box skill meets the following conditions for an AI system:
    1.  If active, insert.
    2.  If not active, insert only if it belongs to the custom skill category and is published.
2.  If the skill exists in AI Control Tower and the source Now Assist skill config record is updated, those changes are applied to the AI system record in AI Control Tower. The state for the AI system is mapped as follows based on source Now Assist skill config record state:

    1.  Active: Mark as Deployed
    2.  Published or Draft: Mark as In Development
    3.  Retired: Mark as Retired
    4.  Deleted: No update is made

<table id="table_xb4_5cq_4hc"><thead><tr><th>

Type

</th><th>

Source Table

</th><th>

Target Tables

</th><th>

Field Tracked

</th><th>

Records included

</th></tr></thead><tbody><tr><td>

Models

</td><td>

sys\_generative\_ai\_model\_config

</td><td>

alm\_ai\_model\_digital\_asset, cmdb\_ai\_model\_product\_model

</td><td>

active, max\_tokens, model, supported\_languages, domain\_id

</td><td>

Active = true

</td></tr><tr><td>

Datasets

</td><td>

sys\_one\_extend\_test\_dataset

</td><td>

alm\_ai\_dataset\_digital\_asset, cmdb\_ai\_dataset\_product\_model

</td><td>

status, parent, name, description

</td><td>

Published = true eval\_run datasets

</td></tr><tr><td>

Skills

</td><td>

sn\_nowassist\_skill\_config

</td><td>

alm\_ai\_system\_digital\_asset, cmdb\_ai\_system\_product\_model

</td><td>

active, datasets, prompts, model, sys\_created\_by, domain\_id, name, description

</td><td>

Active = true or state = published for custom skills; skill family not platform or any of its children\(non platform skills\)

</td></tr><tr><td>

Prompts

</td><td>

sys\_generative\_ai\_config

</td><td>

alm\_ai\_prompt\_digital\_asset, cmdb\_ai\_prompt\_product\_model

</td><td>

active, prompt, model, name, version

</td><td>

Active prompts with active model and linked skill

</td></tr><tr><td>

Tools

</td><td>

sn\_aia\_tool

</td><td>

sn\_ent\_ai\_tool

</td><td>

name, description, type, active, sys\_created\_by, domain\_id

</td><td>

 

</td></tr><tr><td>

AI Agents

</td><td>

sn\_aia\_agent

</td><td>

alm\_ai\_system\_digital\_asset, cmdb\_ai\_system\_product\_model

</td><td>

name, description, role, instructions, sys\_created\_by, domain\_id

</td><td>

Active = true

</td></tr><tr><td>

Agent Tool Mapping

</td><td>

sn\_aia\_agent\_tool\_m2m

</td><td>

sn\_ent\_ai\_system\_subcomponent\_m2m

</td><td>

agent-tool mapping

</td><td>

All agent-tool mappings

</td></tr><tr><td>

Agent Use

 cases

</td><td>

sn\_aia\_usecase

</td><td>

alm\_ai\_system\_digital\_asset, cmdb\_ai\_system\_product\_model

</td><td>

name, description, sys\_created\_by, domain\_id

</td><td>

Active = true

</td></tr><tr><td>

Usecase to

 Agent

 mapping

</td><td>

sn\_aia\_team\_member

</td><td>

sn\_ent\_ai\_system\_subcomponent\_m2m

</td><td>

usecase-agent mapping

</td><td>

All usecase-agent mappings

</td></tr></tbody>
</table>For more information on Model, dataset, prompt, and skill sync process, see [KB2674041](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2674041) article in the Now Support Knowledge Base.

