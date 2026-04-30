---
title: Activity stream
description: Learn about how the Workspace Activity stream functions in Configurable Workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-06"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Activity stream

Learn about how the Workspace Activity stream functions in Configurable Workspace.

Activity stream enables agents to communicate with requesters and make internal notes about the work done on a record. Configure the Activity stream and Activity stream Compose components in UI Builder to set up Activity stream in Configurable Workspace.

For more information about the Activity Stream component, see the [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades) and select Activity Stream from the list of Next Experience Components.

## Activity Stream corresponding parameters

Workspace Activity stream matched with Configurable Workspace parameters.

**Note:** Not every Configurable Workspace component parameter has a corresponding Workspace \(legacy\) parameter.

|Component|Legacy component name|Legacy component parameter name|UIB component parameter name|
|---------|---------------------|-------------------------------|----------------------------|
|Activity Stream|now-activity-stream-connected|table|table|
|sysID|sysID|
|isNewRecord|isNewRecord|
| |title|
| |view|
| |showConversationFilter|
| |showTileAvatars|
| |showTileIcons|
| |events|
| |supplemental|
| |ambChannels|
| |filterOptions|
| |timestamp|
|Activity Stream compose|now-activity-stream-compose-connected|table|table|
|sysID|sysID|
|isNewRecord|isNewRecord|
|fields|Fields|
| |title|
| |useTabs|

