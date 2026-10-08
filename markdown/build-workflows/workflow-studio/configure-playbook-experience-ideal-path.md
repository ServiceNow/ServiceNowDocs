---
title: Configure Playbook Experience to display ideal path
description: Configure Playbook Experience to show the stages and activities in an ideal path before they are executed during a playbook run.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/configure-playbook-experience-ideal-path.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
breadcrumb: [Ideal path for a playbook, Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Configure Playbook Experience to display ideal path

Configure Playbook Experience to show the stages and activities in an ideal path before they are executed during a playbook run.

## Before you begin

Configure the ideal path in the playbook. To learn more, see [Configure the ideal path for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/configure-ideal-path-for-playbook.md).

Role required: admin

## About this task

You can configure Playbook Experience to display conditional stages and activities in an ideal path. During a playbook run, the unresolved decision are shown to the user as conditional activities. It displays a preview of what is likely to come next, even before the decision has been evaluated. This informs the fulfillers about the ideal execution path of the playbook. For more information about ideal path, see [Ideal path for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/ideal-path-for-playbook.md).

## Procedure

1.  Navigate to **All** &gt; **Playbook Experience** &gt; **Playbook Experiences**.

2.  From the list, select a Playbook experience where you want to configure ideal path visibility.

3.  In the **Configurations** list, select an existing configuration or select **New** to create a configuration.

    \[Omitted image "pb-experience-ideal-path-config.png"\] Alt text: Open the Playbook Experience configuration.

4.  In the **Pending Item Visibility** field, select **Show stages and activities on the ideal path**.

    \[Omitted image "pbexperience-ideal-path-visibility.png"\] Alt text: Set the pending item visibility list.

5.  Select **Update** or **Submit**.


## What to do next

Deploy a playbook with ideal path and the configured Playbook Experience.

**Parent Topic:**[Ideal path for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/ideal-path-for-playbook.md)

