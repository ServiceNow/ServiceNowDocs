---
title: Setting up Enterprise graph in sub-production instance
description: Use these steps to setup Enterprise graph in sub-production instance manually.
locale: en-US
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Enterprise graph schema, Knowledge Graph, Enable AI experiences]
---

# Setting up Enterprise graph in sub-production instance

Use these steps to setup Enterprise graph in sub-production instance manually.

## Before you begin

Unlike production instances, the Enterprise Graph setup does not start automatically in the sub-production instance.

You have to manually enable the system property: `sn_kg.description_generation.enable.non_production_envs`

When you enable this system property, the Enterprise Graph setup starts in the sub-production instances and can take several days to complete.

Until this setup is finished, the Enterprise Graph schema won't work effectively for answering queries.

This step creates the necessary descriptions for the Enterprise Graph to respond to queries.

Role required: kg\_admin

