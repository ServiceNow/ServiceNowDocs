---
title: DevOps Change Velocity suite health scan checks
description: View the list of scan checks available in DevOps Change Velocity to get recommendations on fixing any errors that might exist.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# DevOps Change Velocity suite health scan checks

View the list of scan checks available in DevOps Change Velocity to get recommendations on fixing any errors that might exist.

<table id="table_k3z_qv2_vdc"><thead><tr><th>

Check name

</th><th>

Check description

</th><th>

Suite

</th><th>

Resolution details

</th></tr></thead><tbody><tr><td>

DevOps - subflows frequently exceeding execution timeouts

</td><td>

DevOps capability handler subflows have a default time out limit of 45 seconds in the base system. Under normal operating conditions, these timeouts aren’t exceeded. When multiple subflows are timing out frequently, it indicates a potential issue.

</td><td>

DevOps Change Velocity Health - Scheduled

</td><td>

Increase the timeout value for the subflow that is timing out, in the Integration Capability table. You must have the DevOps Admin role to perform this action.

</td></tr><tr><td>

DevOps - empty roles in the base system

</td><td>

If any of your base system roles have an empty role reference, it could impact a wide range of DevOps functionality, including the Discover action and event processing.

</td><td>

DevOps Change Velocity Health - Scheduled

</td><td>

See the \[[KB1642669](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1642669)\] article for resolution details.

</td></tr><tr><td>

DevOps - duplicate pipelines

</td><td>

The DevOps data model doesn't enforce uniqueness on key records like pipelines, which can lead to intermittent or unpredictable issues. This check identifies duplicate pipeline records in primary DevOps tables, which could cause processing problems if not addressed.

</td><td>

DevOps Change Velocity Health - Scheduled

</td><td>

Delete the duplicate pipeline that does not have any associated pipeline executions or is not linked to an app.

</td></tr><tr><td>

DevOps System user access

</td><td>

The devops.system user is used for most server side transaction processing, and in the course of that processing if it cannot access certain key tables the process will fail. Because it's not practical to verify if the user has appropriate access every time it makes a query, the failures tend to manifest indirectly, making them hard and time consuming to diagnose. This check will ensure the devops.system has appropriate access to a specific list of tables required for core product functionality.

</td><td>

DevOps Change Velocity Health - Scheduled

</td><td>

Make sure DevOps System user exists. Ensure there are no field level ACLs on sys\_connection and credential table

</td></tr><tr><td>

DevOps - related plugins compatibility

</td><td>

If the plugin versions for applications associated with DevOps Change Velocity are not compatible with the DevOps Change Velocity version in an instance, it might result in various features not functioning correctly. This check identifies if any plugin starting with the name "sn\_devops"\(excluding the sn\_devops\_pipeline plugin\) does not have same version as that of sn\_devops\_chgvlcty.

</td><td>

DevOps Change Velocity Health - Scheduled

</td><td>

Upgrade the related plugins to the version compatible with DevOps Change Velocity.

</td></tr><tr><td>

DevOps - chronically failing or waiting pipelines

</td><td>

If a pipeline is chronically failing or in the waiting state indefinitely, it might cause the DevOps processes to not proceed further. This check identifies pipelines that have failed for the previous ten executions, so that you can take remedial action.

</td><td>

DevOps Change Velocity Health - Scheduled

</td><td>

Verify the most recent executions for the pipelines flagged, and investigate inbound events and DevOps error logs tables to help determine the root cause for the failures.

</td></tr><tr><td>

DevOps -Stale or Long-Running Discover and Import Requests

</td><td>

Identifies outdated or prolonged discover and import requests. If discover or import requests stay in progress or fail for over 5–6 hours, they may block new requests with the same combination. This check finds such outdated or prolonged requests so that prompt action can be taken to keep the DevOps processes running.

</td><td>

DevOps Change Velocity Health - Scheduled

</td><td>

Verify the tool connectivity, credentials, permissions, and DevOps error logs to identify the cause of failures or stalled requests.

</td></tr><tr><td>

DevOps - scheduled jobs with invalid configuration

</td><td>

Identifies scheduled jobs that have been configured to run as an invalid or non-admin user.

</td><td>

DevOps Change Velocity Health - Scheduled

</td><td>

Configure the jobs to run with admin users.

</td></tr><tr><td>

DevOps - incorrectly configured module access policies

</td><td>

If there are missing or incorrectly configured module access policies in your instance, it could impact a wide range of DevOps functionality, including tool connectivity, event processing, pipeline processing, and change creation. Auto-generated module access policies are set to reject by default. This check identifies the module access policies that are configured with the reject result state.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

Set the result value of the module access policy for the DevOps application to "Track' to allow the DevOps application to access the credentials. See the \[[KB1112530](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1112530)\] KB article for more details.

</td></tr><tr><td>

DevOps - change control steps with untracked pipelines

</td><td>

If a pipeline has change control enabled but it is not marked for tracking, a change request might not get created when it is run, and the pipeline may get stuck.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

Enable tracking for pipelines under change control by selecting the Track option in the tool record page or add the pipeline to an app.

</td></tr><tr><td>

DevOps - Jenkins plugin compatibility

</td><td>

If the Jenkins plugin version installed in your instance is not compatible with the DevOps Change Velocity version, it might result in Jenkins features not functioning correctly.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

Upgrade your Jenkins plugin to the version compatible with DevOps Change Velocity.

</td></tr><tr><td>

DevOps – changes in update set records

</td><td>

If there are modifications in any of the DevOps applications, it could potentially result in updates being skipped or overlooked when upgrading to a newer version. This check scans the update.xml file for DevOps Change Velocity scoped changes.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

Before working with update sets, create a standard process for moving customizations. For more information, see the [General guidelines for planning the update process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/get-started-update-sets.md) topic in product documentation.

</td></tr><tr><td>

DevOps - files skipped during upgrade

</td><td>

If any file was skipped during the upgrade process, it could lead to potential issues or an unstable application state. Proactively addressing missing files ensures the upgrade's integrity and prevents unexpected errors or failures.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

Manually merge the new updates for the skipped files. See the KB article \[[KB0952456](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0952456)\] for more information.

</td></tr><tr><td>

DevOps webhook configuration analysis

</td><td>

Verifies whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in GitHub, GitLab, Azure DevOps, and Jenkins.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

If the webhook is not configured, set it up. If the existing configuration contains errors, update it to ensure the correct settings are applied.

</td></tr><tr><td>

DevOps OAuth app configuration analysis

</td><td>

If a GitHub tool is in the connected state and has a related OAuth app configuration, this check evaluates the configuration for any potential issues. For example, for GitHub Apps, it checks whether the App ID and Client ID values are matching with the values configured in the ServiceNow Application Registry and JWT Provider records.**Note:** This check is available for only GitHub.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

N/A

</td></tr><tr><td>

DevOps Health scan for processing errors in callbacks

</td><td>

As a DevOps engineer, I want a health scan that checks for processing errors in callbacks, so that callback processing issues can be detected early.Things to look for:

-   Callback record has not closed in more than 1 day.
-   Callback record is in Error state.
-   Callback records with errors in the Response.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

N/A

</td></tr><tr><td>

DevOps Health scan for OOB ACL integrity and correct role association

</td><td>

As a DevOps engineer, I want a health scan that checks all out-of-the-box ACLs are intact and correctly associated with the appropriate roles, so that access control is properly enforced.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

N/A

</td></tr><tr><td>

DevOps Health scan for presence of DevOps tables and sys\_\* metadata

</td><td>

As a DevOps engineer, I want a health scan that verifies all DevOps tables and all metadata in sys\_\* tables are present, to detect if any tables were excluded during cloning.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

N/A

</td></tr><tr><td>

DevOps Health scan for complete DevOps roles including inherited roles

</td><td>

As a DevOps engineer, I want a health scan that verifies all DevOps roles contain all expected roles including inherited roles, so that role configurations are complete and correct.

</td><td>

DevOps Change Velocity Health - On-demand

</td><td>

N/A

</td></tr></tbody>
</table>**Parent Topic:**[DevOps Change Velocity reference](devops-change-velocity-reference.md)

