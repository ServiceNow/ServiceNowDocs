---
title: Workflow versions
description: To prevent users from making changes to a workflow that affect other users of the system, workflows must be checked out before they can be edited.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow concepts, Classic Workflow, Build workflows]
---

# Workflow versions

To prevent users from making changes to a workflow that affect other users of the system, workflows must be checked out before they can be edited.

Only one user can check out a workflow at a time. When a workflow is checked out, changes apply only to the user who has the workflow checked out. Other users can continue to use the published workflow. After the changes are complete, the workflow can be published so that it is available to all users.

**Note:** Because each workflow has a unique sys\_id, different workflows can have the same name. This is typically expected in a domain-separated environment where users in different companies cannot see each other's workflows because they are in different domains. However, this can lead to confusion in other environments. In general, give each workflow a unique name to prevent workflow designers from making changes to the wrong workflow.

When a new version of an existing workflow is published, the changes are not applied to running workflow contexts. Any currently running workflow context continues using the workflow version that was available when the workflow started. The next time the workflow runs, it uses the updated, published version.

