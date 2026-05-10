---
title: Cloning guidelines for DevOps Change Velocity
description: Clone the DevOps Change Velocity application from one instance to another.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Cloning guidelines for DevOps Change Velocity

Clone the DevOps Change Velocity application from one instance to another.

**Note:** Valid for Utah and later.

For detailed information for cloning a ServiceNow instance, see the following topics.

-   [Instance Clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)
    -   [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md)
    -   [Register target instance \(legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateACloneTarget.md)
    -   [Exclude a table from cloning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ExcludeATableFromCloning.md)
    -   [Create a data preserver \(legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateADataPreserver.md)
-   [New Backup-based Clone Engine \[KB0540342\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0540342)

## Base system table exclusion and preservers on global tables used in DevOps

|Table name|Exclude table entry present?|Data preservers entry present?|
|----------|----------------------------|------------------------------|
|**For DevOps tool**|
|sys\_alias|No|No|
|http\_connection|Yes|Yes|
|discovery\_credentials|Yes|Yes|
|oauth\_entity\_profile|Yes|Yes|
|oauth\_entity|Yes|Yes|
|jwt\_provider|Yes|Yes|
|jwt\_keystore\_aliases|Yes|Yes|
|sys\_certificate|Yes|Yes|
|token\_verification|Yes|Yes|
|sys\_user\_group|No|No|
|**For DevOps apps**|
|cmdb\_ci\_business\_app|No|No|
|cmdb\_ci\_sdlc\_component|No|No|
|cmdb\_application\_product\_model|No|No|

## Tools cloned from source instance

-   The tools that are cloned from source instance will have a Connection alias \(sys\_alias\) associated with them.
-   The Connection record and the Credential record aren’t cloned over from the source instance since those tables are excluded.
-   Tool URL will be empty because the tool URL is dynamically calculated using connection record.
-   Connect test fails because there’s no active connection.
-   All the underlying entities like projects, plans, pipelines, repositories, work items, commits, pipeline execution, and so on must be present under the tool.
-   The tool's token isn’t cloned.
-   New webhook inbound events won’t automatically start to come to the cloned target instance for these tools. The tools must be reconfigured to receive new inbound events.

**Manual steps on cloned tools**

1.  Create Connection and Credential
    -   Use the **Create New Connection &amp; Credential** action present under the related links on the tool record or manually create the connection \(http\_connection\) and credential \(discovery\_credentials\) record and associate with the tool's connection alias.
    -   Manually run the **Connect** action on the tool and make sure that the tool connection state is **Connected**.
2.  Regenerate token and configure
    -   For the tools that support token-based webhook configuration, use the **Regenerate token** action from the Related Links on the tool record page.
    -   Regenerating the token creates a new token in the token\_verification table and creates webhooks for the tool and repos that have Configure status as **Configured**.
    -   For the tools that don't support token-based webhooks, click **Configure** and enter the user name and password for the DevOps integration user.

## Apps cloned from source instance

-   Apps that are cloned from the source instance will have all the app associations intact.
-   Business app and SDLC component links are maintained.
-   Manual steps aren't required after cloning.

## Preserving data on target instance

Aim to preserve the existing tools, tool connections, and apps on the target instance.

## Level 1 data preservers

|Title|Table name|Purpose|Suggested filter|
|-----|----------|-------|----------------|
|DevOps tool|sn\_devops\_tool|To preserve top-level DevOps tool list.|`connection_state=connected^EQ` to preserve all connected tools or filter on specific tool IDs.|
|Connection &amp; Credential Aliases|sys\_alias|Specified in DevOps tool to hold connection details.|`idLIKEdevops^ORidLIKEspoke^EQ` to preserve all aliases related to DevOps.|
|DevOps app|sn\_devops\_app|To preserve top-level DevOps App list.| |

## Manual steps on preserved tools after cloning

1.  Maintained by

    If the tool on the target instance had any **Maintained by** user groups specified before cloning, update the user groups, and set them on the tool record manually after cloning.

2.  Discover
    -   Projects, pipelines, plans, and repositories aren't present for preserved tools after the clone.
    -   For Azure DevOps tools, first perform **Discover projects**.
    -   Perform **Discover** action on the tool or the project to bring the pipelines, plans, and repositories details.
3.  Track

    Track the required pipelines, plans, and repositories.

4.  Configure
    -   Optional for tools where the webhook url holds a reference to tool sys\_id only. For example, GitHub, GitLab, Jira, Bitbucket.
    -   You must reconfigure Azure DevOps projects because the project sys\_id has changed after rediscover.
    -   Token remains the same for the tool.
    -   Verify that there are no duplicate webhooks created in the third-party DevOps tool after reconfiguring.
5.  Historical import

    Use the import action or workspace to import historical data for plans, repositories, and pipelines.


## Manual steps on preserved apps after cloning

1.  Maintained by

    If the app on the target instance had any **Maintained by** user groups specified before cloning, update the user groups, and set them on the app record manually after cloning.

2.  Associate with app

    Manually reassociate plans, repositories, and pipelines with the app.

3.  Relink to SDLC component and application model

    Manually associate the DevOps app to the SDLC component, and SDLC component to the application model.


## Level 2 data preservers

Aim to preserve the data and relations under DevOps tools and DevOps apps. These preservers should be used along with the level1 preservers and manual steps.

|Title|Table name|Purpose|Suggested filter|
|-----|----------|-------|----------------|
|**Plugin: DevOps Data Model**|
|Artifact Repository|sn\_devops\_artifact\_repository|Top-level list of artifact repositories. Required to keep artifact repos that are associated with a preserved tool.|`tool=toolid^EQ`, where `toolid` is the tool being preserved.|
|Artifact|sn\_devops\_artifact|Top-level list of artifacts. Required to keep artifacts that are associated with a preserved tool.|`artifact_repository.tool=toolid^EQ`, where "`toolid`" is the tool being preserved.|
|Pipeline|sn\_devops\_pipeline|Top-level list of pipelines. Required to keep pipelines that are associated with a preserved tool.|`tool=toolid^EQ`, where `toolid` is the tool being preserved.|
|Release Version|sn\_devops\_plan\_version|Top-level list of release versions. Required to keep release versions that are associated with a preserved planning tool.|`plan.tool=toolid^EQ`, where `toolid` is the tool being preserved.|
|Plan|sn\_devops\_plan|Top-level list of plans. Required to keep plans that are associated with a preserved planning tool.|`tool=toolid^EQ`, where `toolid` is the tool being preserved.|
|Project|sn\_devops\_project|Top-level list of projects. Required to keep projects that are associated with a preserved tool. Currently supported by Azure DevOps.|`tool=toolid^EQ`, where `toolid` is the tool being preserved.|
|Repository|sn\_devops\_repository|Top-level list of repositories. Required to keep repositories that are associated with a preserved coding tool.|`tool=toolid^EQ`, where `toolid` is the tool being preserved.|
|App to Artifact Repository|sn\_devops\_m2m\_app\_artifact\_repository|App/Artifact Repo associations. Required to keep the relationship between preserved apps and artifact repositories.|`app=appid^EQ`, where `appid` is the app being preserved.|
|App to Artifact|sn\_devops\_m2m\_app\_artifact|App/Artifact associations. Required to keep the relationship between preserved apps and artifacts.|`app=appid^EQ`, where `appid` is the app being preserved.|
|App to Plan|sn\_devops\_m2m\_app\_plan|App/Plan associations. Required to keep the relationship between preserved apps and plans.|`app=appid^EQ`, where `appid` is the app being preserved.|
|**Plugin: DevOps Vulnerability Integrations**|
|DevOps Security Orchestration Relation|sn\_devops\_security\_orchestration\_relation|Required to keep the relation between DevOps entitiy \(for example, pipeline\) and a security tool.|reference\_table=sn\_devops\_pipeline|

## Custom integration data preservers

Aim to preserve the meta-data related to any custom tool integrations on the target instance. These data preservers can be used with both level1 and level2 preservers.

|Title|Table name|Purpose|Suggested filter|
|-----|----------|-------|----------------|
|**Plugin: DevOps Data Model**|
|Custom tool Integration Capability|sn\_devops\_integration\_capability|Required to keep the supported actions to integration capability mapping records of custom tool integration.|`tool_integration=customToolIntegrationId^EQ`, where `customToolIntegrationId` is the **sys\_id** of the custom tool integration.|
|Custom tool Integration Capability Mapping|sn\_devops\_tool\_capability\_mapping|Required to keep the integration capability mapping records of custom tool integration.|`tool_integration=customToolIntegrationId^EQ`, where `customToolIntegrationId` is the **sys\_id** of the custom tool integration.|
|Custom DevOps Tool Integration|sn\_devops\_tool\_integration|Required to keep the tool integration record of custom tool integration.|`sys_id=customToolIntegrationId^EQ`, where `customToolIntegrationId` is the **sys\_id** of the custom tool integration.|
|Custom Tool permissions|sn\_devops\_tool\_permission|Required to keep the permission check records of custom tool integration.|`tool_integration=customToolIntegrationId^EQ`, where `customToolIntegrationId` is the **sys\_id** of the custom tool integration.|
|**Plugin: DevOps Workspace**|
|Custom tool Onboarding task type|sn\_devops\_ws\_onboarding\_task\_type|Required to keep the onboarding task types of custom tool integration.|`tool_integration=customToolIntegrationId^EQ`, where `customToolIntegrationId` is the sys\_id of the custom tool integration.|

## Level 3 data preservers

Aim to have all the m2m mapping intact in the target instance.

**Note:** The following are DevOps specific tables. If you require other data to be in place, then you can add those tables in the preservers list. For example, Change Requests.

|Name|Table name|Application|
|----|----------|-----------|
|App|sn\_devops\_app|DevOps Data Model|
|Artifact|sn\_devops\_artifact|DevOps Data Model|
|Artifact Repository|sn\_devops\_artifact\_repository|DevOps Data Model|
|Artifact Staged Request|sn\_devops\_artifact\_staging|DevOps Data Model|
|Artifact Version|sn\_devops\_artifact\_version|DevOps Data Model|
|Base Planning Item|sn\_devops\_base\_planning\_item|DevOps Data Model|
|Branch|sn\_devops\_branch|DevOps Data Model|
|Build Test Result|sn\_devops\_build\_test\_result|DevOps Data Model|
|Build Test Summary|sn\_devops\_build\_test\_summary|DevOps Data Model|
|Callback|sn\_devops\_callback|DevOps Data Model|
|Change Reference|sn\_devops\_change\_reference|DevOps Data Model|
|Commit|sn\_devops\_commit|DevOps Data Model|
|Committer|sn\_devops\_committer|DevOps Data Model|
|Commit Details|sn\_devops\_commit\_details|DevOps Data Model|
|Contributor Score Change Factor|sn\_devops\_contributor\_score\_chg\_factor|DevOps Data Model|
|Environment|sn\_devops\_environment|DevOps Data Model|
|Import Request|sn\_devops\_import\_request|DevOps Data Model|
|Import Request Page|sn\_devops\_import\_request\_page|DevOps Data Model|
|Inbound Event|sn\_devops\_inbound\_event|DevOps Data Model|
|App to Artifact|sn\_devops\_m2m\_app\_artifact|DevOps Data Model|
|App to Artifact Repository|sn\_devops\_m2m\_app\_artifact\_repository|DevOps Data Model|
|App to Plan|sn\_devops\_m2m\_app\_plan|DevOps Data Model|
|Deployed Artifact to TaskExecution|sn\_devops\_m2m\_artifact\_execution|DevOps Data Model|
|Artifact Version to Commit|sn\_devops\_m2m\_artifact\_version\_commit|DevOps Data Model|
|Artifact Version to Package|sn\_devops\_m2m\_artifact\_version\_package|DevOps Data Model|
|Branch To Commit|sn\_devops\_m2m\_branch\_commit|DevOps Data Model|
|Run Commit|sn\_devops\_m2m\_commit\_execution|DevOps Data Model|
|Commit to Pull Request|sn\_devops\_m2m\_commit\_pull\_request|DevOps Data Model|
|Commit To Work Item|sn\_devops\_m2m\_commit\_work\_item|DevOps Data Model|
|Import Request to Inbound Event Mapping|sn\_devops\_m2m\_inbound\_event\_import\_request|DevOps Data Model|
|Tool Integration Configuration Template|sn\_devops\_m2m\_tool\_integration\_configuration\_template|DevOps Data Model|
|Work Item To Release Version|sn\_devops\_m2m\_work\_item\_plan\_version|DevOps Data Model|
|Orchestration Task|sn\_devops\_orchestration\_task|DevOps Data Model|
|Orchestration Task Definition|sn\_devops\_orchestration\_task\_definition|DevOps Data Model|
|DevOps Package|sn\_devops\_package|DevOps Data Model|
|Participant|sn\_devops\_participant|DevOps Data Model|
|Performance test summary|sn\_devops\_performance\_test\_summary|DevOps Data Model|
|Pipeline|sn\_devops\_pipeline|DevOps Data Model|
|Pipeline Execution|sn\_devops\_pipeline\_execution|DevOps Data Model|
|Plan|sn\_devops\_plan|DevOps Data Model|
|Release Version|sn\_devops\_plan\_version|DevOps Data Model|
|Processed Inbound Event|sn\_devops\_processed\_inbound\_event|DevOps Data Model|
|Project|sn\_devops\_project|DevOps Data Model|
|Pull Request|sn\_devops\_pull\_request|DevOps Data Model|
|Repository|sn\_devops\_repository|DevOps Data Model|
|Software Quality Category|sn\_devops\_software\_quality\_category|DevOps Data Model|
|Software Quality Category Detail|sn\_devops\_software\_quality\_category\_detail|DevOps Data Model|
|Software Quality Scan Detail|sn\_devops\_software\_quality\_scan\_detail|DevOps Data Model|
|Software Quality Scan Summary|sn\_devops\_software\_quality\_scan\_summary|DevOps Data Model|
|Software Quality Scan Summary Relations|sn\_devops\_software\_quality\_scan\_summary\_relations|DevOps Data Model|
|Software Quality Sub Category|sn\_devops\_software\_quality\_sub\_category|DevOps Data Model|
|Step|sn\_devops\_step|DevOps Data Model|
|Step Execution|sn\_devops\_step\_execution|DevOps Data Model|
|Tag|sn\_devops\_tag|DevOps Data Model|
|Task Execution|sn\_devops\_task\_execution|DevOps Data Model|
|Test Execution|sn\_devops\_test\_execution|DevOps Data Model|
|Test Result|sn\_devops\_test\_result|DevOps Data Model|
|Test Summary|sn\_devops\_test\_summary|DevOps Data Model|
|Test Summary Relations|sn\_devops\_test\_summary\_relations|DevOps Data Model|
|DevOps Tool|sn\_devops\_tool|DevOps Data Model|
|Tool Connection Status|sn\_devops\_tool\_connection\_status|DevOps Data Model|
|Tool Connectivity History|sn\_devops\_tool\_connectivity\_history|DevOps Data Model|
|Waiting Reason Tracking|sn\_devops\_waiting\_reason\_tracking|DevOps Data Model|
|Work Item|sn\_devops\_work\_item|DevOps Data Model|

**Parent Topic:**[Managing DevOps Change Velocity](../concept/using-devops-change-velocity.md)

