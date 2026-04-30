---
title: Default mapping configuration for SPW Jira Integrations
description: Learn about the default mapping configuration of Epic, Story, and Sprint work types between Strategic Planning and Jira.
locale: en-US
release: yokohama
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Reference, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Default mapping configuration for SPW Jira Integrations

Learn about the default mapping configuration of Epic, Story, and Sprint work types between Strategic Planning and Jira.

## Epic mapping configuration

Epic \[sn\_align\_core\_scrum\_epic\] in Strategic Planning is mapped to Epic in Jira. The field mapping between these two tables is as follows.

|Field in Strategic Planning|Field in Jira|
|---------------------------|-------------|
|approved\_start\_date|Start date|
|state|Status|
|short\_description|Summary|
|approved\_end\_date|Due date|

## Story mapping configuration

Story \[rm\_story\] in Strategic Planning is mapped to Story in Jira. The field mapping between these two tables is as follows.

|Field in Strategic Planning|Field in Jira|
|---------------------------|-------------|
|assigned\_to|Assignee|
|description|Description|
|iteration|Sprint|
|parent\_work\_item|Parent|
|priority|Priority|
|short\_description|Summary|
|state|Status|

## Sprint mapping configuration

Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\] in Strategic Planning is mapped to Sprint in Jira. The field mapping between these two tables is as follows.

|Field in Strategic Planning|Field in Jira|
|---------------------------|-------------|
|state|state|
|start\_date|startDate|
|name|name|
|end\_date|endDate|

**Parent Topic:**[SPW Jira Integrations reference](spw-jira-integrations-reference.md)

**Related topics**  


[Review default mapping configuration for Jira projects in SPW](../task/review-default-map-config-jira-projects-spw.md)

