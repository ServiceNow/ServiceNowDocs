---
title: Define batch size for Jira project metadata
description: Define a batch size value that is used to fetch the metadata from the Jira projects.
locale: en-US
release: xanadu
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Troubleshooting issues of Jira integration with Agile Development 2.0, Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Define batch size for Jira project metadata

Define a batch size value that is used to fetch the metadata from the Jira projects.

## Before you begin

Role required: sn\_jira\_int.admin \(with edit access\) or sn\_jira\_int.user \(with read access\).

## About this task

Reduce the value of the batch size property to resolve the **API response size exceeded** error that you might get while fetching Jira project metadata.

## Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Properties**.

2.  Modify the **Define the batch size for fetching Jira project metadata** field value to a value less than 50.

    The suggested value range is 5–50.

3.  Click **Save**.


