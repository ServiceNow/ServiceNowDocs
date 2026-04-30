---
title: Update the associations for a deployable
description: Update the name and description of a deployable as well as its associations with applications and other items. This procedure is optional.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, DevOps Config, IT Service Management]
---

# Update the associations for a deployable

Update the name and description of a deployable as well as its associations with applications and other items. This procedure is optional.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_policy\_editor or cdm\_editor or cdm\_admin

## About this task

This optional procedure explains how to update the details of a deployable definition. For information on configuring the data in a deployable, see [Create and update a deployable](cdm-deployable-define.md).

**Note:** You cannot change the SDLC environment type \(development, test, or production\) of a deployable because such a change would have significant impact. For example, mapped policies and their inputs might differ significantly between test and production versions of a config dataset.

## Procedure

1.  On the **Settings** tab for an application, select **Deployables** in the tree view.

2.  Select the check box for the deployable, select **Edit**, and then update the settings for the deployable.

<table id="table_b2j_rhq_5pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful name for the deployable.

</td></tr><tr><td>

CDM Deployable Node

</td><td>

Deployable in the dataset.

</td></tr><tr><td>

Node Main

</td><td>

 

</td></tr><tr><td>

CDM Application

</td><td>

CDM application that includes the deployable.

</td></tr><tr><td>

Domain

</td><td>

 

</td></tr><tr><td>

Enforce Compliance

</td><td>

Option to ensure that only snapshots that pass validation can be exported.

</td></tr><tr><td>

CMDB CI

</td><td>

Configuration item in the CMDB.

</td></tr><tr><td>

Environment

</td><td>

SDLC environment that the deployable implements.-   Development
-   Test
-   Production


</td></tr><tr><td>

Description

</td><td>

Text description that helps other users understand the purpose, scope, and intent of the deployable.

</td></tr></tbody>
</table>3.  Select **Update**.


**Parent Topic:**[DevOps Config reference](../../devops-config/reference/devops-config-reference.md)

**Related topics**  


[Create or update a variable CDI](cdm-variables-crud.md)

