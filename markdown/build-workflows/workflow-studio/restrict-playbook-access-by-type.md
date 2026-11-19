---
title: Restrict access by playbook type
description: Use content access filtering to give a group of users access only to playbooks of a specific type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/restrict-playbook-access-by-type.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Content access filtering, Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Restrict access by playbook type

Use content access filtering to give a group of users access only to playbooks of a specific type.

## Before you begin

Role required: admin, playbook.admin

The playbook type you want to filter by must exist.

## About this task

Restrict access by playbook type when a group of users should work with one category of playbook and no others. A business unit that owns its own playbook types can be given access to those types alone.

This uses the same content access filtering mechanism that restricts activity definitions. For more information, see [Content filtering for Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/content-filtering-playbooks.md).

## Procedure

1.  Create a role for the users who need this access.

    Use a descriptive name that identifies the group and the access, for example, a role named for the business unit and the read operation.

2.  Create a content definition for the playbooks.

    1.  Navigate to **Process Automation** &gt; **Flow Administration** &gt; **Content Definitions**.

        The **Workflow Resources** table opens.

    2.  Select **New**.

    3.  Set **Table** to the playbook table.

    4.  In **Conditions**, add a condition on playbook type.

    5.  Select **Submit**.

3.  Create a content filtering rule that connects the role to the content definition.

    1.  Navigate to **Process Automation** &gt; **Flow Administration** &gt; **Content Filtering Rules**.

        The **Workflow Resource Filter Rules** table opens.

    2.  Select **New**.

    3.  Set **User Role** to the role you created.

    4.  Set **Resource Definition** to the content definition you created.

    5.  Select **Submit**.

4.  Assign the role to the users who need this access.


## Result

Users with the role see only playbooks of the type named in the content definition. Playbooks of other types aren't visible to them.

## What to do next

Pair this with the playbook.write role rather than pd\_author. The pd\_author role grants access to all playbooks and overrides the restriction. For more information, see [Role-based access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-roles.md).

**Parent Topic:**[Content access filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/content-access-filtering-playbooks.md)

