---
title: Set up the Local Admin Access topic
description: Administrators and users with the Virtual\_agent\_admin role can install and activate the Agent Client Collector Spoke plugin. Developers can update scripts and configure commands as needed for their organization.
locale: en-US
release: xanadu
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up ITSM Virtual Agent, ITSM Virtual Agent, IT Service Management]
---

# Set up the Local Admin Access topic

Administrators and users with the Virtual\_agent\_admin role can install and activate the Agent Client Collector Spoke plugin. Developers can update scripts and configure commands as needed for their organization.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Install the Agent Client Collector Spoke plugin on the instance according to the [Agent Client Collector installation](https://www.servicenow.com/docs/access?context=acc-installation&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) instructions.

2.  Update the sudoers file of the macOS devices with the following entry.

    This process allows the ServiceNow user to run the grant\_admin\_access script in sudo mode and bypass password requirements.

    ```
    _servicenow ALL= SETENV: /Library/Caches/servicenow/agent-client-collector/admin-access-mac/bin/grant_admin_access.sh *​ 
    Defaults:_servicenow !requiretty​ 
    Defaults exempt_group += _servicenow
    ```

3.  Activate the Agent Client Collector plugin \(admin-access-mac\), after validating the attached payload with your internal IT team.

4.  Configure the following commands as needed for your organization.

    ACC Check Definition: `check-admin-access`, `grant-admin-access`

5.  Duplicate and activate the Local Admin Access topic in the ITSM scope.

    To view, duplicate, preview, or publish IT Service Management topics in the Virtual Agent Designer, see [Getting started with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).


**Parent Topic:**[Setting up ITSM Virtual Agent](../concept/setting-up-itsm-va.md)

