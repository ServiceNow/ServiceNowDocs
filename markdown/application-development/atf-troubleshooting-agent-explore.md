---
title: Exploring ATF troubleshooting agent
description: ATF troubleshooting agent streamlines the process of figuring out why tests are failing on specific metadata.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-26"
reading_time_minutes: 1
breadcrumb: [ATF troubleshooting agent, Testing and debugging applications, Building applications]
---

# Exploring ATF troubleshooting agent

ATF troubleshooting agent streamlines the process of figuring out why tests are failing on specific metadata.

## ATF troubleshooting agent overview

Use ATF troubleshooting agent to simplify test failure diagnosis on specific metadata.

![Landing page](../image/test-agent.gif)

## ATF troubleshooting agent users

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of AI agents during tool execution. AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

ATF troubleshooting agent has the following users.

<table id="table_ph5_fns_xjb"><thead><tr><th>

Users

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-   system\_admin
-   atf\_test\_admin
-   atf\_test\_designer
-   atf\_ws\_designer

</td><td>

Either of these 4 roles is required to access the ATF module and test results tables.

</td></tr><tr><td>

atf\_triager + now\_assist\_panel\_user

</td><td>

This role is required to access metadata tables to accurately troubleshoot test failure reasons. This role allows you to have the following access:-   Read-only access to test/step result tables
-   Read-only access to any sys\_metadata
-   Read-only access to syslog
-   Read/write access to sn\_atf\_assist\_triage\_output

**Note:** You can access the Now Assist panel using the now\_assist\_panel\_user role.

</td></tr></tbody>
</table>## ATF troubleshooting agent benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Simplify test failure diagnosis|[Troubleshoot test failures](../task/atf-troubleshooting-agent-test-failure.md)|atf\_triager + now\_assist\_panel\_user|

## What to explore next

To learn more about configuring and using ATF troubleshooting agent, see:

-   [Install ATF troubleshooting agent](../task/test-agent-install.md)
-   [Use](../task/atf-troubleshooting-agent-test-failure.md)

